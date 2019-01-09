---
title: '&lt;endpointExtensions&gt;'
ms.date: 03/30/2017
ms.assetid: 33396e0a-1fae-4616-b822-923584eebfd1
ms.openlocfilehash: 3883a23c679abc83d7cfe9011b7cdb7e4154adfe
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2019
ms.locfileid: "54146445"
---
# <a name="ltendpointextensionsgt"></a><span data-ttu-id="c5945-102">&lt;endpointExtensions&gt;</span><span class="sxs-lookup"><span data-stu-id="c5945-102">&lt;endpointExtensions&gt;</span></span>
<span data-ttu-id="c5945-103">Dieser Abschnitt registriert einen neuen Standardendpunkt im Erweiterungsabschnitt einer Konfigurationsdatei auf Computer- oder Anwendungsebene.</span><span class="sxs-lookup"><span data-stu-id="c5945-103">This section registers a new standard endpoint in the extensions section in a machine or application configuration file.</span></span> <span data-ttu-id="c5945-104">Sie können dieser Auflistung einen Standardendpunkt hinzufügen, indem Sie das `add`-Schlüsselwort verwenden und das `type`-Attribut des Elements auf den Endpunkttyp sowie das `name`-Attribut auf den Namen des Standardendpunkts festlegen.</span><span class="sxs-lookup"><span data-stu-id="c5945-104">You can add a standard endpoint to this collection by using the `add` keyword, and setting the `type` attribute of the element to the endpoint type, as well as the `name` attribute to the name of the standard endpoint.</span></span>  
  
 <span data-ttu-id="c5945-105">Im folgenden Beispiel werden das `add`-Element sowie das `name`-Attribut zum Hinzufügen eines Standardendpunkts zum `<endpointExtensions>`-Abschnitt der Konfigurationsdatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5945-105">The following example uses the `add` element, as well as the `name` attribute to add a standard endpoint to the `<endpointExtensions>` section of the configuration file.</span></span>  
  
```xml  
<system.serviceModel>
  <extensions>
    <endpointExtensions>
      <add name="udpDiscoveryEndpoint"
           type="System.Discovery.UdpEndpointCollectionElement, System.Discovery.dll, Version=1.0.0.0, Culture=neutral, PublicKeyToken=ffffffffffffffff"/>
    </endpointExtensions>
  </extensions>
</system.serviceModel>
```  
  
 <span data-ttu-id="c5945-106">Nachdem der Standardendpunkt registriert wurde, können Sie ihn verwenden wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c5945-106">After the standard endpoint has been registered, you can use it as shown in the following example.</span></span> <span data-ttu-id="c5945-107">In der [ \<Endpunkt >](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-element.md) -Element, das `kind` Attribut gibt an, den standardendpunkttyp an, die in registriert wurde die `<endpointExtensions>` Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="c5945-107">In the [\<endpoint>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-element.md) element, the `kind` attribute specifies the standard endpoint type that has been registered in the `<endpointExtensions>` section.</span></span> <span data-ttu-id="c5945-108">Die `endpointConfiguration` Attribut werden identisch mit der `name` Attribut des Konfigurationselements für den Standardendpunkt im der `<standardEndpoints>` Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="c5945-108">The `endpointConfiguration` attribute will be identical to the `name` attribute of the configuration element of the standard endpoint in the `<standardEndpoints>` section.</span></span>  
  
```xml  
<system.serviceModel>
  <services>
    <service name="Service1">
      <endpoint kind="udpDiscoveryEndpoint"
                endpointConfiguration="udpConfig" />
    </service>
  </services>
  <standardEndpoints>
    <udpDiscoveryEndpoint>
      <standardEndpoint name="udpConfig"
                        multicastAddress="soap.udp://239.255.255.250:3703"
                        ... />
    </udpDiscoveryEndpoint>
  </standardEndpoints>
</system.serviceModel>
```  
  
