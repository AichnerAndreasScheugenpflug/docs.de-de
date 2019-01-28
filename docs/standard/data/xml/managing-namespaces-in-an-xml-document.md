---
title: Verwalten von Namespaces in einem XML-Dokument
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 682643fc-b848-4e42-8c0d-50deeaeb5f2a
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e9375386360c94f959f638e1227cb847b783b994
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676171"
---
# <a name="managing-namespaces-in-an-xml-document"></a>Verwalten von Namespaces in einem XML-Dokument
XML-Namespaces ordnen benutzerdefinierten und vordefinierten URIs in einem XML-Dokument Element- und Attributnamen zu. Um diese Zuordnungen zu erstellen, definieren Sie Präfixe für Namespace-URIs und verwenden diese zur Kennzeichnung von Element- und Attributnamen in XML-Daten. Namespaces verhindern Konflikte zwischen Element- und Attributnamen. Sie ermöglichen eine unterschiedliche Verarbeitung und Validierung von gleichnamigen Elementen und Attributen.  
  
<a name="declare"></a>   
## <a name="declaring-namespaces"></a>Deklarieren von Namespaces  
 Um einen Namespace für ein Element zu deklarieren, verwenden Sie das `xmlns:`-Attribut:  
  
 `xmlns:<name>=<"uri">`  
  
 `<name>` entspricht dabei dem Namespacepräfix und `<"uri">` dem URI, durch den der Namespace identifiziert wird. Nachdem das Präfix deklariert wurde, können Sie mit ihm Elemente und Attribute in einem XML-Dokument kennzeichnen und diese dem Namespace-URI zuordnen. Da das Namespacepräfix im gesamten Dokument verwendet wird, sollte es möglichst kurz sein.  
  
 Im Beispiel werden zwei `BOOK`-Elemente definiert. Das erste Element wird durch das Präfix `mybook`, das zweite durch das Präfix `bb` gekennzeichnet. Jedes Präfix wird einem anderen Namespace-URI zugeordnet:  
  
```xml  
<mybook:BOOK xmlns:mybook="http://www.contoso.com/books.dtd">  
<bb:BOOK xmlns:bb="urn:blueyonderairlines">  
```  
  
 Sie können angeben, dass ein Element Teil eines bestimmten Namespaces ist, indem Sie das Namespacepräfix hinzufügen. Wenn das `Author`-Element beispielsweise ein Teil des `mybook`-Namespaces ist, wird es als `<mybook:Author>` deklariert.  
  
<a name="scope"></a>   
## <a name="declaration-scope"></a>Gültigkeitsbereich der Deklaration  
 Ein Namespace gilt ab dem Punkt der Deklaration bis zum Ende desjenigen Elements, in dem er deklariert wurde. In diesem Beispiel wird der im `BOOK`-Element definierte Namespace nicht auf Elemente außerhalb des `BOOK`-Elements, z. B. das `Publisher`-Element, angewendet:  
  
```xml  
<Author>Joe Smith</Author>  
<BOOK xmlns:book="http://www.contoso.com">  
    <title>My Wonderful Day</title>  
      <price>$3.95</price>  
</BOOK>  
<Publisher>  
    <Name>MSPress</Name>  
</Publisher>  
```  
  
 Ein Namespace muss deklariert werden, bevor er verwendet werden kann, aber er muss sich nicht unbedingt am Anfang des XML-Dokuments befinden.  
  
 Wenn Sie mehrere Namespaces in einem XML-Dokument verwenden, können Sie einen Namespace als Standardnamespace definieren, um ein übersichtlicheres Dokument zu erstellen. Der Standardnamespace wird im Stammelement deklariert und auf alle nicht gekennzeichneten Elemente im Dokument angewendet. Standardnamespaces gelten nur für Elemente und nicht für Attribute.  
  
 Um den Standardnamespace zu verwenden, lassen Sie das Präfix und den Doppelpunkt in der Elementdeklaration aus:  
  
```xml  
<BOOK xmlns="http://www.contoso.com/books.dtd">  
```  
  
## <a name="managing-namespaces"></a>Verwalten von Namespaces  
 In der <xref:System.Xml.XmlNamespaceManager>-Klasse wird eine Sammlung von Namespace-URIs und ihrer Präfixe gespeichert. Sie können Namespaces in der Sammlung suchen, hinzufügen und entfernen. In bestimmten Kontexten ist die Klasse erforderlich, um die XML-Verarbeitungsleistung zu verbessern. So wird <xref:System.Xml.Xsl.XsltContext> von der <xref:System.Xml.XmlNamespaceManager>-Klasse verwendet, um XPath-Unterstützung bereitzustellen.  
  
 Der Namespace-Manager führt keine Validierung der Namespaces durch, sondern setzt voraus, dass Präfixe und Namespaces bereits überprüft wurden und der [W3C](https://www.w3.org/TR/REC-xml-names/)-Spezifikation für Namespaces entsprechen.  
  
> [!NOTE]
>  <xref:System.Xml.XmlNamespaceManager> wird von [LINQ to XML](https://msdn.microsoft.com/library/f0fe21e9-ee43-4a55-b91a-0800e5782c13) nicht zur Verwaltung von Namespaces verwendet. Informationen zur Verwaltung von Namespaces bei der Verwendung von LINQ to XML finden Sie in der LINQ-Dokumentation unter [Arbeiten mit XML-Namespaces](https://msdn.microsoft.com/library/e3003209-3234-45be-a832-47feb7927430).  
  
 Im Folgenden finden Sie einige der Verwaltungs- und Suchaufgaben, die Sie mit der <xref:System.Xml.XmlNamespaceManager>-Klasse ausführen können. Weitere Informationen und Beispiele finden Sie, indem Sie den Links zur Referenzseite der einzelnen Methoden oder Eigenschaften folgen.  
  
|Beschreibung|Mit|  
|--------|---------|  
|Hinzufügen eines Namespaces|<xref:System.Xml.XmlNamespaceManager.AddNamespace%2A>-Methode|  
|Entfernen eines Namespaces|<xref:System.Xml.XmlNamespaceManager.RemoveNamespace%2A>-Methode|  
|Suchen des URIs für den Standardnamespace|<xref:System.Xml.XmlNamespaceManager.DefaultNamespace%2A> -Eigenschaft|  
|Suchen des URIs für ein Namespacepräfix|<xref:System.Xml.XmlNamespaceManager.LookupNamespace%2A>-Methode|  
|Suchen des Präfixes für einen Namespace-URI|<xref:System.Xml.XmlNamespaceManager.LookupPrefix%2A>-Methode|  
|Abrufen einer Namespaceliste im aktuellen Knoten|<xref:System.Xml.XmlNamespaceManager.GetNamespacesInScope%2A>-Methode|  
|Festlegen des Gültigkeitsbereichs für einen Namespace|Die Methoden <xref:System.Xml.XmlNamespaceManager.PushScope%2A> und <xref:System.Xml.XmlNamespaceManager.PopScope%2A>|  
|Überprüfen, ob im aktuellen Gültigkeitsbereich ein Präfix definiert ist|<xref:System.Xml.XmlNamespaceManager.HasNamespace%2A>-Methode|  
|Abrufen der Namenstabelle, die für die Suche nach Präfixen und URIs verwendet wird|<xref:System.Xml.XmlNamespaceManager.NameTable%2A> -Eigenschaft|  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Xml.XmlNamespaceManager>
- [XML-Dokumente und -Daten](../../../../docs/standard/data/xml/index.md)
