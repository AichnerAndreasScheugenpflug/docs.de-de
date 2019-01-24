---
title: '&lt;trustedIssuers&gt;'
ms.date: 03/30/2017
ms.assetid: d818c917-07b4-40db-9801-8676561859fd
author: BrucePerlerMS
ms.openlocfilehash: 1459027ae22344d5b1abc917c490b8e98fa0f2c3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54633998"
---
# <a name="lttrustedissuersgt"></a><span data-ttu-id="6fc2a-102">&lt;trustedIssuers&gt;</span><span class="sxs-lookup"><span data-stu-id="6fc2a-102">&lt;trustedIssuers&gt;</span></span>
<span data-ttu-id="6fc2a-103">Konfiguriert die Liste der vertrauenswürdigen ausstellerzertifikate, die von der konfigurationsbasierten ausstellernamenregistrierung verwendet (<xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>).</span><span class="sxs-lookup"><span data-stu-id="6fc2a-103">Configures the list of trusted issuer certificates used by the configuration-based issuer name registry (<xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>).</span></span>  
  
 <span data-ttu-id="6fc2a-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="6fc2a-104">\<system.identityModel></span></span>  
<span data-ttu-id="6fc2a-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="6fc2a-105">\<identityConfiguration></span></span>  
<span data-ttu-id="6fc2a-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="6fc2a-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="6fc2a-107">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="6fc2a-107">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="6fc2a-108">\<issuerNameRegistry></span><span class="sxs-lookup"><span data-stu-id="6fc2a-108">\<issuerNameRegistry></span></span>  
<span data-ttu-id="6fc2a-109">\<trustedIssuers></span><span class="sxs-lookup"><span data-stu-id="6fc2a-109">\<trustedIssuers></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6fc2a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fc2a-110">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <issuerNameRegistry>  
          <trustedIssuers>  
            <add thumbprint=xs:string name=xs:string>  
            <clear>  
            <remove thumbprint=xs:string>  
          </trustedIssuers>  
        </issuerNameRegistry>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6fc2a-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6fc2a-111">Attributes and Elements</span></span>  
 <span data-ttu-id="6fc2a-112">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6fc2a-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="6fc2a-113">Attributes</span></span>  
 <span data-ttu-id="6fc2a-114">Keine</span><span class="sxs-lookup"><span data-stu-id="6fc2a-114">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="6fc2a-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fc2a-115">Child Elements</span></span>  
  
|<span data-ttu-id="6fc2a-116">Element</span><span class="sxs-lookup"><span data-stu-id="6fc2a-116">Element</span></span>|<span data-ttu-id="6fc2a-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fc2a-117">Description</span></span>|  
|-------------|-----------------|  
|`<add thumbprint=xs:string name=xs:string>`|<span data-ttu-id="6fc2a-118">Fügt ein Zertifikat zur Auflistung der vertrauenswürdigen Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-118">Adds a certificate to the collection of trusted issuers.</span></span> <span data-ttu-id="6fc2a-119">Das Zertifikat ist angegeben, mit der `thumbprint` Attribut.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-119">The certificate is specified with the `thumbprint` attribute.</span></span> <span data-ttu-id="6fc2a-120">Dieses Attribut ist erforderlich und sollte das Formular codierte ASN. 1 den Fingerabdruck des Zertifikats enthalten.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-120">This attribute is required and should contain the ASN.1 encoded form of the certificate thumbprint.</span></span> <span data-ttu-id="6fc2a-121">Die `name` Attribut ist optional und kann verwendet werden, um einen Anzeigenamen für das Zertifikat anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-121">The `name` attribute is optional and can be used to specify a friendly name for the certificate.</span></span>|  
|`<clear>`|<span data-ttu-id="6fc2a-122">Löscht alle Zertifikate aus der Auflistung der vertrauenswürdigen Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-122">Clears all certificates from the collection of trusted issuers.</span></span>|  
|`<remove thumbprint=xs:string>`|<span data-ttu-id="6fc2a-123">Entfernt ein Zertifikat aus der Auflistung der vertrauenswürdigen Aussteller an.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-123">Removes a certificate from the collection of trusted issuers.</span></span> <span data-ttu-id="6fc2a-124">Das Zertifikat ist angegeben, mit der `thumbprint` Attribut.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-124">The certificate is specified with the `thumbprint` attribute.</span></span> <span data-ttu-id="6fc2a-125">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-125">This attribute is required.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6fc2a-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fc2a-126">Parent Elements</span></span>  
  
