---
title: <dateTimeSerialization>-Element
ms.date: 03/30/2017
helpviewer_keywords:
- dateTimeSerialization element
- XML serialization, configuration
- <dateTimeSerialization> element
ms.assetid: 90fda55c-7730-41e9-bc4b-6423a4b920af
ms.openlocfilehash: af0d8eeb36e023b4d38f9ad5831de3d392a487fd
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2019
ms.locfileid: "55288261"
---
# <a name="datetimeserialization-element"></a><span data-ttu-id="bfcb5-102">\<DateTimeSerialization >-Element</span><span class="sxs-lookup"><span data-stu-id="bfcb5-102">\<dateTimeSerialization> Element</span></span>
<span data-ttu-id="bfcb5-103">Bestimmt den Serialisierungsmodus von <xref:System.DateTime>-Objekten.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-103">Determines the serialization mode of <xref:System.DateTime> objects.</span></span>  
  
 <span data-ttu-id="bfcb5-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="bfcb5-104">\<configuration></span></span>  
<span data-ttu-id="bfcb5-105">\<dateTimeSerialization></span><span class="sxs-lookup"><span data-stu-id="bfcb5-105">\<dateTimeSerialization></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bfcb5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfcb5-106">Syntax</span></span>  
  
```xml  
<dateTimeSerialization  
    mode = "Roundtrip" | "Local"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bfcb5-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bfcb5-107">Attributes and Elements</span></span>  
 <span data-ttu-id="bfcb5-108">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bfcb5-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="bfcb5-109">Attributes</span></span>  
  
|<span data-ttu-id="bfcb5-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="bfcb5-110">Attributes</span></span>|<span data-ttu-id="bfcb5-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfcb5-111">Description</span></span>|  
|----------------|-----------------|  
|`mode`|<span data-ttu-id="bfcb5-112">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-112">Optional.</span></span> <span data-ttu-id="bfcb5-113">Gibt den Serialisierungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-113">Specifies the serialization mode.</span></span> <span data-ttu-id="bfcb5-114">Legen Sie hierfür einen der <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode>-Werte fest.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-114">Set to one of the <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode> values.</span></span> <span data-ttu-id="bfcb5-115">Der Standardwert ist **RoundTrip**.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-115">The default is **RoundTrip**.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bfcb5-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfcb5-116">Child Elements</span></span>  
 <span data-ttu-id="bfcb5-117">Keine</span><span class="sxs-lookup"><span data-stu-id="bfcb5-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bfcb5-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfcb5-118">Parent Elements</span></span>  
  
|<span data-ttu-id="bfcb5-119">Element</span><span class="sxs-lookup"><span data-stu-id="bfcb5-119">Element</span></span>|<span data-ttu-id="bfcb5-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfcb5-120">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bfcb5-121">system.xml.serialization</span><span class="sxs-lookup"><span data-stu-id="bfcb5-121">system.xml.serialization</span></span>|<span data-ttu-id="bfcb5-122">Das Element der obersten Ebene zur Steuerung der XML-Serialisierung.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-122">The top-level element for controlling XML serialization.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bfcb5-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfcb5-123">Remarks</span></span>  
 <span data-ttu-id="bfcb5-124">Wenn in den Versionen 1.0, 1.1, 2.0 und höheren Versionen von .NET Framework diese Eigenschaft auf **Local** festgelegt ist, werden <xref:System.DateTime>-Objekte immer entsprechend der Ortszeit formatiert.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-124">In versions 1.0, 1.1, 2.0 and later versions of the .NET Framework, when this property is set to **Local**, <xref:System.DateTime> objects are always formatted as the local time.</span></span> <span data-ttu-id="bfcb5-125">Das heißt, Ortszeitzoneninformationen sind in den serialisierten Daten immer enthalten.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-125">That is, local time zone information is always included with the serialized data.</span></span> <span data-ttu-id="bfcb5-126">Legen Sie diese Eigenschaft auf **Local** fest, um die Kompatibilität mit früheren Versionen von .NET Framework sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-126">Set this property to **Local** to ensure compatibility with older versions of the .NET Framework.</span></span>  
  
 <span data-ttu-id="bfcb5-127">Wenn diese Eigenschaft in .NET Framework Version 2.0 und höher auf **Roundtrip** festgelegt ist, werden <xref:System.DateTime>-Objekte überprüft, um zu ermitteln, ob sie entsprechend einer lokalen Zeitzone, der UTC-Zone oder einer unbestimmten Zeitzone formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-127">In version 2.0 and later versions of the .NET Framework that have this property set to **Roundtrip**, <xref:System.DateTime> objects are examined to determine whether they are in the local, UTC, or an unspecified time zone.</span></span> <span data-ttu-id="bfcb5-128">Die <xref:System.DateTime>-Objekte werden dann so serialisiert, dass diese Informationen beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-128">The <xref:System.DateTime> objects are then serialized in such a way that this information is preserved.</span></span> <span data-ttu-id="bfcb5-129">Dies ist das Standardverhalten, das für alle neuen Anwendungen empfohlen wird, die nicht mit älteren Versionen des Framework kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="bfcb5-129">This is the default behavior and is the recommended behavior for all new applications that do not communicate with older versions of the framework.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bfcb5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfcb5-130">See also</span></span>

- <xref:System.DateTime>
- <xref:System.Xml.Serialization.XmlSchemaImporter>
- <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode>
- [<span data-ttu-id="bfcb5-131">Konfigurationsdateischema</span><span class="sxs-lookup"><span data-stu-id="bfcb5-131">Configuration File Schema</span></span>](../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="bfcb5-132">\<schemaImporterExtensions>-Element</span><span class="sxs-lookup"><span data-stu-id="bfcb5-132">\<schemaImporterExtensions> Element</span></span>](../../../docs/standard/serialization/schemaimporterextensions-element.md)
- [<span data-ttu-id="bfcb5-133">\<Hinzufügen >-Element für \<SchemaImporterExtensions ></span><span class="sxs-lookup"><span data-stu-id="bfcb5-133">\<add> Element for \<schemaImporterExtensions></span></span>](../../../docs/standard/serialization/add-element-for-schemaimporterextensions.md)
- [<span data-ttu-id="bfcb5-134">\<system.xml.serialization>-Element</span><span class="sxs-lookup"><span data-stu-id="bfcb5-134">\<system.xml.serialization> Element</span></span>](../../../docs/standard/serialization/system-xml-serialization-element.md)
