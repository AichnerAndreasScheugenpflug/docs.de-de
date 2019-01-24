---
title: '&lt;mexTcpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 01baba8d-d784-4255-9ea2-7afff1482bf0
ms.openlocfilehash: 4c3858ee0dc7fd20bd1269c74a4499998d530f03
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54733986"
---
# <a name="ltmextcpbindinggt"></a><span data-ttu-id="dd376-102">&lt;mexTcpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="dd376-102">&lt;mexTcpBinding&gt;</span></span>
<span data-ttu-id="dd376-103">Gibt die Einstellungen für eine Bindung an, die für den WS-MetadataExchange-Nachrichtenaustausch (WS-MEX) über TCP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd376-103">Specifies the settings for a binding used for the WS-MetadataExchange (WS-MEX) message exchange over TCP.</span></span>  
  
 <span data-ttu-id="dd376-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="dd376-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="dd376-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="dd376-105">\<bindings></span></span>  
<span data-ttu-id="dd376-106">\<mexTcpBinding></span><span class="sxs-lookup"><span data-stu-id="dd376-106">\<mexTcpBinding></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd376-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd376-107">Syntax</span></span>  
  
```xml  
<mexTcpBinding>
  <binding closeTimeout="TimeSpan"
           name="string"
           openTimeout="TimeSpan"
           receiveTimeout="TimeSpan"
           sendTimeout="TimeSpan">
  </binding>
</mexTcpBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dd376-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dd376-108">Attributes and Elements</span></span>  
 <span data-ttu-id="dd376-109">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dd376-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dd376-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="dd376-110">Attributes</span></span>  
  
|<span data-ttu-id="dd376-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="dd376-111">Attribute</span></span>|<span data-ttu-id="dd376-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd376-112">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="dd376-113">Ein <xref:System.TimeSpan>-Wert, der das Zeitintervall für den Abschluss eines Schließvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="dd376-113">A <xref:System.TimeSpan> value that specifies the interval of time provided for a close operation to complete.</span></span> <span data-ttu-id="dd376-114">Dieser Wert muss größer oder gleich <xref:System.TimeSpan.Zero> sein.</span><span class="sxs-lookup"><span data-stu-id="dd376-114">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="dd376-115">Der Standardwert ist 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="dd376-115">The default is 00:01:00.</span></span>|  
|`name`|<span data-ttu-id="dd376-116">Eine Zeichenfolge, die den Konfigurationsnamen der Bindung enthält.</span><span class="sxs-lookup"><span data-stu-id="dd376-116">A string that contains the configuration name of the binding.</span></span> <span data-ttu-id="dd376-117">Dieser Wert sollte eindeutig sein, da er von der Bindung zur Identifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd376-117">This value should be unique because it is used as an identification for the binding.</span></span> <span data-ttu-id="dd376-118">Jede Bindung hat ein `name`-Attribut und ein `namespace`-Attribut, die die Bindung in den Metadaten des Diensts eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dd376-118">Each binding has a `name` and `namespace` attribute that together uniquely identify it in the metadata of the service.</span></span> <span data-ttu-id="dd376-119">Außerdem kommt dieser Name bei den Bindungen eines Typs nur einmal vor.</span><span class="sxs-lookup"><span data-stu-id="dd376-119">In addition, this name is unique among bindings of the same type.</span></span> <span data-ttu-id="dd376-120">Ab [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)] müssen Bindungen und Verhalten keinen Namen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dd376-120">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="dd376-121">Weitere Informationen zu Standardkonfiguration und zu namenlosen Bindungen und Verhaltensweisen finden Sie unter [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) und [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="dd376-121">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>|  
|`openTimeout`|<span data-ttu-id="dd376-122">Ein <xref:System.TimeSpan>-Wert, der das Zeitintervall für den Abschluss eines Öffnungsvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="dd376-122">A <xref:System.TimeSpan> value that specifies the interval of time provided for an open operation to complete.</span></span> <span data-ttu-id="dd376-123">Dieser Wert muss größer oder gleich <xref:System.TimeSpan.Zero> sein.</span><span class="sxs-lookup"><span data-stu-id="dd376-123">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="dd376-124">Der Standardwert ist 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="dd376-124">The default is 00:01:00.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="dd376-125">Ein <xref:System.TimeSpan>-Wert, der das Zeitintervall für den Abschluss eines Empfangsvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="dd376-125">A <xref:System.TimeSpan> value that specifies the interval of time provided for a receive operation to complete.</span></span> <span data-ttu-id="dd376-126">Dieser Wert muss größer oder gleich <xref:System.TimeSpan.Zero> sein.</span><span class="sxs-lookup"><span data-stu-id="dd376-126">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="dd376-127">Der Standardwert ist 00:10:00.</span><span class="sxs-lookup"><span data-stu-id="dd376-127">The default is 00:10:00.</span></span>|  
|`sendTimeout`|<span data-ttu-id="dd376-128">Ein <xref:System.TimeSpan>-Wert, der das Zeitintervall für den Abschluss eines Sendevorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="dd376-128">A <xref:System.TimeSpan> value that specifies the interval of time provided for a send operation to complete.</span></span> <span data-ttu-id="dd376-129">Dieser Wert muss größer oder gleich <xref:System.TimeSpan.Zero> sein.</span><span class="sxs-lookup"><span data-stu-id="dd376-129">This value should be greater than or equal to <xref:System.TimeSpan.Zero>.</span></span> <span data-ttu-id="dd376-130">Der Standardwert ist 00:01:00.</span><span class="sxs-lookup"><span data-stu-id="dd376-130">The default is 00:01:00.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dd376-131">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd376-131">Child Elements</span></span>  
 <span data-ttu-id="dd376-132">Keine</span><span class="sxs-lookup"><span data-stu-id="dd376-132">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dd376-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd376-133">Parent Elements</span></span>  
  
|<span data-ttu-id="dd376-134">Element</span><span class="sxs-lookup"><span data-stu-id="dd376-134">Element</span></span>|<span data-ttu-id="dd376-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd376-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dd376-136">\<bindings></span><span class="sxs-lookup"><span data-stu-id="dd376-136">\<bindings></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|<span data-ttu-id="dd376-137">Dieses Element enthält eine Auflistung von standardmäßigen und benutzerdefinierten Bindungen.</span><span class="sxs-lookup"><span data-stu-id="dd376-137">This element holds a collection of standard and custom bindings.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="dd376-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd376-138">See also</span></span>
- <xref:System.ServiceModel.Configuration.MexTcpBindingElement>
- <xref:System.ServiceModel.Description.MetadataExchangeBindings.CreateMexTcpBinding%2A>
- [<span data-ttu-id="dd376-139">Vorgehensweise: Veröffentlichen von Metadaten für einen Dienst mithilfe einer Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="dd376-139">How to: Publish Metadata for a Service Using a Configuration File</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)
- [<span data-ttu-id="dd376-140">Veröffentlichen und Abrufen von Metadaten über eine benutzerdefinierte Bindung</span><span class="sxs-lookup"><span data-stu-id="dd376-140">Publishing and Retrieving Metadata Over a Custom Binding</span></span>](../../../../../docs/framework/wcf/extending/publishing-and-retrieving-metadata-over-a-custom-binding.md)
- [<span data-ttu-id="dd376-141">Metadaten</span><span class="sxs-lookup"><span data-stu-id="dd376-141">Metadata</span></span>](../../../../../docs/framework/wcf/feature-details/metadata.md)
- [<span data-ttu-id="dd376-142">Bindungen</span><span class="sxs-lookup"><span data-stu-id="dd376-142">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="dd376-143">Konfigurieren der vom System bereitgestellten Bindungen</span><span class="sxs-lookup"><span data-stu-id="dd376-143">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="dd376-144">Verwenden von Bindungen, um Dienste und Clients zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="dd376-144">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="dd376-145">\<binding></span><span class="sxs-lookup"><span data-stu-id="dd376-145">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
