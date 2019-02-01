---
title: Paralleles LINQ (PLINQ)
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- PLINQ, overview
ms.assetid: 3d4d0cd3-bde4-490b-99e7-f4e41be96455
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d597bc3590441494478c46b832aeed57ba761ca7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54500836"
---
# <a name="parallel-linq-plinq"></a><span data-ttu-id="7c608-102">Paralleles LINQ (PLINQ)</span><span class="sxs-lookup"><span data-stu-id="7c608-102">Parallel LINQ (PLINQ)</span></span>
<span data-ttu-id="7c608-103">Paralleles LINQ (PLINQ) ist eine parallele Implementierung für LINQ to Objects.</span><span class="sxs-lookup"><span data-stu-id="7c608-103">Parallel LINQ (PLINQ) is a parallel implementation of LINQ to Objects.</span></span> <span data-ttu-id="7c608-104">PLINQ implementiert den kompletten Satz von LINQ-Standardabfrageoperatoren als Erweiterungsmethoden für den <xref:System.Linq>-Namespace und verfügt über zusätzliche Operatoren für parallele Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="7c608-104">PLINQ implements the full set of LINQ standard query operators as extension methods for the <xref:System.Linq> namespace and has additional operators for parallel operations.</span></span> <span data-ttu-id="7c608-105">PLINQ kombiniert die Einfachheit und Lesbarkeit der LINQ-Syntax mit der Leistungsfähigkeit der parallelen Programmierung.</span><span class="sxs-lookup"><span data-stu-id="7c608-105">PLINQ combines the simplicity and readability of LINQ syntax with the power of parallel programming.</span></span> <span data-ttu-id="7c608-106">Ebenso wie Code für die Task Parallel Library skalieren PLINQ-Abfragen abhängig von den Funktionen (Parallelitätsgrad) des Hostcomputers.</span><span class="sxs-lookup"><span data-stu-id="7c608-106">Just like code that targets the Task Parallel Library, PLINQ queries scale in the degree of concurrency based on the capabilities of the host computer.</span></span>  
  
 <span data-ttu-id="7c608-107">PLINQ kann LINQ to Objects-Abfragen in vielen Fällen erheblich beschleunigen, indem alle verfügbaren Kerne auf dem Hostcomputer effizienter genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="7c608-107">In many scenarios, PLINQ can significantly increase the speed of LINQ to Objects queries by using all available cores on the host computer more efficiently.</span></span> <span data-ttu-id="7c608-108">Diese höhere Leistung stellt eine maximale Verarbeitungsleistung am Desktop bereit.</span><span class="sxs-lookup"><span data-stu-id="7c608-108">This increased performance brings high-performance computing power onto the desktop.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7c608-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7c608-109">In This Section</span></span>  
 [<span data-ttu-id="7c608-110">Einführung in PLINQ</span><span class="sxs-lookup"><span data-stu-id="7c608-110">Introduction to PLINQ</span></span>](../../../docs/standard/parallel-programming/introduction-to-plinq.md)  
  
 [<span data-ttu-id="7c608-111">Grundlagen zur Beschleunigung in PLINQ</span><span class="sxs-lookup"><span data-stu-id="7c608-111">Understanding Speedup in PLINQ</span></span>](../../../docs/standard/parallel-programming/understanding-speedup-in-plinq.md)  
  
 [<span data-ttu-id="7c608-112">Beibehaltung der Reihenfolge in PLINQ</span><span class="sxs-lookup"><span data-stu-id="7c608-112">Order Preservation in PLINQ</span></span>](../../../docs/standard/parallel-programming/order-preservation-in-plinq.md)  
  
 [<span data-ttu-id="7c608-113">Mergeoptionen in PLINQ</span><span class="sxs-lookup"><span data-stu-id="7c608-113">Merge Options in PLINQ</span></span>](../../../docs/standard/parallel-programming/merge-options-in-plinq.md)  
  
 [<span data-ttu-id="7c608-114">Vorgehensweise: Erstellen und Ausführen einer einfachen PLINQ-Abfrage</span><span class="sxs-lookup"><span data-stu-id="7c608-114">How to: Create and Execute a Simple PLINQ Query</span></span>](../../../docs/standard/parallel-programming/how-to-create-and-execute-a-simple-plinq-query.md)  
  
 [<span data-ttu-id="7c608-115">Vorgehensweise: Steuern der Reihenfolge in einer PLINQ-Abfrage</span><span class="sxs-lookup"><span data-stu-id="7c608-115">How to: Control Ordering in a PLINQ Query</span></span>](../../../docs/standard/parallel-programming/how-to-control-ordering-in-a-plinq-query.md)  
  
 [<span data-ttu-id="7c608-116">Vorgehensweise: Kombinieren von parallelen und sequenziellen LINQ-Abfragen</span><span class="sxs-lookup"><span data-stu-id="7c608-116">How to: Combine Parallel and Sequential LINQ Queries</span></span>](../../../docs/standard/parallel-programming/how-to-combine-parallel-and-sequential-linq-queries.md)  
  
 [<span data-ttu-id="7c608-117">Vorgehensweise: Behandeln von Ausnahmen in einer PLINQ-Abfrage</span><span class="sxs-lookup"><span data-stu-id="7c608-117">How to: Handle Exceptions in a PLINQ Query</span></span>](../../../docs/standard/parallel-programming/how-to-handle-exceptions-in-a-plinq-query.md)  
  
 [<span data-ttu-id="7c608-118">Vorgehensweise: Abbrechen einer PLINQ-Abfrage</span><span class="sxs-lookup"><span data-stu-id="7c608-118">How to: Cancel a PLINQ Query</span></span>](../../../docs/standard/parallel-programming/how-to-cancel-a-plinq-query.md)  
  
 [<span data-ttu-id="7c608-119">Vorgehensweise: Schreiben einer benutzerdefinierten PLINQ-Aggregatfunktion</span><span class="sxs-lookup"><span data-stu-id="7c608-119">How to: Write a Custom PLINQ Aggregate Function</span></span>](../../../docs/standard/parallel-programming/how-to-write-a-custom-plinq-aggregate-function.md)  
  
 [<span data-ttu-id="7c608-120">Vorgehensweise: Angeben des Ausführungsmodus in PLINQ</span><span class="sxs-lookup"><span data-stu-id="7c608-120">How to: Specify the Execution Mode in PLINQ</span></span>](../../../docs/standard/parallel-programming/how-to-specify-the-execution-mode-in-plinq.md)  
  
 [<span data-ttu-id="7c608-121">Vorgehensweise: Angeben von Mergeoptionen in PLINQ</span><span class="sxs-lookup"><span data-stu-id="7c608-121">How to: Specify Merge Options in PLINQ</span></span>](../../../docs/standard/parallel-programming/how-to-specify-merge-options-in-plinq.md)  
  
 [<span data-ttu-id="7c608-122">Vorgehensweise: Iterieren von Dateiverzeichnissen mit PLINQ</span><span class="sxs-lookup"><span data-stu-id="7c608-122">How to: Iterate File Directories with PLINQ</span></span>](../../../docs/standard/parallel-programming/how-to-iterate-file-directories-with-plinq.md)  
  
 [<span data-ttu-id="7c608-123">Vorgehensweise: Messen der Leistung von PLINQ-Abfragen</span><span class="sxs-lookup"><span data-stu-id="7c608-123">How to: Measure PLINQ Query Performance</span></span>](../../../docs/standard/parallel-programming/how-to-measure-plinq-query-performance.md)  
  
 [<span data-ttu-id="7c608-124">PLINQ-Datenbeispiel</span><span class="sxs-lookup"><span data-stu-id="7c608-124">PLINQ Data Sample</span></span>](../../../docs/standard/parallel-programming/plinq-data-sample.md)  
  
## <a name="see-also"></a><span data-ttu-id="7c608-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c608-125">See also</span></span>

- <xref:System.Linq.ParallelEnumerable>
- [<span data-ttu-id="7c608-126">Parallele Programmierung</span><span class="sxs-lookup"><span data-stu-id="7c608-126">Parallel Programming</span></span>](../../../docs/standard/parallel-programming/index.md)
- [<span data-ttu-id="7c608-127">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="7c608-127">LINQ (Language-Integrated Query)</span></span>](https://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d)
