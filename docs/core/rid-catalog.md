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
# <a name="net-core-rid-catalog"></a><span data-ttu-id="33c60-103">.NET Core-RID-Katalog</span><span class="sxs-lookup"><span data-stu-id="33c60-103">.NET Core RID Catalog</span></span>

<span data-ttu-id="33c60-104">RID ist die Kurzform für *Runtime-ID* (Laufzeitbezeichner).</span><span class="sxs-lookup"><span data-stu-id="33c60-104">RID is short for *Runtime IDentifier*.</span></span> <span data-ttu-id="33c60-105">Mithilfe von RID-Werten werden Zielplattformen identifiziert, unter der die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33c60-105">RID values are used to identify target platforms where the application runs.</span></span>
<span data-ttu-id="33c60-106">Sie werden von .NET-Paketen verwendet, um plattformspezifische Ressourcen in NuGet-Paketen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="33c60-106">They're used by .NET packages to represent platform-specific assets in NuGet packages.</span></span> <span data-ttu-id="33c60-107">Die folgenden Werte sind Beispiele für RIDs: `linux-x64`, `ubuntu.14.04-x64`, `win7-x64` oder `osx.10.12-x64`.</span><span class="sxs-lookup"><span data-stu-id="33c60-107">The following values are examples of RIDs: `linux-x64`, `ubuntu.14.04-x64`, `win7-x64`, or `osx.10.12-x64`.</span></span>
<span data-ttu-id="33c60-108">Für die Pakete mit nativen Abhängigkeiten legt die RID fest, auf welchen Plattformen das Paket wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="33c60-108">For the packages with native dependencies, the RID designates on which platforms the package can be restored.</span></span>

<span data-ttu-id="33c60-109">Eine einzelne RID kann im `<RuntimeIdentifier>`-Element Ihrer Projektdatei festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="33c60-109">A single RID can be set in the `<RuntimeIdentifier>` element of your project file.</span></span> <span data-ttu-id="33c60-110">Mehrere RIDs können als Liste mit Semikolon als Trennzeichen im `<RuntimeIdentifiers>`-Element der Projektdatei definiert werden.</span><span class="sxs-lookup"><span data-stu-id="33c60-110">Multiple RIDs can be defined as a semicolon-delimited list in the project file's `<RuntimeIdentifiers>` element.</span></span> <span data-ttu-id="33c60-111">Sie können auch über die Option `--runtime` mit den folgenden [.NET Core-CLI-Befehlen](./tools/index.md) verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="33c60-111">They're also used via the `--runtime` option with the following [.NET Core CLI commands](./tools/index.md):</span></span>

- [<span data-ttu-id="33c60-112">dotnet build</span><span class="sxs-lookup"><span data-stu-id="33c60-112">dotnet build</span></span>](./tools/dotnet-build.md)
- [<span data-ttu-id="33c60-113">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="33c60-113">dotnet clean</span></span>](./tools/dotnet-clean.md)
- [<span data-ttu-id="33c60-114">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="33c60-114">dotnet pack</span></span>](./tools/dotnet-pack.md)
- [<span data-ttu-id="33c60-115">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="33c60-115">dotnet publish</span></span>](./tools/dotnet-publish.md)
- [<span data-ttu-id="33c60-116">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="33c60-116">dotnet restore</span></span>](./tools/dotnet-restore.md)
- [<span data-ttu-id="33c60-117">dotnet run</span><span class="sxs-lookup"><span data-stu-id="33c60-117">dotnet run</span></span>](./tools/dotnet-run.md)
- [<span data-ttu-id="33c60-118">dotnet store</span><span class="sxs-lookup"><span data-stu-id="33c60-118">dotnet store</span></span>](./tools/dotnet-store.md)

<span data-ttu-id="33c60-119">RIDs, die konkrete Betriebssysteme darstellen, weisen in der Regel folgendes Muster auf: `[os].[version]-[architecture]-[additional qualifiers]`, wobei:</span><span class="sxs-lookup"><span data-stu-id="33c60-119">RIDs that represent concrete operating systems usually follow this pattern: `[os].[version]-[architecture]-[additional qualifiers]` where:</span></span>

