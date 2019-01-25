---
title: 'Beispiele für die methodenbasierte Abfragesyntax: Umwandeln'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 19f66872-d5ab-49f8-969f-e53f9632a13d
ms.openlocfilehash: 3e3986bcd956fae45005671cc945ea0c861d7e07
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702313"
---
# <a name="method-based-query-syntax-examples-conversion"></a><span data-ttu-id="ab2bd-102">Beispiele für die methodenbasierte Abfragesyntax: Umwandeln</span><span class="sxs-lookup"><span data-stu-id="ab2bd-102">Method-Based Query Syntax Examples: Conversion</span></span>
<span data-ttu-id="ab2bd-103">In diesem Thema wird gezeigt, wie mit der <xref:System.Linq.Enumerable.ToArray%2A>, <xref:System.Linq.Enumerable.ToDictionary%2A> und <xref:System.Linq.Enumerable.ToList%2A> Methoden zum Abfragen der [AdventureWorks Sales-Modell](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) mit der methodenbasierten Abfragesyntax.</span><span class="sxs-lookup"><span data-stu-id="ab2bd-103">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.ToArray%2A>, <xref:System.Linq.Enumerable.ToDictionary%2A> and <xref:System.Linq.Enumerable.ToList%2A> methods to query the [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) using method-based query syntax.</span></span> <span data-ttu-id="ab2bd-104">Für das in den Beispielen verwendete "AdventureWorks Sales"-Modell wurde auf die Tabellen Contact, Address, Product, SalesOrderHeader und SalesOrderDetail der "AdventureWorks"-Beispieldatenbank zurückgegriffen.</span><span class="sxs-lookup"><span data-stu-id="ab2bd-104">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="ab2bd-105">In die Beispielen in diesem Thema verwenden Sie die folgenden `using` / `Imports` Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="ab2bd-105">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="toarray"></a><span data-ttu-id="ab2bd-106">ToArray</span><span class="sxs-lookup"><span data-stu-id="ab2bd-106">ToArray</span></span>  
  
### <a name="example"></a><span data-ttu-id="ab2bd-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ab2bd-107">Example</span></span>  
 <span data-ttu-id="ab2bd-108">Im folgenden Beispiel wird die <xref:System.Linq.Enumerable.ToArray%2A>-Methode verwendet, um eine Sequenz unmittelbar in ein Array auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="ab2bd-108">The following example uses the <xref:System.Linq.Enumerable.ToArray%2A> method to immediately evaluate a sequence into an array.</span></span>  
  
 [!code-csharp[DP L2E Examples#ToArray](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#toarray)]
 [!code-vb[DP L2E Examples#ToArray](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#toarray)]  
  
## <a name="todictionary"></a><span data-ttu-id="ab2bd-109">ToDictionary</span><span class="sxs-lookup"><span data-stu-id="ab2bd-109">ToDictionary</span></span>  
  
### <a name="example"></a><span data-ttu-id="ab2bd-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ab2bd-110">Example</span></span>  
 <span data-ttu-id="ab2bd-111">Im folgenden Beispiel wird die <xref:System.Linq.Enumerable.ToDictionary%2A>-Methode verwendet, um eine Sequenz und einen zugehörigen Schlüsselausdruck unmittelbar in ein Wörterbuch umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="ab2bd-111">The following example uses the <xref:System.Linq.Enumerable.ToDictionary%2A> method to immediately evaluate a sequence and a related key expression into a dictionary.</span></span>  
  
 [!code-csharp[DP L2E Examples#ToDictionary](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#todictionary)]
 [!code-vb[DP L2E Examples#ToDictionary](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#todictionary)]  
  
## <a name="tolist"></a><span data-ttu-id="ab2bd-112">ToList</span><span class="sxs-lookup"><span data-stu-id="ab2bd-112">ToList</span></span>  
  
### <a name="example"></a><span data-ttu-id="ab2bd-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ab2bd-113">Example</span></span>  
 <span data-ttu-id="ab2bd-114">Im folgenden Beispiel wird die <xref:System.Linq.Enumerable.ToList%2A>-Methode verwendet, um eine Sequenz unmittelbar in eine <xref:System.Collections.Generic.List%601> umzuwandeln, wobei `T` vom Typ <xref:System.Data.DataRow> ist.</span><span class="sxs-lookup"><span data-stu-id="ab2bd-114">The following example uses the <xref:System.Linq.Enumerable.ToList%2A> method to immediately evaluate a sequence into a <xref:System.Collections.Generic.List%601>, where `T` is of type <xref:System.Data.DataRow>.</span></span>  
  
 [!code-csharp[DP L2E Examples#ToList](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#tolist)]
 [!code-vb[DP L2E Examples#ToList](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#tolist)]  
  
## <a name="see-also"></a><span data-ttu-id="ab2bd-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab2bd-115">See also</span></span>
- [<span data-ttu-id="ab2bd-116">Abfragen in LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="ab2bd-116">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
