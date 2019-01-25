---
title: '&lt;resolver&gt;'
ms.date: 03/30/2017
ms.assetid: 0c00200c-f135-4e5c-a024-76b72bcbc021
ms.openlocfilehash: 2a3e0de2bb5d2ed022f53aa5e498f338eaf56ca8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54578598"
---
# <a name="ltresolvergt"></a><span data-ttu-id="35044-102">&lt;resolver&gt;</span><span class="sxs-lookup"><span data-stu-id="35044-102">&lt;resolver&gt;</span></span>
<span data-ttu-id="35044-103">Gibt einen Peerresolver an, der zum Auflösen einer Peermesh-ID in einen Satz von Peerknotenadressen verwendet wird, die verschiedene Knoten im Mesh angeben.</span><span class="sxs-lookup"><span data-stu-id="35044-103">Specifies a peer resolver that is used to resolve a peer mesh ID to a set of peer node addresses that represents several nodes that participate in the mesh.</span></span>  
  
 <span data-ttu-id="35044-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="35044-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="35044-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="35044-105">\<bindings></span></span>  
<span data-ttu-id="35044-106">\<netPeerBinding></span><span class="sxs-lookup"><span data-stu-id="35044-106">\<netPeerBinding></span></span>  
<span data-ttu-id="35044-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="35044-107">\<binding></span></span>  
<span data-ttu-id="35044-108">\<resolver></span><span class="sxs-lookup"><span data-stu-id="35044-108">\<resolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35044-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="35044-109">Syntax</span></span>  
  
```xml  
<resolver mode="Auto/Custom/Pnrp"
          referralPolicy="DoNotShare/Service/Share">
</resolver>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="35044-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="35044-110">Attributes and Elements</span></span>  
 <span data-ttu-id="35044-111">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="35044-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="35044-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="35044-112">Attributes</span></span>  
  
|<span data-ttu-id="35044-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="35044-113">Attribute</span></span>|<span data-ttu-id="35044-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35044-114">Description</span></span>|  
|---------------|-----------------|  
|`mode`|<span data-ttu-id="35044-115">Eine Zeichenfolge, die angibt, ob die diesem Dienst zugeordnete Peerresolverinstanz PNRP-spezifisch ist, ein benutzerdefinierter Resolver ist oder automatisch festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="35044-115">A string that specifies whether the peer resolver instance associated with this service is either PNRP-specific, a custom resolver, or automatically determined.</span></span> <span data-ttu-id="35044-116">Dieses Attribut ist vom Typ <xref:System.ServiceModel.PeerResolvers.PeerResolverMode>.</span><span class="sxs-lookup"><span data-stu-id="35044-116">This attribute is of type <xref:System.ServiceModel.PeerResolvers.PeerResolverMode>.</span></span>|  
|`referralPolicy`|<span data-ttu-id="35044-117">Eine Zeichenfolge, die angibt, wie Verweise unter Peers freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="35044-117">A string that specifies the way referrals are shared among peers.</span></span> <span data-ttu-id="35044-118">Dieses Attribut ist vom Typ <xref:System.ServiceModel.PeerResolvers.PeerReferralPolicy>.</span><span class="sxs-lookup"><span data-stu-id="35044-118">This attribute is of type <xref:System.ServiceModel.PeerResolvers.PeerReferralPolicy>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="35044-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35044-119">Child Elements</span></span>  
  
|<span data-ttu-id="35044-120">Element</span><span class="sxs-lookup"><span data-stu-id="35044-120">Element</span></span>|<span data-ttu-id="35044-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35044-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="35044-122">\<headers></span><span class="sxs-lookup"><span data-stu-id="35044-122">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers.md)|<span data-ttu-id="35044-123">Gibt die spezifischen Einstellungen für einen benutzerdefinierten Peerresolverdienst an.</span><span class="sxs-lookup"><span data-stu-id="35044-123">Specifies settings for a custom peer resolver service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="35044-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35044-124">Parent Elements</span></span>  
  
|<span data-ttu-id="35044-125">Element</span><span class="sxs-lookup"><span data-stu-id="35044-125">Element</span></span>|<span data-ttu-id="35044-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35044-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="35044-127">\<binding></span><span class="sxs-lookup"><span data-stu-id="35044-127">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="35044-128">Definiert alle bindungsfähigkeiten von der [ \<NetPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="35044-128">Defines all binding capabilities of the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="35044-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35044-129">Remarks</span></span>  
 <span data-ttu-id="35044-130">Ein Peernamensresolver ist ein Ermittlungsdienst, der von Peerkanälen zum Suchen von Peerknoten in einem Peermesh verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="35044-130">A peer name resolver is a discovery service used by peer channels to find peer nodes that participate in a peer mesh.</span></span> <span data-ttu-id="35044-131">Außerdem wird er verwendet, um einen Knoten in einem Peermesh zu registrieren, wodurch der Peerknoten erkannt und im Peermesh verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="35044-131">It is also used to "register" a node with a peer mesh, the mechanism by which the peer node becomes known and available from the peer mesh.</span></span> <span data-ttu-id="35044-132">Weitere Informationen über PeerResolver finden Sie unter [PeerResolver](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md).</span><span class="sxs-lookup"><span data-stu-id="35044-132">For more information on peer resolvers, see [Peer Resolvers](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="35044-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35044-133">See also</span></span>
- <xref:System.ServiceModel.PeerResolver>
- <xref:System.ServiceModel.PeerResolvers.PeerResolverSettings>
- <xref:System.ServiceModel.NetPeerTcpBinding.Resolver%2A>
- <xref:System.ServiceModel.Configuration.NetPeerTcpBindingElement.Resolver%2A>
- <xref:System.ServiceModel.Configuration.PeerResolverElement>
- [<span data-ttu-id="35044-134">Peerresolver</span><span class="sxs-lookup"><span data-stu-id="35044-134">Peer Resolvers</span></span>](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)
- [<span data-ttu-id="35044-135">Hinzufügen eines benutzerdefinierten Konfliktlösers zu einer PeerChannel-Anwendung</span><span class="sxs-lookup"><span data-stu-id="35044-135">Adding a Custom Resolver to a PeerChannel Application</span></span>](https://msdn.microsoft.com/library/12aa3787-2962-439c-ad27-46523c8b0419)
