---
title: '&lt;metadata&gt;'
ms.date: 03/30/2017
ms.assetid: d09653eb-e355-4c73-b87b-28f93d56480d
ms.openlocfilehash: 017a58c7e48a1c4c5b4abdcb7cc603e95f6516a1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54723965"
---
# <a name="ltmetadatagt"></a><span data-ttu-id="208d7-102">&lt;metadata&gt;</span><span class="sxs-lookup"><span data-stu-id="208d7-102">&lt;metadata&gt;</span></span>
<span data-ttu-id="208d7-103">Gibt an, wie Dienstmetadaten verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="208d7-103">Specifies how service metadata can be processed.</span></span>  
  
 <span data-ttu-id="208d7-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="208d7-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="208d7-105">\<client></span><span class="sxs-lookup"><span data-stu-id="208d7-105">\<client></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="208d7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="208d7-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <client>
    <metadata>
      <policyImporters>
        <policyImporter type="string" />
      </policyImporters>
      <wsdlImporters>
        <wsdlImporter type="string" />
      </wsdlImporters>
    </metadata>
  </client>
</system.serviceModel>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="208d7-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="208d7-107">Attributes and Elements</span></span>  
 <span data-ttu-id="208d7-108">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="208d7-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="208d7-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="208d7-109">Attributes</span></span>  
 <span data-ttu-id="208d7-110">Keine</span><span class="sxs-lookup"><span data-stu-id="208d7-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="208d7-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="208d7-111">Child Elements</span></span>  
  
|<span data-ttu-id="208d7-112">Element</span><span class="sxs-lookup"><span data-stu-id="208d7-112">Element</span></span>|<span data-ttu-id="208d7-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="208d7-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="208d7-114">\<policyImporters></span><span class="sxs-lookup"><span data-stu-id="208d7-114">\<policyImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/policyimporters.md)|<span data-ttu-id="208d7-115">Gibt alle Richtlinienimporter an, die den Import von benutzerdefinierten Richtlinienerklärungen über Bindungen steuern.</span><span class="sxs-lookup"><span data-stu-id="208d7-115">Specifies all the policy importers that control the import of custom policy assertions about bindings.</span></span> <span data-ttu-id="208d7-116">Mit einem Richtlinienimporter werden benutzerdefinierte Richtlinienerklärungen über Bindungsfunktionen gesucht, und es wird ein benutzerdefiniertes Bindungselement angefügt, mit dem die für die Erklärung erforderlichen Funktionen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="208d7-116">A policy importer is used to search custom policy assertions about binding features, as well as attach a custom binding element that implements the features the assertion requires.</span></span>|  
|[<span data-ttu-id="208d7-117">\<wsdlImporters></span><span class="sxs-lookup"><span data-stu-id="208d7-117">\<wsdlImporters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/wsdlimporters.md)|<span data-ttu-id="208d7-118">Gibt alle WSDL-Importer an, mit denen Web Services Description Language (WSDL) 1.1-Metadaten mit WS-Richtlinienanhängen importiert werden.</span><span class="sxs-lookup"><span data-stu-id="208d7-118">Specifies all the WSDL importers that import Web Services Description Language (WSDL) 1.1 metadata with WS-Policy attachments.</span></span> <span data-ttu-id="208d7-119">Ein WSDL-Importer wird zum Importieren von Metadaten und zum Konvertieren der Informationen in verschiedene Klassen verwendet, die Vertrags- und Endpunktinformationen darstellen.</span><span class="sxs-lookup"><span data-stu-id="208d7-119">A WSDL importer is used to import metadata as well as convert that information into various classes that represent contract and endpoint information.</span></span> <span data-ttu-id="208d7-120">Vertrags- und Endpunktinformationen sowie Eigenschaften, die Importfehler offenlegen und Typinformationen akzeptieren, die für den Import- und Konvertierungsvorgang relevant sind, können selektiv importiert werden.</span><span class="sxs-lookup"><span data-stu-id="208d7-120">It can selectively import contract and endpoint information and properties that expose any import errors and accept type information relevant to the import and conversion process.</span></span> <span data-ttu-id="208d7-121">Außerdem wird der Import von Bindungsinformationen und -eigenschaften unterstützt, die Zugriff auf Richtliniendokumente, WSDL-Dokumente, WSDL-Erweiterungen und XML-Schemadokumente bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="208d7-121">It also supports importing binding information and properties that provide access to any policy documents, WSDL documents, WSDL extensions, and XML schema documents.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="208d7-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="208d7-122">Parent Elements</span></span>  
  
|<span data-ttu-id="208d7-123">Element</span><span class="sxs-lookup"><span data-stu-id="208d7-123">Element</span></span>|<span data-ttu-id="208d7-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="208d7-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="208d7-125">\<client></span><span class="sxs-lookup"><span data-stu-id="208d7-125">\<client></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/client.md)|<span data-ttu-id="208d7-126">Der Clientabschnitt definiert eine Liste der Endpunkte, mit denen ein Client eine Verbindung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="208d7-126">The client section defines a list of endpoints that a client can connect to.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="208d7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="208d7-127">See also</span></span>
- <xref:System.ServiceModel.Configuration.MetadataElement>
- <xref:System.ServiceModel.Configuration.PolicyImporterElementCollection>
- <xref:System.ServiceModel.Configuration.WsdlImporterElementCollection>
- <xref:System.ServiceModel.Description.MetadataImporter>
- <xref:System.ServiceModel.Description.WsdlImporter>
- [<span data-ttu-id="208d7-128">WCF-Clientkonfiguration</span><span class="sxs-lookup"><span data-stu-id="208d7-128">WCF Client Configuration</span></span>](../../../../../docs/framework/wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="208d7-129">Clients</span><span class="sxs-lookup"><span data-stu-id="208d7-129">Clients</span></span>](../../../../../docs/framework/wcf/feature-details/clients.md)
