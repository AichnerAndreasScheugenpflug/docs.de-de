---
title: '&lt;customTrackingQueries&gt; von WCF'
ms.date: 03/30/2017
ms.assetid: 14cfe47e-9935-4120-84f1-8f38de8ca4c1
ms.openlocfilehash: f75c6bf50d30da5a136137c858a5cd96ce0783ff
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150083"
---
# <a name="ltcustomtrackingqueriesgt-of-wcf"></a>&lt;customTrackingQueries&gt; von WCF

Stellt eine Auflistung von Abfragen dar, die verwendet werden, um Ereignisse nachzuverfolgen, die Sie in den Codeaktivitäten definieren. Die Abfrage ist notwendig, damit ein Nachverfolgungsteilnehmer benutzerdefinierte Nachverfolgungsdatensätze abonnieren kann.  
  
 Weitere Informationen zu überwachungsprofilabfragen finden Sie unter [Nachverfolgungsprofile](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).
  
\<system.serviceModel>  
\<Nachverfolgen von >  
\<Profile >  
\<trackingProfile>  
\<Workflow >  
\<CustomTrackingQueries >  
  
## <a name="syntax"></a>Syntax  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <customTrackingQueries>
          <customTrackingQuery activityName="String"
                               name="String"/>
        </customTrackingQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.  
  
### <a name="attributes"></a>Attribute

Keine
  
### <a name="child-elements"></a>Untergeordnete Elemente
  
|Element|Beschreibung|  
|-------------|-----------------|  
|[\<CustomTrackingQuery >](customtrackingquery-of-wcf.md)|Eine Abfrage, die verwendet wird, um Ereignisse nachzuverfolgen, die Sie in den Codeaktivitäten definieren.|  
  
### <a name="parent-elements"></a>Übergeordnete Elemente  
  
|Element|Beschreibung|  
|-------------|-----------------|  
|[\<workflow>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|Ein Konfigurationselement, das alle Abfragen für einen bestimmten Workflow enthält, der durch die `activityDefinitionId`-Eigenschaft identifiziert wird.|  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.ServiceModel.Activities.Tracking.Configuration.CustomTrackingQueryElementCollection?displayProperty=nameWithType>       
- <xref:System.Activities.Tracking.CustomTrackingQuery?displayProperty=nameWithType>       
- [Nachverfolgung und Ablaufverfolgung für Workflows](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
- [Überwachungsprofile](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
