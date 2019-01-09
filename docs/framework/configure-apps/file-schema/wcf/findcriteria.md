---
title: '&lt;FindCriteria&gt;'
ms.date: 03/30/2017
ms.assetid: 5454cd19-6bf5-4ba8-94d1-f58d10dc1917
ms.openlocfilehash: 0a2fb7ae641f8ec34c518d8dc2c11fbc2ae26190
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146926"
---
# <a name="ltfindcriteriagt"></a><span data-ttu-id="e3450-102">&lt;FindCriteria&gt;</span><span class="sxs-lookup"><span data-stu-id="e3450-102">&lt;findCriteria&gt;</span></span>
<span data-ttu-id="e3450-103">Ein Konfigurationselement, das einen Kriteriensatz bereitstellt, der von einer Clientanwendung zum Suchen nach einem Ermittlungsdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3450-103">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="e3450-104">Kriterien können in Suchkriterien (nach welchen Diensten soll gesucht werden, für die) gruppiert werden und Beendigungskriterien (wie lange soll die Suche dauern).</span><span class="sxs-lookup"><span data-stu-id="e3450-104">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>  
  
 <span data-ttu-id="e3450-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="e3450-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="e3450-106">\<StandardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="e3450-106">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3450-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3450-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <standardEndpoints>
    <dynamicEndpoint>
      <standardEndpoint>
        <discoveryClientSettings discoveryEndpoint="String">
          <findCriteria duration="TimeSpan"
                        maxResults="Integer"
                        scopeMatchBy="Uri">
            <contractTypeNames>
              <add name="String"
                   namespace="String" />
            </contractTypeNames>
            <extensions />
            <scopes>
              <add scope="URI" />
            </scopes>
          </findCriteria>
        </discoveryClientSettings>
      </standardEndpoint>
    </dynamicEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e3450-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e3450-108">Attributes and Elements</span></span>  
 <span data-ttu-id="e3450-109">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e3450-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e3450-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="e3450-110">Attributes</span></span>  
  
|<span data-ttu-id="e3450-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="e3450-111">Attribute</span></span>|<span data-ttu-id="e3450-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3450-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e3450-113">duration</span><span class="sxs-lookup"><span data-stu-id="e3450-113">duration</span></span>|<span data-ttu-id="e3450-114">Ein Timespan-Wert, der die maximale Zeit angibt, die auf Antworten von Diensten im Netzwerk gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="e3450-114">A Timespan value that specifies the maximum time to wait for replies from services on the network.</span></span> <span data-ttu-id="e3450-115">Der Standardzeitraum beträgt 20 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="e3450-115">The default duration is 20 seconds.</span></span>|  
|<span data-ttu-id="e3450-116">maxResults</span><span class="sxs-lookup"><span data-stu-id="e3450-116">maxResults</span></span>|<span data-ttu-id="e3450-117">Eine ganze Zahl, die die maximale Anzahl an Antworten angibt, auf die von Diensten in einem Netzwerk oder im Internet gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="e3450-117">An integer that specifies the maximum number of replies to wait for, from services on a network or the Internet.</span></span> <span data-ttu-id="e3450-118">Wenn die maximale Anzahl erreicht wird, bevor der mit dem `duration`-Attribut festgelegte Zeitraum verstrichen ist, wird der Suchvorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="e3450-118">If maximum replies are received before the value specified in the `duration` attribute has elapsed, the find operation ends.</span></span>|  
|<span data-ttu-id="e3450-119">scopeMatchBy</span><span class="sxs-lookup"><span data-stu-id="e3450-119">scopeMatchBy</span></span>|<span data-ttu-id="e3450-120">Ein URI, der angibt, welcher Übereinstimmungsalgorithmus verwendet werden soll, während die Übereinstimmung der Bereiche der Probe-Nachricht mit denen des Endpunkts ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="e3450-120">A URI that specify the matching algorithm to use while matching the scopes in the Probe message with that of the endpoint.</span></span><br /><br /> <span data-ttu-id="e3450-121">Es gibt fünf unterstützte Bereichsübereinstimmungsregeln.</span><span class="sxs-lookup"><span data-stu-id="e3450-121">There are five supported scope-matching rules.</span></span> <span data-ttu-id="e3450-122">Wenn keine Bereichsübereinstimmungsregel angegeben wird, wird `ScopeMatchByPrefix` verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3450-122">If you do not specify a scope-matching rule, `ScopeMatchByPrefix` is used.</span></span> <span data-ttu-id="e3450-123">Weitere Informationen hierzu finden Sie unter <xref:System.ServiceModel.Discovery.FindCriteria>.</span><span class="sxs-lookup"><span data-stu-id="e3450-123">For more information on this, see <xref:System.ServiceModel.Discovery.FindCriteria>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e3450-124">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3450-124">Child Elements</span></span>  
  
|<span data-ttu-id="e3450-125">Element</span><span class="sxs-lookup"><span data-stu-id="e3450-125">Element</span></span>|<span data-ttu-id="e3450-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3450-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e3450-127">\<ContractTypeNames ></span><span class="sxs-lookup"><span data-stu-id="e3450-127">\<contractTypeNames></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/contracttypenames.md)|<span data-ttu-id="e3450-128">Eine Auflistung von Konfigurationselementen, die die Namen von Workflowdienst-Vertragstypen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e3450-128">A collection of configuration elements that contain the names of workflow service contract types.</span></span>|  
|<span data-ttu-id="e3450-129">\<Extensions > von \<FindCriteria ></span><span class="sxs-lookup"><span data-stu-id="e3450-129">\<extensions> of \<findCriteria></span></span>|<span data-ttu-id="e3450-130">Eine Auflistung von XML-Elementobjekten, die Erweiterungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e3450-130">A collection of XML element objects that provide extensions.</span></span>|  
|[<span data-ttu-id="e3450-131">\<Bereiche ></span><span class="sxs-lookup"><span data-stu-id="e3450-131">\<scopes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|<span data-ttu-id="e3450-132">Eine Auflistung von Objekten, die absolute URIs enthalten, die während eines Suchvorgangs verwendet werden, um einen bestimmten Dienst oder bestimmte Dienste zu suchen.</span><span class="sxs-lookup"><span data-stu-id="e3450-132">A collection of objects that contain absolute URIs that are used during a find operation to locate a specific service or services.</span></span><br /><br /> <span data-ttu-id="e3450-133">Wenn der bestimmte Dienst gefunden wird, wurde eine erfolgreiche Übereinstimmung zwischen dem Dienst- und Bereichs-URI hergestellt. Dies geschieht mitunter mittels Bereichsregeln, die Probleme beim Abgleichen behandeln.</span><span class="sxs-lookup"><span data-stu-id="e3450-133">If the specific service is found, a successful match has been made between the service URI and the Scope URI, sometimes with the help of scope rules that handle complications of matching.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e3450-134">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3450-134">Parent Elements</span></span>  
  
|<span data-ttu-id="e3450-135">Element</span><span class="sxs-lookup"><span data-stu-id="e3450-135">Element</span></span>|<span data-ttu-id="e3450-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3450-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e3450-137">\<StandardEndpoints ></span><span class="sxs-lookup"><span data-stu-id="e3450-137">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="e3450-138">Enthält die Einstellungen, die von einer Anwendung benötigt werden, um am Dienstermittlungsprozess als Client teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="e3450-138">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e3450-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3450-139">See Also</span></span>  
 <xref:System.ServiceModel.Discovery.FindCriteria>  
 <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>
