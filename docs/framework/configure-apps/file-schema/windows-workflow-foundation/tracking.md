---
title: '&lt;tracking&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: fd9b50ed-98a1-4518-836d-e4e02c670822
ms.openlocfilehash: 26f8c6f82ba752c9d431e30771256a58df9b14a8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54553580"
---
# <a name="lttrackinggt"></a><span data-ttu-id="2dab6-102">&lt;tracking&gt;</span><span class="sxs-lookup"><span data-stu-id="2dab6-102">&lt;tracking&gt;</span></span>
<span data-ttu-id="2dab6-103">Stellt einen Konfigurationsabschnitt zum Definieren von Nachverfolgungseinstellungen für einen Workflowdienst dar.</span><span class="sxs-lookup"><span data-stu-id="2dab6-103">Represents a configuration section for defining tracking settings for a workflow service.</span></span>  
  
 <span data-ttu-id="2dab6-104">Weitere Informationen workflownachverfolgung und zur Konfiguration finden Sie unter [nachverfolgung und Ablaufverfolgung für Workflows](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) und [Konfigurieren der nachverfolgung für einen Workflow](../../../../../docs/framework/windows-workflow-foundation/configuring-tracking-for-a-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="2dab6-104">For more information in workflow tracking and its configuration, see [Workflow Tracking and Tracing](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) and [Configuring Tracking for a Workflow](../../../../../docs/framework/windows-workflow-foundation/configuring-tracking-for-a-workflow.md).</span></span>  
  
<span data-ttu-id="2dab6-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="2dab6-105">\<system.serviceModel></span></span>  
<span data-ttu-id="2dab6-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="2dab6-106">\<tracking></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2dab6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dab6-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <tracking>
    <profiles>
      <participants>
        <add name="String" 
             profileName="String" 
             type="String" />
      </participants>
      <trackingProfile name="String">
        <workflow activityDefinitionId="String">
          <activityScheduledQueries>
            <activityScheduledQuery activityName="String" 
                                    childActivityName="String"/>
          </activityScheduledQueries>
          <activityStateQueries>
            <activityStateQuery activityName="String" />
            <arguments>
              <argument name="String" />
            </arguments>
            <states>
              <state name="String"  />
            </states>
            <variables>
              <variable name="String" />
            </variables>
          </activityStateQueries>
          <bookmarkResumptionQueries>
            <bookmarkResumptionQuery name="String" />
          </bookmarkResumptionQueries>
          <cancelRequestQueries>
            <cancelRequestQuery activityName="String" 
                                childActivityName="String"/>
          </cancelRequestQueries>
          <customTrackingQueries>
            <customTrackingQuery activityName="String" 
                                 name="String"/>
          </customTrackingQueries>
          <faultPropagationQueries>
            <faultPropagationQuery activityName="String" 
                                   faultHandlerActivityName="String" />
          </faultPropagationQueries>
          <workflowInstanceQueries>
            <workflowInstanceQuery>
              <states>
                <state name="String" />
              </states>
            </workflowInstanceQuery>
          </workflowInstanceQueries>
        </workflow>
      </trackingProfile>
    </profiles>
  </tracking>
</system.serviceModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2dab6-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2dab6-108">Attributes and Elements</span></span>  
 <span data-ttu-id="2dab6-109">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2dab6-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2dab6-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="2dab6-110">Attributes</span></span>  
 <span data-ttu-id="2dab6-111">Keine</span><span class="sxs-lookup"><span data-stu-id="2dab6-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="2dab6-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2dab6-112">Child Elements</span></span>  
  
|<span data-ttu-id="2dab6-113">Element</span><span class="sxs-lookup"><span data-stu-id="2dab6-113">Element</span></span>|<span data-ttu-id="2dab6-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dab6-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2dab6-115">\<participants></span><span class="sxs-lookup"><span data-stu-id="2dab6-115">\<participants></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/participants.md)|<span data-ttu-id="2dab6-116">Eine Auflistung von Konfigurationselementen, die Teilnehmer, die Nachverfolgungsdatensätze abonnieren.</span><span class="sxs-lookup"><span data-stu-id="2dab6-116">A collection of configuration elements defining participants that subscribe to tracking records.</span></span> <span data-ttu-id="2dab6-117">Die Nachverfolgungsteilnehmer enthalten die Logik zur Verarbeitung der Nutzdaten der Nachverfolgungsdatensätze (beispielsweise für das Schreiben in eine Datei).</span><span class="sxs-lookup"><span data-stu-id="2dab6-117">The tracking participants contain the logic to process the payload from the tracking records (for example, they could choose to write to a file).</span></span>|  
|[<span data-ttu-id="2dab6-118">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="2dab6-118">\<trackingProfile></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/trackingprofile.md)|<span data-ttu-id="2dab6-119">Ein Nachverfolgungsprofil, das die von einer Workflowinstanz ausgegebenen Nachverfolgungsdatensätze filtert.</span><span class="sxs-lookup"><span data-stu-id="2dab6-119">A tracking profile to filter tracking records emitted from a workflow instance.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2dab6-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2dab6-120">Parent Elements</span></span>  
  
