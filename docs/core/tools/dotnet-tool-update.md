---
title: Befehl „dotnet tool update“
description: Der Befehl „dotnet tool update“ aktualisiert die angegebenen globalen .NET Core-Tools auf Ihrem Computer.
ms.date: 05/29/2018
ms.openlocfilehash: 2716f7f88ffe364bebacf970d7152f5509edc888
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169735"
---
# <a name="dotnet-tool-update"></a><span data-ttu-id="993ef-103">dotnet tool update</span><span class="sxs-lookup"><span data-stu-id="993ef-103">dotnet tool update</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="993ef-104">Name</span><span class="sxs-lookup"><span data-stu-id="993ef-104">Name</span></span>

<span data-ttu-id="993ef-105">`dotnet tool update`: Aktualisiert das angegebene [globale .NET Core-Tool](global-tools.md) auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="993ef-105">`dotnet tool update` - Updates the specified [.NET Core Global Tool](global-tools.md) on your machine.</span></span>

## <a name="synopsis"></a><span data-ttu-id="993ef-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="993ef-106">Synopsis</span></span>

```console
dotnet tool update <PACKAGE_NAME> <-g|--global> [--configfile] [--framework] [-v|--verbosity]
dotnet tool update <PACKAGE_NAME> <--tool-path> [--configfile] [--framework] [-v|--verbosity]
dotnet tool update <-h|--help>
```

## <a name="description"></a><span data-ttu-id="993ef-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="993ef-107">Description</span></span>

<span data-ttu-id="993ef-108">Der Befehl `dotnet tool update` ermöglicht Ihnen das Aktualisieren der globalen .NET Core-Tools auf Ihrem Computer auf die neueste stabile Version des Pakets.</span><span class="sxs-lookup"><span data-stu-id="993ef-108">The `dotnet tool update` command provides a way for you to update .NET Core Global Tools on your machine to the latest stable version of the package.</span></span> <span data-ttu-id="993ef-109">Der Befehl deinstalliert und installiert ein Tool neu, sodass es aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="993ef-109">The command uninstalls and reinstalls a tool, effectively updating it.</span></span> <span data-ttu-id="993ef-110">Zum Verwenden des Befehls müssen Sie entweder mit der Option `--global` angeben, dass Sie ein Tool einer benutzerweiten Installation aktualisieren möchten, oder mit der Option `--tool-path` einen Pfad zum installierten Tool angeben.</span><span class="sxs-lookup"><span data-stu-id="993ef-110">To use the command, you either have to specify that you want to update a tool from a user-wide installation using the `--global` option or specify a path to where the tool is installed using the `--tool-path` option.</span></span>

## <a name="arguments"></a><span data-ttu-id="993ef-111">Argumente</span><span class="sxs-lookup"><span data-stu-id="993ef-111">Arguments</span></span>

`PACKAGE_NAME`

<span data-ttu-id="993ef-112">Name oder ID des NuGet-Pakets, das das zu aktualisierende globale .NET Core-Tool enthält.</span><span class="sxs-lookup"><span data-stu-id="993ef-112">Name/ID of the NuGet package that contains the .NET Core Global Tool to update.</span></span> <span data-ttu-id="993ef-113">Mithilfe des Befehls [dotnet tool list](dotnet-tool-list.md) können Sie den Paketnamen abrufen.</span><span class="sxs-lookup"><span data-stu-id="993ef-113">You can find the package name using the [dotnet tool list](dotnet-tool-list.md) command.</span></span>

## <a name="options"></a><span data-ttu-id="993ef-114">Optionen</span><span class="sxs-lookup"><span data-stu-id="993ef-114">Options</span></span>

`--add-source <SOURCE>`

<span data-ttu-id="993ef-115">Fügt eine zusätzliche NuGet-Paketquelle für die Installation hinzu.</span><span class="sxs-lookup"><span data-stu-id="993ef-115">Adds an additional NuGet package source to use during installation.</span></span>

`--configfile <FILE>`

