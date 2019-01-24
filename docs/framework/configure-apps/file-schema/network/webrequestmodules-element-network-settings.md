---
title: '&lt;WebRequestModules&gt; -Element (Netzwerkeinstellungen)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/webRequestModules
- http://schemas.microsoft.com/.NetConfiguration/v2.0#webRequestModules
helpviewer_keywords:
- webRequestModules element
- <webRequestModules> element
ms.assetid: 1263de11-3e0a-4f94-97c9-710b2ae53817
ms.openlocfilehash: 4e2a37f6829341b33475f91796e8671d867ac151
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54699791"
---
# <a name="ltwebrequestmodulesgt-element-network-settings"></a><span data-ttu-id="d7484-102">&lt;WebRequestModules&gt; -Element (Netzwerkeinstellungen)</span><span class="sxs-lookup"><span data-stu-id="d7484-102">&lt;webRequestModules&gt; Element (Network Settings)</span></span>
<span data-ttu-id="d7484-103">Gibt die Module zu verwenden, um Informationen aus der Hosts im Netzwerk anzufordern.</span><span class="sxs-lookup"><span data-stu-id="d7484-103">Specifies modules to use to request information from network hosts.</span></span>  
  
 <span data-ttu-id="d7484-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="d7484-104">\<configuration></span></span>  
<span data-ttu-id="d7484-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="d7484-105">\<system.net></span></span>  
<span data-ttu-id="d7484-106">\<webRequestModules></span><span class="sxs-lookup"><span data-stu-id="d7484-106">\<webRequestModules></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d7484-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7484-107">Syntax</span></span>  
  
```xml  
<webRequestModules>   
</webRequestModules>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d7484-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d7484-108">Attributes and Elements</span></span>  
 <span data-ttu-id="d7484-109">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d7484-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d7484-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d7484-110">Attributes</span></span>  
 <span data-ttu-id="d7484-111">Keine</span><span class="sxs-lookup"><span data-stu-id="d7484-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d7484-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d7484-112">Child Elements</span></span>  
  
|<span data-ttu-id="d7484-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7484-113">**Element**</span></span>|<span data-ttu-id="d7484-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d7484-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="d7484-115">add</span><span class="sxs-lookup"><span data-stu-id="d7484-115">add</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-webrequestmodules-network-settings.md)|<span data-ttu-id="d7484-116">Die Anwendung hinzugefügt ein benutzerdefinierte Webanforderungsmodul.</span><span class="sxs-lookup"><span data-stu-id="d7484-116">Adds a custom Web request module to the application.</span></span>|  
|[<span data-ttu-id="d7484-117">clear</span><span class="sxs-lookup"><span data-stu-id="d7484-117">clear</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-webrequestmodules-network-settings.md)|<span data-ttu-id="d7484-118">Entfernt alle registrierte Webanforderungsmodulen aus der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="d7484-118">Removes all registered Web request modules from the application.</span></span>|  
|[<span data-ttu-id="d7484-119">remove</span><span class="sxs-lookup"><span data-stu-id="d7484-119">remove</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-webrequestmodules-network-settings.md)|<span data-ttu-id="d7484-120">Entfernt ein benutzerdefinierte Webanforderungsmodul aus der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="d7484-120">Removes a custom Web request module from the application.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d7484-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d7484-121">Parent Elements</span></span>  
  
|<span data-ttu-id="d7484-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7484-122">**Element**</span></span>|<span data-ttu-id="d7484-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d7484-123">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="d7484-124">system.net</span><span class="sxs-lookup"><span data-stu-id="d7484-124">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="d7484-125">Enthält Einstellungen, die festlegen, wie Verbindungen zwischen .NET Framework und dem Netzwerk hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d7484-125">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d7484-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7484-126">Remarks</span></span>  
 <span data-ttu-id="d7484-127">Die `webRequestModules` Element registriert Nachfolger der <xref:System.Net.WebRequest> -Klasse zur Verarbeitung von Anforderungen an die Hosts im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d7484-127">The `webRequestModules` element registers descendants of the <xref:System.Net.WebRequest> class to handle information requests to network hosts.</span></span> <span data-ttu-id="d7484-128">Webanforderungsmodule müssen implementieren die <xref:System.Net.IWebRequestCreate> Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d7484-128">Web request modules must implement the <xref:System.Net.IWebRequestCreate> interface.</span></span>  
  
 <span data-ttu-id="d7484-129">.NET Framework enthält Webanforderungsmodule für URIs, die mit beginnen `http://`, `https://`, und `file://`.</span><span class="sxs-lookup"><span data-stu-id="d7484-129">The .NET Framework includes Web request modules for URIs that begin with `http://`, `https://`, and `file://`.</span></span> <span data-ttu-id="d7484-130">Sie können die Standardmodule nur durch Registrieren eines benutzerdefinierten Moduls in der Konfigurationsdatei überschreiben.</span><span class="sxs-lookup"><span data-stu-id="d7484-130">You can override the default modules only by registering a custom module in the configuration file.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="d7484-131">Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="d7484-131">Configuration Files</span></span>  
 <span data-ttu-id="d7484-132">Dieses Element kann in der Anwendungskonfigurationsdatei oder in der Computerkonfigurationsdatei ("Machine.config") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7484-132">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d7484-133">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d7484-133">Example</span></span>  
 <span data-ttu-id="d7484-134">Im folgende Beispiel wird das Standard-HTTP-Modul registriert.</span><span class="sxs-lookup"><span data-stu-id="d7484-134">The following example registers the default HTTP module.</span></span> <span data-ttu-id="d7484-135">Sie sollten die Werte für die Version und ' PublicKeyToken ' machen durch die richtigen Werte für das angegebene Modul ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d7484-135">You should replace the values for Version and PublicKeyToken with the correct values for the specified module.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <webRequestModules>  
      <add prefix="http"  
           type="System.Net.HttpRequestCreator, System, Version=2.0.3600.0,  
           Culture=neutral, PublicKeyToken=b77a5c561934e089"  
      />  
    </webRequestModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d7484-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7484-136">See also</span></span>
- <xref:System.Net.WebRequest>
- <xref:System.Net.IWebRequestCreate>
- [<span data-ttu-id="d7484-137">Network Settings Schema (Schema für Netzwerkeinstellungen)</span><span class="sxs-lookup"><span data-stu-id="d7484-137">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