- <span data-ttu-id="33c60-120">`[os]` ist der Moniker des Betriebs-/Plattformsystems.</span><span class="sxs-lookup"><span data-stu-id="33c60-120">`[os]` is the operating/platform system moniker.</span></span> <span data-ttu-id="33c60-121">Beispielsweise `ubuntu`.</span><span class="sxs-lookup"><span data-stu-id="33c60-121">For example, `ubuntu`.</span></span>

- <span data-ttu-id="33c60-122">`[version]` ist die Version des Betriebssystems in Form einer durch Punkte getrennten (`.`) Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="33c60-122">`[version]` is the operating system version in the form of a dot-separated (`.`) version number.</span></span> <span data-ttu-id="33c60-123">Beispielsweise `15.10`.</span><span class="sxs-lookup"><span data-stu-id="33c60-123">For example, `15.10`.</span></span>

  - <span data-ttu-id="33c60-124">Die Version sollte **keine** Marketingversion sein, da diese häufig mehrere separate Versionen des Betriebssystems mit unterschiedlichen Plattform-API-Oberflächen darstellt.</span><span class="sxs-lookup"><span data-stu-id="33c60-124">The version **shouldn't** be marketing versions, as they often represent multiple discrete versions of the operating system with varying platform API surface area.</span></span>

- <span data-ttu-id="33c60-125">`[architecture]` ist die Prozessorarchitektur.</span><span class="sxs-lookup"><span data-stu-id="33c60-125">`[architecture]` is the processor architecture.</span></span> <span data-ttu-id="33c60-126">Beispielsweise `x86`, `x64`, `arm` oder `arm64`.</span><span class="sxs-lookup"><span data-stu-id="33c60-126">For example: `x86`, `x64`, `arm`, or `arm64`.</span></span>

- <span data-ttu-id="33c60-127">`[additional qualifiers]` differenziert die verschiedenen Plattformen noch stärker.</span><span class="sxs-lookup"><span data-stu-id="33c60-127">`[additional qualifiers]` further differentiate different platforms.</span></span> <span data-ttu-id="33c60-128">Beispiel: `aot` oder `corert`.</span><span class="sxs-lookup"><span data-stu-id="33c60-128">For example: `aot` or `corert`.</span></span>

## <a name="rid-graph"></a><span data-ttu-id="33c60-129">RID-Diagramm</span><span class="sxs-lookup"><span data-stu-id="33c60-129">RID graph</span></span>

