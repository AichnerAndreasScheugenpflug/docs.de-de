---
title: Optionale Parameter (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- parameters [Visual Basic], optional
- Visual Basic code, procedures
- procedures [Visual Basic], optional arguments
- optional arguments
- named arguments [Visual Basic], and optional arguments
- optional parameters
- Optional keyword [Visual Basic], optional arguments
- arguments [Visual Basic], optional
- optional arguments [Visual Basic], and named arguments
ms.assetid: 398d2845-1069-4e94-b934-a73b545c8b87
ms.openlocfilehash: 0f7f7910b5e19c3e1a22598c1a987aa2b02e256e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54552228"
---
# <a name="optional-parameters-visual-basic"></a>Optionale Parameter (Visual Basic)
Sie können angeben, dass ein Prozedurparameter optional ist und in Aufrufen der Prozedur kein Argument dafür bereitgestellt werden muss. *Optionale Parameter* sind gekennzeichnet durch die `Optional` Schlüsselwort in der Prozedurdefinition. Dabei gelten folgende Regeln:  
  
-   Für jeden optionalen Parameter in der Prozedurdefinition muss ein Standardwert angegeben werden.  
  
-   Der Standardwert für einen optionalen Parameter muss ein konstanter Ausdruck sein.  
  
-   Jeder Parameter, der in der Prozedurdefinition auf einen optionalen Parameter folgt, muss ebenfalls optional sein.  
  
 Die folgende Syntax zeigt eine Prozedurdeklaration mit einem optionalen Parameter:  
  
```vb  
Sub name(ByVal parameter1 As datatype1, Optional ByVal parameter2 As datatype2 = defaultvalue)  
```  
  
## <a name="calling-procedures-with-optional-parameters"></a>Aufrufprozeduren mit optionalen Parametern  
 Wenn eine Prozedur mit einem optionalen Parameter aufgerufen wird, können Sie entscheiden, ob das Argument bereitgestellt werden soll. Wird das Argument nicht bereitgestellt, verwendet die Prozedur den für diesen Parameter deklarierten Standardwert.  
  
 Wenn Sie in der Argumentliste eines oder mehrere optionale Argumente auslassen, werden deren Positionen durch aufeinanderfolgende Kommas markiert. Im folgenden Beispielaufruf werden das erste und das vierte Argument bereitgestellt, das zweite und dritte jedoch nicht:  
  
```vb  
Sub name(argument 1, , , argument 4)  
```  
  
 Im folgenden Beispiel wird die `MsgBox`-Funktion mehrmals aufgerufen. `MsgBox` besitzt einen erforderlichen Parameter und zwei optionale Parameter.  
  
 Beim ersten Aufruf von `MsgBox` werden alle drei Argumente in der Reihenfolge angegeben, in der sie von `MsgBox` definiert werden. Beim zweiten Aufruf wird nur das erforderliche Argument angegeben. Beim dritten und vierten Aufruf werden das erste und dritte Argument angegeben. Im dritten Aufruf geschieht dies über die Position, im vierten Aufruf über den Namen.  
  
 [!code-vb[VbVbcnProcedures#47](./codesnippet/VisualBasic/optional-parameters_1.vb)]  
  
## <a name="determining-whether-an-optional-argument-is-present"></a>Bestimmen, ob ein optionales Argument vorhanden ist  
 Prozeduren können zur Laufzeit nicht feststellen, ob ein bestimmtes Argument ausgelassen oder der Standardwert durch den Aufrufcode explizit bereitgestellt wurde. Wenn diese Unterscheidung wichtig ist, sollten Sie einen unwahrscheinlichen Standardwert festlegen. Die folgende Prozedur definiert den optionalen Parameter `office`, und dessen Standardwert `QJZ`, um festzustellen, ob er im Aufruf ausgelassen wurde:  
  
 [!code-vb[VbVbcnProcedures#46](./codesnippet/VisualBasic/optional-parameters_2.vb)]  
  
 Wenn es sich beim optionalen Parameter um einen Verweistyp wie `String` handelt, kann `Nothing` als Standardwert verwendet werden, sofern dieser kein zu erwartender Wert für das Argument ist.  
  
## <a name="optional-parameters-and-overloading"></a>Optionale Parameter und Überladen  
 Eine weitere Möglichkeit, eine Prozedur mit optionalen Parametern zu definieren, ist das Überladen. Wenn ein optionaler Parameter vorhanden ist, können Sie zwei überladene Versionen der Prozedur definieren, eine mit und eine ohne Parameter. Mit steigender Anzahl an optionalen Parametern wird dieses Konzept jedoch komplizierter. Allerdings hat es den Vorteil, dass Sie immer genau wissen, ob das aufrufende Programm jedes optionale Argument bereitgestellt hat.  
  
## <a name="see-also"></a>Siehe auch
- [Verfahren](./index.md)
- [Parameter und Argumente von Prozeduren](./procedure-parameters-and-arguments.md)
- [Übergeben von Argumenten als Wert und als Verweis](./passing-arguments-by-value-and-by-reference.md)
- [Übergeben von Argumenten nach Position und Name](./passing-arguments-by-position-and-by-name.md)
- [Parameterarrays](./parameter-arrays.md)
- [Prozedurüberladung](./procedure-overloading.md)
- [Optional](../../../../visual-basic/language-reference/modifiers/optional.md)
- [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md)
