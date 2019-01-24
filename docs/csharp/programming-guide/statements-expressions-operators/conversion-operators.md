---
title: Konvertierungsoperatoren – C#-Programmierhandbuch
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, conversion operators
- conversion operators [C#]
- operators [C#], conversion
- user-defined conversions [C#]
ms.assetid: c5ad73a3-d57b-4d2b-b4c9-24e3c2856efc
ms.openlocfilehash: 927640b63773d24be93cc90427668f9568a39652
ms.sourcegitcommit: 542aa405b295955eb055765f33723cb8b588d0d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "54362729"
---
# <a name="conversion-operators-c-programming-guide"></a>Konvertierungsoperatoren (C#-Programmierhandbuch)

Mit C# können Programmierer Konvertierungen für Klassen oder Strukturen deklarieren, damit Klassen oder Strukturen in andere Klassen und Strukturen und Basistypen oder aus diesen konvertiert werden können. Konvertierungen werden wie Operatoren definiert und nach dem Typ benannt, in den Sie konvertiert werden. Entweder muss der Typ des zu konvertierenden Arguments oder der Typ des Konvertierungsergebnisses, aber nicht beide, der enthaltende Typ sein.  
  
 [!code-csharp[csProgGuideStatements#10](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/conversion-operators_1.cs)]  
  
## <a name="conversion-operators-overview"></a>Überblick über Konvertierungsoperatoren

 Konvertierungsoperatoren verfügen über folgende Eigenschaften:  
  
-   Konvertierungen, die als `implicit` deklariert wurden, werden bei Bedarf automatisch durchgeführt.  
  
-   Konvertierungen, die als `explicit` deklariert wurden, erfordern zum Aufruf eine Umwandlung.  
  
-   Alle Konvertierungen müssen als `static` deklariert werden.  
  
## <a name="related-sections"></a>Verwandte Abschnitte

 Weitere Informationen finden Sie unter:   
  
-   [Verwenden von Konvertierungsoperatoren](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md)  
  
-   [Umwandlung und Typkonvertierungen](../../../csharp/programming-guide/types/casting-and-type-conversions.md)  
  
-   [Vorgehensweise: Implementieren von benutzerdefinierten Konvertierungen zwischen Strukturen](../../../csharp/programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)  
  
-   [explicit](../../../csharp/language-reference/keywords/explicit.md)  
  
-   [implicit](../../../csharp/language-reference/keywords/implicit.md)  
  
-   [static](../../../csharp/language-reference/keywords/static.md)  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Convert>  
- [C#-Programmierhandbuch](../../../csharp/programming-guide/index.md)  
- [Chained user-defined explicit conversions in C# (Verkettete benutzerdefinierte, explizite Konvertierungen in C#)](https://blogs.msdn.microsoft.com/ericlippert/2007/04/16/chained-user-defined-explicit-conversions-in-c/)