<span data-ttu-id="33c60-130">Das RID-Diagramm oder Runtimefallbackdiagramm ist eine Liste von RIDs, die miteinander kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="33c60-130">The RID graph or runtime fallback graph is a list of RIDs that are compatible with each other.</span></span> <span data-ttu-id="33c60-131">Die RIDs werden im Paket [Microsoft.NETCore.Platforms](https://www.nuget.org/packages/Microsoft.NETCore.Platforms/) definiert.</span><span class="sxs-lookup"><span data-stu-id="33c60-131">The RIDs are defined in the [Microsoft.NETCore.Platforms](https://www.nuget.org/packages/Microsoft.NETCore.Platforms/) package.</span></span> <span data-ttu-id="33c60-132">Die Liste der unterstützten RIDs und das RID-Diagramm finden Sie in der Datei [*runtime.json*](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) im CoreFX-Repository.</span><span class="sxs-lookup"><span data-stu-id="33c60-132">You can see the list of supported RIDs and the RID graph in the [*runtime.json*](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) file, which is located at the CoreFX repo.</span></span> <span data-ttu-id="33c60-133">In dieser Datei können Sie sehen, dass alle RIDs außer der Basis-RID eine `"#import"`-Anweisung enthalten.</span><span class="sxs-lookup"><span data-stu-id="33c60-133">In this file, you can see that all RIDs, except for the base one, contain an `"#import"` statement.</span></span> <span data-ttu-id="33c60-134">Diese Anweisungen geben kompatible RIDs an.</span><span class="sxs-lookup"><span data-stu-id="33c60-134">These statements indicate compatible RIDs.</span></span>

<span data-ttu-id="33c60-135">Bei NuGet-Wiederherstellungspaketen wird versucht, eine genaue Übereinstimmung für die angegebene Runtime zu finden.</span><span class="sxs-lookup"><span data-stu-id="33c60-135">When NuGet restores packages, it tries to find an exact match for the specified runtime.</span></span>
<span data-ttu-id="33c60-136">Wenn keine genaue Übereinstimmung gefunden wird, durchläuft das NuGet erneut das Diagramm, bis es das System mit der größten Kompatibilität gemäß dem RID-Diagramm findet.</span><span class="sxs-lookup"><span data-stu-id="33c60-136">If an exact match is not found, NuGet walks back the graph until it finds the closest compatible system according to the RID graph.</span></span>

<span data-ttu-id="33c60-137">Im Folgenden wird ein Beispiel für den tatsächlichen Eintrag für die `osx.10.12-x64`-RID vorgestellt:</span><span class="sxs-lookup"><span data-stu-id="33c60-137">The following example is the actual entry for the `osx.10.12-x64` RID:</span></span>

```json
"osx.10.12-x64": {
    "#import": [ "osx.10.12", "osx.10.11-x64" ]
}
```

<span data-ttu-id="33c60-138">Die oben genannte RID gibt an, dass `osx.10.12-x64` `osx.10.11-x64` importiert.</span><span class="sxs-lookup"><span data-stu-id="33c60-138">The above RID specifies that `osx.10.12-x64` imports `osx.10.11-x64`.</span></span> <span data-ttu-id="33c60-139">Bei NuGet-Wiederherstellungspaketen wird daher versucht, eine genaue Übereinstimmung für `osx.10.12-x64` im Paket zu finden.</span><span class="sxs-lookup"><span data-stu-id="33c60-139">So, when NuGet restores packages, it tries to find an exact match for  `osx.10.12-x64` in the package.</span></span> <span data-ttu-id="33c60-140">Wenn das NuGet die angegebene Runtime nicht finden kann, kann es beispielsweise Wiederherstellungspakete mit den Runtimes `osx.10.11-x64` finden.</span><span class="sxs-lookup"><span data-stu-id="33c60-140">If NuGet cannot find the specific runtime, it can restore packages that specify `osx.10.11-x64` runtimes, for example.</span></span>

<span data-ttu-id="33c60-141">Das folgende Beispiel zeigt, wie ein etwas größeres RID-Diagramm auch in der Datei *runtime.json* definiert wird:</span><span class="sxs-lookup"><span data-stu-id="33c60-141">The following example shows a slightly bigger RID graph also defined in the *runtime.json*  file:</span></span>

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

<span data-ttu-id="33c60-142">Alle RIDs bilden schließlich wieder den Stamm `any`-RID ab.</span><span class="sxs-lookup"><span data-stu-id="33c60-142">All RIDs eventually map back to the root `any` RID.</span></span>

<span data-ttu-id="33c60-143">Es gibt einige Aspekte zu RIDs, die Sie bei der Verwendung bedenken müssen:</span><span class="sxs-lookup"><span data-stu-id="33c60-143">There are some considerations about RIDs that you have to keep in mind when working with them:</span></span>

- <span data-ttu-id="33c60-144">RIDs sind **opake Zeichenfolgen** und sollten als Blackboxes behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="33c60-144">RIDs are **opaque strings** and should be treated as black boxes.</span></span>
- <span data-ttu-id="33c60-145">Erstellen Sie RIDs nicht programmgesteuert.</span><span class="sxs-lookup"><span data-stu-id="33c60-145">Don't build RIDs programmatically.</span></span>
- <span data-ttu-id="33c60-146">Verwenden Sie RIDs, die bereits für die Plattform definiert sind.</span><span class="sxs-lookup"><span data-stu-id="33c60-146">Use RIDs that are already defined for the platform.</span></span>
- <span data-ttu-id="33c60-147">Die RIDs müssen spezifisch sein. Leiten Sie daher keine Annahmen anhand des tatsächlichen RID-Werts ab.</span><span class="sxs-lookup"><span data-stu-id="33c60-147">The RIDs need to be specific, so don't assume anything from the actual RID value.</span></span>

## <a name="using-rids"></a><span data-ttu-id="33c60-148">Die Verwendung von RIDs</span><span class="sxs-lookup"><span data-stu-id="33c60-148">Using RIDs</span></span>

<span data-ttu-id="33c60-149">Um RIDs verwenden zu können, müssen Sie wissen, welche RIDs es gibt.</span><span class="sxs-lookup"><span data-stu-id="33c60-149">To be able to use RIDs, you have to know which RIDs exist.</span></span> <span data-ttu-id="33c60-150">Zur Plattform werden regelmäßig neue Werte hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="33c60-150">New values are added regularly to the platform.</span></span>
<span data-ttu-id="33c60-151">Prüfen Sie die Datei [runtime.json](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) im CoreFX-Repository auf die neueste und vollständige Version.</span><span class="sxs-lookup"><span data-stu-id="33c60-151">For the latest and complete version, see the [runtime.json](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) file on CoreFX repo.</span></span>

<span data-ttu-id="33c60-152">Mit dem .NET Core 2.0 SDK wird das Konzept von portablen RIDs eingeführt.</span><span class="sxs-lookup"><span data-stu-id="33c60-152">.NET Core 2.0 SDK introduces the concept of portable RIDs.</span></span> <span data-ttu-id="33c60-153">Dabei handelt es sich um neue zum RID-Diagramm hinzugefügte Werte, die nicht an eine bestimmte Version oder Betriebssystemverteilung gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="33c60-153">They are new values added to the RID graph that aren't tied to a specific version or OS distribution.</span></span> <span data-ttu-id="33c60-154">Diese sind besonders bei mehreren Linux-Verteilungen nützlich.</span><span class="sxs-lookup"><span data-stu-id="33c60-154">They're particularly useful when dealing with multiple Linux distros.</span></span>

<span data-ttu-id="33c60-155">Die folgende Liste enthält die am häufigsten verwendeten RIDs für jedes Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="33c60-155">The following list shows the most common RIDs used for each OS.</span></span> <span data-ttu-id="33c60-156">Die Werte `arm` oder `corert` werden nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="33c60-156">It doesn't cover `arm` or `corert` values.</span></span>

## <a name="windows-rids"></a><span data-ttu-id="33c60-157">RIDs für Windows</span><span class="sxs-lookup"><span data-stu-id="33c60-157">Windows RIDs</span></span>

- <span data-ttu-id="33c60-158">Portabel</span><span class="sxs-lookup"><span data-stu-id="33c60-158">Portable</span></span>
  - `win-x86`
  - `win-x64`
- <span data-ttu-id="33c60-159">Windows 7 / Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33c60-159">Windows 7 / Windows Server 2008 R2</span></span>
  - `win7-x64`
  - `win7-x86`
- <span data-ttu-id="33c60-160">Windows 8 / Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33c60-160">Windows 8 / Windows Server 2012</span></span>
  - `win8-x64`
  - `win8-x86`
  - `win8-arm`
- <span data-ttu-id="33c60-161">Windows 8.1 / Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="33c60-161">Windows 8.1 / Windows Server 2012 R2</span></span>
  - `win81-x64`
  - `win81-x86`
  - `win81-arm`
- <span data-ttu-id="33c60-162">Windows 10 / Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="33c60-162">Windows 10 / Windows Server 2016</span></span>
  - `win10-x64`
  - `win10-x86`
  - `win10-arm`
  - `win10-arm64`

<span data-ttu-id="33c60-163">Weitere Informationen finden Sie unter [Prerequisites for .NET Core on Mac (Erforderliche Komponenten für .NET Core unter Mac)](windows-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="33c60-163">See [Prerequisites for .NET Core on Windows](windows-prerequisites.md) for more information.</span></span>

## <a name="linux-rids"></a><span data-ttu-id="33c60-164">RIDs für Linux</span><span class="sxs-lookup"><span data-stu-id="33c60-164">Linux RIDs</span></span>

- <span data-ttu-id="33c60-165">Portabel</span><span class="sxs-lookup"><span data-stu-id="33c60-165">Portable</span></span>
  - `linux-x64`
- <span data-ttu-id="33c60-166">CentOS</span><span class="sxs-lookup"><span data-stu-id="33c60-166">CentOS</span></span>
  - `centos-x64`
  - `centos.7-x64`
- <span data-ttu-id="33c60-167">Debian</span><span class="sxs-lookup"><span data-stu-id="33c60-167">Debian</span></span>
  - `debian-x64`
  - `debian.8-x64`
  - <span data-ttu-id="33c60-168">`debian.9-x64` (.NET Core 1.1 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-168">`debian.9-x64` (.NET Core 1.1 or later versions)</span></span>
- <span data-ttu-id="33c60-169">Fedora</span><span class="sxs-lookup"><span data-stu-id="33c60-169">Fedora</span></span>
  - `fedora-x64`
  - `fedora.27-x64`
  - <span data-ttu-id="33c60-170">`fedora.28-x64` (.NET Core 1.1 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-170">`fedora.28-x64` (.NET Core 1.1 or later versions)</span></span>
- <span data-ttu-id="33c60-171">Gentoo (.NET Core 2.0 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-171">Gentoo (.NET Core 2.0 or later versions)</span></span>
  - `gentoo-x64`
- <span data-ttu-id="33c60-172">openSUSE</span><span class="sxs-lookup"><span data-stu-id="33c60-172">openSUSE</span></span>
  - `opensuse-x64`
  - `opensuse.42.3-x64`
- <span data-ttu-id="33c60-173">Oracle Linux</span><span class="sxs-lookup"><span data-stu-id="33c60-173">Oracle Linux</span></span>
  - `ol-x64`
  - `ol.7-x64`
  - `ol.7.0-x64`
  - `ol.7.1-x64`
  - `ol.7.2-x64`
  - `ol.7.3-x64`
  - `ol.7.4-x64`
- <span data-ttu-id="33c60-174">Red Hat Enterprise Linux</span><span class="sxs-lookup"><span data-stu-id="33c60-174">Red Hat Enterprise Linux</span></span>
  - `rhel-x64`
  - <span data-ttu-id="33c60-175">`rhel.6-x64` (.NET Core 2.0 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-175">`rhel.6-x64` (.NET Core 2.0 or later versions)</span></span>
  - `rhel.7-x64`
  - `rhel.7.1-x64`
  - `rhel.7.2-x64`
  - <span data-ttu-id="33c60-176">`rhel.7.3-x64` (.NET Core 2.0 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-176">`rhel.7.3-x64` (.NET Core 2.0 or later versions)</span></span>
  - <span data-ttu-id="33c60-177">`rhel.7.4-x64` (.NET Core 2.0 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-177">`rhel.7.4-x64` (.NET Core 2.0 or later versions)</span></span>
- <span data-ttu-id="33c60-178">Tizen (.NET Core 2.0 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-178">Tizen (.NET Core 2.0 or later versions)</span></span>
  - `tizen`
  - `tizen.4.0.0`
  - `tizen.5.0.0`
- <span data-ttu-id="33c60-179">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="33c60-179">Ubuntu</span></span>
  - `ubuntu-x64`
  - `ubuntu.14.04-x64`
  - `ubuntu.16.04-x64`
  - `ubuntu.17.10-x64`
  - `ubuntu.18.04-x64`
- <span data-ttu-id="33c60-180">Ubuntu-Ableitungen</span><span class="sxs-lookup"><span data-stu-id="33c60-180">Ubuntu derivatives</span></span>
  - `linuxmint.17-x64`
  - `linuxmint.17.1-x64`
  - `linuxmint.17.2-x64`
  - `linuxmint.17.3-x64`
  - <span data-ttu-id="33c60-181">`linuxmint.18-x64` (.NET Core 2.0 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-181">`linuxmint.18-x64` (.NET Core 2.0 or later versions)</span></span>
  - <span data-ttu-id="33c60-182">`linuxmint.18.1-x64` (.NET Core 2.0 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-182">`linuxmint.18.1-x64` (.NET Core 2.0 or later versions)</span></span>
  - <span data-ttu-id="33c60-183">`linuxmint.18.2-x64` (.NET Core 2.0 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-183">`linuxmint.18.2-x64` (.NET Core 2.0 or later versions)</span></span>
  - <span data-ttu-id="33c60-184">`linuxmint.18.3-x64` (.NET Core 2.0 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-184">`linuxmint.18.3-x64` (.NET Core 2.0 or later versions)</span></span>
- <span data-ttu-id="33c60-185">SUSE Enterprise Linux (SLES) (.NET Core 2.0 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-185">SUSE Enterprise Linux (SLES) (.NET Core 2.0 or later versions)</span></span>
  - `sles-x64`
  - `sles.12-x64`
  - `sles.12.1-x64`
  - `sles.12.2-x64`
  - `sles.12.3-x64`
- <span data-ttu-id="33c60-186">Alpine Linux (.NET Core 2.1 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-186">Alpine Linux (.NET Core 2.1 or later versions)</span></span>
  - `alpine-x64`
  - `alpine.3.7-x64`

<span data-ttu-id="33c60-187">Weitere Informationen finden Sie unter [Prerequisites for .NET Core on Linux (Erforderliche Komponenten für .NET Core unter Linux)](linux-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="33c60-187">See [Prerequisites for .NET Core on Linux](linux-prerequisites.md) for more information.</span></span>

## <a name="macos-rids"></a><span data-ttu-id="33c60-188">Relative IDs für macOS</span><span class="sxs-lookup"><span data-stu-id="33c60-188">macOS RIDs</span></span>

<span data-ttu-id="33c60-189">Relative IDs für macOS verwenden das ältere Branding „OSX“.</span><span class="sxs-lookup"><span data-stu-id="33c60-189">macOS RIDs use the older "OSX" branding.</span></span>

- <span data-ttu-id="33c60-190">`osx-x64` (.NET Core 2.0 oder höher, die mindestens erforderliche Version ist `osx.10.12-x64`)</span><span class="sxs-lookup"><span data-stu-id="33c60-190">`osx-x64` (.NET Core 2.0 or later versions, minimum version is `osx.10.12-x64`)</span></span>
- `osx.10.10-x64`
- `osx.10.11-x64`
- <span data-ttu-id="33c60-191">`osx.10.12-x64` (.NET Core 1.1 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-191">`osx.10.12-x64` (.NET Core 1.1 or later versions)</span></span>
- `osx.10.13-x64`

<span data-ttu-id="33c60-192">Weitere Informationen finden Sie unter [Prerequisites for .NET Core on macOS (Erforderliche Komponenten für .NET Core unter macOS)](macos-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="33c60-192">See [Prerequisites for .NET Core on macOS](macos-prerequisites.md) for more information.</span></span>

## <a name="android-rids-net-core-20-or-later-versions"></a><span data-ttu-id="33c60-193">Android-RIDs (.NET Core 2.0 oder höher)</span><span class="sxs-lookup"><span data-stu-id="33c60-193">Android RIDs (.NET Core 2.0 or later versions)</span></span>

- `android`
- `android.21`

## <a name="see-also"></a><span data-ttu-id="33c60-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33c60-194">See also</span></span>

- [<span data-ttu-id="33c60-195">Runtime-IDs</span><span class="sxs-lookup"><span data-stu-id="33c60-195">Runtime IDs</span></span>](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/readme.md)
