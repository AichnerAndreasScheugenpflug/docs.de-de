---
title: 'Vorgehensweise: Aufrufen von kanonischen Funktionen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b3d84873-7403-4957-8e20-b4ae39f50214
ms.openlocfilehash: 33abf1a56750d6f13dabe773605ba1474ec75d45
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/07/2019
ms.locfileid: "55827304"
---
# <a name="how-to-call-canonical-functions"></a>Vorgehensweise: Aufrufen von kanonischen Funktionen
Die <xref:System.Data.Objects.EntityFunctions>-Klasse enthält Methoden, mit denen kanonische Funktionen in LINQ to Entities-Abfragen verwendet werden können. Weitere Informationen zur kanonischen Funktionen finden Sie unter [Kanonische Funktionen](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md).  
  
> [!NOTE]
>  Die Methoden <xref:System.Data.Objects.EntityFunctions.AsUnicode%2A> und <xref:System.Data.Objects.EntityFunctions.AsNonUnicode%2A> der <xref:System.Data.Objects.EntityFunctions>-Klasse verfügen über keine kanonischen Funktionsentsprechungen.  
  
 Kanonische Funktionen, die eine Berechnung für einen Satz von Werten ausführen und einen einzelnen Wert (auch bekannt als aggregierte kanonische Funktionen) zurückgeben, können direkt aufgerufen werden. Andere kanonische Funktionen können nur als Teil einer LINQ to Entities-Abfrage aufgerufen werden. Zum direkten Aufrufen einer Aggregatfunktion muss eine <xref:System.Data.Objects.ObjectQuery%601> an die Funktion übergeben werden. Weitere Informationen finden Sie unten im zweiten Beispiel.  
  
 Sie können einige kanonische Funktionen mit Common Language Runtime (CLR)-Methoden in LINQ to Entities-Abfragen aufrufen. Eine Liste der CLR-Methoden, die kanonischen Funktionen zugeordnet, werden soll, finden Sie unter [CLR-Methoden zu kanonischen Funktionszuordnung](../../../../../../docs/framework/data/adonet/ef/language-reference/clr-method-to-canonical-function-mapping.md).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die [AdventureWorks Sales-Modell](https://archive.codeplex.com/?p=msftdbprodsamples). Im Beispiel wird eine die <xref:System.Data.Objects.EntityFunctions.DiffDays%2A>-Methode verwendende LINQ to Entities-Abfrage zum Zurückgeben aller Produkte ausgeführt, für die die Differenz zwischen `SellEndDate` und `SellStartDate` weniger als 365 Tage beträgt:  
  
 [!code-csharp[DP L2E CanonicalAndStoreFunctions#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp l2e canonicalandstorefunctions/cs/program.cs#1)]
 [!code-vb[DP L2E CanonicalAndStoreFunctions#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp l2e canonicalandstorefunctions/vb/module1.vb#1)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die [AdventureWorks Sales-Modell](https://archive.codeplex.com/?p=msftdbprodsamples). Im Beispiel wird die <xref:System.Data.Objects.EntityFunctions.StandardDeviation%2A>-Aggregatmethode aufgerufen, um die Standardabweichung von `SalesOrderHeader`-Teilergebnissen direkt zurückzugeben. Eine <xref:System.Data.Objects.ObjectQuery%601> wird an die Funktion übergeben, durch die sie aufgerufen werden kann, ohne Teil einer LINQ to Entities-Abfrage sein zu müssen.  
  
 [!code-csharp[DP L2E CanonicalAndStoreFunctions#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp l2e canonicalandstorefunctions/cs/program.cs#2)]
 [!code-vb[DP L2E CanonicalAndStoreFunctions#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp l2e canonicalandstorefunctions/vb/module1.vb#2)]  
  
## <a name="see-also"></a>Siehe auch
- [Aufrufen von Funktionen in LINQ to Entities-Abfragen](../../../../../../docs/framework/data/adonet/ef/language-reference/calling-functions-in-linq-to-entities-queries.md)
- [Abfragen in LINQ to Entities](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
