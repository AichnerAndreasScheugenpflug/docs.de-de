---
title: 'Beispiel-XML-Datei: Numerische Daten in einem Namespace'
ms.date: 07/20/2015
ms.assetid: 51750cab-3c66-4511-90fb-b9d211308d31
ms.openlocfilehash: d00ad41c6703945b80dd49ff5f375a3896b43bed
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702131"
---
# <a name="sample-xml-file-numerical-data-in-a-namespace"></a><span data-ttu-id="0f298-102">Beispiel-XML-Datei: Numerische Daten in einem Namespace</span><span class="sxs-lookup"><span data-stu-id="0f298-102">Sample XML File: Numerical Data in a Namespace</span></span>
<span data-ttu-id="0f298-103">Die folgende XML-Datei wird in verschiedenen Beispielen in der [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]-Dokumentation verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f298-103">The following XML file is used in various examples in the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] documentation.</span></span> <span data-ttu-id="0f298-104">Diese Datei enthält numerische Daten zum Summieren, zur Durchschnittsberechnung und zum Gruppieren.</span><span class="sxs-lookup"><span data-stu-id="0f298-104">This file contains numerical data for summing, averaging, and grouping.</span></span> <span data-ttu-id="0f298-105">Der XML-Code befindet sich in einem Namespace.</span><span class="sxs-lookup"><span data-stu-id="0f298-105">The XML is in a namespace.</span></span>  
  
## <a name="data"></a><span data-ttu-id="0f298-106">Daten</span><span class="sxs-lookup"><span data-stu-id="0f298-106">Data</span></span>  
  
```xml  
<Root xmlns='http://www.adatum.com'>  
  <TaxRate>7.25</TaxRate>  
  <Data>  
    <Category>A</Category>  
    <Quantity>3</Quantity>  
    <Price>24.50</Price>  
  </Data>  
  <Data>  
    <Category>B</Category>  
    <Quantity>1</Quantity>  
    <Price>89.99</Price>  
  </Data>  
  <Data>  
    <Category>A</Category>  
    <Quantity>5</Quantity>  
    <Price>4.95</Price>  
  </Data>  
  <Data>  
    <Category>A</Category>  
    <Quantity>3</Quantity>  
    <Price>66.00</Price>  
  </Data>  
  <Data>  
    <Category>B</Category>  
    <Quantity>10</Quantity>  
    <Price>.99</Price>  
  </Data>  
  <Data>  
    <Category>A</Category>  
    <Quantity>15</Quantity>  
    <Price>29.00</Price>  
  </Data>  
  <Data>  
    <Category>B</Category>  
    <Quantity>8</Quantity>  
    <Price>6.99</Price>  
  </Data>  
</Root>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0f298-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f298-107">See also</span></span>

- [<span data-ttu-id="0f298-108">XML-Beispieldokumente (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="0f298-108">Sample XML Documents (LINQ to XML)</span></span>](../../../../csharp/programming-guide/concepts/linq/sample-xml-documents-linq-to-xml.md)
