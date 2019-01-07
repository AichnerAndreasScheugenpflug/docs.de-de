---
title: Befehl „dotnet add package“
description: Der Befehl „dotnet add package“ bietet eine praktische Option zum Hinzufügen von NuGet-Paketverweisen zu einem Projekt.
ms.date: 12/04/2018
ms.openlocfilehash: 159b208feafb82e267629ea47dcef02d6b575055
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2018
ms.locfileid: "53170001"
---
# <a name="dotnet-add-package"></a><span data-ttu-id="07442-103">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="07442-103">dotnet add package</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="07442-104">Name</span><span class="sxs-lookup"><span data-stu-id="07442-104">Name</span></span>

<span data-ttu-id="07442-105">`dotnet add package`: Fügt einen Paketverweis zu einer Projektdatei hinzu.</span><span class="sxs-lookup"><span data-stu-id="07442-105">`dotnet add package` - Adds a package reference to a project file.</span></span>

## <a name="synopsis"></a><span data-ttu-id="07442-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="07442-106">Synopsis</span></span>

`dotnet add [<PROJECT>] package <PACKAGE_NAME> [-h|--help] [-f|--framework] [--interactive] [-n|--no-restore] [--package-directory] [-s|--source] [-v|--version]`

## <a name="description"></a><span data-ttu-id="07442-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07442-107">Description</span></span>

<span data-ttu-id="07442-108">Der `dotnet add package`-Befehl bietet eine praktische Option zum Hinzufügen von Paketverweisen zu einer Projektdatei.</span><span class="sxs-lookup"><span data-stu-id="07442-108">The `dotnet add package` command provides a convenient option to add a package reference to a project file.</span></span> <span data-ttu-id="07442-109">Nach dem Ausführen des Befehls wird die Kompatibilität überprüft, um sicherzustellen, dass das Paket mit den Frameworks im Projekt kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="07442-109">After running the command, there's a compatibility check to ensure the package is compatible with the frameworks in the project.</span></span> <span data-ttu-id="07442-110">Wenn die Überprüfung erfolgreich ist, wird ein `<PackageReference>`-Element zur Projektdatei hinzugefügt, und [dotnet restore](dotnet-restore.md) wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07442-110">If the check passes, a `<PackageReference>` element is added to the project file and [dotnet restore](dotnet-restore.md) is run.</span></span>

[!INCLUDE[DotNet Restore Note](../../../includes/dotnet-restore-note.md)]

<span data-ttu-id="07442-111">Beispielsweise wird durch Hinzufügen von `Newtonsoft.Json` zu *ToDo.csproj* eine Ausgabe ähnlich der folgenden erzeugt:</span><span class="sxs-lookup"><span data-stu-id="07442-111">For example, adding `Newtonsoft.Json` to *ToDo.csproj* produces output similar to the following example:</span></span>

```console
  Writing C:\Users\mairaw\AppData\Local\Temp\tmp95A8.tmp
info : Adding PackageReference for package 'Newtonsoft.Json' into project 'C:\projects\ToDo\ToDo.csproj'.
log  : Restoring packages for C:\Temp\projects\consoleproj\consoleproj.csproj...
info :   GET https://api.nuget.org/v3-flatcontainer/newtonsoft.json/index.json
info :   OK https://api.nuget.org/v3-flatcontainer/newtonsoft.json/index.json 79ms
info :   GET https://api.nuget.org/v3-flatcontainer/newtonsoft.json/12.0.1/newtonsoft.json.12.0.1.nupkg
info :   OK https://api.nuget.org/v3-flatcontainer/newtonsoft.json/12.0.1/newtonsoft.json.12.0.1.nupkg 232ms
log  : Installing Newtonsoft.Json 12.0.1.
info : Package 'Newtonsoft.Json' is compatible with all the specified frameworks in project 'C:\projects\ToDo\ToDo.csproj'.
info : PackageReference for package 'Newtonsoft.Json' version '12.0.1' added to file 'C:\projects\ToDo\ToDo.csproj'.
```

<span data-ttu-id="07442-112">Die *ToDo.csproj*-Datei enthält nun ein [`<PackageReference>`](/nuget/consume-packages/package-references-in-project-files)-Element für das Paket, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="07442-112">The *ToDo.csproj* file now contains a [`<PackageReference>`](/nuget/consume-packages/package-references-in-project-files) element for the referenced package.</span></span>

```xml
<PackageReference Include="Newtonsoft.Json" Version="12.0.1" />
```

