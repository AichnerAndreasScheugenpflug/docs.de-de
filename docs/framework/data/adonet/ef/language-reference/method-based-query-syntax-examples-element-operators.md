---
title: 'Beispiele für die methodenbasierte Abfragesyntax: Elementoperatoren'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8438b995-bd07-4223-b22d-13adadef33fb
ms.openlocfilehash: 89cbda4d049b30ee50accf94d5b7ec172bc25ae2
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/07/2019
ms.locfileid: "55826498"
---
# <a name="method-based-query-syntax-examples-element-operators"></a>Beispiele für die methodenbasierte Abfragesyntax: Elementoperatoren
In diesem Thema wird gezeigt, wie mit der <xref:System.Linq.Enumerable.First%2A> -Methode und die [AdventureWorks Sales-Modell](https://archive.codeplex.com/?p=msftdbprodsamples) mit der methodenbasierten Abfragesyntax. Für das in den Beispielen verwendete "AdventureWorks Sales"-Modell wurde auf die Tabellen Contact, Address, Product, SalesOrderHeader und SalesOrderDetail der "AdventureWorks"-Beispieldatenbank zurückgegriffen.  
  
 Das Beispiel in diesem Thema verwendet die folgenden `using` / `Imports` Anweisungen:  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="first"></a>First  
  
### <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die <xref:System.Linq.Enumerable.First%2A> Methode, um die erste e-Mail-Adresse, die beginnt mit "Caroline" ermitteln.  
  
 [!code-csharp[DP L2E Examples#FirstCondition_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#firstcondition_mq)]
 [!code-vb[DP L2E Examples#FirstCondition_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#firstcondition_mq)]  
  
## <a name="see-also"></a>Siehe auch
- [Abfragen in LINQ to Entities](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
