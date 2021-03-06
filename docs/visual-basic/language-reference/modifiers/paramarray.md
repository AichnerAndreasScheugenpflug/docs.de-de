---
title: ParamArray (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ParamArray
- ParamArray
helpviewer_keywords:
- ParamArray keyword [Visual Basic]
- ParamArray keyword [Visual Basic], syntax
ms.assetid: a5f18789-92bd-488f-9c7e-cf3719963635
ms.openlocfilehash: 16a69e547d14c619d427aa8860e9bf4002b6db04
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54703600"
---
# <a name="paramarray-visual-basic"></a>ParamArray (Visual Basic)
Gibt an, dass ein Prozedurparameter ein optionales Array von Elementen des angegebenen Typs akzeptiert. `ParamArray` kann nur auf einer Parameterliste der letzte Parameter verwendet werden.  
  
## <a name="remarks"></a>Hinweise  
 `ParamArray` können Sie eine beliebige Anzahl von Argumenten an die Prozedur übergeben. Ein `ParamArray` Parameter wird immer mit deklariert [ByVal](../../../visual-basic/language-reference/modifiers/byval.md).  
  
 Sie können angeben, dass eine oder mehrere Argumente für eine `ParamArray` durch Übergeben eines Arrays des entsprechenden Typparameter, eine durch Trennzeichen getrennte Liste von Werten oder "nothing" überhaupt. Weitere Informationen finden Sie unter "ParamArray aufrufen" in [Parameterarrays](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md).  
  
> [!IMPORTANT]
>  Wenn Sie mit einem Array, das unendlich groß sein kann arbeiten, besteht die Gefahr, dass die interne Kapazität der Anwendung überschritten. Wenn Sie ein Parameterarray vom aufrufenden Code akzeptieren, sollten Sie testen ihre Länge und geeignete Maßnahmen ergreifen, wenn sie für Ihre Anwendung zu groß ist.  
  
 Der `ParamArray`-Modifizierer kann in folgenden Kontexten verwendet werden:  
  
 [Declare-Anweisung](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [Function-Anweisung](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Property-Anweisung](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Sub-Anweisung](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a>Siehe auch
- [Schlüsselwörter](../../../visual-basic/language-reference/keywords/index.md)
- [Parameterarrays](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md)
