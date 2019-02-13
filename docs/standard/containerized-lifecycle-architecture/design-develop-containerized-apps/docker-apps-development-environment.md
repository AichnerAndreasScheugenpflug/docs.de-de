---
title: Entwicklungsumgebung für Docker-Apps
description: Lernen Sie die wichtigsten Entwicklung Tooloptionen kennen, die den Docker-Entwicklungslebenszyklus zu unterstützen.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 1d22b45a8eee9198d337df9f0b8b4b78371fa31a
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219996"
---
# <a name="development-environment-for-docker-apps"></a><span data-ttu-id="44612-103">Entwicklungsumgebung für Docker-Apps</span><span class="sxs-lookup"><span data-stu-id="44612-103">Development environment for Docker apps</span></span>

## <a name="development-tools-choices-ide-or-editor"></a><span data-ttu-id="44612-104">Auswahlmöglichkeiten für Entwicklungstools: IDE oder Editor</span><span class="sxs-lookup"><span data-stu-id="44612-104">Development tools choices: IDE or editor</span></span>

<span data-ttu-id="44612-105">Unabhängig davon, wenn Sie eine vollständige und leistungsstarke IDE oder einen einfachen und flexiblen Editor bevorzugen hat Microsoft Sie bei der Entwicklung von Docker-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="44612-105">No matter if you prefer a full and powerful IDE or a lightweight and agile editor, Microsoft has you covered when it comes to developing Docker applications.</span></span>

### <a name="visual-studio-code-and-docker-cli-cross-platform-tools-for-mac-linux-and-windows"></a><span data-ttu-id="44612-106">Visual Studio Code und Docker-CLI (Cross-Platform-Tools für Mac, Linux und Windows)</span><span class="sxs-lookup"><span data-stu-id="44612-106">Visual Studio Code and Docker CLI (cross-platform tools for Mac, Linux, and Windows)</span></span>

<span data-ttu-id="44612-107">Wenn Sie einen einfachen, plattformübergreifenden Editor, die jede beliebige Entwicklungssprache unterstützt bevorzugen, können Sie Visual Studio Code und Docker-CLI.</span><span class="sxs-lookup"><span data-stu-id="44612-107">If you prefer a lightweight, cross-platform editor supporting any development language, you can use Visual Studio Code and Docker CLI.</span></span> <span data-ttu-id="44612-108">Diese Produkte bieten eine einfachen aber widerstandsfähigen Prozess, der für den Entwicklungsworkflow optimiert von entscheidender Bedeutung ist.</span><span class="sxs-lookup"><span data-stu-id="44612-108">These products provide a simple yet robust experience, which is critical for streamlining the developer workflow.</span></span> <span data-ttu-id="44612-109">Durch die Installation von "Docker for Mac" oder "Docker für Windows" (Development Environment), können Docker-Entwickler eine einzelne Docker-CLI verwenden, um apps für Windows und Linux (Common Language Runtime Environment) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="44612-109">By installing "Docker for Mac" or "Docker for Windows" (development environment), Docker developers can use a single Docker CLI to build apps for both Windows or Linux (runtime environment).</span></span> <span data-ttu-id="44612-110">Darüber hinaus Visual Studio Code unterstützt Erweiterungen für Docker mit IntelliSense für die dockerfile-Dateien und Verknüpfungsaufgaben Docker-Befehle aus dem Editor ausführen.</span><span class="sxs-lookup"><span data-stu-id="44612-110">Plus, Visual Studio Code supports extensions for Docker with IntelliSense for Dockerfiles and shortcut-tasks to run Docker commands from the editor.</span></span>

> [!NOTE]
> <span data-ttu-id="44612-111">Informationen zum Herunterladen von Visual Studio Code finden Sie unter <https://code.visualstudio.com/download>.</span><span class="sxs-lookup"><span data-stu-id="44612-111">To download Visual Studio Code, go to <https://code.visualstudio.com/download>.</span></span>

<span data-ttu-id="44612-112">Um Docker für Mac und Windows herunterzuladen, wechseln Sie zu <https://www.docker.com/products/docker>.</span><span class="sxs-lookup"><span data-stu-id="44612-112">To download Docker for Mac and Windows, go to <https://www.docker.com/products/docker>.</span></span>

