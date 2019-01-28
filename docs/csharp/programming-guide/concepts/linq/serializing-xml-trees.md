---
title: Serialisieren von XML-Strukturen (C#)
ms.date: 07/20/2015
ms.assetid: b3937e54-4ce9-4236-ac96-14e7972aa594
ms.openlocfilehash: a1c39c4c85cbd01fa7c3f3f99f2dfae49e3721d9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54583443"
---
# <a name="serializing-xml-trees-c"></a><span data-ttu-id="14cee-102">Serialisieren von XML-Strukturen (C#)</span><span class="sxs-lookup"><span data-stu-id="14cee-102">Serializing XML Trees (C#)</span></span>
<span data-ttu-id="14cee-103">Beim Serialisieren einer XML-Struktur wird aus der XML-Struktur XML generiert.</span><span class="sxs-lookup"><span data-stu-id="14cee-103">Serializing an XML tree means generating XML from the XML tree.</span></span> <span data-ttu-id="14cee-104">Eine Serialisierung kann in eine Datei, in eine konkrete Implementierung der <xref:System.IO.TextWriter>-Klasse oder in eine konkrete Implementierung eines <xref:System.Xml.XmlWriter> erfolgen.</span><span class="sxs-lookup"><span data-stu-id="14cee-104">You can serialize to a file, to a concrete implementation of the <xref:System.IO.TextWriter> class, or to a concrete implementation of an <xref:System.Xml.XmlWriter>.</span></span>  
  
 <span data-ttu-id="14cee-105">Sie können verschiedene Aspekte der Serialisierung steuern.</span><span class="sxs-lookup"><span data-stu-id="14cee-105">You can control various aspects of serialization.</span></span> <span data-ttu-id="14cee-106">So können Sie z. B. steuern, ob das serialisierte XML mit Einzügen versehen und ob eine XML-Deklaration geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="14cee-106">For example, you can control whether to indent the serialized XML, and whether to write an XML declaration.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="14cee-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="14cee-107">In This Section</span></span>  
  
|<span data-ttu-id="14cee-108">Thema</span><span class="sxs-lookup"><span data-stu-id="14cee-108">Topic</span></span>|<span data-ttu-id="14cee-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14cee-109">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="14cee-110">Beibehalten von Leerzeichen beim Serialisieren</span><span class="sxs-lookup"><span data-stu-id="14cee-110">Preserving White Space While Serializing</span></span>](../../../../csharp/programming-guide/concepts/linq/preserving-white-space-while-serializing.md)|<span data-ttu-id="14cee-111">Beschreibt, wie Sie beim Serialisieren von XML-Strukturen das Leerraumverhalten steuern können.</span><span class="sxs-lookup"><span data-stu-id="14cee-111">Describes how to control white space behavior when you serialize XML trees.</span></span>|  
|[<span data-ttu-id="14cee-112">Serialisieren mit einer XML-Deklaration (C#)</span><span class="sxs-lookup"><span data-stu-id="14cee-112">Serializing with an XML Declaration (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/serializing-with-an-xml-declaration.md)|<span data-ttu-id="14cee-113">Beschreibt, wie Sie eine XML-Struktur serialisieren können, die eine XML-Deklaration enthält.</span><span class="sxs-lookup"><span data-stu-id="14cee-113">Describes how to serialize an XML tree that includes an XML declaration.</span></span>|  
|[<span data-ttu-id="14cee-114">Serialisieren in Dateien, TextWriters und XmlWriters</span><span class="sxs-lookup"><span data-stu-id="14cee-114">Serializing to Files, TextWriters, and XmlWriters</span></span>](../../../../csharp/programming-guide/concepts/linq/serializing-to-files-textwriters-and-xmlwriters.md)|<span data-ttu-id="14cee-115">Beschreibt, wie Sie ein Dokument in eine <xref:System.IO.File>, in einen <xref:System.IO.TextWriter> oder in einen <xref:System.Xml.XmlWriter> serialisieren können.</span><span class="sxs-lookup"><span data-stu-id="14cee-115">Describes how to serialize a document to a <xref:System.IO.File>, a <xref:System.IO.TextWriter>, or an <xref:System.Xml.XmlWriter>.</span></span>|  
|[<span data-ttu-id="14cee-116">Serialisieren in einen XmlReader (XSLT aufrufen) (C#)</span><span class="sxs-lookup"><span data-stu-id="14cee-116">Serializing to an XmlReader (Invoking XSLT) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/serializing-to-an-xmlreader-invoking-xslt.md)|<span data-ttu-id="14cee-117">Beschreibt, wie Sie einen <xref:System.Xml.XmlReader> erstellen können, der einem anderen Modul das Lesen des Inhalts einer XML-Struktur ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="14cee-117">Describes how to create a <xref:System.Xml.XmlReader> that enables another module to read the contents of an XML tree.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="14cee-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14cee-118">See also</span></span>

- [<span data-ttu-id="14cee-119">Programming Guide (LINQ to XML) (C#) (Programmierhandbuch (LINQ to XML) (C#))</span><span class="sxs-lookup"><span data-stu-id="14cee-119">Programming Guide (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/programming-guide-linq-to-xml.md)
