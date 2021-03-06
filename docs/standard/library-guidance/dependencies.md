---
title: Abhängigkeiten und .NET-Bibliotheken
description: Hier finden Sie Empfehlungen zu Best Practices für die Verwaltung von NuGet-Abhängigkeiten in .NET-Bibliotheken.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 5566ab83040ce5dc23520401e3fc4bb619af4ec4
ms.sourcegitcommit: 82a3f7882bc03ed733af91fc2a0b113195bf5dc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2018
ms.locfileid: "49400527"
---
# <a name="dependencies"></a>Abhängigkeiten

Die einfachste Methode zum Hinzufügen von Abhängigkeiten zu einer .NET-Bibliothek sind NuGet-Paketverweise. Mit NuGet-Paketverweisen können Sie bereits geschriebene Funktionen schnell wiederverwenden. Allerdings sind sie für .NET-Entwickler auch eine häufige Ursache von Problemen. Die ordnungsgemäße Verwaltung von Abhängigkeiten ist wichtig, um zu verhindern, dass Änderungen in anderen .NET-Bibliotheken zu Problemen in Ihrer .NET-Bibliothek und umgekehrt führen.

## <a name="diamond-dependencies"></a>Rautenabhängigkeiten

Bei einem .NET-Projekt sind sehr häufig mehrere Versionen eines Pakets in der Abhängigkeitsstruktur vorhanden. Eine App kann beispielsweise von zwei NuGet-Paketen abhängig sein, von denen jedes wiederum von verschiedenen Versionen desselben Pakets abhängig ist. Dadurch entsteht eine Rautenabhängigkeit im Abhängigkeitsdiagramm der App.

![Rautenabhängigkeit](./media/dependencies/diamond-dependency.png "Rautenabhängigkeit")

Zur Buildzeit analysiert NuGet alle Pakete, von denen ein Projekt abhängig ist, einschließlich der Abhängigkeiten von Abhängigkeiten. Wenn mehrere Versionen eines Pakets erkannt werden, werden Regeln ausgewertet, um ein Paket auszuwählen. Das Vereinheitlichen von Paketen ist notwendig, weil es in .NET problematisch ist, in der gleichen Anwendung verschiedene Versionen einer Assembly nebeneinander auszuführen.

Die meisten Rautenabhängigkeiten lassen sich recht einfach auflösen. Unter bestimmten Umständen können sie jedoch Probleme verursachen:

1. **In Konflikt stehende NuGet-Paketverweise** verhindern, dass eine Version während der Paketwiederherstellung aufgelöst werden kann.
2. **Breaking Changes zwischen den Versionen** verursachen Fehler und Ausnahmen während der Laufzeit.
3. **Die Paketassembly weist einen starken Namen auf**, die Assemblyversion wurde geändert, und die App wird im .NET Framework ausgeführt. Assemblybindungsumleitungen sind erforderlich.

Es ist unmöglich zu bestimmen, welche Pakete neben Ihrem eigenen noch verwendet werden. Eine gute Möglichkeit, die Wahrscheinlichkeit von Rautenabhängigkeiten für Ihre Bibliothek zu senken, besteht darin, die Anzahl von benötigten Paketen zu reduzieren.

**✔️ ÜBERPRÜFEN** Sie Ihre .NET-Bibliothek auf unnötige Abhängigkeiten.

## <a name="nuget-dependency-version-ranges"></a>Versionsbereiche bei NuGet-Abhängigkeiten

Ein Paketverweis gibt den Bereich gültiger Pakete an, die zulässig sind. In der Regel ist die Paketverweisversion in der Projektdatei die Mindestversion, und es gibt keine höchste Version.

```xml
<!-- Accepts any version 1.0 and above. -->
<PackageReference Include="ExamplePackage" Version="1.0" />
```

Die Regeln, die NuGet zum Auflösen von Abhängigkeiten verwendet, sind [komplex](/nuget/consume-packages/dependency-resolution), aber NuGet sucht immer nach der niedrigsten anwendbaren Version. NuGet zieht die niedrigste anwendbare Version der höchsten verfügbaren Version vor, da die niedrigste Version wahrscheinlich die wenigsten Kompatibilitätsprobleme verursachen wird.

Aufgrund der NuGet-Regel, dass immer die niedrigste anwendbare Version verwendet wird, müssen Sie in Paketverweisen weder eine höchste Version noch einen genauen Bereich angeben, um zu vermeiden, dass die letzte Version abgerufen wird. NuGet versucht bereits, die niedrigste Version mit der höchsten Kompatibilität für Sie zu finden.

```xml
<!-- Accepts 1.0 up to 1.x, but not 2.0 and higher. -->
<PackageReference Include="ExamplePackage" Version="[1.0,2.0)" />

<!-- Accepts exactly 1.0. -->
<PackageReference Include="ExamplePackage" Version="[1.0]" />
```