|<span data-ttu-id="6fc2a-127">Element</span><span class="sxs-lookup"><span data-stu-id="6fc2a-127">Element</span></span>|<span data-ttu-id="6fc2a-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fc2a-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6fc2a-129">\<issuerNameRegistry></span><span class="sxs-lookup"><span data-stu-id="6fc2a-129">\<issuerNameRegistry></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuernameregistry.md)|<span data-ttu-id="6fc2a-130">Konfiguriert die Ausstellernamen-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-130">Configures the issuer name registry.</span></span> <span data-ttu-id="6fc2a-131">**Wichtig:**  Die `type` Attribut der `<issuerNameRegistry>` Elementverweis muss die <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> -Klasse für die `<trustedIssuers>` Element gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-131">**Important:**  The `type` attribute of the `<issuerNameRegistry>` element must reference the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class for the `<trustedIssuers>` element to be valid.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6fc2a-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6fc2a-132">Remarks</span></span>  
 <span data-ttu-id="6fc2a-133">Windows Identity Foundation (WIF) bietet eine einzige Implementierung der <xref:System.IdentityModel.Tokens.IssuerNameRegistry> Klasse standardmäßig den <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> Klasse.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-133">Windows Identity Foundation (WIF) provides a single implementation of the <xref:System.IdentityModel.Tokens.IssuerNameRegistry> class out of the box, the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class.</span></span> <span data-ttu-id="6fc2a-134">Die Konfiguration Ausstellernamen-Registrierung verwaltet eine Liste der vertrauenswürdigen Aussteller, die aus der Konfiguration geladen wird.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-134">The configuration issuer name registry maintains a list of trusted issuers that is loaded from configuration.</span></span> <span data-ttu-id="6fc2a-135">Die Liste ordnet jeden Ausstellernamen dem x. 509-Zertifikat, das benötigt wird, um zu überprüfen, ob die Signatur von Token, die vom Aussteller erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-135">The list associates each issuer name with the X.509 certificate that is needed to verify the signature of tokens produced by the issuer.</span></span> <span data-ttu-id="6fc2a-136">Die Liste von Zertifikaten vertrauenswürdiger Aussteller wird angegeben, unter dem `<trustedIssuers>` Element.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-136">The list of trusted issuer certificates is specified under the `<trustedIssuers>` element.</span></span> <span data-ttu-id="6fc2a-137">Jedes Element in der Liste ordnet einen Ausstellernamen für die mnemonischen, mit dem x. 509-Zertifikat, das zum Überprüfen der Signatur von Token, die von diesem Aussteller erzeugt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-137">Each element in the list associates a mnemonic issuer name with the X.509 certificate that is needed to verify the signature of tokens produced by that issuer.</span></span> <span data-ttu-id="6fc2a-138">Vertrauenswürdige Zertifikate mithilfe der ASN. 1-codierte Form der Fingerabdruck des Zertifikats angegeben werden und werden die Auflistung hinzugefügt, mit `<add>` Element.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-138">Trusted certificates are specified using the ASN.1 encoded form of the certificate thumbprint and are added the collection by using `<add>` element.</span></span> <span data-ttu-id="6fc2a-139">Sie können das Löschen oder Entfernen von Aussteller (Zertifikate) aus der Liste mit den `<clear>` und `<remove>` Elemente.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-139">You can clear or remove issuers (certificates) from the list by using the `<clear>` and `<remove>` elements.</span></span>  
  
 <span data-ttu-id="6fc2a-140">Die `type` Attribut der `<issuerNameRegistry>` Elementverweis muss die <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> -Klasse für die `<trustedIssuers>` Element gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-140">The `type` attribute of the `<issuerNameRegistry>` element must reference the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class for the `<trustedIssuers>` element to be valid.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6fc2a-141">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6fc2a-141">Example</span></span>  
 <span data-ttu-id="6fc2a-142">Das folgende XML zeigt, wie an den Aussteller für die Konfiguration basiert-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="6fc2a-142">The following XML shows how to specify the configuration based issuer name registry.</span></span>  
  
```xml  
<issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
  <trustedIssuers>  
    <add thumbprint="9B74CB2F32 … B1DC01EF40D0" name="LocalSTS" />  
  </trustedIssuers>  
</issuerNameRegistry>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6fc2a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fc2a-143">See also</span></span>
- <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>
- <xref:System.IdentityModel.Tokens.IssuerNameRegistry>
