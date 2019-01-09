---
title: '&lt;behavior&gt; von &lt;endpointBehaviors&gt;'
ms.date: 03/30/2017
ms.assetid: b90ca3bc-3c22-4174-b903-e3a39898bd27
ms.openlocfilehash: 73ba25cd2f4fe588aa620bfe566a979c08a83e22
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2019
ms.locfileid: "54148200"
---
# <a name="ltbehaviorgt-of-ltendpointbehaviorsgt"></a>&lt;behavior&gt; von &lt;endpointBehaviors&gt;
Das `behavior`-Element enthält eine Auflistung der Einstellungen für das Verhalten eines Endpunkts. Jedes Verhalten wird durch seinen `name` indiziert. Endpunkte können über diesen Namen mit den Verhalten verknüpft sein. Ab [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)] müssen Bindungen und Verhalten keinen Namen aufweisen. Weitere Informationen zu Standardkonfiguration und zu namenlosen Bindungen und Verhaltensweisen finden Sie unter [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) und [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).  
  
 \<system.ServiceModel>  
\<behaviors>  
\<endpointBehaviors>  
\<Verhalten >  
  
## <a name="syntax"></a>Syntax  
  
```xml  
<system.ServiceModel>
  <behaviors>
    <endpointBehaviors>
      <behavior name="String" />
    </endpointBehaviors>
  </behaviors>
</system.ServiceModel>
```  
  
## <a name="attributes-and-elements"></a>Attribute und Elemente  
 In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.  
  
### <a name="attributes"></a>Attribute  
  
|Attribut|Beschreibung|  
|---------------|-----------------|  
|Name|Eine eindeutige Zeichenfolge, die den Konfigurationsnamen des Verhaltens enthält. Dieser Wert muss eine benutzerdefinierte und eindeutige Zeichenfolge sein, da sie als identifizierende Zeichenfolge für das Element fungiert. Ab [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)] müssen Bindungen und Verhalten keinen Namen aufweisen. Weitere Informationen zu Standardkonfiguration und zu namenlosen Bindungen und Verhaltensweisen finden Sie unter [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) und [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).|  
  
### <a name="child-elements"></a>Untergeordnete Elemente  
  
|Element|Beschreibung|  
|-------------|-----------------|  
|[\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|Gibt die zum Authentifizieren des Clients an einem Dienst verwendeten Anmeldeinformationen an.|  
|[\<CallbackDebug >](../../../../../docs/framework/configure-apps/file-schema/wcf/callbackdebug.md)|Gibt an, das dienstdebugging für ein Windows Communication Foundation (WCF)-Rückrufobjekt.|  
|[\<CallbackTimeouts >](../../../../../docs/framework/configure-apps/file-schema/wcf/callbacktimeouts.md)|Gibt das Timeout für den Clientrückruf an.|  
|[\<ClientVia >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientvia.md)|Gibt die Route an, die eine Nachricht nehmen sollte.|  
|[\<DataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer.md)|Speichert die Konfigurationsinformationen für DataContractSerializer.|  
|[\<DispatcherSynchronization >](../../../../../docs/framework/configure-apps/file-schema/wcf/dispatchersynchronization.md)|Gibt ein Endpunktverhalten an, das einem Dienst das asynchrone Senden von Antworten ermöglicht.|  
|[\<EnableWebScript >](../../../../../docs/framework/configure-apps/file-schema/wcf/enablewebscript.md)|Aktiviert das Endpunktverhalten, durch das der Dienst über ASP.NET AJAX-Webseiten genutzt werden kann. Das Verhalten sollte nur verwendet werden, in Verbindung mit der \<WebHttpBinding >-standardbindung oder dem \<WebMessageEncoding > Binding-Element.|  
|[\<EndpointDiscovery >](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointdiscovery.md)|Gibt die verschiedenen Ermittlungseinstellungen für einen Endpunkt an, z. B. seine Ermittelbarkeit, seine Bereiche und benutzerdefinierte Erweiterungen seiner Metadaten.|  
|[\<SoapProcessing >](../../../../../docs/framework/configure-apps/file-schema/wcf/soapprocessing.md)|Definiert das Clientendpunktverhalten, das verwendet wird, um Nachrichten zwischen unterschiedlichen Bindungstypen und Nachrichtenversionen zu marshallen.|  
|[\<SynchronousReceive >](../../../../../docs/framework/configure-apps/file-schema/wcf/synchronousreceive-element.md)|Gibt das Laufzeitverhalten für das Empfangen von Nachrichten in einem Dienst oder einer Clientanwendung an. Es enthält keine Attribute oder untergeordnete Elemente.|  
|[\<TransactedBatching >](../../../../../docs/framework/configure-apps/file-schema/wcf/transactedbatching.md)|Gibt an, ob Transaktionsbatching für Empfangsvorgänge unterstützt wird.|  
|[\<WebHttp >](../../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md)|Gibt WebHttpBehavior anhand der Konfiguration in einem Endpunkt an. Dieses Verhalten, bei der Verwendung in Verbindung mit der \<WebHttpBinding >-standardbindung aktiviert das Webprogrammiermodell für einen WCF-Dienst.|  
  
### <a name="parent-elements"></a>Übergeordnete Elemente  
  
|Element|Beschreibung|  
|-------------|-----------------|  
|[\<EndpointBehaviors >](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointbehaviors.md)|Eine Auflistung von Endpunktverhaltenselementen.|
