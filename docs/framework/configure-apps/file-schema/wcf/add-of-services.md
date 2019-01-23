---
title: '&lt;add&gt; von &lt;services&gt;'
ms.date: 03/30/2017
ms.assetid: 6bdc4590-aa9c-4ec8-9345-879d780cd141
ms.openlocfilehash: dc68357332ebe06affd18f1539a66587b6ed1b91
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549993"
---
# <a name="ltaddgt-of-ltservicesgt"></a><span data-ttu-id="edffa-102">&lt;add&gt; von &lt;services&gt;</span><span class="sxs-lookup"><span data-stu-id="edffa-102">&lt;add&gt; of &lt;services&gt;</span></span>
<span data-ttu-id="edffa-103">Gibt die Einstellungen für eine Instanz von <xref:System.Workflow.Runtime.WorkflowRuntime> zum Hosten workflowbasierter Windows Communication Foundation (WCF)-Diensten.</span><span class="sxs-lookup"><span data-stu-id="edffa-103">Specifies settings for an instance of <xref:System.Workflow.Runtime.WorkflowRuntime> for hosting workflow-based Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="edffa-104">Dieses Element ist vom Typ <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="edffa-104">This element is of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  
  
 <span data-ttu-id="edffa-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="edffa-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="edffa-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="edffa-106">\<behaviors></span></span>  
<span data-ttu-id="edffa-107">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="edffa-107">\<serviceBehaviors></span></span>  
<span data-ttu-id="edffa-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="edffa-108">\<behavior></span></span>  
<span data-ttu-id="edffa-109">\<services></span><span class="sxs-lookup"><span data-stu-id="edffa-109">\<services></span></span>  
<span data-ttu-id="edffa-110">\<add></span><span class="sxs-lookup"><span data-stu-id="edffa-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="edffa-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="edffa-111">Syntax</span></span>  
  
```xml  
<workflowRuntime>
  <services>
    <add type="String" />
  </services>
</workflowRuntime>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="edffa-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="edffa-112">Attributes and Elements</span></span>  
 <span data-ttu-id="edffa-113">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="edffa-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="edffa-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="edffa-114">Attributes</span></span>  
  
|<span data-ttu-id="edffa-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="edffa-115">Attribute</span></span>|<span data-ttu-id="edffa-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edffa-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="edffa-117">Typ</span><span class="sxs-lookup"><span data-stu-id="edffa-117">type</span></span>|<span data-ttu-id="edffa-118">Eine Zeichenfolge, die den durch die Assembly bezeichneten Typnamen des zu initialisierenden Diensts angibt.</span><span class="sxs-lookup"><span data-stu-id="edffa-118">A string that specifies the assembly-qualified type name of the service to be initialized.</span></span> <span data-ttu-id="edffa-119">Der angegebene Dienst muss bestimmten Regeln über die Signaturen ihrer Konstruktoren folgen.</span><span class="sxs-lookup"><span data-stu-id="edffa-119">The service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="edffa-120">Weitere Informationen finden Sie unter <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="edffa-120">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="edffa-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="edffa-121">Child Elements</span></span>  
 <span data-ttu-id="edffa-122">Keine</span><span class="sxs-lookup"><span data-stu-id="edffa-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="edffa-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="edffa-123">Parent Elements</span></span>  
  
|<span data-ttu-id="edffa-124">Element</span><span class="sxs-lookup"><span data-stu-id="edffa-124">Element</span></span>|<span data-ttu-id="edffa-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edffa-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="edffa-126">\<services></span><span class="sxs-lookup"><span data-stu-id="edffa-126">\<services></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/services-of-workflowruntime.md)|<span data-ttu-id="edffa-127">Eine Auflistung von Diensten, die der <xref:System.Workflow.Runtime.WorkflowRuntime>-Engine hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="edffa-127">A collection of services that will be added to the <xref:System.Workflow.Runtime.WorkflowRuntime> engine.</span></span> <span data-ttu-id="edffa-128">Die Elemente sind vom Typ <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="edffa-128">The elements are of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  <span data-ttu-id="edffa-129">Die in der Auflistung angegebenen Dienste werden vom Workflow-Laufzeitmodul initialisiert und den Diensten hinzugefügt, wenn der entsprechende <xref:System.Workflow.Runtime.WorkflowRuntime>-Konstruktor aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="edffa-129">The services specified in the collection will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="edffa-130">Aus diesem Grund müssen die in der Auflistung angegebenen Dienste bestimmte Regeln bezüglich der Signaturen ihrer Konstruktoren erfüllen.</span><span class="sxs-lookup"><span data-stu-id="edffa-130">Therefore, the services specified in the collection must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="edffa-131">Weitere Informationen finden Sie unter <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="edffa-131">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="edffa-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="edffa-132">Remarks</span></span>  
 <span data-ttu-id="edffa-133">Der in diesem Element angegebene Dienst wird von der Workflowruntime-Engine initialisiert und seinen Diensten hinzugefügt, wenn der entsprechende <xref:System.Workflow.Runtime.WorkflowRuntime>-Konstruktor aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="edffa-133">The service specified in this element will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="edffa-134">Deshalb muss der in der Auflistung angegebenen Dienst bestimmten Regeln über die Signaturen ihrer Konstruktoren folgen.</span><span class="sxs-lookup"><span data-stu-id="edffa-134">Therefore, the service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="edffa-135">Weitere Informationen finden Sie unter <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="edffa-135">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="edffa-136">Beispiel</span><span class="sxs-lookup"><span data-stu-id="edffa-136">Example</span></span>  
  
```xml  
<serviceBehaviors>
  <behavior name="ServiceBehavior">
    <workflowRuntime name="WorkflowServiceHostRuntime"
                     validateOnCreate="true"
                     enablePerformanceCounters="true">
      <services>
        <add type="NetFx.Checkin.Scenario.WorkflowServices.WorkflowBasedServices.Common.TestPersistenceService.FilePersistenceService, NetFx.Checkin.Scenario.WorkflowServices.WorkflowBasedServices.Common" />
      </services>
    </workflowRuntime>
  </behavior>
</serviceBehaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="edffa-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edffa-137">See also</span></span>
- <xref:System.ServiceModel.Configuration.WorkflowRuntimeElement>
- <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>
- <xref:System.Workflow.Runtime.WorkflowRuntime>
- <span data-ttu-id="edffa-138">[Workflowkonfigurationsdateien](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="edffa-138">[Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span></span>