|<span data-ttu-id="2dab6-121">Element</span><span class="sxs-lookup"><span data-stu-id="2dab6-121">Element</span></span>|<span data-ttu-id="2dab6-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dab6-122">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2dab6-123">system.ServiceModel</span><span class="sxs-lookup"><span data-stu-id="2dab6-123">system.ServiceModel</span></span>|<span data-ttu-id="2dab6-124">Das Stammelement aller Workflow-Konfigurationselemente.</span><span class="sxs-lookup"><span data-stu-id="2dab6-124">The root element of all workflow configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2dab6-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2dab6-125">Remarks</span></span>  
 <span data-ttu-id="2dab6-126">Die Nachverfolgung bietet Ihnen die Möglichkeit, die Ausführung eines Workflows zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="2dab6-126">Tracking provides you with the ability to examine the execution of a workflow.</span></span> <span data-ttu-id="2dab6-127">Die Infrastruktur für die Workflownachverfolgung verwendet einen Workflow, um während der Ausführung Datensätze auszugeben, die Schlüsselereignisse festhalten.</span><span class="sxs-lookup"><span data-stu-id="2dab6-127">The workflow tracking infrastructure instruments a workflow to emit records reflecting key events during the execution.</span></span> <span data-ttu-id="2dab6-128">Nachverfolgungsdatensätze werden zum Beispiel ausgegeben, wenn eine Workflowinstanz startet oder abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="2dab6-128">For example, when a workflow instance starts or completes tracking records are emitted.</span></span> <span data-ttu-id="2dab6-129">Die Nachverfolgung kann auch geschäftsrelevante, den Workflowvariablen zugeordnete Daten extrahieren.</span><span class="sxs-lookup"><span data-stu-id="2dab6-129">Tracking can also extract business relevant data associated with the workflow variables.</span></span> <span data-ttu-id="2dab6-130">Wenn zum Beispiel der Workflow ein System zur Verarbeitung von Bestellungen darstellt, kann die Bestellungs-ID zusammen mit dem Nachverfolgungsdatensatz extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="2dab6-130">For example, if the workflow represents an order processing system the order id can be extracted along with the tracking record.</span></span> <span data-ttu-id="2dab6-131">Im Allgemeinen erleichtert die WF-Nachverfolgung während einer Workflowausführung die Diagnose oder die Geschäftsanalyse.</span><span class="sxs-lookup"><span data-stu-id="2dab6-131">In general, enabling WF tracking facilitates diagnostics or business analytics over a workflow execution.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2dab6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dab6-132">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.TrackingSection?displayProperty=nameWithType>
- [<span data-ttu-id="2dab6-133">Nachverfolgung und Ablaufverfolgung für Workflows</span><span class="sxs-lookup"><span data-stu-id="2dab6-133">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
