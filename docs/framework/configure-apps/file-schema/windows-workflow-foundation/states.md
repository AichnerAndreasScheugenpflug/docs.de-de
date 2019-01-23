---
title: '&lt;states&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: ebea5e7c-ad58-43c5-8f2d-cca25ae1b721
ms.openlocfilehash: d1ec35b1c434b8188fde7b546e2dee42a93f5c91
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54550577"
---
# <a name="ltstatesgt"></a><span data-ttu-id="aac47-102">&lt;states&gt;</span><span class="sxs-lookup"><span data-stu-id="aac47-102">&lt;states&gt;</span></span>
<span data-ttu-id="aac47-103">Stellt bei der Erstellung von Nachverfolgungsdatensätzen eine Auflistung abonnierter Zustände der nachverfolgten Workflowinstanz dar.</span><span class="sxs-lookup"><span data-stu-id="aac47-103">Represents a collection of subscribed states from the tracked workflow instance when the tracking records are created.</span></span>  
  
 <span data-ttu-id="aac47-104">Weitere Informationen zu überwachungsprofilabfragen finden Sie unter [Überwachungsprofile](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="aac47-104">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
<span data-ttu-id="aac47-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="aac47-105">\<system.serviceModel></span></span>  
<span data-ttu-id="aac47-106">\<tracking></span><span class="sxs-lookup"><span data-stu-id="aac47-106">\<tracking></span></span>  
<span data-ttu-id="aac47-107">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="aac47-107">\<trackingProfile></span></span>  
<span data-ttu-id="aac47-108">\<workflow></span><span class="sxs-lookup"><span data-stu-id="aac47-108">\<workflow></span></span>  
<span data-ttu-id="aac47-109">\<workflowInstanceQueries></span><span class="sxs-lookup"><span data-stu-id="aac47-109">\<workflowInstanceQueries></span></span>  
<span data-ttu-id="aac47-110">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="aac47-110">\<workflowInstanceQuery></span></span>  
<span data-ttu-id="aac47-111">\<states></span><span class="sxs-lookup"><span data-stu-id="aac47-111">\<states></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aac47-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="aac47-112">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <workflowInstanceQueries>
        <workflowInstanceQuery>
          <states>
            <state name="Name"/>
          </states>
        </workflowInstanceQuery>
      </workflowInstanceQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="aac47-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="aac47-113">Attributes and Elements</span></span>  
 <span data-ttu-id="aac47-114">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="aac47-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="aac47-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="aac47-115">Attributes</span></span>  
 <span data-ttu-id="aac47-116">Keine</span><span class="sxs-lookup"><span data-stu-id="aac47-116">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="aac47-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aac47-117">Child Elements</span></span>  
  
|<span data-ttu-id="aac47-118">Element</span><span class="sxs-lookup"><span data-stu-id="aac47-118">Element</span></span>|<span data-ttu-id="aac47-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aac47-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="aac47-120">\<state></span><span class="sxs-lookup"><span data-stu-id="aac47-120">\<state></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/states.md)|<span data-ttu-id="aac47-121">Ein abonnierter Zustand der verfolgten Workflowinstanz, wenn der Nachverfolgungsdatensatz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="aac47-121">A subscribed state from the tracked workflow instance when the tracking record is created.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="aac47-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aac47-122">Parent Elements</span></span>  
  
|<span data-ttu-id="aac47-123">Element</span><span class="sxs-lookup"><span data-stu-id="aac47-123">Element</span></span>|<span data-ttu-id="aac47-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aac47-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="aac47-125">\<workflowInstanceQuery></span><span class="sxs-lookup"><span data-stu-id="aac47-125">\<workflowInstanceQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflowinstancequery.md)|<span data-ttu-id="aac47-126">Eine Abfrage, die Änderungen im Lebenszyklus einer Workflowinstanz nachverfolgt, beispielsweise ein gestartetes oder abgeschlossenes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="aac47-126">A query that tracks workflow instance life cycle changes such as a started or completed event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="aac47-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aac47-127">Remarks</span></span>  
 <span data-ttu-id="aac47-128">Die zurückgegebenen Datensätze werden entsprechend den Zuständen in dieser Auflistung gefiltert.</span><span class="sxs-lookup"><span data-stu-id="aac47-128">The returned records are filtered by the states in this collection.</span></span>  
  
 <span data-ttu-id="aac47-129">Eine Beschreibung der möglichen Zustandswerte finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="aac47-129">Possible state values are described in the following table.</span></span>  
  
|<span data-ttu-id="aac47-130">Zustand</span><span class="sxs-lookup"><span data-stu-id="aac47-130">State</span></span>|<span data-ttu-id="aac47-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aac47-131">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="aac47-132">Aborted</span><span class="sxs-lookup"><span data-stu-id="aac47-132">Aborted</span></span>|<span data-ttu-id="aac47-133">Die Workflowinstanz wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="aac47-133">The workflow instance is aborted.</span></span>|  
|<span data-ttu-id="aac47-134">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="aac47-134">Completed</span></span>|<span data-ttu-id="aac47-135">Die Workflowinstanz wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="aac47-135">The workflow instance is completed.</span></span>|  
|<span data-ttu-id="aac47-136">Deleted</span><span class="sxs-lookup"><span data-stu-id="aac47-136">Deleted</span></span>|<span data-ttu-id="aac47-137">Die Workflowinstanz wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="aac47-137">The workflow instance is deleted.</span></span>|  
|<span data-ttu-id="aac47-138">Idle</span><span class="sxs-lookup"><span data-stu-id="aac47-138">Idle</span></span>|<span data-ttu-id="aac47-139">Die Workflowinstanz ist im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="aac47-139">The workflow instance is idle.</span></span>|  
|<span data-ttu-id="aac47-140">Persisted</span><span class="sxs-lookup"><span data-stu-id="aac47-140">Persisted</span></span>|<span data-ttu-id="aac47-141">Die Workflowinstanz wurde beibehalten.</span><span class="sxs-lookup"><span data-stu-id="aac47-141">The workflow instance is persisted.</span></span>|  
|<span data-ttu-id="aac47-142">Resumed</span><span class="sxs-lookup"><span data-stu-id="aac47-142">Resumed</span></span>|<span data-ttu-id="aac47-143">Die Workflowinstanz wurde wiederaufgenommen.</span><span class="sxs-lookup"><span data-stu-id="aac47-143">The workflow instance is resumed.</span></span>|  
|<span data-ttu-id="aac47-144">Started</span><span class="sxs-lookup"><span data-stu-id="aac47-144">Started</span></span>|<span data-ttu-id="aac47-145">Die Workflowinstanz wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="aac47-145">The workflow instance is started.</span></span>|  
|<span data-ttu-id="aac47-146">UnhandledException</span><span class="sxs-lookup"><span data-stu-id="aac47-146">UnhandledException</span></span>|<span data-ttu-id="aac47-147">In der Workflowinstanz ist eine nicht behandelte Ausnahme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="aac47-147">The workflow instance encountered an unhandled exception.</span></span>|  
|<span data-ttu-id="aac47-148">Unloaded</span><span class="sxs-lookup"><span data-stu-id="aac47-148">Unloaded</span></span>|<span data-ttu-id="aac47-149">Die Workflowinstanz wurde entladen.</span><span class="sxs-lookup"><span data-stu-id="aac47-149">The workflow instance is unloaded.</span></span>|  
|<span data-ttu-id="aac47-150">Canceled</span><span class="sxs-lookup"><span data-stu-id="aac47-150">Canceled</span></span>|<span data-ttu-id="aac47-151">Die Workflowinstanz wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="aac47-151">The workflow instance is canceled.</span></span>|  
|<span data-ttu-id="aac47-152">Angehalten</span><span class="sxs-lookup"><span data-stu-id="aac47-152">Suspended</span></span>|<span data-ttu-id="aac47-153">Die Workflowinstanz wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="aac47-153">The workflow instance is suspended.</span></span>|  
|<span data-ttu-id="aac47-154">Terminated</span><span class="sxs-lookup"><span data-stu-id="aac47-154">Terminated</span></span>|<span data-ttu-id="aac47-155">Die Workflowinstanz wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="aac47-155">The workflow instance is terminated.</span></span>|  
|<span data-ttu-id="aac47-156">Unsuspended</span><span class="sxs-lookup"><span data-stu-id="aac47-156">Unsuspended</span></span>|<span data-ttu-id="aac47-157">Die Workflowinstanz wurde fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="aac47-157">The workflow instance is unsuspended.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="aac47-158">Beispiel</span><span class="sxs-lookup"><span data-stu-id="aac47-158">Example</span></span>  
 <span data-ttu-id="aac47-159">In der folgende Konfiguration werden mithilfe einer Abfrage Workflownachverfolgungsdatensätze auf Instanzebene für den `Started`-Instanzzustand abonniert.</span><span class="sxs-lookup"><span data-stu-id="aac47-159">The following configuration subscribes to workflow instance-level tracking records for the `Started` instance state using this query.</span></span>  
  
```xml  
<workflowInstanceQueries>  
    <workflowInstanceQuery>  
      <states>  
        <state name="Started"/>  
      </states>  
    </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
## <a name="see-also"></a><span data-ttu-id="aac47-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aac47-160">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.StateElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [<span data-ttu-id="aac47-161">Nachverfolgung und Ablaufverfolgung für Workflows</span><span class="sxs-lookup"><span data-stu-id="aac47-161">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="aac47-162">Überwachungsprofile</span><span class="sxs-lookup"><span data-stu-id="aac47-162">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
