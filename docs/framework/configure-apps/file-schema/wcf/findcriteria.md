---
title: '&lt;findCriteria&gt;'
ms.date: 03/30/2017
ms.assetid: 5454cd19-6bf5-4ba8-94d1-f58d10dc1917
ms.openlocfilehash: b90e6cab923075dbf750dc0d26a0eb1196cfde32
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54741241"
---
# <a name="ltfindcriteriagt"></a><span data-ttu-id="a22e2-102">&lt;findCriteria&gt;</span><span class="sxs-lookup"><span data-stu-id="a22e2-102">&lt;findCriteria&gt;</span></span>
<span data-ttu-id="a22e2-103">Ein Konfigurationselement, das einen Kriteriensatz bereitstellt, der von einer Clientanwendung zum Suchen nach einem Ermittlungsdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a22e2-103">A configuration element that supplies a set of criteria used by a client application to search for a discovery service.</span></span> <span data-ttu-id="a22e2-104">Kriterien können in Suchkriterien (nach welchen Diensten soll gesucht werden, für die) gruppiert werden und Beendigungskriterien (wie lange soll die Suche dauern).</span><span class="sxs-lookup"><span data-stu-id="a22e2-104">Criteria can be grouped into search criteria (specifying what services you’re looking for) and find termination criteria (how long the search should last).</span></span>  
  
 <span data-ttu-id="a22e2-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="a22e2-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="a22e2-106">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="a22e2-106">\<standardEndpoints></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a22e2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a22e2-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a22e2-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a22e2-108">Attributes and Elements</span></span>  
 <span data-ttu-id="a22e2-109">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a22e2-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a22e2-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="a22e2-110">Attributes</span></span>  
  
|<span data-ttu-id="a22e2-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="a22e2-111">Attribute</span></span>|<span data-ttu-id="a22e2-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a22e2-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a22e2-113">duration</span><span class="sxs-lookup"><span data-stu-id="a22e2-113">duration</span></span>|<span data-ttu-id="a22e2-114">Ein Timespan-Wert, der die maximale Zeit angibt, die auf Antworten von Diensten im Netzwerk gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="a22e2-114">A Timespan value that specifies the maximum time to wait for replies from services on the network.</span></span> <span data-ttu-id="a22e2-115">Der Standardzeitraum beträgt 20 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a22e2-115">The default duration is 20 seconds.</span></span>|  
|<span data-ttu-id="a22e2-116">maxResults</span><span class="sxs-lookup"><span data-stu-id="a22e2-116">maxResults</span></span>|<span data-ttu-id="a22e2-117">Eine ganze Zahl, die die maximale Anzahl an Antworten angibt, auf die von Diensten in einem Netzwerk oder im Internet gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="a22e2-117">An integer that specifies the maximum number of replies to wait for, from services on a network or the Internet.</span></span> <span data-ttu-id="a22e2-118">Wenn die maximale Anzahl erreicht wird, bevor der mit dem `duration`-Attribut festgelegte Zeitraum verstrichen ist, wird der Suchvorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="a22e2-118">If maximum replies are received before the value specified in the `duration` attribute has elapsed, the find operation ends.</span></span>|  
|<span data-ttu-id="a22e2-119">scopeMatchBy</span><span class="sxs-lookup"><span data-stu-id="a22e2-119">scopeMatchBy</span></span>|<span data-ttu-id="a22e2-120">Ein URI, der angibt, welcher Übereinstimmungsalgorithmus verwendet werden soll, während die Übereinstimmung der Bereiche der Probe-Nachricht mit denen des Endpunkts ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="a22e2-120">A URI that specify the matching algorithm to use while matching the scopes in the Probe message with that of the endpoint.</span></span><br /><br /> <span data-ttu-id="a22e2-121">Es gibt fünf unterstützte Bereichsübereinstimmungsregeln.</span><span class="sxs-lookup"><span data-stu-id="a22e2-121">There are five supported scope-matching rules.</span></span> <span data-ttu-id="a22e2-122">Wenn keine Bereichsübereinstimmungsregel angegeben wird, wird `ScopeMatchByPrefix` verwendet.</span><span class="sxs-lookup"><span data-stu-id="a22e2-122">If you do not specify a scope-matching rule, `ScopeMatchByPrefix` is used.</span></span> <span data-ttu-id="a22e2-123">Weitere Informationen hierzu finden Sie unter <xref:System.ServiceModel.Discovery.FindCriteria>.</span><span class="sxs-lookup"><span data-stu-id="a22e2-123">For more information on this, see <xref:System.ServiceModel.Discovery.FindCriteria>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a22e2-124">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a22e2-124">Child Elements</span></span>  
  
|<span data-ttu-id="a22e2-125">Element</span><span class="sxs-lookup"><span data-stu-id="a22e2-125">Element</span></span>|<span data-ttu-id="a22e2-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a22e2-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a22e2-127">\<contractTypeNames></span><span class="sxs-lookup"><span data-stu-id="a22e2-127">\<contractTypeNames></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/contracttypenames.md)|<span data-ttu-id="a22e2-128">Eine Auflistung von Konfigurationselementen, die die Namen von Workflowdienst-Vertragstypen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a22e2-128">A collection of configuration elements that contain the names of workflow service contract types.</span></span>|  
|<span data-ttu-id="a22e2-129">\<Extensions > von \<FindCriteria ></span><span class="sxs-lookup"><span data-stu-id="a22e2-129">\<extensions> of \<findCriteria></span></span>|<span data-ttu-id="a22e2-130">Eine Auflistung von XML-Elementobjekten, die Erweiterungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a22e2-130">A collection of XML element objects that provide extensions.</span></span>|  
|[<span data-ttu-id="a22e2-131">\<scopes></span><span class="sxs-lookup"><span data-stu-id="a22e2-131">\<scopes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|<span data-ttu-id="a22e2-132">Eine Auflistung von Objekten, die absolute URIs enthalten, die während eines Suchvorgangs verwendet werden, um einen bestimmten Dienst oder bestimmte Dienste zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a22e2-132">A collection of objects that contain absolute URIs that are used during a find operation to locate a specific service or services.</span></span><br /><br /> <span data-ttu-id="a22e2-133">Wenn der bestimmte Dienst gefunden wird, wurde eine erfolgreiche Übereinstimmung zwischen dem Dienst- und Bereichs-URI hergestellt. Dies geschieht mitunter mittels Bereichsregeln, die Probleme beim Abgleichen behandeln.</span><span class="sxs-lookup"><span data-stu-id="a22e2-133">If the specific service is found, a successful match has been made between the service URI and the Scope URI, sometimes with the help of scope rules that handle complications of matching.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a22e2-134">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a22e2-134">Parent Elements</span></span>  
  
|<span data-ttu-id="a22e2-135">Element</span><span class="sxs-lookup"><span data-stu-id="a22e2-135">Element</span></span>|<span data-ttu-id="a22e2-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a22e2-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a22e2-137">\<standardEndpoints></span><span class="sxs-lookup"><span data-stu-id="a22e2-137">\<standardEndpoints></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/standardendpoints.md)|<span data-ttu-id="a22e2-138">Enthält die Einstellungen, die von einer Anwendung benötigt werden, um am Dienstermittlungsprozess als Client teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="a22e2-138">Contains the settings needed by an application to participate in the service discovery process as a client.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a22e2-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a22e2-139">See also</span></span>
- <xref:System.ServiceModel.Discovery.FindCriteria>
- <xref:System.ServiceModel.Discovery.Configuration.FindCriteriaElement>
