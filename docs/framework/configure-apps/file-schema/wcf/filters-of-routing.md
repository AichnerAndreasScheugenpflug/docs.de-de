---
title: '&lt;filters&gt; von &lt;routing&gt;'
ms.date: 03/30/2017
ms.assetid: 7993cf90-9afd-4c3c-9608-184d5da1105c
ms.openlocfilehash: 468c10bc06b60f80ce93cf413c02582fe3861f70
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54704432"
---
# <a name="ltfiltersgt-of-ltroutinggt"></a><span data-ttu-id="8501e-102">&lt;filters&gt; von &lt;routing&gt;</span><span class="sxs-lookup"><span data-stu-id="8501e-102">&lt;filters&gt; of &lt;routing&gt;</span></span>

<span data-ttu-id="8501e-103">Stellt einen Konfigurationsabschnitt zum Definieren eines Satzes von routingfiltern, die den Typ der Windows Communication Foundation (WCF) bestimmen <xref:System.ServiceModel.Dispatcher.MessageFilter> beim Auswerten eingehender Nachrichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8501e-103">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF) <xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages.</span></span>

<span data-ttu-id="8501e-104">[**\<system.serviceModel>**](system-servicemodel.md) </span><span class="sxs-lookup"><span data-stu-id="8501e-104">[**\<system.serviceModel>**](system-servicemodel.md) </span></span>  
<span data-ttu-id="8501e-105">&nbsp;&nbsp;[**\<routing>**](routing.md) </span><span class="sxs-lookup"><span data-stu-id="8501e-105">&nbsp;&nbsp;[**\<routing>**](routing.md) </span></span>  
<span data-ttu-id="8501e-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<filters>**</span><span class="sxs-lookup"><span data-stu-id="8501e-106">&nbsp;&nbsp;&nbsp;&nbsp;**\<filters>**</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8501e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8501e-107">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <routing>
    <filters>
      <filter customType="String"
              filterData="String"
              filterType="Action/Address/AddressPrefix/And/Custom/Endpoint/MatchAll/XPath"
              name="String" />
    </filters>
  </routing>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8501e-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8501e-108">Attributes and elements</span></span>

<span data-ttu-id="8501e-109">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8501e-109">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="8501e-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="8501e-110">Attributes</span></span>

<span data-ttu-id="8501e-111">Keine</span><span class="sxs-lookup"><span data-stu-id="8501e-111">None</span></span>

### <a name="child-elements"></a><span data-ttu-id="8501e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8501e-112">Child elements</span></span>

|     | <span data-ttu-id="8501e-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8501e-113">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="8501e-114">**\<filter>**</span><span class="sxs-lookup"><span data-stu-id="8501e-114">**\<filter>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filter.md) | <span data-ttu-id="8501e-115">Enthält einen Routingfilter, der den Typ der Windows Communication Foundation (WCF) bestimmt<xref:System.ServiceModel.Dispatcher.MessageFilter> beim Auswerten eingehender Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="8501e-115">Contains a routing filter that determines the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> will be used when evaluating incoming messages.</span></span> |

### <a name="parent-elements"></a><span data-ttu-id="8501e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8501e-116">Parent elements</span></span>

|     | <span data-ttu-id="8501e-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8501e-117">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="8501e-118">**\<routing>**</span><span class="sxs-lookup"><span data-stu-id="8501e-118">**\<routing>**</span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md) | <span data-ttu-id="8501e-119">Stellt einen Konfigurationsabschnitt zum Definieren eines Satzes von routingfiltern, die den Typ der Windows Communication Foundation (WCF) bestimmen<xref:System.ServiceModel.Dispatcher.MessageFilter> verwendet werden, bei der Auswertung eingehender Nachrichten sowie das routing, Tabellen, die die zielendpunkten, definieren Senden von Nachrichten bei filterübereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="8501e-119">Represents a configuration section for defining a set of routing filters, which determine the type of Windows Communication Foundation (WCF)<xref:System.ServiceModel.Dispatcher.MessageFilter> to be used when evaluating incoming messages, as well as routing tables that define the target endpoints to send messages to when a filter matches.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8501e-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8501e-120">See also</span></span>

- <xref:System.ServiceModel.Routing.Configuration.FilterElement?displayProperty=nameWithType>
