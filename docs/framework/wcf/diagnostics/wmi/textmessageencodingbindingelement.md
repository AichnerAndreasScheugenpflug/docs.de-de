---
title: TextMessageEncodingBindingElement
ms.date: 03/30/2017
ms.assetid: 885e2d7a-3436-4093-bc5f-0a404c62acdc
ms.openlocfilehash: 188a766807cd779ac51df390b1332641584dbb06
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662711"
---
# <a name="textmessageencodingbindingelement"></a>TextMessageEncodingBindingElement
TextMessageEncodingBindingElement  
  
## <a name="syntax"></a>Syntax  
  
```csharp
class TextMessageEncodingBindingElement : MessageEncodingBindingElement  
{  
  string Encoding;  
  sint32 MaxReadPoolSize;  
  sint32 MaxWritePoolSize;  
  XmlDictionaryReaderQuotas ReaderQuotas;  
};  
```  
  
## <a name="methods"></a>Methoden  
 Die TextMessageEncodingBindingElement-Klasse definiert keine Methoden.  
  
## <a name="properties"></a>Eigenschaften  
 Die TextMessageEncodingBindingElement-Klasse verfügt über die folgenden Eigenschaften:  
  
### <a name="encoding"></a>Codierung  
 Datentyp: string (Zeichenfolge)  
  
 Zugriffstyp: Schreibgeschützt  
  
 Die Zeichensatzcodierung, die zum Ausgeben von Nachrichten über die Bindung verwendet werden soll.  
  
### <a name="maxreadpoolsize"></a>MaxReadPoolSize  
 Datentyp: sint32  
  
 Zugriffstyp: Schreibgeschützt  
  
 Eine ganze Zahl, die definiert, wie viele Nachrichten gleichzeitig gelesen werden können, ohne neue Leser zuzuordnen.  
  
### <a name="maxwritepoolsize"></a>MaxWritePoolSize  
 Datentyp: sint32  
  
 Zugriffstyp: Schreibgeschützt  
  
 Eine ganze Zahl, die definiert, wie viele Nachrichten gleichzeitig gesendet werden können, ohne neue Schreiber zuzuordnen.  
  
### <a name="readerquotas"></a>ReaderQuotas  
 Datentyp: XmlDictionaryReaderQuotas  
  
 Zugriffstyp: Schreibgeschützt  
  
 Die Kontingente der Leser.  
  
## <a name="requirements"></a>Anforderungen  
  
|MOF|Deklariert in Servicemodel.mof.|  
|---------|-----------------------------------|  
|Namespace|Definiert in root\ServiceModel|  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.ServiceModel.Channels.TextMessageEncodingBindingElement>
