---
title: 'Vorgehensweise: Erstellen Sie einen Anforderung-Antwort-Vertrag'
ms.date: 03/30/2017
ms.assetid: 801d90da-3d45-4284-9c9f-56c8aadb4060
ms.openlocfilehash: 085514e09eb13676d5c939724071e89535d443f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663608"
---
# <a name="how-to-create-a-request-reply-contract"></a>Vorgehensweise: Erstellen Sie einen Anforderung-Antwort-Vertrag
Ein Anforderung-Antwort-Vertrag gibt eine Methode an, die eine Antwort zurückgibt. Die Antwort muss gesendet und unter den Bedingungen dieses Vertrags mit der Anforderung in Beziehung gesetzt werden. Selbst wenn die Methode keine Antwort (`void` in C# oder `Sub` in Visual Basic) zurückgibt, wird von der Infrastruktur eine leere Nachricht erstellt und gesendet, um dem Aufrufer mitzuteilen, dass die Methode einen Wert zurückgegeben hat. Verwenden Sie einen unidirektionalen Vertrag für die Operation, um das Senden einer leeren Mitteilung zu unterbinden.  
  
### <a name="to-create-a-request-reply-contract"></a>So erstellen Sie einen Anforderung-Antwort-Vertrag  
  
1.  Erstellen Sie in der Programmiersprache Ihrer Wahl eine Schnittstelle.  
  
2.  Fügen Sie das <xref:System.ServiceModel.ServiceContractAttribute>-Attribut der Schnittstelle hinzu.  
  
3.  Fügen Sie das <xref:System.ServiceModel.OperationContractAttribute>-Attribut jeder von Clients aufrufbaren Methode hinzu.  
  
4.  Dies ist optional. Legen Sie den Wert der <xref:System.ServiceModel.OperationContractAttribute.IsOneWay%2A>-Eigenschaft auf `true` fest, um das Senden einer leeren Mitteilung zu verhindern. Standardmäßig sind alle Operationen Anforderung-Antwort-Verträge.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Vertrag für einen Rechnerdienst definiert, der die `Add`-Methode und die `Subtract`-Methode bereitstellt. Die `Multiply`-Methode ist nicht Teil des Vertrags, weil sie von der <xref:System.ServiceModel.OperationContractAttribute>-Klasse nicht gekennzeichnet wurde und somit nicht für Clients verfügbar ist.  
  
```csharp
using System.ServiceModel;

[ServiceContract]
public interface ICalculator
{
    [OperationContract]
    // It would be equivalent to write explicitly:
    // [OperationContract(IsOneWay=false)]
    int Add(int a, int b);
    
    [OperationContract]
    int Subtract(int a, int b);
    
    int Multiply(int a, int b)
}
```
  
-   Weitere Informationen zur Vorgehensweise beim Angeben von vorgangsverträgen finden Sie unter den <xref:System.ServiceModel.OperationContractAttribute> Klasse und die <xref:System.ServiceModel.OperationContractAttribute.IsOneWay%2A> Eigenschaft.  
  
-   Durch Anwenden des <xref:System.ServiceModel.ServiceContractAttribute>-Attributs und des <xref:System.ServiceModel.OperationContractAttribute>-Attributs wird die automatische Generierung von Dienstvertragsdefinitionen in einem WSDL (Web Services Description Language)-Dokument ermöglicht, sobald der Dienst bereitgestellt wird. Das Dokument wird durch Anfügen von `?wsdl` an die HTTP-Basisadresse des Diensts heruntergeladen. Beispiel: `http://microsoft/CalculatorService?wsdl`  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.ServiceModel.OperationContractAttribute>
- [Entwerfen von Dienstverträgen](../../../../docs/framework/wcf/designing-service-contracts.md)
- [Vorgehensweise: Erstellen eines Duplexvertrags](../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md)
