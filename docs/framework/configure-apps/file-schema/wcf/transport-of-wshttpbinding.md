---
title: '&lt;transport&gt; von &lt;wsHttpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 21e38acf-450a-4bda-82b6-de305e1f7cd8
ms.openlocfilehash: 4bd385e8c4fee1ea340e1d9df9816e25760efb02
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148629"
---
# <a name="lttransportgt-of-ltwshttpbindinggt"></a><span data-ttu-id="9e560-102">&lt;transport&gt; von &lt;wsHttpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="9e560-102">&lt;transport&gt; of &lt;wsHttpBinding&gt;</span></span>
<span data-ttu-id="9e560-103">Definiert die Authentifizierungseinstellungen für den HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="9e560-103">Defines authentication settings for the HTTP transport.</span></span>  
  
 <span data-ttu-id="9e560-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="9e560-104">\<system.serviceModel></span></span>  
<span data-ttu-id="9e560-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="9e560-105">\<bindings></span></span>  
<span data-ttu-id="9e560-106">\<wsHttpBinding></span><span class="sxs-lookup"><span data-stu-id="9e560-106">\<wsHttpBinding></span></span>  
<span data-ttu-id="9e560-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="9e560-107">\<binding></span></span>  
<span data-ttu-id="9e560-108">\<Sicherheit ></span><span class="sxs-lookup"><span data-stu-id="9e560-108">\<security></span></span>  
<span data-ttu-id="9e560-109">\<Transport ></span><span class="sxs-lookup"><span data-stu-id="9e560-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e560-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e560-110">Syntax</span></span>  
  
```xml  
<wsHttpBinding>
  <binding>
    <security mode="None|Transport|TransportWithMessageCredential|TransportCredentialOnly">
      <transport clientCredentialType="Basic|Certificate|Digest|None|Ntlm|Windows"
                 proxyCredentialType="Basic|Digest|None|Ntlm|Windows"
                 realm="string" />
        <extendedProtectionPolicy policyEnforcement="Never|WhenSupported|Always"
                                  protectionScenario="TransportSelected|TrustedProxy">
          <customServiceNames>
          </customServiceNames>
        </extendedProtecutionPolicy>
      </transport>
    </security>
  </binding>
</wsHttpBinding>
```  
  
## <a name="type"></a><span data-ttu-id="9e560-111">Typ</span><span class="sxs-lookup"><span data-stu-id="9e560-111">Type</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9e560-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9e560-112">Attributes and Elements</span></span>  
 <span data-ttu-id="9e560-113">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9e560-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9e560-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="9e560-114">Attributes</span></span>  
  
|<span data-ttu-id="9e560-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="9e560-115">Attribute</span></span>|<span data-ttu-id="9e560-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e560-116">Description</span></span>|  
|---------------|-----------------|  
|`clientCredentialType`|<span data-ttu-id="9e560-117">Gibt die zum Authentifizieren des Clients beim Dienst verwendeten Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="9e560-117">Specifies the credential used to authenticate the client to the service.</span></span> <span data-ttu-id="9e560-118">Dieses Attribut ist vom Typ <xref:System.ServiceModel.HttpClientCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="9e560-118">This attribute is of type <xref:System.ServiceModel.HttpClientCredentialType>.</span></span>|  
|`proxyCredentialType`|<span data-ttu-id="9e560-119">Gibt die Anmeldeinformationen an, die verwendet werden, um den Client bei einem Domänenproxy zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="9e560-119">Specifies the credential used to authenticate the client to a domain proxy.</span></span> <span data-ttu-id="9e560-120">Dieses Attribut ist vom Typ <xref:System.ServiceModel.HttpProxyCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="9e560-120">This attribute is of type <xref:System.ServiceModel.HttpProxyCredentialType>.</span></span>|  
|`realm`|<span data-ttu-id="9e560-121">Eine Zeichenfolge, die den Authentifizierungsbereich für die Digest- oder Standardauthentifizierung angibt.</span><span class="sxs-lookup"><span data-stu-id="9e560-121">A string that specifies the authentication realm for digest or basic authentication.</span></span> <span data-ttu-id="9e560-122">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9e560-122">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="9e560-123">Ein Authentifizierungsbereich gibt mindestens den Namen des Hosts an, der die Authentifizierung durchführt.</span><span class="sxs-lookup"><span data-stu-id="9e560-123">An authentication realm specifies at least the name of the host that performs the authentication.</span></span> <span data-ttu-id="9e560-124">Er kann auch eine Auflistung von Benutzern angeben, die Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="9e560-124">It can also specify a collection of users that has access.</span></span> <span data-ttu-id="9e560-125">Ein Benutzer kann den Authentifizierungsbereich abfragen, um zu erfahren, welche der verschiedenen möglichen Benutzernamen und Kennwörter verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9e560-125">A user can query the authentication realm to ascertain which one of the several possible usernames and passwords can be used.</span></span>|  
|`policyEnforcement`|<span data-ttu-id="9e560-126">Diese Enumeration gibt an, wann die <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e560-126">This enumeration specifies when the <xref:System.Security.Authentication.ExtendedProtection.ExtendedProtectionPolicy> should be enforced.</span></span><br /><br /> <span data-ttu-id="9e560-127">1.  Never – die Richtlinie wird nie erzwungen (erweiterter Schutz ist deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="9e560-127">1.  Never – The policy is never enforced (Extended Protection is disabled).</span></span><br /><span data-ttu-id="9e560-128">2.  WhenSupported – die Richtlinie wird nur erzwungen, wenn der Client erweiterten Schutz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e560-128">2.  WhenSupported – The policy is enforced only if the client supports Extended Protection.</span></span><br /><span data-ttu-id="9e560-129">3.  Always – die Richtlinie wird immer erzwungen.</span><span class="sxs-lookup"><span data-stu-id="9e560-129">3.  Always – The policy is always enforced.</span></span> <span data-ttu-id="9e560-130">Clients, die erweiterten Schutz nicht unterstützen, werden nicht authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="9e560-130">Clients which don’t support Extended Protection will fail to authenticate.</span></span>|  
  