Obergrenzen für Versionen verursachen einen Fehler in NuGet, wenn ein Konflikt auftritt. Ein Beispiel: Eine Bibliothek akzeptiert genau Version 1.0, während eine andere Bibliothek Version 2.0 oder höher erfordert. Wenn in Version 2.0 Breaking Changes eingeführt wurden, sind bei einer Abhängigkeit, die eine exakte Version oder die höchste verfügbare Version anfordert, Fehler garantiert.

![Konflikt bei Rautenabhängigkeit](./media/dependencies/diamond-dependency-conflict.png "Konflikt bei Rautenabhängigkeit")

**❌ VERWENDEN SIE KEINE** NuGet-Paketverweise ohne Mindestversion.

**❌ VERMEIDEN** Sie NuGet-Paketverweise, die eine exakte Version erfordern.

**❌ VERMEIDEN** Sie NuGet-Paketverweise mit Angabe einer Höchstversion.

## <a name="nuget-shared-source-packages"></a>NuGet-Pakete mit freigegebenen Quellen

Eine Möglichkeit, externe Abhängigkeiten für NuGet-Pakete zu reduzieren, ist der Verweis auf Pakete mit freigegebenen Quellen. Ein Paket mit freigegebenen Quellen enthält [Quellcodedateien](/nuget/reference/nuspec#including-content-files), die beim Verweisen in ein Projekt einbezogen werden. Da Sie nur Quellcodedateien einbeziehen, die mit dem Rest Ihres Projekts kompiliert werden, gibt es keine externe Abhängigkeit und damit auch keine potenziellen Konflikte.

Pakete mit freigegebenen Quellen eignen sich hervorragend für kleine Funktionsteile. Beispiel: ein Paket mit freigegebenen Quellen mit Hilfsmethoden für das Ausführen von HTTP-Aufrufen.

![Paket mit freigegebenen Quellen](./media/dependencies/shared-source-package.png "Paket mit freigegebenen Quellen")

```xml
<PackageReference Include="Microsoft.Extensions.Buffers.Testing.Sources" PrivateAssets="All" Version="1.0" />
```

![Projekt mit freigegebenen Quellen](./media/dependencies/shared-source-project.png "Projekt mit freigegebenen Quellen")

Pakete mit freigegebenen Quellen weisen einige Einschränkungen auf. Auf sie kann nur durch `PackageReference` verwiesen werden, ältere `packages.config`-Projekte sind also ausgeschlossen. Pakete mit freigegebenen Quellen können nur von Paketen mit dem gleichen Sprachtyp verwendet werden. Aufgrund dieser Einschränkungen eignen sich Pakete mit freigegebenen Quellen am besten für die Freigabe von Funktionen in einem Open Source-Projekt.

**✔️ ERWÄGEN** Sie Verweise auf freigegebene Quellen für kleine, interne Funktionsteile.

**✔️ ERWÄGEN** Sie die Festlegung Ihres Pakets als Paket mit freigegebenen Quellen, wenn es kleine, interne Funktionsteile bereitstellt.

**✔️ VERWEISEN** Sie mit `PrivateAssets="All"` auf Pakete mit freigegebenen Quellen.

> Diese Einstellung informiert NuGet darüber, dass das Paket nur während der Entwicklung verwendet werden soll und nicht als öffentliche Abhängigkeit verfügbar gemacht werden darf.

**❌ VERWENDEN SIE KEINE** Pakettypen mit freigegebenen Quellen in Ihrer öffentlichen API.

> Pakettypen mit freigegebenen Quellen werden in die verweisende Assembly kompiliert und können nicht über Assemblygrenzen hinweg ausgetauscht werden. Ein `IRepository`-Typ mit freigegebenen Quellen in einem Projekt ist ein anderer Typ als der gleiche `IRepository`-Typ mit freigegebenen Quellen in einem anderen Projekt. Für Typen in Paketen mit freigegebenen Quellen sollte die Sichtbarkeit auf `internal` festgelegt werden.

**❌ VERÖFFENTLICHEN SIE KEINE** Pakete mit freigegebenen Quellen in NuGet.org.

> Pakete mit freigegebenen Quellen enthalten Quellcode und können nur von Projekten mit dem gleichen Sprachtyp verwendet werden. Ein in C# geschriebenes Paket mit freigegebenen Quellen kann z.B. nicht von einer F#-Anwendung verwendet werden.
>
> Veröffentlichen Sie Pakete mit freigegebenen Quellen in einem [lokalen Feed oder in MyGet](./publish-nuget-package.md), um sie intern in Ihrem Projekt zu verwenden.

>[!div class="step-by-step"]
>[Zurück](nuget.md)
>[Weiter](sourcelink.md)