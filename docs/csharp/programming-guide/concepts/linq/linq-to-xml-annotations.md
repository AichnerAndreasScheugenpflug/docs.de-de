---
title: LINQ to XML-Anmerkungen 3
ms.date: 07/20/2015
ms.assetid: 54e7b9d0-07f5-488f-9065-b6e6b870f810
ms.openlocfilehash: 753fc656d78f2cefde98a8cbfb48713c7a107f77
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676718"
---
# <a name="linq-to-xml-annotations"></a>LINQ to XML-Anmerkungen
Mit Anmerkungen in [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] können Sie Objekte eines beliebigen Typs mit jeder beliebigen XML-Komponente in einer XML-Struktur verknüpfen.  
  
 Zum Hinzufügen einer Anmerkung zu einer XML-Komponente, wie einem <xref:System.Xml.Linq.XElement> oder einem <xref:System.Xml.Linq.XAttribute>, rufen Sie die <xref:System.Xml.Linq.XObject.AddAnnotation%2A>-Methode auf. Anmerkungen werden nach Typ abgerufen.  
  
 Beachten Sie, dass Anmerkungen nicht Teil des XML-Infosets sind; sie werden nicht serialisiert oder deserialisiert.  
  
## <a name="methods"></a>Methoden  
 Beim Arbeiten mit Anmerkungen können Sie die folgenden Methoden verwenden:  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XObject.AddAnnotation%2A>|Fügt der Anmerkungsliste eines <xref:System.Xml.Linq.XObject> ein Objekt hinzu.|  
|<xref:System.Xml.Linq.XObject.Annotation%2A>|Ruft das erste Anmerkungsobjekt des angegebenen Typs aus einem <xref:System.Xml.Linq.XObject> ab.|  
|<xref:System.Xml.Linq.XObject.Annotations%2A>|Ruft eine Auflistung von Anmerkungen des angegebenen Typs für ein <xref:System.Xml.Linq.XObject> ab.|  
|<xref:System.Xml.Linq.XObject.RemoveAnnotations%2A>|Entfernt die Anmerkungen des angegebenen Typs aus einem <xref:System.Xml.Linq.XObject>.|  
  
## <a name="see-also"></a>Siehe auch

- [Advanced LINQ to XML Programming (C#) (Erweiterte LINQ to XML-Programmierung (C#))](../../../../csharp/programming-guide/concepts/linq/advanced-linq-to-xml-programming.md)
