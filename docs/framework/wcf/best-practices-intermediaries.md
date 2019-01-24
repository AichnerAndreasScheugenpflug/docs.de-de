---
title: 'Bewährte Methoden: Vermittler'
ms.date: 03/30/2017
ms.assetid: 2d41b337-8132-4ac2-bea2-6e9ae2f00f8d
ms.openlocfilehash: 8a95bd555e6c1acf896daa77e93d7c735d1f091c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663621"
---
# <a name="best-practices-intermediaries"></a>Bewährte Methoden: Vermittler
Beim Aufrufen von Vermittlern müssen Fehler ordnungsgemäß behandelt werden, um sicherzustellen, dass dienstseitige Kanäle im Vermittler ordnungsgemäß geschlossen werden.  
  
 Betrachten Sie folgendes Szenario. Ein Client ruft einen Vermittler auf, der dann einen Back-End-Dienst aufruft.  Der Back-End-Dienst definiert keinen Fehlervertrag. Deshalb wird jeder von diesem Dienst ausgelöste Fehler als nicht typisierter Fehler behandelt.  Der Back-End-Dienst löst eine <xref:System.ApplicationException> aus und bricht den dienstseitigen Kanal ordnungsgemäß von WCF ab. Die <xref:System.ApplicationException> wird dann als <xref:System.ServiceModel.FaultException> für den Vermittler ausgelöste Ausnahme ausgegeben. Der Vermittler löst die <xref:System.ApplicationException> erneut aus. WCF interpretiert diese als nicht typisierten Fehler vom Vermittler und leitet den Fehler an den Client weiter. Bei Empfang des Fehlers lösen der Vermittler und der Client Fehler für ihre clientseitigen Kanäle aus. Der dienstseitige Kanal des Vermittlers bleibt jedoch geöffnet, da WCF nicht weiß, ob es sich um einen schwerwiegenden Fehler handelt.  
  
 Für dieses Szenario wird empfohlen, zu bestimmen, ob der vom Dienst stammende Fehler schwerwiegend ist, und wenn er schwerwiegend ist, sollte der Vermittler einen Fehler für seinen dienstseitigen Kanal auslösen, wie im folgenden Codeausschnitt gezeigt.  
  
```csharp  
catch (Exception e)  
{  
    bool faulted = service.State == CommunicationState.Faulted;  
    service.Abort();  
    if (faulted)  
    {  
        throw new ApplicationException(e.Message);  
    }  
    else  
    {  
        throw;  
    }  
}  
```  
  
## <a name="see-also"></a>Siehe auch
- [WCF-Fehlerbehandlung](../../../docs/framework/wcf/wcf-error-handling.md)
- [Angeben und Behandeln von Fehlern in Verträgen und Diensten](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