### <a name="visual-studio-with-docker-tools"></a><span data-ttu-id="44612-113">Visual Studio mit der Docker-Tools</span><span class="sxs-lookup"><span data-stu-id="44612-113">Visual Studio with Docker Tools</span></span>

<span data-ttu-id="44612-114">Wenn Sie Visual Studio 2015 verwenden, können Sie "Docker-Tools für Visual Studio". die Add-on-Tools installieren</span><span class="sxs-lookup"><span data-stu-id="44612-114">When you're using Visual Studio 2015 you can install the add-on tools "Docker Tools for Visual Studio."</span></span> <span data-ttu-id="44612-115">Für Visual Studio 2017 werden Docker-Tools bereits integrierten.</span><span class="sxs-lookup"><span data-stu-id="44612-115">For Visual Studio 2017, Docker Tools come built in already.</span></span> <span data-ttu-id="44612-116">In beiden Fällen können Sie entwickeln, ausführen und überprüfen Ihre Anwendungen direkt in der ausgewählten Docker-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="44612-116">In both cases you can develop, run, and validate your applications directly in the chosen Docker environment.</span></span> <span data-ttu-id="44612-117">F5 Ihrer Anwendung (einzelne oder mehrere Container) direkt in Docker hosten, die beim Debuggen oder drücken Sie STRG + F5 zum Bearbeiten und aktualisieren Sie die app ohne den Container erneut erstellen.</span><span class="sxs-lookup"><span data-stu-id="44612-117">F5 your application (single container or multiple containers) directly into a Docker host with debugging, or press Ctrl+F5 to edit and refresh your app without having to rebuild the container.</span></span> <span data-ttu-id="44612-118">Dies ist die einfachste und leistungsfähigere Wahl für Windows-Entwickler, die Docker-Container für Linux oder Windows erstellen.</span><span class="sxs-lookup"><span data-stu-id="44612-118">This is the simplest and more powerful choice for Windows developers creating Docker containers for Linux or Windows.</span></span>

> [!NOTE]
> <span data-ttu-id="44612-119">Um Docker-Tools für Visual Studio herunterzuladen, wechseln Sie zu <https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>.</span><span class="sxs-lookup"><span data-stu-id="44612-119">To download Docker Tools for Visual Studio, go to <https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>.</span></span>

## <a name="language-and-framework-choices"></a><span data-ttu-id="44612-120">Sprache und Framework-Optionen</span><span class="sxs-lookup"><span data-stu-id="44612-120">Language and framework choices</span></span>

<span data-ttu-id="44612-121">Sie können Docker-Anwendungen und Microsoft-Tools mit den meisten modernen Sprachen entwickeln.</span><span class="sxs-lookup"><span data-stu-id="44612-121">You can develop Docker applications and Microsoft tools with most modern languages.</span></span> <span data-ttu-id="44612-122">Im folgenden ist eine anfängliche Liste, aber Sie sind nicht darauf beschränkt:</span><span class="sxs-lookup"><span data-stu-id="44612-122">The following is an initial list, but you are not limited to it:</span></span>

-   <span data-ttu-id="44612-123">.NET Core und ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="44612-123">.NET Core and ASP.NET Core</span></span>
-   <span data-ttu-id="44612-124">Node.js</span><span class="sxs-lookup"><span data-stu-id="44612-124">Node.js</span></span>
-   <span data-ttu-id="44612-125">Golang</span><span class="sxs-lookup"><span data-stu-id="44612-125">Golang</span></span>
-   <span data-ttu-id="44612-126">Java</span><span class="sxs-lookup"><span data-stu-id="44612-126">Java</span></span>
-   <span data-ttu-id="44612-127">Ruby</span><span class="sxs-lookup"><span data-stu-id="44612-127">Ruby</span></span>
-   <span data-ttu-id="44612-128">Python</span><span class="sxs-lookup"><span data-stu-id="44612-128">Python</span></span>

<span data-ttu-id="44612-129">Im Grunde genommen können Sie alle modernen Sprache, die von Docker unter Linux oder Windows unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="44612-129">Basically, you can use any modern language supported by Docker in Linux or Windows.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="44612-130">[Zurück](deploy-azure-kubernetes-service.md)
>[Weiter](docker-apps-inner-loop-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="44612-130">[Previous](deploy-azure-kubernetes-service.md)
[Next](docker-apps-inner-loop-workflow.md)</span></span>