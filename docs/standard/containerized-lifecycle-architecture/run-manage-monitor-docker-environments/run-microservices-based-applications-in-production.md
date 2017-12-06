---
title: "Führen Sie in produktionsumgebungen verfasst und Microservices-basierte Anwendungen"
description: Lebenszyklus von Datenvolumes Docker-Anwendung mit Microsoft-Webplattform und Tools
keywords: Docker, Microservices, ASP.NET, Container
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: e7a2788098aa731699cbb201c7177e7578907673
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="run-composed-and-microservices-based-applications-in-production-environments"></a><span data-ttu-id="edb8f-104">Führen Sie in produktionsumgebungen verfasst und Microservices-basierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="edb8f-104">Run composed and microservices-based applications in production environments</span></span>

<span data-ttu-id="edb8f-105">Anwendungen aus, das mehrere Microservices in Orchestrator-Clustern, um die Komplexität der Bereitstellung und aus Sicht eines IT realisierbar bereitgestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="edb8f-105">Applications composed by multiple microservices do need to be deployed into orchestrator clusters in order to simplify the complexity of deployment and make it viable from an IT point of view.</span></span> <span data-ttu-id="edb8f-106">Ohne eine Orchestrator-Clusters wäre es sehr schwierig, bereitstellen und die horizontale Skalierung einer komplexen Microservices-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="edb8f-106">Without an orchestrator cluster, it would be very difficult to deploy and scale-out a complex microservices application.</span></span>

## <a name="introduction-to-orchestrators-schedulers-and-container-clusters"></a><span data-ttu-id="edb8f-107">Einführung in Orchestrators, Planern und Container-Clustern</span><span class="sxs-lookup"><span data-stu-id="edb8f-107">Introduction to orchestrators, schedulers, and container clusters</span></span>

<span data-ttu-id="edb8f-108">Weiter oben in diesem e-Book eingeführt *Cluster* und *Zeitplanungsmodule* als Teil der detaillierte Informationen zu Software-Architektur und Entwicklung.</span><span class="sxs-lookup"><span data-stu-id="edb8f-108">Earlier in this e-book, we introduced *clusters* and *schedulers* as part of the discussion on software architecture and development.</span></span> <span data-ttu-id="edb8f-109">Beispiele für Docker-Cluster sind Docker Containerhostclustern und Mesosphere Datacenter-Betriebssystem (DC/OS).</span><span class="sxs-lookup"><span data-stu-id="edb8f-109">Examples of Docker clusters are Docker Swarm and Mesosphere Datacenter Operating System (DC/OS).</span></span> <span data-ttu-id="edb8f-110">Beide Optionen können als Teil von Microsoft Azure-Containerdienst bereitgestellten Infrastruktur ausführen.</span><span class="sxs-lookup"><span data-stu-id="edb8f-110">Both of these can run as a part of the infrastructure provided by Microsoft Azure Container Service.</span></span>

<span data-ttu-id="edb8f-111">Wenn Anwendungen auf mehreren Hosts Systemen skalierten sind, wird die Fähigkeit zum Verwalten von jedem Hostsystem und Abstraktion für die Komplexität der zugrunde liegenden Plattform attraktiv.</span><span class="sxs-lookup"><span data-stu-id="edb8f-111">When applications are scaled-out across multiple host systems, the ability to manage each host system and abstract away the complexity of the underlying platform becomes attractive.</span></span> <span data-ttu-id="edb8f-112">Genau ist, was Orchestrators und Planer angeben.</span><span class="sxs-lookup"><span data-stu-id="edb8f-112">That is precisely what orchestrators and schedulers provide.</span></span> <span data-ttu-id="edb8f-113">Werfen wir einen kurzen Blick auf die sie hier:</span><span class="sxs-lookup"><span data-stu-id="edb8f-113">Let's take a brief look at them here:</span></span>

