---
title: SKIP (Entity SQL)
ms.date: 03/30/2017
ms.assetid: e2139412-8ea4-451b-8f10-91af18dfa3ec
ms.openlocfilehash: 467329f74304b64c7fc7ada2920751aba744f76e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54637637"
---
# <a name="skip-entity-sql"></a><span data-ttu-id="37dad-102">SKIP (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="37dad-102">SKIP (Entity SQL)</span></span>
<span data-ttu-id="37dad-103">Physisches Paging kann mithilfe der SKIP-Unterklausel in der ORDER BY-Klausel durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="37dad-103">You can perform physical paging by using the SKIP sub-clause in the ORDER BY clause.</span></span> <span data-ttu-id="37dad-104">SKIP kann nicht ohne die ORDER BY-Klausel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37dad-104">SKIP cannot be used separately from the ORDER BY clause.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="37dad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37dad-105">Syntax</span></span>  
  
```  
[ SKIP n ]  
```  
  
## <a name="arguments"></a><span data-ttu-id="37dad-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="37dad-106">Arguments</span></span>  
 `n`  
 <span data-ttu-id="37dad-107">Die Anzahl zu überspringender Elemente.</span><span class="sxs-lookup"><span data-stu-id="37dad-107">The number of items to skip.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="37dad-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="37dad-108">Remarks</span></span>  
 <span data-ttu-id="37dad-109">Wenn eine ORDER BY-Klausel den Ausdruck SKIP als Unterklausel enthält, werden die Ergebnisse den Sortierangaben entsprechend sortiert, und das Resultset enthält die Zeilen, die auf den SKIP-Ausdruck folgen.</span><span class="sxs-lookup"><span data-stu-id="37dad-109">If a SKIP expression sub-clause is present in an ORDER BY clause, the results will be sorted according the sort specification and the result set will include rows starting from the next row immediately after the SKIP expression.</span></span> <span data-ttu-id="37dad-110">Mit SKIP 5 werden beispielsweise die ersten fünf Zeilen übersprungen und nur die Zeilen ab der sechsten Zeile zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37dad-110">For example, SKIP 5 will skip the first five rows and return from the sixth row forward.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="37dad-111">Eine [!INCLUDE[esql](../../../../../../includes/esql-md.md)] -Abfrage ist ungültig, wenn im selben Abfrageausdruck sowohl ein TOP-Modifizierer als auch eine SKIP-Unterklausel vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="37dad-111">An [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query is invalid if both the TOP modifier and the SKIP sub-clause are present in the same query expression.</span></span> <span data-ttu-id="37dad-112">In der Abfrage sollte der TOP-Ausdruck in einen LIMIT-Ausdruck geändert werden.</span><span class="sxs-lookup"><span data-stu-id="37dad-112">The query should be rewritten by changing the TOP expression to the LIMIT expression.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="37dad-113">Die Verwendung von SKIP mit ORDER BY für Nichtschlüsselspalten kann in [!INCLUDE[ssVersion2000](../../../../../../includes/ssversion2000-md.md)]zu falschen Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="37dad-113">In [!INCLUDE[ssVersion2000](../../../../../../includes/ssversion2000-md.md)], using SKIP with ORDER BY on non-key columns might return incorrect results.</span></span> <span data-ttu-id="37dad-114">Es kann vorkommen, dass mehr als die angegebene Anzahl von Zeilen übersprungen wird, wenn die Nichtschlüsselspalte Daten doppelt enthält.</span><span class="sxs-lookup"><span data-stu-id="37dad-114">More than the specified number of rows might be skipped if the non-key column has duplicate data in it.</span></span> <span data-ttu-id="37dad-115">Der Grund dafür ist die Übersetzung von SKIP für [!INCLUDE[ssVersion2000](../../../../../../includes/ssversion2000-md.md)].</span><span class="sxs-lookup"><span data-stu-id="37dad-115">This is due to how SKIP is translated for [!INCLUDE[ssVersion2000](../../../../../../includes/ssversion2000-md.md)].</span></span> <span data-ttu-id="37dad-116">Im folgenden Code können beispielsweise mehr als fünf Zeilen übersprungen werden, wenn `E.NonKeyColumn` Werte doppelt enthält:</span><span class="sxs-lookup"><span data-stu-id="37dad-116">For example, in the following code more than five rows might be skipped if `E.NonKeyColumn` has duplicate values:</span></span>  
>   
>  `SELECT [E] FROM Container.EntitySet AS [E] ORDER BY [E].[NonKeyColumn] DESC SKIP 5L`  
  
 <span data-ttu-id="37dad-117">In der  [!INCLUDE[esql](../../../../../../includes/esql-md.md)] -Abfrage in [diesem](https://msdn.microsoft.com/library/bb738702\(v=vs.100\).aspx#_ESQL) Beispiel wird der ORDER BY-Operator mit SKIP verwendet, um für die von der SELECT-Anweisung zurückgegebenen Objekte die zu verwendende Sortierreihenfolge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="37dad-117">The  [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query in [this](https://msdn.microsoft.com/library/bb738702\(v=vs.100\).aspx#_ESQL) example uses the ORDER BY operator with SKIP to specify the sort order used on objects returned in a SELECT statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37dad-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37dad-118">See also</span></span>
- [<span data-ttu-id="37dad-119">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="37dad-119">ORDER BY</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/order-by-entity-sql.md)
- [<span data-ttu-id="37dad-120">Vorgehensweise: Seitenweise Abfrageresultate durch Navigieren</span><span class="sxs-lookup"><span data-stu-id="37dad-120">How to: Page Through Query Results</span></span>](https://msdn.microsoft.com/library/ffc0f920-e7de-42e0-9b12-ef356421d030)
- [<span data-ttu-id="37dad-121">Paging</span><span class="sxs-lookup"><span data-stu-id="37dad-121">Paging</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/paging-entity-sql.md)
- [<span data-ttu-id="37dad-122">TOP</span><span class="sxs-lookup"><span data-stu-id="37dad-122">TOP</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/top-entity-sql.md)
