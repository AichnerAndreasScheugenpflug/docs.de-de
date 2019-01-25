---
title: Erstellen eines "DataSets"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 57629d8f-393e-4677-8b83-29ffde27f5fc
ms.openlocfilehash: 62f0aca98c861771d3b7cc20c9f473165bc6546d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743373"
---
# <a name="creating-a-dataset"></a><span data-ttu-id="cb05e-102">Erstellen eines "DataSets"</span><span class="sxs-lookup"><span data-stu-id="cb05e-102">Creating a DataSet</span></span>
<span data-ttu-id="cb05e-103">Durch Aufrufen des <xref:System.Data.DataSet>-Konstruktors wird eine Instanz eines <xref:System.Data.DataSet> erstellt.</span><span class="sxs-lookup"><span data-stu-id="cb05e-103">You create an instance of a <xref:System.Data.DataSet> by calling the <xref:System.Data.DataSet> constructor.</span></span> <span data-ttu-id="cb05e-104">Optional kann ein Argument für den Namen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cb05e-104">Optionally specify a name argument.</span></span> <span data-ttu-id="cb05e-105">Wenn für das <xref:System.Data.DataSet> kein Name angegeben wird, wird der Name auf "NewDataSet" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cb05e-105">If you do not specify a name for the <xref:System.Data.DataSet>, the name is set to "NewDataSet".</span></span>  
  
 <span data-ttu-id="cb05e-106">Sie können auch ein neues <xref:System.Data.DataSet> auf der Grundlage eines vorhandenen <xref:System.Data.DataSet> erstellen.</span><span class="sxs-lookup"><span data-stu-id="cb05e-106">You can also create a new <xref:System.Data.DataSet> based on an existing <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="cb05e-107">Das neue <xref:System.Data.DataSet> kann eine exakte Kopie des vorhandenen <xref:System.Data.DataSet> sein. Es kann ein Klon des <xref:System.Data.DataSet> sein, der die relationale Struktur oder das relationale Schema kopiert, aber keine Daten aus dem vorhandenen <xref:System.Data.DataSet> enthält. Es kann auch eine mithilfe der <xref:System.Data.DataSet>-Methode erstellte Teilmenge des <xref:System.Data.DataSet> sein, das nur die geänderten Zeilen aus dem vorhandenen <xref:System.Data.DataSet.GetChanges%2A> enthält.</span><span class="sxs-lookup"><span data-stu-id="cb05e-107">The new <xref:System.Data.DataSet> can be an exact copy of the existing <xref:System.Data.DataSet>; a clone of the <xref:System.Data.DataSet> that copies the relational structure or schema but that does not contain any of the data from the existing <xref:System.Data.DataSet>; or a subset of the <xref:System.Data.DataSet>, containing only the modified rows from the existing <xref:System.Data.DataSet> using the <xref:System.Data.DataSet.GetChanges%2A> method.</span></span> <span data-ttu-id="cb05e-108">Weitere Informationen finden Sie unter [Kopieren von DataSet-Inhalten](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/copying-dataset-contents.md).</span><span class="sxs-lookup"><span data-stu-id="cb05e-108">For more information, see [Copying DataSet Contents](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/copying-dataset-contents.md).</span></span>  
  
 <span data-ttu-id="cb05e-109">Im folgenden Codebeispiel wird das Erstellen einer Instanz eines <xref:System.Data.DataSet> veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="cb05e-109">The following code example demonstrates how to construct an instance of a <xref:System.Data.DataSet>.</span></span>  
  
```vb  
Dim customerOrders As DataSet = New DataSet("CustomerOrders")  
```  
  
```csharp  
DataSet customerOrders = new DataSet("CustomerOrders");  
```  
  
## <a name="see-also"></a><span data-ttu-id="cb05e-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb05e-110">See also</span></span>
- [<span data-ttu-id="cb05e-111">Populating a DataSet from a DataAdapter (Auffüllen eines DataSets durch einen DataAdapter)</span><span class="sxs-lookup"><span data-stu-id="cb05e-111">Populating a DataSet from a DataAdapter</span></span>](../../../../../docs/framework/data/adonet/populating-a-dataset-from-a-dataadapter.md)
- [<span data-ttu-id="cb05e-112">DataSets, DataTables und DataViews</span><span class="sxs-lookup"><span data-stu-id="cb05e-112">DataSets, DataTables, and DataViews</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [<span data-ttu-id="cb05e-113">ADO.NET Managed Provider und DataSet Developer Center</span><span class="sxs-lookup"><span data-stu-id="cb05e-113">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
