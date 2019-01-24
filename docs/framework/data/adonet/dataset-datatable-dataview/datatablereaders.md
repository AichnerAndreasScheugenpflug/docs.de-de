---
title: "\"DataTableReaders\""
ms.date: 03/30/2017
ms.assetid: 97546ae2-0e42-4d26-961d-e0b244d81ded
ms.openlocfilehash: 9984dc9c215a34ab35524560e4dcbcd6bd12596d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54602844"
---
# <a name="datatablereaders"></a><span data-ttu-id="fa497-102">"DataTableReaders"</span><span class="sxs-lookup"><span data-stu-id="fa497-102">DataTableReaders</span></span>
<span data-ttu-id="fa497-103">Der <xref:System.Data.DataTableReader> stellt den Inhalt einer <xref:System.Data.DataTable> oder eines <xref:System.Data.DataSet> in Form eines oder mehrerer schreibgeschützter vorwärts gerichteter Resultsets dar.</span><span class="sxs-lookup"><span data-stu-id="fa497-103">The <xref:System.Data.DataTableReader> presents the contents of a <xref:System.Data.DataTable> or a <xref:System.Data.DataSet> in the form of one or more read-only, forward-only result sets.</span></span>  
  
 <span data-ttu-id="fa497-104">Bei der Erstellung einer **DataTableReader** aus einer **DataTable**, die resultierende **DataTableReader** Objekt enthält die gleichen Daten wie ein Resultset der  **DataTable** aus dem er, mit Ausnahme von Zeilen erstellt wurde, die als gelöscht markiert wurden.</span><span class="sxs-lookup"><span data-stu-id="fa497-104">When you create a **DataTableReader** from a **DataTable**, the resulting **DataTableReader** object contains one result set with the same data as the **DataTable** from which it was created, except for any rows that have been marked as deleted.</span></span> <span data-ttu-id="fa497-105">Die Spalten angezeigt werden, in der gleichen Reihenfolge wie in der ursprünglichen **DataTable**.</span><span class="sxs-lookup"><span data-stu-id="fa497-105">The columns appear in the same order as in the original **DataTable**.</span></span>  
  
 <span data-ttu-id="fa497-106">Ein **DataTableReader** kann mehrere Resultsets enthalten, wenn er durch den Aufruf erstellt wurde <xref:System.Data.DataSet.CreateDataReader%2A>.</span><span class="sxs-lookup"><span data-stu-id="fa497-106">A **DataTableReader** may contain multiple result sets if it was created by calling <xref:System.Data.DataSet.CreateDataReader%2A>.</span></span> <span data-ttu-id="fa497-107">Die Ergebnisse werden in der gleichen Reihenfolge wie die **DataTables** in die **DataSet** des Objekts <xref:System.Data.DataSet.Tables%2A> Auflistung.</span><span class="sxs-lookup"><span data-stu-id="fa497-107">The results are in the same order as the **DataTables** in the **DataSet** object's <xref:System.Data.DataSet.Tables%2A> collection.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="fa497-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="fa497-108">In This Section</span></span>  
 [<span data-ttu-id="fa497-109">Erstellen eines DataReader</span><span class="sxs-lookup"><span data-stu-id="fa497-109">Creating a DataReader</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/creating-a-datareader.md)  
 <span data-ttu-id="fa497-110">Erläutert das Erstellen einer **DataTableReader** Objekt.</span><span class="sxs-lookup"><span data-stu-id="fa497-110">Discusses how to create a **DataTableReader** object.</span></span>  
  
 [<span data-ttu-id="fa497-111">Navigieren in DataTables</span><span class="sxs-lookup"><span data-stu-id="fa497-111">Navigating DataTables</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/navigating-datatables.md)  
 <span data-ttu-id="fa497-112">Beschreibt die Verwendung von der **lesen** -Methode durch den Inhalt des Verschieben einer **DataTableReader**.</span><span class="sxs-lookup"><span data-stu-id="fa497-112">Describes the use of the **Read** method to move through the contents of a **DataTableReader**.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa497-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa497-113">See also</span></span>
- [<span data-ttu-id="fa497-114">Abrufen und Ändern von Daten in ADO.NET</span><span class="sxs-lookup"><span data-stu-id="fa497-114">Retrieving and Modifying Data in ADO.NET</span></span>](../../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [<span data-ttu-id="fa497-115">ADO.NET Managed Provider und DataSet Developer Center</span><span class="sxs-lookup"><span data-stu-id="fa497-115">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
