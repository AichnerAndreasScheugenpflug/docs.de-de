---
title: '&lt;allowedAudienceUris&gt;'
ms.date: 03/30/2017
ms.assetid: 0f4dc73d-d95d-4193-9755-7df4cf2b8e1c
ms.openlocfilehash: cbbe817cb647589bf30dfeb6068c2c37536277fe
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151849"
---
# <a name="ltallowedaudienceurisgt"></a><span data-ttu-id="0d214-102">&lt;allowedAudienceUris&gt;</span><span class="sxs-lookup"><span data-stu-id="0d214-102">&lt;allowedAudienceUris&gt;</span></span>
<span data-ttu-id="0d214-103">Stellt eine Auflistung von Ziel-URIs dar, für die das <xref:System.IdentityModel.Tokens.SamlSecurityToken>-Sicherheitstoken verwendet werden kann, sodass diese von einer <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>-Instanz als gültig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="0d214-103">Represents a collection of target URIs for which the <xref:System.IdentityModel.Tokens.SamlSecurityToken> security token can be targeted for in order to be considered valid by a <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> instance.</span></span>  
  
 <span data-ttu-id="0d214-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="0d214-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="0d214-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="0d214-105">\<behaviors></span></span>  
<span data-ttu-id="0d214-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="0d214-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="0d214-107">\<Verhalten ></span><span class="sxs-lookup"><span data-stu-id="0d214-107">\<behavior></span></span>  
<span data-ttu-id="0d214-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="0d214-108">\<serviceCredentials></span></span>  
<span data-ttu-id="0d214-109">\<IssuedTokenAuthentication ></span><span class="sxs-lookup"><span data-stu-id="0d214-109">\<issuedTokenAuthentication></span></span>  
<span data-ttu-id="0d214-110">\<AllowedAudienceUris ></span><span class="sxs-lookup"><span data-stu-id="0d214-110">\<allowedAudienceUris></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0d214-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d214-111">Syntax</span></span>  
  
