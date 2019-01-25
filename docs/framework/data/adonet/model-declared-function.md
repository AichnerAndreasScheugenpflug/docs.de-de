---
title: Im Modell deklarierte Funktion
ms.date: 03/30/2017
ms.assetid: aba87f13-5685-4f6b-ad14-918e8a7d5c2a
ms.openlocfilehash: 5db7d49fd4b839cef47db8086b4ef39ce4dc6aea
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54725141"
---
# <a name="model-declared-function"></a><span data-ttu-id="a3c52-102">Im Modell deklarierte Funktion</span><span class="sxs-lookup"><span data-stu-id="a3c52-102">model-declared function</span></span>
<span data-ttu-id="a3c52-103">Ein *im Modell deklarierte Funktion* ist eine Funktion, die in einem konzeptionellen Modell deklariert ist, aber nicht in diesem konzeptionellen Modell definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a3c52-103">A *model-declared function* is a function that is declared in a conceptual model, but is not defined in that conceptual model.</span></span> <span data-ttu-id="a3c52-104">Die Funktion kann in der Hosting- oder Speicherumgebung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a3c52-104">The function might be defined in the hosting or storage environment.</span></span> <span data-ttu-id="a3c52-105">Eine im Modell deklarierte Funktion kann z. B. einer in einer Datenbank definierten Funktion zugeordnet werden, sodass die serverseitige Funktionalität im konzeptionellen Modell verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="a3c52-105">For example, a model-declared function might be mapped to a function that is defined in a database, thus exposing server-side functionality in the conceptual model.</span></span>  
  
 <span data-ttu-id="a3c52-106">Die Deklaration einer im Modell deklarierten Funktion enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="a3c52-106">The declaration of a model-declared function contains the following information:</span></span>  
  
-   <span data-ttu-id="a3c52-107">Der Name der Funktion.</span><span class="sxs-lookup"><span data-stu-id="a3c52-107">The name of the function.</span></span> <span data-ttu-id="a3c52-108">(erforderlich)</span><span class="sxs-lookup"><span data-stu-id="a3c52-108">(Required)</span></span>  
  
-   <span data-ttu-id="a3c52-109">Den Typ des Rückgabewerts.</span><span class="sxs-lookup"><span data-stu-id="a3c52-109">The type of the return value.</span></span> <span data-ttu-id="a3c52-110">(Optional)</span><span class="sxs-lookup"><span data-stu-id="a3c52-110">(Optional)</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="a3c52-111">Wenn kein Rückgabewert angegeben wird, ist der Rückgabetyp leer.</span><span class="sxs-lookup"><span data-stu-id="a3c52-111">If no return value is specified, the return type is void.</span></span>  
  
-   <span data-ttu-id="a3c52-112">Parameterinformationen, einschließlich Parametername und -typ.</span><span class="sxs-lookup"><span data-stu-id="a3c52-112">Parameter information, including parameter name and type.</span></span> <span data-ttu-id="a3c52-113">(Optional)</span><span class="sxs-lookup"><span data-stu-id="a3c52-113">(Optional)</span></span>  
  
## <a name="example"></a><span data-ttu-id="a3c52-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3c52-114">Example</span></span>  
 <span data-ttu-id="a3c52-115">Die [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) verwendet eine domänenspezifische Sprache (DSL) Bezeichnung konzeptionelle Schemadefinitionssprache ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)), konzeptionelle Modelle zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a3c52-115">The [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md) uses a domain-specific language (DSL) called conceptual schema definition language ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) to define conceptual models.</span></span> <span data-ttu-id="a3c52-116">In CSDL ist eine Implementierung einer im Modell deklarierte Funktion ist eine [Funktionsimport](https://msdn.microsoft.com/library/125704ae-56c7-4233-80b7-389a10f3a65d).</span><span class="sxs-lookup"><span data-stu-id="a3c52-116">In CSDL, one implementation of a model-declared function is a [function import](https://msdn.microsoft.com/library/125704ae-56c7-4233-80b7-389a10f3a65d).</span></span> <span data-ttu-id="a3c52-117">Die folgende CSDL definiert einen Entitätscontainer mit einer Funktionsimportdefinition.</span><span class="sxs-lookup"><span data-stu-id="a3c52-117">The following CSDL defines an entity container with a function import definition.</span></span> <span data-ttu-id="a3c52-118">Beachten Sie, dass der Rückgabetyp für die Funktion leer ist, da kein Rückgabetyp angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a3c52-118">Note that the return type for the function is void since no return type is specified.</span></span>  
  
 [!code-xml[EDM_Example_Model#FunctionImport](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books4.edmx#functionimport)]  
  
## <a name="see-also"></a><span data-ttu-id="a3c52-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3c52-119">See also</span></span>
- [<span data-ttu-id="a3c52-120">Schlüsselkonzepte im Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="a3c52-120">Entity Data Model Key Concepts</span></span>](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)
- [<span data-ttu-id="a3c52-121">Entity Data Model</span><span class="sxs-lookup"><span data-stu-id="a3c52-121">Entity Data Model</span></span>](../../../../docs/framework/data/adonet/entity-data-model.md)
