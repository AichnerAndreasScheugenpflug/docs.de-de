---
title: Transaktionsausnahmen
ms.date: 03/30/2017
ms.assetid: 1d27ed51-7eda-477f-9eca-94fa129f3e07
ms.openlocfilehash: 85d8d043a5610743d6cbad4d950330ed4bedb502
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33474830"
---
# <a name="transaction-exceptions"></a>Transaktionsausnahmen
Dieses Thema enthält alle Ausnahmen, die von Windows Communication Foundation (WCF) Transaktion generiert.  
  
## <a name="exception-list"></a>Ausnahmeliste  
  
|Ressourcencode|Ressourcenzeichenfolge|  
|-------------------|---------------------|  
|SFxCannotHaveDifferentTransactionProtocolsInOneBinding|Die Richtlinieninformationen, die von Metadaten importiert werden, geben andere Werte für TransactionProtocol unter den Vorgängen an. Nur ein einziges TransactionProtocol für jeden Endpunkt wird unterstützt.|  
|SFxTransactionAutoCompleteFalseAndInstanceContextMode|TransactionAutoComplete kann den Wert "false" nicht annehmen, es sei denn, der InstanceContextMode des Diensts ist PerSession. Bei der Implementierung des festgelegten Vertrags und Vorgangs wurde ein Fehler gefunden.|  
|SFxTransactionInvalidSetTransactionComplete|OperationContext.SetTransactionComplete kann nur in einem Vorgang aufgerufen werden, wenn TransactionAutoComplete auf "false" und TransactionScopeRequired auf "true" stehen. Dies ist ein ungültiges Szenario, und die aktuelle Transaktion wurde beendet.|  
|TransactionFlowRequiredIssuedTokens|Um eine Transaktion auszuführen, muss das Ausführen von ausgestellten Token unterstützt werden.|  
|TrustDriverVersionDoesNotSupportIssuedTokens|Die konfigurierte Trust-Version unterstützt keine ausgestellten Token. Verwenden Sie WSTrustFeb2005 oder höher.|