## <a name="arguments"></a><span data-ttu-id="07442-113">Argumente</span><span class="sxs-lookup"><span data-stu-id="07442-113">Arguments</span></span>

* **`PROJECT`**

  <span data-ttu-id="07442-114">Gibt die Projektdatei an.</span><span class="sxs-lookup"><span data-stu-id="07442-114">Specifies the project file.</span></span> <span data-ttu-id="07442-115">Wenn keine angegeben ist, sucht der Befehl im aktuellen Verzeichnis nach einer Projektdatei.</span><span class="sxs-lookup"><span data-stu-id="07442-115">If not specified, the command searches the current directory for one.</span></span>

* **`PACKAGE_NAME`**

  <span data-ttu-id="07442-116">Hinzuzufügender Paketverweis.</span><span class="sxs-lookup"><span data-stu-id="07442-116">The package reference to add.</span></span>

## <a name="options"></a><span data-ttu-id="07442-117">Optionen</span><span class="sxs-lookup"><span data-stu-id="07442-117">Options</span></span>

* **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="07442-118">Fügt Paketverweise nur hinzu, wenn ein bestimmtes [Framework](../../standard/frameworks.md) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="07442-118">Adds a package reference only when targeting a specific [framework](../../standard/frameworks.md).</span></span>

* **`-h|--help`**

  <span data-ttu-id="07442-119">Druckt eine kurze Hilfe für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="07442-119">Prints out a short help for the command.</span></span>

* **`--interactive`**

  <span data-ttu-id="07442-120">Ermöglicht es dem Befehl, anzuhalten und auf Benutzereingaben oder Aktionen zu warten (z.B. um die Authentifizierung abzuschließen).</span><span class="sxs-lookup"><span data-stu-id="07442-120">Allows the command to stop and wait for user input or action (for example to complete authentication).</span></span> <span data-ttu-id="07442-121">Verfügbar ab .NET Core 2.1 SDK, Version 2.1.400 oder höher.</span><span class="sxs-lookup"><span data-stu-id="07442-121">Available since .NET Core 2.1 SDK, version 2.1.400 or later.</span></span>

* **`-n|--no-restore`**

  <span data-ttu-id="07442-122">Fügt Paketverweise hinzu, ohne eine Vorschau der Wiederherstellung und eine Kompatibilitätsüberprüfung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="07442-122">Adds a package reference without performing a restore preview and compatibility check.</span></span>

* **`--package-directory <PACKAGE_DIRECTORY>`**

  <span data-ttu-id="07442-123">Stellt das Paket im angegebenen Verzeichnis wieder her.</span><span class="sxs-lookup"><span data-stu-id="07442-123">Restores the package to the specified directory.</span></span>

* **`-s|--source <SOURCE>`**

  <span data-ttu-id="07442-124">Verwendet während des Wiederherstellungsvorgangs eine bestimmte NuGet-Paketquelle.</span><span class="sxs-lookup"><span data-stu-id="07442-124">Uses a specific NuGet package source during the restore operation.</span></span>

* **`-v|--version <VERSION>`**

  <span data-ttu-id="07442-125">Die Version des Pakets.</span><span class="sxs-lookup"><span data-stu-id="07442-125">Version of the package.</span></span>

## <a name="examples"></a><span data-ttu-id="07442-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07442-126">Examples</span></span>

* <span data-ttu-id="07442-127">Fügen Sie das `Newtonsoft.Json`-NuGet-Pakets zu einem Projekt hinzu:</span><span class="sxs-lookup"><span data-stu-id="07442-127">Add `Newtonsoft.Json` NuGet package to a project:</span></span>

  ```console
  dotnet add package Newtonsoft.Json
  ```

* <span data-ttu-id="07442-128">Fügen Sie eine bestimmte Version eines Pakets zu einem Projekt hinzu:</span><span class="sxs-lookup"><span data-stu-id="07442-128">Add a specific version of a package to a project:</span></span>

  ```console
  dotnet add ToDo.csproj package Microsoft.Azure.DocumentDB.Core -v 1.0.0
  ```

* <span data-ttu-id="07442-129">Fügen Sie ein Paket mit einer bestimmten NuGet-Quelle hinzu:</span><span class="sxs-lookup"><span data-stu-id="07442-129">Add a package using a specific NuGet source:</span></span>

  ```console
  dotnet add package Microsoft.AspNetCore.StaticFiles -s https://dotnet.myget.org/F/dotnet-core/api/v3/index.json
  ```