-   <span data-ttu-id="edb8f-114">**Zeitplanungsmodule*** *"Planung" bezieht sich auf die Möglichkeit für einen Administrator, um eine Datei auf einem Hostsystem zu laden, die zum Ausführen von eines bestimmten Containers herstellt.</span><span class="sxs-lookup"><span data-stu-id="edb8f-114">**Schedulers*** *"Scheduling" refers to the ability for an administrator to load a service file onto a host system that establishes how to run a specific container.</span></span> <span data-ttu-id="edb8f-115">Starten der Container in einem Cluster Docker ist als Planung bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="edb8f-115">Launching containers in a Docker cluster tends to be known as scheduling.</span></span> <span data-ttu-id="edb8f-116">Obwohl planen, die auf den bestimmten Vorgang des Ladens der Dienstdefinition in einer allgemeineren Sinne bezieht sich sind Planer für Berichterstellungsprozess mit Init-System zum Verwalten von Diensten in die benötigte Kapazität des Hosts verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="edb8f-116">Although scheduling refers to the specific act of loading the service definition, in a more general sense, schedulers are responsible for hooking into a host's init system to manage services in whatever capacity needed.</span></span>

<span data-ttu-id="edb8f-117">Ein Cluster Zeitplanungsmodul verfügt über mehrere Ziele: Effizientes Verwenden von Clusterressourcen, arbeiten mit vom Benutzer anzugebende platzierungsbeschränkungen, Planen von Anwendungen schnell, um sie nicht in einen Status "Ausstehend" zu belassen, müssen ein Maß "Ausgewogenheit," robust sind, um Fehler, wird und immer verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="edb8f-117">A cluster scheduler has multiple goals: using the cluster's resources efficiently, working with user-supplied placement constraints, scheduling applications rapidly to not leave them in a pending state, having a degree of "fairness," being robust to errors, and always be available.</span></span>

-   <span data-ttu-id="edb8f-118">**Orchestrierung*** *Plattformen ausdehnen Lebenszyklus komplexer, multicontainer Arbeitslasten auf einem Cluster mit Hosts bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="edb8f-118">**Orchestration*** *Platforms extend life-cycle management capabilities to complex, multicontainer workloads deployed on a cluster of hosts.</span></span> <span data-ttu-id="edb8f-119">Durch die Hostinfrastruktur werden so abstrahiert, bieten Orchestrierung Tools Benutzern eine Möglichkeit, den gesamten Cluster als ein einzelnes Bereitstellungsziel zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="edb8f-119">By abstracting the host infrastructure, orchestration tools give users a way to treat the entire cluster as a single deployment target.</span></span>

<span data-ttu-id="edb8f-120">Der Prozess der Orchestrierung umfasst Tools und eine Plattform, die alle Aspekte der anwendungsverwaltung aus der ersten Platzierung oder Bereitstellung pro Container automatisiert werden kann; Verschieben von Containern auf verschiedenen Hosts je nach Zustand oder die Leistung des Hosts; versionsverwaltung und parallelen Updates und Integritätsüberwachung von Funktionen, die Skalierung und das Failover zu unterstützen; und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="edb8f-120">The process of orchestration involves tooling and a platform that can automate all aspects of application management from initial placement or deployment per container; moving containers to different hosts depending on its host's health or performance; versioning and rolling updates and health monitoring functions that support scaling and failover; and many more.</span></span>

<span data-ttu-id="edb8f-121">Orchestrierung ist ein breites Begriff aus, auf den Container zu planen, Clusterverwaltung und möglicherweise die Bereitstellung zusätzlicher Hosts verweist.</span><span class="sxs-lookup"><span data-stu-id="edb8f-121">Orchestration is a broad term that refers to container scheduling, cluster management, and possibly the provisioning of additional hosts.</span></span>

<span data-ttu-id="edb8f-122">Die Funktionen von Orchestrators und Planer sind sehr komplex zu entwickeln und Erstellen von Grund auf neu, und daher in der Regel sollten stellen mithilfe der Orchestrierung Lösungen von Lieferanten angeboten.</span><span class="sxs-lookup"><span data-stu-id="edb8f-122">The capabilities provided by orchestrators and schedulers are very complex to develop and create from scratch, and therefore you usually would want to make use of orchestration solutions offered by vendors.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="edb8f-123">[Vorherigen] (index.md) [weiter] (Verwalten von-Production-Docker-environments.md)</span><span class="sxs-lookup"><span data-stu-id="edb8f-123">[Previous] (index.md) [Next] (manage-production-docker-environments.md)</span></span>