## <a name="clientcredentialtype-attribute"></a><span data-ttu-id="9e560-131">clientCredentialType-Attribut</span><span class="sxs-lookup"><span data-stu-id="9e560-131">clientCredentialType Attribute</span></span>  
  
|<span data-ttu-id="9e560-132">Wert</span><span class="sxs-lookup"><span data-stu-id="9e560-132">Value</span></span>|<span data-ttu-id="9e560-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e560-133">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="9e560-134">Die Sicherheitsfunktionen sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9e560-134">Security is disabled.</span></span>|  
|`Basic`|<span data-ttu-id="9e560-135">Verwendet die Standardauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="9e560-135">Uses basic authentication.</span></span>|  
|`Digest`|<span data-ttu-id="9e560-136">Verwendet Digestauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="9e560-136">Uses digest authentication.</span></span>|  
|`Ntlm`|<span data-ttu-id="9e560-137">Verwendet als Ausweichlösung die NTLM-Authentifizierung für eine Windows-Domäne.</span><span class="sxs-lookup"><span data-stu-id="9e560-137">Uses NTLM authentication as a fallback with a Windows domain.</span></span>|  
|`Windows`|<span data-ttu-id="9e560-138">Verwendet die integrierte Windows-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="9e560-138">Uses integrated Windows authentication.</span></span>|  
|`Certificate`|<span data-ttu-id="9e560-139">Verwendet X.509-Zertifikate zum Authentifizieren des Clients.</span><span class="sxs-lookup"><span data-stu-id="9e560-139">Uses X.509 certificates to authenticate the client.</span></span>|  
  
## <a name="proxycredentialtype-attribute"></a><span data-ttu-id="9e560-140">proxyCredentialType-Attribut</span><span class="sxs-lookup"><span data-stu-id="9e560-140">proxyCredentialType Attribute</span></span>  
  
|<span data-ttu-id="9e560-141">Wert</span><span class="sxs-lookup"><span data-stu-id="9e560-141">Value</span></span>|<span data-ttu-id="9e560-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e560-142">Description</span></span>|  
|-----------|-----------------|  
|`None`|<span data-ttu-id="9e560-143">Die Sicherheitsfunktionen sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9e560-143">Security is disabled.</span></span>|  
|`Basic`|<span data-ttu-id="9e560-144">Verwendet die Standardauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="9e560-144">Uses basic authentication.</span></span>|  
|`Digest`|<span data-ttu-id="9e560-145">Verwendet Digestauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="9e560-145">Uses digest authentication.</span></span>|  
|`Ntlm`|<span data-ttu-id="9e560-146">Verwendet als Ausweichlösung NTLM für eine Windows-Domäne.</span><span class="sxs-lookup"><span data-stu-id="9e560-146">Uses NTLM as a fallback with a Windows domain.</span></span>|  
|`Windows`|<span data-ttu-id="9e560-147">Verwendet die integrierte Windows-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="9e560-147">Uses integrated Windows authentication.</span></span>|  
|`Certificate`|<span data-ttu-id="9e560-148">Verwendet X.509-Zertifikate zum Authentifizieren des Clients.</span><span class="sxs-lookup"><span data-stu-id="9e560-148">Uses X.509 certificates to authenticate the client.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9e560-149">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e560-149">Child Elements</span></span>  
 <span data-ttu-id="9e560-150">Keine</span><span class="sxs-lookup"><span data-stu-id="9e560-150">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9e560-151">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e560-151">Parent Elements</span></span>  
  
|<span data-ttu-id="9e560-152">Element</span><span class="sxs-lookup"><span data-stu-id="9e560-152">Element</span></span>|<span data-ttu-id="9e560-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e560-153">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9e560-154">\<security></span><span class="sxs-lookup"><span data-stu-id="9e560-154">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-wshttpbinding.md)|<span data-ttu-id="9e560-155">Gibt die Sicherheitsfunktionen von der [ \<WsHttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="9e560-155">Represents the security capabilities of the [\<wsHttpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9e560-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e560-156">See Also</span></span>  
 <xref:System.ServiceModel.HttpTransportSecurity>  
 <xref:System.ServiceModel.WSHttpSecurity.Transport%2A>  
 <xref:System.ServiceModel.Configuration.WSHttpSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.Configuration.HttpTransportSecurityElement>  
 [<span data-ttu-id="9e560-157">Sichern von Diensten und Clients</span><span class="sxs-lookup"><span data-stu-id="9e560-157">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="9e560-158">Bindungen</span><span class="sxs-lookup"><span data-stu-id="9e560-158">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="9e560-159">Konfigurieren der vom System bereitgestellten Bindungen</span><span class="sxs-lookup"><span data-stu-id="9e560-159">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="9e560-160">Verwenden von Bindungen, um Dienste und Clients zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9e560-160">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="9e560-161">\<binding></span><span class="sxs-lookup"><span data-stu-id="9e560-161">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
