---
title: '&lt;localIssuer&gt;'
ms.date: 03/30/2017
ms.assetid: 26bdd0df-0e7d-4b9e-bbeb-f28c53769385
ms.openlocfilehash: 893ac2cb0e6c54beae68e2607c31564baafd95fe
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54527548"
---
# <a name="ltlocalissuergt"></a><span data-ttu-id="5ffbc-102">&lt;localIssuer&gt;</span><span class="sxs-lookup"><span data-stu-id="5ffbc-102">&lt;localIssuer&gt;</span></span>
<span data-ttu-id="5ffbc-103">Gibt die Adresse und Bindung des lokalen Ausstellers zum Abrufen eines Sicherheitstokens an.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-103">Specifies the address and binding of the local issuer to be used to obtain a security token.</span></span>  
  
 <span data-ttu-id="5ffbc-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="5ffbc-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="5ffbc-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="5ffbc-105">\<behaviors></span></span>  
<span data-ttu-id="5ffbc-106">EndpointBehaviors-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5ffbc-106">endpointBehaviors section</span></span>  
<span data-ttu-id="5ffbc-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="5ffbc-107">\<behavior></span></span>  
<span data-ttu-id="5ffbc-108">\<clientCredentials></span><span class="sxs-lookup"><span data-stu-id="5ffbc-108">\<clientCredentials></span></span>  
<span data-ttu-id="5ffbc-109">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="5ffbc-109">\<issuedToken></span></span>  
<span data-ttu-id="5ffbc-110">\<localIssuer></span><span class="sxs-lookup"><span data-stu-id="5ffbc-110">\<localIssuer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ffbc-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ffbc-111">Syntax</span></span>  
  
```xml  
<localIssuer address="String"
             binding="String"
             bindingConfiguration="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5ffbc-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5ffbc-112">Attributes and Elements</span></span>  
 <span data-ttu-id="5ffbc-113">In den folgenden Abschnitten werden Attribute, untergeordnete Elemente sowie übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-113">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5ffbc-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="5ffbc-114">Attributes</span></span>  
  
|<span data-ttu-id="5ffbc-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="5ffbc-115">Attribute</span></span>|<span data-ttu-id="5ffbc-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ffbc-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5ffbc-117">Adresse</span><span class="sxs-lookup"><span data-stu-id="5ffbc-117">address</span></span>|<span data-ttu-id="5ffbc-118">Erforderliche Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-118">Required string.</span></span> <span data-ttu-id="5ffbc-119">Gibt den URI des lokalen Ausstellers an.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-119">Specifies the URI of the local issuer.</span></span>|  
|<span data-ttu-id="5ffbc-120">Bindung</span><span class="sxs-lookup"><span data-stu-id="5ffbc-120">binding</span></span>|<span data-ttu-id="5ffbc-121">Optionale Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-121">Optional string.</span></span> <span data-ttu-id="5ffbc-122">Eine der vom System bereitgestellten Bindungen.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-122">One of the system-provided bindings.</span></span> <span data-ttu-id="5ffbc-123">Eine Liste finden Sie unter [System-provided Bindings](../../../../../docs/framework/wcf/system-provided-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="5ffbc-123">For a list, see [System-Provided Bindings](../../../../../docs/framework/wcf/system-provided-bindings.md).</span></span>|  
|<span data-ttu-id="5ffbc-124">bindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ffbc-124">bindingConfiguration</span></span>|<span data-ttu-id="5ffbc-125">Optionale Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-125">Optional string.</span></span> <span data-ttu-id="5ffbc-126">Gibt eine Bindungskonfiguration aus der Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-126">Specifies a binding configuration found in the configuration file.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5ffbc-127">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5ffbc-127">Child Elements</span></span>  
  
|<span data-ttu-id="5ffbc-128">Element</span><span class="sxs-lookup"><span data-stu-id="5ffbc-128">Element</span></span>|<span data-ttu-id="5ffbc-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ffbc-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5ffbc-130">\<identity></span><span class="sxs-lookup"><span data-stu-id="5ffbc-130">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="5ffbc-131">Gibt Identitätsinformationen für den lokalen Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-131">Specifies identity information for the local issuer.</span></span>|  
|[<span data-ttu-id="5ffbc-132">\<headers></span><span class="sxs-lookup"><span data-stu-id="5ffbc-132">\<headers></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|<span data-ttu-id="5ffbc-133">Eine Auflistung von Adressheadern, die erforderlich sind, um den lokalen Aussteller ordnungsgemäß zu adressieren.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-133">A collection of address headers that are required in order to correctly address the local issuer.</span></span> <span data-ttu-id="5ffbc-134">Sie können das `add`-Schlüsselwort verwenden, um dieser Auflistung einen Header hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-134">You can use the `add` keyword to add a header to this collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5ffbc-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5ffbc-135">Parent Elements</span></span>  
  
|<span data-ttu-id="5ffbc-136">Element</span><span class="sxs-lookup"><span data-stu-id="5ffbc-136">Element</span></span>|<span data-ttu-id="5ffbc-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ffbc-137">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5ffbc-138">\<issuedToken></span><span class="sxs-lookup"><span data-stu-id="5ffbc-138">\<issuedToken></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|<span data-ttu-id="5ffbc-139">Gibt ein benutzerdefiniertes Token an, das zum Authentifizieren eines Clients bei einem Dienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-139">Specifies a custom token used to authenticate a client to a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5ffbc-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ffbc-140">Remarks</span></span>  
 <span data-ttu-id="5ffbc-141">Beim Abrufen eines von einem Sicherheitstokendienst (Security Token Service, STS) ausgestellten Tokens muss die Clientanwendung mit der zu verwendenden Adresse und Bindung konfiguriert sein, um mit dem STS kommunizieren zu können.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-141">When obtaining an issued token from a Security Token Service (STS), the client application must be configured with the address and binding to use to communicate with the STS.</span></span> <span data-ttu-id="5ffbc-142">Wenn die <xref:System.ServiceModel.WSFederationHttpBinding> stellt keine URL für den Sicherheitstokendienst, oder wenn die Ausstelleradresse einer verbundbindung `http://schemas.microsoft.com/2005/12/ServiceModel/Addressing/Anonymous` oder `null`, Windows Communication Foundation (WCF)-Clientchannel verwendet die angegebenen Werte von `address`und `binding` für die Kommunikation mit dem STS, um das ausgestellte Token abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5ffbc-142">When the <xref:System.ServiceModel.WSFederationHttpBinding> does not supply a URL for the security token service, or when the issuer address of a federated binding is `http://schemas.microsoft.com/2005/12/ServiceModel/Addressing/Anonymous` or `null`, the client's Windows Communication Foundation (WCF) channel uses the values specified by `address` and `binding` to communicate with the STS to obtain the issued token.</span></span> <span data-ttu-id="5ffbc-143">Weitere Informationen zum Konfigurieren eines lokalen Ausstellers finden Sie unter [Vorgehensweise: Konfigurieren eines lokalen Ausstellers](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md).</span><span class="sxs-lookup"><span data-stu-id="5ffbc-143">For more information on configuring a local issuer, see [How to: Configure a Local Issuer](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="5ffbc-144">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5ffbc-144">Example</span></span>  
 <span data-ttu-id="5ffbc-145">Im folgenden Beispiel werden die Attribute `address`, `binding` und `bindingConfiguration` eines `localIssuer`-Elements festgelegt:</span><span class="sxs-lookup"><span data-stu-id="5ffbc-145">The following example sets the `address`, `binding`, and `bindingConfiguration` attributes of a `localIssuer` element.</span></span>  
  
