---
title: '&lt;peerTransport&gt;'
ms.date: 03/30/2017
ms.assetid: c1a5013a-9dd4-4a27-b114-795b8b323177
ms.openlocfilehash: c8ca9f37b799087337f7dff6be48744f4f9dea6a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54703626"
---
# <a name="ltpeertransportgt"></a><span data-ttu-id="ef129-102">&lt;peerTransport&gt;</span><span class="sxs-lookup"><span data-stu-id="ef129-102">&lt;peerTransport&gt;</span></span>
<span data-ttu-id="ef129-103">Definiert einen Peertransport für eine benutzerdefinierte Bindung.</span><span class="sxs-lookup"><span data-stu-id="ef129-103">Defines a peer transport for a custom binding.</span></span>  
  
 <span data-ttu-id="ef129-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="ef129-104">\<system.serviceModel></span></span>  
<span data-ttu-id="ef129-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="ef129-105">\<bindings></span></span>  
<span data-ttu-id="ef129-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="ef129-106">\<customBinding></span></span>  
<span data-ttu-id="ef129-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="ef129-107">\<binding></span></span>  
<span data-ttu-id="ef129-108">\<peerTransport></span><span class="sxs-lookup"><span data-stu-id="ef129-108">\<peerTransport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ef129-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef129-109">Syntax</span></span>  
  
