---
title: GetXmlNamespace-Operator (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.GetXmlNamespace
- GetXmlNamespace
helpviewer_keywords:
- GetXmlNamespace operator [Visual Basic]
- GetXmlNamespace keyword [Visual Basic]
ms.assetid: d0d28cfd-0755-4896-ae0b-4981aa35517c
ms.openlocfilehash: f9201aa4b2aa9280b9b3a4e0a2badf25ea819088
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54684748"
---
# <a name="getxmlnamespace-operator-visual-basic"></a>GetXmlNamespace-Operator (Visual Basic)
Ruft die <xref:System.Xml.Linq.XNamespace> Objekt, das dem angegebenen XML-Namespacepräfix entspricht.  
  
## <a name="syntax"></a>Syntax  
  
```  
GetXmlNamespace(xmlNamespacePrefix)  
```  
  
## <a name="parts"></a>Teile  
 `xmlNamespacePrefix`  
 Dies ist optional. Die Zeichenfolge, die das XML-Namespacepräfix identifiziert. Wenn angegeben, muss diese Zeichenfolge ein gültiger XML-Bezeichner sein. Weitere Informationen finden Sie unter [Namen von deklarierten XML-Elementen und Attributen](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md). Wenn kein Präfix angegeben ist, wird der Standardnamespace zurückgegeben. Wenn kein Standardnamespace angegeben wird, wird der leere Namespace zurückgegeben.  
  
## <a name="return-value"></a>Rückgabewert  
 Die <xref:System.Xml.Linq.XNamespace> Objekt, das das XML-Namespacepräfix entspricht.  
  
## <a name="remarks"></a>Hinweise  
 Die `GetXmlNamespace` Operator Ruft die <xref:System.Xml.Linq.XNamespace> Objekt, das das XML-Namespacepräfix entspricht `xmlNamespacePrefix`.  
  
 Sie können XML-Namespacepräfixe direkt in XML-Literale und XML-Achseneigenschaften verwenden. Allerdings müssen Sie verwenden die `GetXmlNamespace` Operator, um ein Namespacepräfix zu konvertieren eine <xref:System.Xml.Linq.XNamespace> Objekt, bevor Sie es in Ihrem Code verwenden können. Können Sie einen nicht qualifizierten Elementnamen zum Anfügen einer <xref:System.Xml.Linq.XNamespace> einen vollqualifizierten abzurufenden Objekts <xref:System.Xml.Linq.XName> Objekt, das für viele [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] Methoden erfordern.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel importiert `ns` als ein XML-Namespacepräfix. Klicken Sie dann das Namespacepräfix des Namespace eine XML-literal erstellt und Zugriff auf den ersten untergeordneten Knoten mit dem qualifizierten Namen verwendet `ns:phone`. Anschließend übergibt es dieses untergeordneten Knotens, der `ShowName` -Unterroutine, die einen qualifizierten Namen erstellt, mit der `GetXmlNamespace` Operator. Die `ShowName` Unterroutine übergibt dann den qualifizierten Namen auf die <xref:System.Xml.Linq.XNode.Ancestors%2A> -Methode zum Abrufen der übergeordneten `ns:contact` Knoten.  
  
 [!code-vb[VbXMLSamples#38](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/getxmlnamespace-operator_1.vb)]  
  
 Beim Aufruf `TestGetXmlNamespace.RunSample()`, es wird ein Meldungsfeld mit dem folgenden Text angezeigt:  
  
 `Name: Patrick Hines`  
  
## <a name="see-also"></a>Siehe auch
- [Imports-Anweisung (XML-Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md)
- [Zugreifen auf XML in Visual Basic](../../../visual-basic/programming-guide/language-features/xml/accessing-xml.md)
