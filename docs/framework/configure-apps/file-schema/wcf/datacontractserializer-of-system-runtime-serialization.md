---
title: '&lt;dataContractSerializer&gt; von &lt;system.runtime.serialization&gt;'
ms.date: 03/30/2017
ms.assetid: d9b3d625-be3f-4768-8e0d-1b7e6929f6a8
ms.openlocfilehash: f31dd8479f3bd6b36915b3ff00ff53babe3c0248
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2019
ms.locfileid: "54150174"
---
# <a name="ltdatacontractserializergt-of-ltsystemruntimeserializationgt"></a><span data-ttu-id="6e6ce-102">&lt;dataContractSerializer&gt; von &lt;system.runtime.serialization&gt;</span><span class="sxs-lookup"><span data-stu-id="6e6ce-102">&lt;dataContractSerializer&gt; of &lt;system.runtime.serialization&gt;</span></span>
<span data-ttu-id="6e6ce-103">Enthält Konfigurationsdaten für den <xref:System.Runtime.Serialization.DataContractSerializer>.</span><span class="sxs-lookup"><span data-stu-id="6e6ce-103">Contains configuration data for the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
 <span data-ttu-id="6e6ce-104">\<System.Runtime.Serialization ></span><span class="sxs-lookup"><span data-stu-id="6e6ce-104">\<system.runtime.serialization></span></span>  
<span data-ttu-id="6e6ce-105">\<DataContractSerializer ></span><span class="sxs-lookup"><span data-stu-id="6e6ce-105">\<dataContractSerializer></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e6ce-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e6ce-106">Syntax</span></span>  
  
```xml  
<configuration>
  <system.runtime.serialization>
    <dataContractSerializer ignoreExtensionDataObject="Boolean"
                            maxItemsInObjectGraph="Integer">
      <declaredTypes>
        <add type="String">
          <knownType type="String">
            <parameter index="Integer"
                       type="String" />
          </knownType>
        </add>
      </declaredTypes>
    <dataContractSerializer>
  </system.runtime.serialization>
</configuration>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6e6ce-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6e6ce-107">Attributes and Elements</span></span>  
 <span data-ttu-id="6e6ce-108">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6e6ce-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6e6ce-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="6e6ce-109">Attributes</span></span>  
  
|<span data-ttu-id="6e6ce-110">Element</span><span class="sxs-lookup"><span data-stu-id="6e6ce-110">Element</span></span>|<span data-ttu-id="6e6ce-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e6ce-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6e6ce-112">IgnoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="6e6ce-112">ignoreExtensionDataObject</span></span>|<span data-ttu-id="6e6ce-113">Ein boolescher Wert, der angibt, ob vom Endpunkt bereitgestellte Daten ignoriert werden sollen, wenn dieser serialisiert oder deserialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6e6ce-113">A Boolean value that specifies whether to ignore data supplied by the endpoint when it is being serialized or deserialized.</span></span> <span data-ttu-id="6e6ce-114">Dieses Attribut kann nur im `<dataContractSerializer>` unter dem `<behavior>`-Element festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6e6ce-114">This attribute is settable only on the `<dataContractSerializer>` under the `<behavior>` element.</span></span>|  
|<span data-ttu-id="6e6ce-115">maxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="6e6ce-115">maxItemsInObjectGraph</span></span>|<span data-ttu-id="6e6ce-116">Eine ganze Zahl, die die maximale Anzahl der zu serialisierenden oder zu deserialisierenden Elemente angibt.</span><span class="sxs-lookup"><span data-stu-id="6e6ce-116">An integer that specifies the maximum number of items to serialize or deserialize.</span></span> <span data-ttu-id="6e6ce-117">Dieses Attribut hat den Wert 65536.</span><span class="sxs-lookup"><span data-stu-id="6e6ce-117">This attribute is 65536.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6e6ce-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e6ce-118">Child Elements</span></span>  
  
|<span data-ttu-id="6e6ce-119">Element</span><span class="sxs-lookup"><span data-stu-id="6e6ce-119">Element</span></span>|<span data-ttu-id="6e6ce-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e6ce-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6e6ce-121">\<DeclaredTypes ></span><span class="sxs-lookup"><span data-stu-id="6e6ce-121">\<declaredTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/declaredtypes.md)|<span data-ttu-id="6e6ce-122">Enthält die bekannten Typen, die der <xref:System.Runtime.Serialization.DataContractSerializer> bei der Deserialisierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e6ce-122">Contains the known types that the <xref:System.Runtime.Serialization.DataContractSerializer> uses when deserializing.</span></span><br /><br /> <span data-ttu-id="6e6ce-123">Weitere Informationen über Datenverträge und bekannte Typen finden Sie unter [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span><span class="sxs-lookup"><span data-stu-id="6e6ce-123">For more information about data contracts and known types, see [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="6e6ce-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6e6ce-124">Parent Elements</span></span>  
  
|<span data-ttu-id="6e6ce-125">Element</span><span class="sxs-lookup"><span data-stu-id="6e6ce-125">Element</span></span>|<span data-ttu-id="6e6ce-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e6ce-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="6e6ce-127">\<system.runtime.serialization></span><span class="sxs-lookup"><span data-stu-id="6e6ce-127">\<system.runtime.serialization></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-runtime-serialization.md)|<span data-ttu-id="6e6ce-128">Stellt das Stammelement für den <xref:System.Runtime.Serialization>-Namespaceabschnitt dar und enthält Elemente zum Festlegen von <xref:System.Runtime.Serialization.DataContractSerializer>-Optionen.</span><span class="sxs-lookup"><span data-stu-id="6e6ce-128">Represents the root element for the <xref:System.Runtime.Serialization> namespace section and contains elements for setting options of the <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6e6ce-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e6ce-129">Remarks</span></span>  
 <span data-ttu-id="6e6ce-130">Weitere Informationen zu bekannten Typen finden Sie unter <xref:System.Runtime.Serialization.DataContractSerializer> und [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span><span class="sxs-lookup"><span data-stu-id="6e6ce-130">For more information about known types, see <xref:System.Runtime.Serialization.DataContractSerializer> and [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e6ce-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e6ce-131">See Also</span></span>  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
 <xref:System.ServiceModel.Description.DataContractSerializerOperationBehavior>  
 [<span data-ttu-id="6e6ce-132">Bekannte Typen in Datenverträgen</span><span class="sxs-lookup"><span data-stu-id="6e6ce-132">Data Contract Known Types</span></span>](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