<span data-ttu-id="993ef-116">Die zu verwendende NuGet-Konfigurationsdatei (*nuget.config*).</span><span class="sxs-lookup"><span data-stu-id="993ef-116">The NuGet configuration (*nuget.config*) file to use.</span></span>

`--framework <FRAMEWORK>`

<span data-ttu-id="993ef-117">Legt das [Zielframework](../../standard/frameworks.md) des zu aktualisierenden Tools fest.</span><span class="sxs-lookup"><span data-stu-id="993ef-117">Specifies the [target framework](../../standard/frameworks.md) to update the tool for.</span></span>

`-g|--global`

<span data-ttu-id="993ef-118">Gibt an, dass das Update für ein benutzerweites Tool ist.</span><span class="sxs-lookup"><span data-stu-id="993ef-118">Specifies that the update is for a user-wide tool.</span></span> <span data-ttu-id="993ef-119">Kann nicht mit der Option `--tool-path` kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="993ef-119">Can't be combined with the `--tool-path` option.</span></span> <span data-ttu-id="993ef-120">Wenn Sie diese Option nicht angeben, müssen Sie die Option `--tool-path` angeben.</span><span class="sxs-lookup"><span data-stu-id="993ef-120">If you don't specify this option, you must specify the `--tool-path` option.</span></span>

`-h|--help`

<span data-ttu-id="993ef-121">Druckt eine kurze Hilfe für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="993ef-121">Prints out a short help for the command.</span></span>

`--tool-path <PATH>`

<span data-ttu-id="993ef-122">Gibt den Speicherort an, in dem das globale Tool installiert ist.</span><span class="sxs-lookup"><span data-stu-id="993ef-122">Specifies the location where the Global Tool is installed.</span></span> <span data-ttu-id="993ef-123">„PATH“ kann absolut oder relativ sein.</span><span class="sxs-lookup"><span data-stu-id="993ef-123">PATH can be absolute or relative.</span></span> <span data-ttu-id="993ef-124">Kann nicht mit der Option `--global` kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="993ef-124">Can't be combined with the `--global` option.</span></span> <span data-ttu-id="993ef-125">Wenn Sie diese Option nicht angeben, müssen Sie die Option `--global` angeben.</span><span class="sxs-lookup"><span data-stu-id="993ef-125">If you don't specify this option, you must specify the `--global` option.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="993ef-126">Legt den Ausführlichkeitsgrad für den Befehl fest.</span><span class="sxs-lookup"><span data-stu-id="993ef-126">Sets the verbosity level of the command.</span></span> <span data-ttu-id="993ef-127">Zulässige Werte sind `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` und `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="993ef-127">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

## <a name="examples"></a><span data-ttu-id="993ef-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="993ef-128">Examples</span></span>

<span data-ttu-id="993ef-129">Aktualisiert das globale Tool [dotnetsay](https://www.nuget.org/packages/dotnetsay/):</span><span class="sxs-lookup"><span data-stu-id="993ef-129">Updates the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool:</span></span>

`dotnet tool update -g dotnetsay`

<span data-ttu-id="993ef-130">Aktualisiert das globale Tool [dotnetsay](https://www.nuget.org/packages/dotnetsay/), das sich in einem bestimmten Windows-Ordner befindet:</span><span class="sxs-lookup"><span data-stu-id="993ef-130">Updates the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool located on a specific Windows folder:</span></span>

`dotnet tool update dotnetsay --tool-path c:\global-tools`

<span data-ttu-id="993ef-131">Aktualisiert das globale Tool [dotnetsay](https://www.nuget.org/packages/dotnetsay/), das sich in einem bestimmten Linux-/macOS-Ordner befindet:</span><span class="sxs-lookup"><span data-stu-id="993ef-131">Updates the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool located on a specific Linux/macOS folder:</span></span>

`dotnet tool update dotnetsay --tool-path ~/bin`

## <a name="see-also"></a><span data-ttu-id="993ef-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="993ef-132">See also</span></span>

* [<span data-ttu-id="993ef-133">.NET Core Global Tools (Globale .NET Core-Tools)</span><span class="sxs-lookup"><span data-stu-id="993ef-133">.NET Core Global Tools</span></span>](global-tools.md)