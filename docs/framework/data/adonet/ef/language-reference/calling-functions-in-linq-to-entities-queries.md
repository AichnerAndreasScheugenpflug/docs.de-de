---
title: Aufrufen von Funktionen in LINQ to Entities-Abfragen
ms.date: 03/30/2017
ms.assetid: 12a525a9-727c-4464-a0c7-71a0ef541792
ms.openlocfilehash: 012f55113cbea00c95c92712d640313a960ef8ca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54542717"
---
# <a name="calling-functions-in-linq-to-entities-queries"></a>Aufrufen von Funktionen in LINQ to Entities-Abfragen
In den Themen in diesem Abschnitt wird beschrieben, wie Funktionen in LINQ to Entities-Abfragen aufgerufen werden.  
  
 Die <xref:System.Data.Objects.EntityFunctions>-Klasse und die <xref:System.Data.Objects.SqlClient.SqlFunctions>-Klasse bieten im Rahmen des Entity Framework Zugriff auf kanonische Funktionen und Datenbankfunktionen. Weitere Informationen finden Sie unter [Vorgehensweise: Aufrufen von kanonischen Funktionen](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-canonical-functions.md) und [Vorgehensweise: Aufrufen von Datenbankfunktionen](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-database-functions.md).  
  
 Zum Aufrufen einer benutzerdefinierten Funktion sind drei grundlegende Schritte erforderlich:  
  
1.  Definieren Sie im konzeptionellen Modell eine Funktion, oder deklarieren Sie im Speichermodell eine Funktion.  
  
2.  Fügen Sie der Anwendung eine Methode hinzu, und ordnen Sie es mit einem <xref:System.Data.Objects.DataClasses.EdmFunctionAttribute> der Funktion im Modell zu.  
  
3.  Rufen Sie die Funktion in einer LINQ to Entities-Abfrage auf.  
  
 Weitere Informationen hierzu finden Sie in diesem Abschnitt.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Vorgehensweise: Aufrufen von kanonischen Funktionen](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-canonical-functions.md)  
  
 [Vorgehensweise: Aufrufen von Datenbankfunktionen](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-database-functions.md)  
  
 [Vorgehensweise: Rufen benutzerdefinierter Datenbankfunktionen auf](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-custom-database-functions.md)  
  
 [Vorgehensweise: Rufen Sie Modelldefinierter Funktionen in Abfragen auf](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-model-defined-functions-in-queries.md)  
  
 [Vorgehensweise: Rufen Sie Modelldefinierter Funktionen als Objektmethoden auf](../../../../../../docs/framework/data/adonet/ef/language-reference/how-to-call-model-defined-functions-as-object-methods.md)  
  
## <a name="see-also"></a>Siehe auch
- [Abfragen in LINQ to Entities](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
- [Canonical Functions (Kanonische Funktionen)](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
- [Übersicht über die EDMX-Datei](https://msdn.microsoft.com/library/f4c8e7ce-1db6-417e-9759-15f8b55155d4)
- [Vorgehensweise: Definieren von benutzerdefinierten Funktionen im konzeptionellen Modell](https://msdn.microsoft.com/library/0dad7b8b-58f6-4271-b238-f34810d68e5f)
