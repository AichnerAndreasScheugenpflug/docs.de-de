---
title: Ausdrücke in LINQ to Entities-Abfragen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d70b502f-6a15-4120-b4fe-500b173ad9cc
ms.openlocfilehash: f449e7d5626d4a8c9709ae2cb4c026869d1e2dc9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54661775"
---
# <a name="expressions-in-linq-to-entities-queries"></a>Ausdrücke in LINQ to Entities-Abfragen
Ein Ausdruck ist ein Codefragment, das als einzelner Wert, einzelnes Objekt, einzelne Methode oder einzelner Namespace ausgewertet werden kann. Ausdrücke können einen literalen Wert, einen Methodenaufruf, einen Operator und die entsprechenden Operanden oder einen einfachen Namen enthalten. Einfache Namen können der Name einer Variablen, eines Typmembers, eines Methodenparameters, eines Namespaces oder eines Typs sein. Ausdrücke können Operatoren verwenden, die wiederum andere Ausdrücke als Parameter oder Methodenaufrufe verwenden können, deren Parameter wiederum andere Methodenaufrufe darstellen. Die Bandbreite der möglichen Ausdrücke reicht daher von einfach bis sehr komplex.  
  
 In [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] Abfragen Ausdrücke alles enthalten, zulässigen Typen innerhalb der <xref:System.Linq.Expressions> -Namespace, einschließlich der Lambda-Ausdrücke. Die Ausdrücke, die in [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)]-Abfragen verwendet werden können, umfassen die Ausdrücke, mit denen das [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)] abgefragt werden kann.  Ausdrücke, die Teil einer Abfrage der [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)] sind von unterstützten Vorgänge auf `ObjectQuery<T>` und der zugrunde liegenden Datenquelle.  
  
 Im folgenden Beispiel ist der Vergleich in der `Where`-Klausel ein Ausdruck:  
  
 [!code-csharp[DP L2E Conceptual Examples#WhereExpression](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#whereexpression)]
 [!code-vb[DP L2E Conceptual Examples#WhereExpression](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#whereexpression)]  
  
> [!NOTE]
>  Bestimmte Sprachkonstrukte, wie `unchecked` in C#, haben in [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] keine Bedeutung.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Constant Expressions (Konstante Ausdrücke)](../../../../../../docs/framework/data/adonet/ef/language-reference/constant-expressions.md)  
  
 [Vergleichsausdrücke](../../../../../../docs/framework/data/adonet/ef/language-reference/comparison-expressions.md)  
  
 [NULL-Vergleiche](../../../../../../docs/framework/data/adonet/ef/language-reference/null-comparisons.md)  
  
 [Initialisierungsausdrücke](../../../../../../docs/framework/data/adonet/ef/language-reference/initialization-expressions.md)  
  
 [Navigationseigenschaften](https://msdn.microsoft.com/library/41e1e6b9-8a57-467d-99d9-1857d2ca2ea5)  
  
## <a name="see-also"></a>Siehe auch
- [ADO.NET Entity Framework](../../../../../../docs/framework/data/adonet/ef/index.md)
