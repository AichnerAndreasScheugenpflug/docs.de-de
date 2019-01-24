---
title: sein. (Memberzugriff) (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 4733e3b2-3efa-4b96-b591-ac31350e96ad
ms.openlocfilehash: e2874e5bff8d8c34f700a81bf52c6729df49aca5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54626668"
---
# <a name="-member-access-entity-sql"></a><span data-ttu-id="75683-103">sein.</span><span class="sxs-lookup"><span data-stu-id="75683-103">.</span></span> <span data-ttu-id="75683-104">(Memberzugriff) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="75683-104">(Member Access) (Entity SQL)</span></span>
<span data-ttu-id="75683-105">Der Punktoperator (.) wird die [!INCLUDE[esql](../../../../../../includes/esql-md.md)] Memberzugriffsoperator.</span><span class="sxs-lookup"><span data-stu-id="75683-105">The dot operator (.) is the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] member access operator.</span></span> <span data-ttu-id="75683-106">Mit dem Operator für den Memberzugriff kann auf den Wert einer Eigenschaft oder eines Felds der Instanz eines strukturellen konzeptionellen Modelltyps zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="75683-106">You use the member access operator to yield the value of a property or field of an instance of structural conceptual model type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="75683-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="75683-107">Syntax</span></span>  
  
```  
expression.identifier  
```  
  
## <a name="arguments"></a><span data-ttu-id="75683-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="75683-108">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="75683-109">Eine Instanz eines strukturellen konzeptionellen Modelltyps.</span><span class="sxs-lookup"><span data-stu-id="75683-109">An instance of a structural conceptual model type.</span></span>  
  
 `identifier`  
 <span data-ttu-id="75683-110">Eine Eigenschaft oder ein Feld einer Objektinstanz.</span><span class="sxs-lookup"><span data-stu-id="75683-110">A property or field that belongs to an object instance.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="75683-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="75683-111">Remarks</span></span>  
 <span data-ttu-id="75683-112">Mit dem Punktoperator (.) können Sie Felder eines Datensatzes extrahieren, ähnlich wie beim Extrahieren der Eigenschaften eines komplexen Typs oder Entitätstyps.</span><span class="sxs-lookup"><span data-stu-id="75683-112">The dot (.) operator may be used to extract fields from a record, similar to extracting properties of a complex or entity type.</span></span> <span data-ttu-id="75683-113">Wenn z. B. "n" vom Typ "Name" ein Member des Typs "Person" ist und "p" eine Instanz des Typs "Person" ist, ist "p.n" ein zulässiger Memberzugriffsausdruck, der einen Wert des Typs "Name" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="75683-113">For example, if n of type Name is a member of type Person, and p is an instance of type Person, then p.n is a legal member access expression that yields a value of type Name.</span></span>  
  
 `select p.Name.FirstName from LOB.Person as p`  
  
## <a name="see-also"></a><span data-ttu-id="75683-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75683-114">See also</span></span>
- [<span data-ttu-id="75683-115">Entity SQL-Referenz</span><span class="sxs-lookup"><span data-stu-id="75683-115">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
