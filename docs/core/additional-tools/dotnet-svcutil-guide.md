---
title: Übersicht zum WCF-Tool „svcutil“
description: Übersicht zum Microsoft-WCF-Tool „dotnet-svcutil“, über das Funktionen für .NET Core- und ASP.NET Core-Projekte hinzugefügt werden, z.B. das WCF-Tool „svcutil“ für .NET Framework-Projekte.
author: mlacouture
ms.date: 08/20/2018
ms.custom: seodec18
ms.openlocfilehash: e42ec0d4072c56456c824a814f1b383ea70a9307
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237258"
---
# <a name="wcf-dotnet-svcutil-tool-for-net-core"></a><span data-ttu-id="5d915-103">WCF-Tool „dotnet-svcutil“ für .NET Core</span><span class="sxs-lookup"><span data-stu-id="5d915-103">WCF dotnet-svcutil tool for .NET Core</span></span>

<span data-ttu-id="5d915-104">Das Windows Communication Foundation-Tool (WCF) **dotnet-svcutil** ist ein .NET Core-CLI-Tool, das Metadaten von einem Webdienst aus einem Netzwerkspeicherort oder einer WSDL-Datei abruft und eine WCF-Klasse mit Clientproxymethoden generiert, die Sie verwenden können, um auf die Webdienstvorgänge zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="5d915-104">The Windows Communication Foundation (WCF) **dotnet-svcutil** tool is a .NET Core CLI tool that retrieves metadata from a web service on a network location or from a WSDL file, and generates a WCF class containing client proxy methods that access the web service operations.</span></span>

<span data-ttu-id="5d915-105">Ähnlich wie das [**Service Model Metadata - svcutil**](../../framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)-Tool für .NET Framework-Projekte ist **dotnet-svcutil** ein Befehlszeilentool zum Generieren eines Webdienstverweises, der mit .NET Core- und .NET Standard-Projekten kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="5d915-105">Similar to the [**Service Model Metadata - svcutil**](../../framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) tool for .NET Framework projects, the **dotnet-svcutil** is a command-line tool for generating a web service reference compatible with .NET Core and .NET Standard projects.</span></span>

<span data-ttu-id="5d915-106">Das Tool **dotnet-svcutil** ist eine alternative Option zum mit Visual Studio verbundenen Dienstanbieter [**WCF Web Service Reference**](wcf-web-service-reference-guide.md), der zuerst in Visual Studio 2017 Version15.5 enthalten war.</span><span class="sxs-lookup"><span data-stu-id="5d915-106">The **dotnet-svcutil** tool is an alternative option to the [**WCF Web Service Reference**](wcf-web-service-reference-guide.md) Visual Studio connected service provider that first shipped with Visual Studio 2017 v15.5.</span></span> <span data-ttu-id="5d915-107">Das Tool **dotnet-svcutil** ist plattformübergeifend als .NET Core-CLI-Tool unter Linux, macOS und Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d915-107">The **dotnet-svcutil** tool as a .NET Core CLI tool, is available cross-platform on Linux, macOS, and Windows.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d915-108">Sie sollten nur auf Dienste aus einer vertrauenswürdigen Quelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="5d915-108">You should only reference services from a trusted source.</span></span> <span data-ttu-id="5d915-109">Wenn Sie Verweise aus nicht vertrauenswürdigen Quellen hinzufügen, hat das möglicherweise Auswirkungen auf die Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="5d915-109">Adding references from an untrusted source may compromise security.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5d915-110">Erforderliche Komponenten</span><span class="sxs-lookup"><span data-stu-id="5d915-110">Prerequisites</span></span>