```xml  
<system.serviceModel>
  <behaviors>
    <endpointBehaviors>
      <behavior name="MyEndpointBehavior">
        <clientCredentials>
          <issuedToken cacheIssuedTokens="false"
                       defaultKeyEntropyMode="ClientEntropy">
            <localIssuer address="net.tcp://cohowinery/tokens"
                         binding="netTcpBinding"
                         bindingConfiguration="myTcpBindingConfig" />
          </issuedToken>
        </clientCredentials>
      </behavior>
    </endpointBehaviors>
  </behaviors>
</system.serviceModel>
```  
  
## <a name="see-also"></a><span data-ttu-id="5ffbc-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ffbc-146">See also</span></span>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.LocalIssuer%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersEndpointAddressElement>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential>
- [<span data-ttu-id="5ffbc-147">Sicherheitsverhalten</span><span class="sxs-lookup"><span data-stu-id="5ffbc-147">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="5ffbc-148">Vorgehensweise: Konfigurieren eines lokalen Ausstellers</span><span class="sxs-lookup"><span data-stu-id="5ffbc-148">How to: Configure a Local Issuer</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [<span data-ttu-id="5ffbc-149">Dienstidentität und Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="5ffbc-149">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="5ffbc-150">Sicherheitsverhalten</span><span class="sxs-lookup"><span data-stu-id="5ffbc-150">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="5ffbc-151">Verbund und ausgestellte Token</span><span class="sxs-lookup"><span data-stu-id="5ffbc-151">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="5ffbc-152">Sichern von Diensten und Clients</span><span class="sxs-lookup"><span data-stu-id="5ffbc-152">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="5ffbc-153">Sichern von Clients</span><span class="sxs-lookup"><span data-stu-id="5ffbc-153">Securing Clients</span></span>](../../../../../docs/framework/wcf/securing-clients.md)
- [<span data-ttu-id="5ffbc-154">Vorgehensweise: Erstellen eines Verbundclients</span><span class="sxs-lookup"><span data-stu-id="5ffbc-154">How to: Create a Federated Client</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [<span data-ttu-id="5ffbc-155">Verbund und ausgestellte Token</span><span class="sxs-lookup"><span data-stu-id="5ffbc-155">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