```xml  
<peerTransport listenIpAddress="String"
               maxBufferPoolSize="Integer"
               maxReceivedMessageSize="Integer"
               port="Integer">
  <security>
  </security>
</peerTransport>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ef129-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ef129-110">Attributes and Elements</span></span>  
 <span data-ttu-id="ef129-111">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ef129-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ef129-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef129-112">Attributes</span></span>  
  
|<span data-ttu-id="ef129-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="ef129-113">Attribute</span></span>|<span data-ttu-id="ef129-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef129-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ef129-115">listenIpAddress</span><span class="sxs-lookup"><span data-stu-id="ef129-115">listenIpAddress</span></span>|<span data-ttu-id="ef129-116">Eine Zeichenfolge mit einer IP-Adresse, die der Peerknoten auf TCP-Nachrichten überwacht.</span><span class="sxs-lookup"><span data-stu-id="ef129-116">A string that specifies an IP address on which the peer node will listen for TCP messages.</span></span> <span data-ttu-id="ef129-117">Die Standardeinstellung ist `null`.</span><span class="sxs-lookup"><span data-stu-id="ef129-117">The default is `null`.</span></span>|  
|<span data-ttu-id="ef129-118">maxBufferPoolSize</span><span class="sxs-lookup"><span data-stu-id="ef129-118">maxBufferPoolSize</span></span>|<span data-ttu-id="ef129-119">Eine positive ganze Zahl, die die maximale Pufferpoolgröße angibt.</span><span class="sxs-lookup"><span data-stu-id="ef129-119">A positive integer that specifies the maximum size of the buffer pool.</span></span> <span data-ttu-id="ef129-120">Der Standard ist 524288.</span><span class="sxs-lookup"><span data-stu-id="ef129-120">The default is 524288.</span></span><br /><br /> <span data-ttu-id="ef129-121">Viele Bereiche von WCF verwenden Puffer.</span><span class="sxs-lookup"><span data-stu-id="ef129-121">Many parts of WCF use buffers.</span></span> <span data-ttu-id="ef129-122">Das Erstellen und Zerstören von Puffern bei jeder Verwendung ist kostspielig. Dasselbe gilt für die Garbage Collection für Puffer.</span><span class="sxs-lookup"><span data-stu-id="ef129-122">Creating and destroying buffers each time they are used is expensive, and garbage collection for buffers is also expensive.</span></span> <span data-ttu-id="ef129-123">Bei Pufferpools können Sie einen zu verwendenden Puffer aus dem Pool nehmen und ihn nach der Verwendung wieder dem Pool zuführen.</span><span class="sxs-lookup"><span data-stu-id="ef129-123">With buffer pools, you can take a buffer from the pool, use it, and return it to the pool once you are done.</span></span> <span data-ttu-id="ef129-124">So wird der Aufwand beim Erstellen und Zerstören von Puffern vermieden.</span><span class="sxs-lookup"><span data-stu-id="ef129-124">Thus the overhead in creating and destroying buffers is avoided.</span></span>|  
|<span data-ttu-id="ef129-125">maxReceivedMessageSize</span><span class="sxs-lookup"><span data-stu-id="ef129-125">maxReceivedMessageSize</span></span>|<span data-ttu-id="ef129-126">Eine positive ganze Zahl, die die maximale Nachrichtengröße in Byte, einschließlich Header, festlegt.</span><span class="sxs-lookup"><span data-stu-id="ef129-126">A positive integer that defines the maximum message size in bytes including headers.</span></span> <span data-ttu-id="ef129-127">Der Absender einer Nachricht erhält einen SOAP-Fehler, wenn die Nachricht zu groß für den Empfänger ist.</span><span class="sxs-lookup"><span data-stu-id="ef129-127">The sender of a message receives a SOAP fault when the message is too large for the receiver.</span></span> <span data-ttu-id="ef129-128">Der Empfänger verwirft die Nachricht und erstellt einen Eintrag des Ereignisses im Ablaufverfolgungsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="ef129-128">The receiver drops the message and creates an entry of the event in the trace log.</span></span> <span data-ttu-id="ef129-129">Der Standard ist 65536.</span><span class="sxs-lookup"><span data-stu-id="ef129-129">The default is 65536.</span></span>|  
|<span data-ttu-id="ef129-130">Port</span><span class="sxs-lookup"><span data-stu-id="ef129-130">port</span></span>|<span data-ttu-id="ef129-131">Eine ganze Zahl, die den Netzwerk-Schnittstellenanschluss angibt, an dem diese Bindung TCP-Peerkanalnachrichten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ef129-131">An integer that specifies the network interface port on which this binding will process peer channel TCP messages.</span></span> <span data-ttu-id="ef129-132">Dabei muss es sich um einen Wert zwischen <xref:System.Net.IPEndPoint.MinPort> und <xref:System.Net.IPEndPoint.MaxPort> handeln.</span><span class="sxs-lookup"><span data-stu-id="ef129-132">This value must be between <xref:System.Net.IPEndPoint.MinPort> and <xref:System.Net.IPEndPoint.MaxPort>.</span></span> <span data-ttu-id="ef129-133">Der Standard ist 0.</span><span class="sxs-lookup"><span data-stu-id="ef129-133">The default is 0.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ef129-134">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef129-134">Child Elements</span></span>  
  
|<span data-ttu-id="ef129-135">Element</span><span class="sxs-lookup"><span data-stu-id="ef129-135">Element</span></span>|<span data-ttu-id="ef129-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef129-136">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ef129-137">\<security></span><span class="sxs-lookup"><span data-stu-id="ef129-137">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-peertransport.md)|<span data-ttu-id="ef129-138">Definiert die Sicherheitseinstellungen für diesen Transport.</span><span class="sxs-lookup"><span data-stu-id="ef129-138">Defines the security settings for this transport.</span></span> <span data-ttu-id="ef129-139">Dieses Element ist vom Typ <xref:System.ServiceModel.Configuration.PeerSecurityElement>.</span><span class="sxs-lookup"><span data-stu-id="ef129-139">This element is of type <xref:System.ServiceModel.Configuration.PeerSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ef129-140">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef129-140">Parent Elements</span></span>  
  
|<span data-ttu-id="ef129-141">Element</span><span class="sxs-lookup"><span data-stu-id="ef129-141">Element</span></span>|<span data-ttu-id="ef129-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef129-142">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ef129-143">\<binding></span><span class="sxs-lookup"><span data-stu-id="ef129-143">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="ef129-144">Definiert alle Bindungsmöglichkeiten der benutzerdefinierten Bindung.</span><span class="sxs-lookup"><span data-stu-id="ef129-144">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ef129-145">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ef129-145">Remarks</span></span>  
 <span data-ttu-id="ef129-146">Dieser Transport kann nicht mit Verträgen verwendet werden, die Anforderungs-/Antwortvorgänge enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef129-146">This transport cannot be used with contracts that have request/reply operations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef129-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef129-147">See also</span></span>
- <xref:System.ServiceModel.Configuration.PeerTransportElement>
- <xref:System.ServiceModel.Channels.PeerTransportBindingElement>
- <xref:System.ServiceModel.Channels.TransportBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="ef129-148">Transportprotokolle</span><span class="sxs-lookup"><span data-stu-id="ef129-148">Transports</span></span>](../../../../../docs/framework/wcf/feature-details/transports.md)
- [<span data-ttu-id="ef129-149">Auswählen eines Transports</span><span class="sxs-lookup"><span data-stu-id="ef129-149">Choosing a Transport</span></span>](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)
- [<span data-ttu-id="ef129-150">Bindungen</span><span class="sxs-lookup"><span data-stu-id="ef129-150">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="ef129-151">Erweitern von Bindungen</span><span class="sxs-lookup"><span data-stu-id="ef129-151">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="ef129-152">Benutzerdefinierte Bindungen</span><span class="sxs-lookup"><span data-stu-id="ef129-152">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="ef129-153">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="ef129-153">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
