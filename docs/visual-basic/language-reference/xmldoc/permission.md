---
title: '&lt;Berechtigung&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <permission> XML tag
- permission XML tag
ms.assetid: 0edf0500-5cd7-49c0-9255-64c48f972b77
ms.openlocfilehash: 56b25955cf36598909176170235623b27da20867
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54573191"
---
# <a name="ltpermissiongt-visual-basic"></a>&lt;Berechtigung&gt; (Visual Basic)
Gibt eine erforderliche Berechtigung für das Element an.  
  
## <a name="syntax"></a>Syntax  
  
```xml  
<permission cref="member">description</permission>  
```  
  
#### <a name="parameters"></a>Parameter  
 `member`  
 Ein Verweis auf einen Member oder ein Feld, das von der aktuellen Kompilierungsumgebung aufgerufen werden kann. Der Compiler prüft, ob das angegebene Codeelement vorhanden ist, und übersetzt in der Ausgabe-XML `member` in den kanonischen Elementnamen. Schließen Sie `member` in Anführungszeichen ("").  
  
 `description`  
 Eine Beschreibung des Zugriffs auf den Member  
  
## <a name="remarks"></a>Hinweise  
 Verwenden der `<permission>` Tag, um den Zugriff auf einen Member dokumentieren. Verwenden der <xref:System.Security.PermissionSet> Klasse, um den Zugriff auf ein Element anzugeben.  
  
 Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) kompiliert werden.  
  
## <a name="example"></a>Beispiel  
 Dieses Beispiel verwendet die `<permission>` Tag beschrieben, dass die <xref:System.Security.Permissions.FileIOPermission> erforderlich ist der `ReadFile` Methode.  
  
 [!code-vb[VbVbcnXmlDocComments#7](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/permission_1.vb)]  
  
## <a name="see-also"></a>Siehe auch
- [XML-Kommentartags](../../../visual-basic/language-reference/xmldoc/index.md)
