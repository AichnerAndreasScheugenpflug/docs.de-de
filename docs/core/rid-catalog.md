---
title: .NET Core Runtime-ID-Katalog (RID)
description: Erfahren Sie mehr über die Runtime-ID (RID) und wie RIDs in .NET Core verwendet werden.
ms.date: 07/19/2018
ms.openlocfilehash: 5a6dda260b4be85e54f4075f3edf12210b385289
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54534542"
---
# <a name="net-core-rid-catalog"></a>.NET Core-RID-Katalog

RID ist die Kurzform für *Runtime-ID* (Laufzeitbezeichner). Mithilfe von RID-Werten werden Zielplattformen identifiziert, unter der die Anwendung ausgeführt wird.
Sie werden von .NET-Paketen verwendet, um plattformspezifische Ressourcen in NuGet-Paketen darzustellen. Die folgenden Werte sind Beispiele für RIDs: `linux-x64`, `ubuntu.14.04-x64`, `win7-x64` oder `osx.10.12-x64`.
Für die Pakete mit nativen Abhängigkeiten legt die RID fest, auf welchen Plattformen das Paket wiederhergestellt werden kann.

Eine einzelne RID kann im `<RuntimeIdentifier>`-Element Ihrer Projektdatei festgelegt werden. Mehrere RIDs können als Liste mit Semikolon als Trennzeichen im `<RuntimeIdentifiers>`-Element der Projektdatei definiert werden. Sie können auch über die Option `--runtime` mit den folgenden [.NET Core-CLI-Befehlen](./tools/index.md) verwendet werden:

- [dotnet build](./tools/dotnet-build.md)
- [dotnet clean](./tools/dotnet-clean.md)
- [dotnet pack](./tools/dotnet-pack.md)
- [dotnet publish](./tools/dotnet-publish.md)
- [dotnet restore](./tools/dotnet-restore.md)
- [dotnet run](./tools/dotnet-run.md)
- [dotnet store](./tools/dotnet-store.md)

RIDs, die konkrete Betriebssysteme darstellen, weisen in der Regel folgendes Muster auf: `[os].[version]-[architecture]-[additional qualifiers]`, wobei:

- `[os]` ist der Moniker des Betriebs-/Plattformsystems. Beispielsweise `ubuntu`.

- `[version]` ist die Version des Betriebssystems in Form einer durch Punkte getrennten (`.`) Versionsnummer. Beispielsweise `15.10`.

  - Die Version sollte **keine** Marketingversion sein, da diese häufig mehrere separate Versionen des Betriebssystems mit unterschiedlichen Plattform-API-Oberflächen darstellt.

- `[architecture]` ist die Prozessorarchitektur. Beispielsweise `x86`, `x64`, `arm` oder `arm64`.

- `[additional qualifiers]` differenziert die verschiedenen Plattformen noch stärker. Beispiel: `aot` oder `corert`.

## <a name="rid-graph"></a>RID-Diagramm