```xml  
<allowedAudienceUris>
  <add allowedAudienceUri="String" />
</allowedAudienceUris>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0d214-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0d214-112">Attributes and Elements</span></span>  
 <span data-ttu-id="0d214-113">In den folgenden Abschnitten werden Attribute, untergeordnete Elemente sowie übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d214-113">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0d214-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d214-114">Attributes</span></span>  
 <span data-ttu-id="0d214-115">Keine</span><span class="sxs-lookup"><span data-stu-id="0d214-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0d214-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d214-116">Child Elements</span></span>  
  
|<span data-ttu-id="0d214-117">Element</span><span class="sxs-lookup"><span data-stu-id="0d214-117">Element</span></span>|<span data-ttu-id="0d214-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d214-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0d214-119">\<add></span><span class="sxs-lookup"><span data-stu-id="0d214-119">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowedaudienceuris.md)|<span data-ttu-id="0d214-120">Fügt einen Ziel-URI hinzu, für den das <xref:System.IdentityModel.Tokens.SamlSecurityToken>-Sicherheitstoken verwendet werden kann, sodass dieser von einer <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>-Instanz als gültig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="0d214-120">Adds a target Uri for which the <xref:System.IdentityModel.Tokens.SamlSecurityToken> security token can be targeted for in order to be considered valid by a <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> instance.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0d214-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d214-121">Parent Elements</span></span>  
  
|<span data-ttu-id="0d214-122">Element</span><span class="sxs-lookup"><span data-stu-id="0d214-122">Element</span></span>|<span data-ttu-id="0d214-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d214-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0d214-124">\<IssuedTokenAuthentication ></span><span class="sxs-lookup"><span data-stu-id="0d214-124">\<issuedTokenAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md)|<span data-ttu-id="0d214-125">Gibt ein Token an, das als Dienstanmeldeinformation ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d214-125">Specifies a token issued as a service credential.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0d214-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d214-126">Remarks</span></span>  
 <span data-ttu-id="0d214-127">Verwenden Sie diese Auflistung in einer Verbundanwendung, die einen Sicherheitstokendienst (Security Token Service, STS) nutzt, der <xref:System.IdentityModel.Tokens.SamlSecurityToken>-Sicherheitstoken ausstellt.</span><span class="sxs-lookup"><span data-stu-id="0d214-127">You should use this collection in a federated application that utilizes a security token service (STS) that issues <xref:System.IdentityModel.Tokens.SamlSecurityToken> security tokens.</span></span> <span data-ttu-id="0d214-128">Wenn der STS das Sicherheitstoken ausstellt, kann er den URI des Webdiensts angeben, für den das Sicherheitstoken verwendet werden soll, indem <xref:System.IdentityModel.Tokens.SamlAudienceRestrictionCondition> dem Sicherheitstoken hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0d214-128">When the STS issues the security token, it can specify the URI of the Web services for which the security token is intended by adding a <xref:System.IdentityModel.Tokens.SamlAudienceRestrictionCondition> to the security token.</span></span> <span data-ttu-id="0d214-129">Der <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> für den Webdienst kann so überprüfen, ob das ausgestellte Sicherheitstoken für diesen Webdienst ausgelegt ist, indem diese Überprüfung durchgeführt wird. Führen Sie hierzu die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0d214-129">That allows the <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> for the recipient Web service to verify that the issued security token is intended for this Web service by specifying that this check should happen by doing the following:</span></span>  
  
-   <span data-ttu-id="0d214-130">Legen Sie das `audienceUriMode`-Attribut für `<issuedTokenAuthentication>` auf <xref:System.IdentityModel.Selectors.AudienceUriMode.Always> oder <xref:System.IdentityModel.Selectors.AudienceUriMode.BearerKeyOnly> fest.</span><span class="sxs-lookup"><span data-stu-id="0d214-130">Set the `audienceUriMode` attribute of `<issuedTokenAuthentication>` to <xref:System.IdentityModel.Selectors.AudienceUriMode.Always> or <xref:System.IdentityModel.Selectors.AudienceUriMode.BearerKeyOnly>.</span></span>  
  
-   <span data-ttu-id="0d214-131">Geben Sie den Satz gültiger URIs an, indem Sie die URIs dieser Auflistung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d214-131">Specify the set of valid URIs, by adding the URIs to this collection.</span></span>  
  
 <span data-ttu-id="0d214-132">Weitere Informationen finden Sie unter <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>.</span><span class="sxs-lookup"><span data-stu-id="0d214-132">For more information, see <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>.</span></span>  
  
 <span data-ttu-id="0d214-133">Weitere Informationen zur Verwendung dieses Konfigurationselements finden Sie unter [Vorgehensweise: Konfigurieren von Anmeldeinformationen für einen Verbunddienst](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md).</span><span class="sxs-lookup"><span data-stu-id="0d214-133">For more information on using this configuration element, see [How to: Configure Credentials on a Federation Service](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d214-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d214-134">See Also</span></span>  
 <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>  
 <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator.AllowedAudienceUris%2A>  
 <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator.AudienceUriMode%2A>  
 <xref:System.ServiceModel.Configuration.IssuedTokenServiceElement.AllowedAudienceUris%2A>  
 <xref:System.ServiceModel.Configuration.AllowedAudienceUriElementCollection>  
 <xref:System.ServiceModel.Configuration.AllowedAudienceUriElement>  
 <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.AllowedAudienceUris%2A>  
 [<span data-ttu-id="0d214-135">\<IssuedTokenAuthentication ></span><span class="sxs-lookup"><span data-stu-id="0d214-135">\<issuedTokenAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md)  
 [<span data-ttu-id="0d214-136">\<add></span><span class="sxs-lookup"><span data-stu-id="0d214-136">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowedaudienceuris.md)  
 [<span data-ttu-id="0d214-137">Sicherheitsverhalten</span><span class="sxs-lookup"><span data-stu-id="0d214-137">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)  
 [<span data-ttu-id="0d214-138">Sichern von Diensten und Clients</span><span class="sxs-lookup"><span data-stu-id="0d214-138">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="0d214-139">Vorgehensweise: Konfigurieren von Anmeldeinformationen für einen Verbunddienst</span><span class="sxs-lookup"><span data-stu-id="0d214-139">How to: Configure Credentials on a Federation Service</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md)