* <span data-ttu-id="5d915-111">[.NET Core SDK](https://dotnet.microsoft.com/download), Version 1.0.4 oder höher</span><span class="sxs-lookup"><span data-stu-id="5d915-111">[.NET Core SDK](https://dotnet.microsoft.com/download) v1.0.4 or later versions</span></span>
* <span data-ttu-id="5d915-112">Ihr bevorzugter Code-Editor</span><span class="sxs-lookup"><span data-stu-id="5d915-112">Your favorite code editor</span></span>

## <a name="getting-started"></a><span data-ttu-id="5d915-113">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="5d915-113">Getting started</span></span>

<span data-ttu-id="5d915-114">Das folgende Beispiel führt Sie durch die erforderlichen Schritte zum Hinzufügen eines Webdienstverweises zu einem .NET Core- Konsolenprojekt und Aufrufen des Diensts.</span><span class="sxs-lookup"><span data-stu-id="5d915-114">The following example walks you through the steps required to add a web service reference to a .NET Core console project and invoke the service.</span></span> <span data-ttu-id="5d915-115">Sie erstellen eine .NET Core-Konsolenanwendung mit dem Namen _HelloSvcutil_ und fügen einen Verweis auf einen Webdienst hinzu, der folgenden Vertrag implementiert:</span><span class="sxs-lookup"><span data-stu-id="5d915-115">You will create a .NET Core console application named _HelloSvcutil_ and will add a reference to a web service that implements the following contract:</span></span>

```csharp
[ServiceContract]
public interface ISayHello
{
    [OperationContract]
    string Hello(string name);
}
```

<span data-ttu-id="5d915-116">In diesem Beispiel wird angenommen, dass der Webdienst unter folgender Adresse gehostet wird: `http://contoso.com/SayHello.svc`.</span><span class="sxs-lookup"><span data-stu-id="5d915-116">For this example, the web service will be assumed to be hosted at the following address: `http://contoso.com/SayHello.svc`</span></span>

<span data-ttu-id="5d915-117">Führen Sie in einem Windows-, macOS- oder Linux-Befehlsfenster die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="5d915-117">From a Windows, macOS, or Linux command window perform the following steps:</span></span>

1. <span data-ttu-id="5d915-118">Erstellen Sie ein Verzeichnis mit dem Namen _HelloSvcutil_ für das Projekt, und machen Sie es zu Ihrem aktuellen Verzeichnis, wie im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5d915-118">Create a directory named _HelloSvcutil_ for your project and make it your current directory, as in the following example:</span></span>

```console
mkdir HelloSvcutil
cd HelloSvcutil
```

2. <span data-ttu-id="5d915-119">Erstellen Sie mithilfe des [`dotnet new`](../tools/dotnet-new.md)-Befehls wie folgt ein neues C#-Konsolenprojekt in diesem Verzeichnis:</span><span class="sxs-lookup"><span data-stu-id="5d915-119">Create a new C# console project in that directory using the [`dotnet new`](../tools/dotnet-new.md) command as follows:</span></span>

```console
dotnet new console
```

3. <span data-ttu-id="5d915-120">Öffnen Sie die `HelloSvcutil.csproj`-Projektdatei im Editor, bearbeiten Sie das `Project`-Element, und fügen Sie mithilfe des folgenden Codes das [`dotnet-svcutil`NuGet-Paket](https://nuget.org/packages/dotnet-svcutil) als CLI-Toolverweis hinzu:</span><span class="sxs-lookup"><span data-stu-id="5d915-120">Open the `HelloSvcutil.csproj` project file in your editor, edit the `Project` element, and add the [`dotnet-svcutil` NuGet package](https://nuget.org/packages/dotnet-svcutil) as a CLI tool reference, using the following code:</span></span>

```xml
<ItemGroup>
  <DotNetCliToolReference Include="dotnet-svcutil" Version="1.0.*" />
</ItemGroup>
```

4. <span data-ttu-id="5d915-121">Stellen Sie das _dotnet-svcutil_-Paket mithilfe des [`dotnet restore`](../tools/dotnet-restore.md)-Befehls wie folgt wieder her:</span><span class="sxs-lookup"><span data-stu-id="5d915-121">Restore the _dotnet-svcutil_ package using the [`dotnet restore`](../tools/dotnet-restore.md) command as follows:</span></span>

```console
dotnet restore
```

5. <span data-ttu-id="5d915-122">Führen Sie wie folgt _dotnet_ mit dem Befehl _svcutil_ aus, um die Webdienstverweisdatei zu generieren:</span><span class="sxs-lookup"><span data-stu-id="5d915-122">Run _dotnet_ with the _svcutil_ command to generate the web service reference file as follows:</span></span>

```console
dotnet svcutil http://contoso.com/SayHello.svc
```
<span data-ttu-id="5d915-123">Die generierte Datei wird als _HelloSvcutil/ServiceReference1/Reference.cs_ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5d915-123">The generated file is saved as _HelloSvcutil/ServiceReference1/Reference.cs_.</span></span> <span data-ttu-id="5d915-124">Das _dotnet_svcutil_-Tool fügt dem Projekt auch die entsprechenden WCF-Pakete hinzu, die der Proxycode als Paketverweise benötigt.</span><span class="sxs-lookup"><span data-stu-id="5d915-124">The _dotnet_svcutil_ tool also adds to the project the appropriate WCF packages required by the proxy code as package references.</span></span>

6. <span data-ttu-id="5d915-125">Stellen Sie wie folgt die WCF-Pakete mithilfe des [`dotnet restore`](../tools/dotnet-restore.md)-Befehls wieder her:</span><span class="sxs-lookup"><span data-stu-id="5d915-125">Restore the WCF packages using the [`dotnet restore`](../tools/dotnet-restore.md) command as follows:</span></span>

```console
dotnet restore
```

7. <span data-ttu-id="5d915-126">Öffnen Sie die `Program.cs`-Datei in einem Editor, bearbeiten Sie die `Main()`-Methode, und ersetzen Sie den automatisch generierten Code durch den folgenden Code, um den Webdienst aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="5d915-126">Open the `Program.cs` file in your editor, edit the `Main()` method, and replace the auto-generated code with the following code to invoke the web service:</span></span>

```csharp
static void Main(string[] args)
{
    var client = new SayHelloClient();
    Console.WriteLine(client.HelloAsync("dotnet-svcutil").Result);
}
```

8. <span data-ttu-id="5d915-127">Führen Sie die Anwendung wie folgt mithilfe des [`dotnet run`](../tools/dotnet-run.md)-Befehls aus:</span><span class="sxs-lookup"><span data-stu-id="5d915-127">Run the application using the [`dotnet run`](../tools/dotnet-run.md) command as follows:</span></span>

```console
dotnet run
```
<span data-ttu-id="5d915-128">Die folgende Ausgabe wird angezeigt: „Hello dotnet-svcutil!“</span><span class="sxs-lookup"><span data-stu-id="5d915-128">You should see the following output: "Hello dotnet-svcutil!"</span></span>

<span data-ttu-id="5d915-129">Um eine ausführliche Beschreibung der Parameter des `dotnet-svcutil`-Tools zu erhalten, rufen Sie das Tool wie folgt mit Übergabe des Hilfeparameters auf:</span><span class="sxs-lookup"><span data-stu-id="5d915-129">For a detailed description of the `dotnet-svcutil` tool parameters, invoke the tool passing the help parameter as follows:</span></span>

```console
dotnet svcutil --help
```

## <a name="next-steps"></a><span data-ttu-id="5d915-130">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="5d915-130">Next steps</span></span>

### <a name="feedback--questions"></a><span data-ttu-id="5d915-131">Feedback und Fragen</span><span class="sxs-lookup"><span data-stu-id="5d915-131">Feedback & questions</span></span>

<span data-ttu-id="5d915-132">Wenn Sie Fragen haben oder uns Feedback geben möchten, [öffnen Sie ein Problem auf GitHub](https://github.com/dotnet/wcf/issues/new).</span><span class="sxs-lookup"><span data-stu-id="5d915-132">If you have any questions or feedback, [open an issue on GitHub](https://github.com/dotnet/wcf/issues/new).</span></span> <span data-ttu-id="5d915-133">Sie können außerdem bereits vorhandene Fragen oder Probleme [im WCF-Repository auf GitHub](https://github.com/dotnet/wcf/issues?utf8=%E2%9C%93&q=is:issue%20label:tooling) überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5d915-133">You can also review any existing questions or issues [at the WCF repo on GitHub](https://github.com/dotnet/wcf/issues?utf8=%E2%9C%93&q=is:issue%20label:tooling).</span></span>

### <a name="release-notes"></a><span data-ttu-id="5d915-134">Anmerkungen zu diesem Release</span><span class="sxs-lookup"><span data-stu-id="5d915-134">Release notes</span></span>

* <span data-ttu-id="5d915-135">Aktualisierte Informationen zu den einzelnen Versionen, einschließlich bekannter Probleme, finden Sie in den [Anmerkungen zu den jeweiligen Versionen](https://github.com/dotnet/wcf/blob/master/release-notes/dotnet-svcutil-notes.md).</span><span class="sxs-lookup"><span data-stu-id="5d915-135">Refer to the [Release notes](https://github.com/dotnet/wcf/blob/master/release-notes/dotnet-svcutil-notes.md) for updated release information, including known issues.</span></span>

### <a name="information"></a><span data-ttu-id="5d915-136">Information</span><span class="sxs-lookup"><span data-stu-id="5d915-136">Information</span></span>

* [<span data-ttu-id="5d915-137">dotnet-svcutil-NuGet-Paket</span><span class="sxs-lookup"><span data-stu-id="5d915-137">dotnet-svcutil NuGet Package</span></span>](https://nuget.org/packages/dotnet-svcutil)