Das RID-Diagramm oder Runtimefallbackdiagramm ist eine Liste von RIDs, die miteinander kompatibel sind. Die RIDs werden im Paket [Microsoft.NETCore.Platforms](https://www.nuget.org/packages/Microsoft.NETCore.Platforms/) definiert. Die Liste der unterstützten RIDs und das RID-Diagramm finden Sie in der Datei [*runtime.json*](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) im CoreFX-Repository. In dieser Datei können Sie sehen, dass alle RIDs außer der Basis-RID eine `"#import"`-Anweisung enthalten. Diese Anweisungen geben kompatible RIDs an.

Bei NuGet-Wiederherstellungspaketen wird versucht, eine genaue Übereinstimmung für die angegebene Runtime zu finden.
Wenn keine genaue Übereinstimmung gefunden wird, durchläuft das NuGet erneut das Diagramm, bis es das System mit der größten Kompatibilität gemäß dem RID-Diagramm findet.

Im Folgenden wird ein Beispiel für den tatsächlichen Eintrag für die `osx.10.12-x64`-RID vorgestellt:

```json
"osx.10.12-x64": {
    "#import": [ "osx.10.12", "osx.10.11-x64" ]
}
```

Die oben genannte RID gibt an, dass `osx.10.12-x64` `osx.10.11-x64` importiert. Bei NuGet-Wiederherstellungspaketen wird daher versucht, eine genaue Übereinstimmung für `osx.10.12-x64` im Paket zu finden. Wenn das NuGet die angegebene Runtime nicht finden kann, kann es beispielsweise Wiederherstellungspakete mit den Runtimes `osx.10.11-x64` finden.

Das folgende Beispiel zeigt, wie ein etwas größeres RID-Diagramm auch in der Datei *runtime.json* definiert wird:

```
    win7-x64    win7-x86
       |   \   /    |
       |   win7     |
       |     |      |
    win-x64  |  win-x86
          \  |  /
            win
             |
            any
```

Alle RIDs bilden schließlich wieder den Stamm `any`-RID ab.

Es gibt einige Aspekte zu RIDs, die Sie bei der Verwendung bedenken müssen:

- RIDs sind **opake Zeichenfolgen** und sollten als Blackboxes behandelt werden.
- Erstellen Sie RIDs nicht programmgesteuert.
- Verwenden Sie RIDs, die bereits für die Plattform definiert sind.
- Die RIDs müssen spezifisch sein. Leiten Sie daher keine Annahmen anhand des tatsächlichen RID-Werts ab.

## <a name="using-rids"></a>Die Verwendung von RIDs

Um RIDs verwenden zu können, müssen Sie wissen, welche RIDs es gibt. Zur Plattform werden regelmäßig neue Werte hinzugefügt.
Prüfen Sie die Datei [runtime.json](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) im CoreFX-Repository auf die neueste und vollständige Version.

Mit dem .NET Core 2.0 SDK wird das Konzept von portablen RIDs eingeführt. Dabei handelt es sich um neue zum RID-Diagramm hinzugefügte Werte, die nicht an eine bestimmte Version oder Betriebssystemverteilung gebunden sind. Diese sind besonders bei mehreren Linux-Verteilungen nützlich.

Die folgende Liste enthält die am häufigsten verwendeten RIDs für jedes Betriebssystem. Die Werte `arm` oder `corert` werden nicht behandelt.

## <a name="windows-rids"></a>RIDs für Windows

- Portabel
  - `win-x86`
  - `win-x64`
- Windows 7 / Windows Server 2008 R2
  - `win7-x64`
  - `win7-x86`
- Windows 8 / Windows Server 2012
  - `win8-x64`
  - `win8-x86`
  - `win8-arm`
- Windows 8.1 / Windows Server 2012 R2
  - `win81-x64`
  - `win81-x86`
  - `win81-arm`
- Windows 10 / Windows Server 2016
  - `win10-x64`
  - `win10-x86`
  - `win10-arm`
  - `win10-arm64`

Weitere Informationen finden Sie unter [Prerequisites for .NET Core on Mac (Erforderliche Komponenten für .NET Core unter Mac)](windows-prerequisites.md).

## <a name="linux-rids"></a>RIDs für Linux

- Portabel
  - `linux-x64`
- CentOS
  - `centos-x64`
  - `centos.7-x64`
- Debian
  - `debian-x64`
  - `debian.8-x64`
  - `debian.9-x64` (.NET Core 1.1 oder höher)
- Fedora
  - `fedora-x64`
  - `fedora.27-x64`
  - `fedora.28-x64` (.NET Core 1.1 oder höher)
- Gentoo (.NET Core 2.0 oder höher)
  - `gentoo-x64`
- openSUSE
  - `opensuse-x64`
  - `opensuse.42.3-x64`
- Oracle Linux
  - `ol-x64`
  - `ol.7-x64`
  - `ol.7.0-x64`
  - `ol.7.1-x64`
  - `ol.7.2-x64`
  - `ol.7.3-x64`
  - `ol.7.4-x64`
- Red Hat Enterprise Linux
  - `rhel-x64`
  - `rhel.6-x64` (.NET Core 2.0 oder höher)
  - `rhel.7-x64`
  - `rhel.7.1-x64`
  - `rhel.7.2-x64`
  - `rhel.7.3-x64` (.NET Core 2.0 oder höher)
  - `rhel.7.4-x64` (.NET Core 2.0 oder höher)
- Tizen (.NET Core 2.0 oder höher)
  - `tizen`
  - `tizen.4.0.0`
  - `tizen.5.0.0`
- Ubuntu
  - `ubuntu-x64`
  - `ubuntu.14.04-x64`
  - `ubuntu.16.04-x64`
  - `ubuntu.17.10-x64`
  - `ubuntu.18.04-x64`
- Ubuntu-Ableitungen
  - `linuxmint.17-x64`
  - `linuxmint.17.1-x64`
  - `linuxmint.17.2-x64`
  - `linuxmint.17.3-x64`
  - `linuxmint.18-x64` (.NET Core 2.0 oder höher)
  - `linuxmint.18.1-x64` (.NET Core 2.0 oder höher)
  - `linuxmint.18.2-x64` (.NET Core 2.0 oder höher)
  - `linuxmint.18.3-x64` (.NET Core 2.0 oder höher)
- SUSE Enterprise Linux (SLES) (.NET Core 2.0 oder höher)
  - `sles-x64`
  - `sles.12-x64`
  - `sles.12.1-x64`
  - `sles.12.2-x64`
  - `sles.12.3-x64`
- Alpine Linux (.NET Core 2.1 oder höher)
  - `alpine-x64`
  - `alpine.3.7-x64`

Weitere Informationen finden Sie unter [Prerequisites for .NET Core on Linux (Erforderliche Komponenten für .NET Core unter Linux)](linux-prerequisites.md).

## <a name="macos-rids"></a>Relative IDs für macOS

Relative IDs für macOS verwenden das ältere Branding „OSX“.

- `osx-x64` (.NET Core 2.0 oder höher, die mindestens erforderliche Version ist `osx.10.12-x64`)
- `osx.10.10-x64`
- `osx.10.11-x64`
- `osx.10.12-x64` (.NET Core 1.1 oder höher)
- `osx.10.13-x64`

Weitere Informationen finden Sie unter [Prerequisites for .NET Core on macOS (Erforderliche Komponenten für .NET Core unter macOS)](macos-prerequisites.md).

## <a name="android-rids-net-core-20-or-later-versions"></a>Android-RIDs (.NET Core 2.0 oder höher)

- `android`
- `android.21`

## <a name="see-also"></a>Siehe auch

- [Runtime-IDs](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/readme.md)
