---
title: 'Vorgehensweise: Kombinieren von Delegaten (Multicastdelegaten) – C#-Programmierhandbuch'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- delegates [C#], combining
- multicast delegates [C#]
ms.assetid: 4e689450-6d0c-46de-acfd-f961018ae5dd
ms.openlocfilehash: ebfcba4d2ebebe2697aa01b7109bbf50b8f144e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631554"
---
# <a name="how-to-combine-delegates-multicast-delegatesc-programming-guide"></a>Vorgehensweise: Kombinieren von Delegaten (Multicastdelegaten) (C#-Programmierhandbuch)
Das folgende Beispiel veranschaulicht das Erstellen von Multicastdelegaten. Eine nützliche Eigenschaft von [delegate](../../../csharp/language-reference/keywords/delegate.md)-Objekten besteht darin, dass einer Delegatinstanz mithilfe des Operators `+` mehrere Objekte zugewiesen werden können. Der Multicastdelegat enthält eine Liste der zugewiesenen Delegaten. Wenn der Multicastdelegat aufgerufen wird, ruft er die Delegaten in der Liste nacheinander auf. Es können nur Delegaten desselben Typs kombiniert werden.  
  
 Mithilfe des Operators `-` kann ein Komponentendelegat aus einem Multicastdelegaten entfernt werden.  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[csProgGuideDelegates#11](../../../csharp/programming-guide/delegates/codesnippet/CSharp/how-to-combine-delegates-multicast-delegates_1.cs)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.MulticastDelegate>
- [C#-Programmierhandbuch](../../../csharp/programming-guide/index.md)
- [Ereignisse](../../../csharp/programming-guide/events/index.md)
