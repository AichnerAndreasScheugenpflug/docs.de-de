---
title: Querying XML Trees (C#) (Abfragen von XML-Strukturen (C#))
ms.date: 07/20/2015
ms.assetid: 0913d81b-541a-4fd4-9cbf-7ec89fd817ea
ms.openlocfilehash: 71a3d8538d96a9a5c273188a1bbb920ad6fa2d37
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54741729"
---
# <a name="querying-xml-trees-c"></a><span data-ttu-id="0cc9c-102">Querying XML Trees (C#) (Abfragen von XML-Strukturen (C#))</span><span class="sxs-lookup"><span data-stu-id="0cc9c-102">Querying XML Trees (C#)</span></span>
<span data-ttu-id="0cc9c-103">Dieser Abschnitt enthält Beispiele für [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]-Abfragen.</span><span class="sxs-lookup"><span data-stu-id="0cc9c-103">This section provides examples of [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] queries.</span></span>  
  
 <span data-ttu-id="0cc9c-104">Weitere Informationen zum Schreiben von [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)]-Abfragen finden Sie unter [Erste Schritte mit LINQ in C#](../../../../csharp/programming-guide/concepts/linq/getting-started-with-linq.md).</span><span class="sxs-lookup"><span data-stu-id="0cc9c-104">For more information about writing [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] queries, see [Getting Started with LINQ in C#](../../../../csharp/programming-guide/concepts/linq/getting-started-with-linq.md).</span></span>  
  
 <span data-ttu-id="0cc9c-105">Die effektivste Möglichkeit, Daten aus einer von Ihnen instanziierten XML-Struktur zu extrahieren, besteht im Schreiben von Abfragen.</span><span class="sxs-lookup"><span data-stu-id="0cc9c-105">After you have instantiated an XML tree, writing queries is the most effective way to extract data from the tree.</span></span> <span data-ttu-id="0cc9c-106">Das Kombinieren von Abfragen mit der funktionalen Konstruktion versetzt Sie in die Lage, ein neues XML-Dokument zu generieren, das eine andere Form als das ursprüngliche Dokument hat.</span><span class="sxs-lookup"><span data-stu-id="0cc9c-106">Also, querying combined with functional construction enables you to generate a new XML document that has a different shape from the original document.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="0cc9c-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0cc9c-107">In This Section</span></span>  
  
|<span data-ttu-id="0cc9c-108">Thema</span><span class="sxs-lookup"><span data-stu-id="0cc9c-108">Topic</span></span>|<span data-ttu-id="0cc9c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0cc9c-109">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="0cc9c-110">Basic Queries (LINQ to XML) (C#) (Standardabfragen (LINQ to XML) (C#))</span><span class="sxs-lookup"><span data-stu-id="0cc9c-110">Basic Queries (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)|<span data-ttu-id="0cc9c-111">Enthält allgemeine Beispiele für das Abfragen von XML-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="0cc9c-111">Provides common examples of querying XML trees.</span></span>|  
|[<span data-ttu-id="0cc9c-112">Projections and Transformations (LINQ to XML) (C#) (Projektionen und Transformationen (LINQ to XML) (C#))</span><span class="sxs-lookup"><span data-stu-id="0cc9c-112">Projections and Transformations (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/projections-and-transformations-linq-to-xml.md)|<span data-ttu-id="0cc9c-113">Enthält allgemeine Beispiele für das Projizieren aus und das Transformieren in XML-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="0cc9c-113">Provides common examples of projecting from and transforming XML trees.</span></span>|  
|[<span data-ttu-id="0cc9c-114">Erweiterte Abfragetechniken (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="0cc9c-114">Advanced Query Techniques (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/advanced-query-techniques-linq-to-xml.md)|<span data-ttu-id="0cc9c-115">Enthält Abfragetechniken für komplexere Szenarios.</span><span class="sxs-lookup"><span data-stu-id="0cc9c-115">Provides query techniques that are useful in more advanced scenarios.</span></span>|  
|[<span data-ttu-id="0cc9c-116">LINQ to XML für XPath-Benutzer (C#)</span><span class="sxs-lookup"><span data-stu-id="0cc9c-116">LINQ to XML for XPath Users (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)|<span data-ttu-id="0cc9c-117">Listet eine Reihe von XPath-Ausdrücken mit ihren [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]-Entsprechungen auf.</span><span class="sxs-lookup"><span data-stu-id="0cc9c-117">Presents a number of XPath expressions and their [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] equivalents.</span></span>|  
|[<span data-ttu-id="0cc9c-118">Pure Functional Transformations of XML (C#) (Reine funktionale XML-Transformationen (C#))</span><span class="sxs-lookup"><span data-stu-id="0cc9c-118">Pure Functional Transformations of XML (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/pure-functional-transformations-of-xml.md)|<span data-ttu-id="0cc9c-119">Enthält ein kleines Lernprogramm zum Schreiben von Abfragen im Stil der funktionalen Programmierung.</span><span class="sxs-lookup"><span data-stu-id="0cc9c-119">Presents a small tutorial on writing queries in the style of functional programming.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0cc9c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cc9c-120">See also</span></span>

- [<span data-ttu-id="0cc9c-121">Programming Guide (LINQ to XML) (C#) (Programmierhandbuch (LINQ to XML) (C#))</span><span class="sxs-lookup"><span data-stu-id="0cc9c-121">Programming Guide (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/programming-guide-linq-to-xml.md)
- [<span data-ttu-id="0cc9c-122">Erste Schritte mit LINQ in C#</span><span class="sxs-lookup"><span data-stu-id="0cc9c-122">Getting Started with LINQ in C#</span></span>](../../../../csharp/programming-guide/concepts/linq/getting-started-with-linq.md)
