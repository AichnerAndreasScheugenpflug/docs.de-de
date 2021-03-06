---
title: Gelockerte Delegatenkonvertierung (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- relaxed delegate conversion [Visual Basic]
- delegates [Visual Basic], relaxed conversion
- conversions [Visual Basic], relaxed delegate
ms.assetid: 64f371d0-5416-4f65-b23b-adcbf556e81c
ms.openlocfilehash: e2838b6473b8c00927073a530b4b49870fcfa9c6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54600379"
---
# <a name="relaxed-delegate-conversion-visual-basic"></a>Gelockerte Delegatenkonvertierung (Visual Basic)
Gelockerte delegatenkonvertierung können Sie Subs und Funktionen Delegaten oder Handlern zugewiesen werden, auch wenn deren Signaturen nicht identisch sind. Aus diesem Grund ist die Bindung an Delegaten konsistent mit der Bindung, die bereits für Methodenaufrufe zulässig.  
  
## <a name="parameters-and-return-type"></a>Parameter und Rückgabetyp  
 Anstelle der Signatur der genaue Übereinstimmung, gelockerte Konvertierung erfordert, dass die folgenden Bedingungen erfüllt sein, wenn `Option Strict` nastaven NA hodnotu `On`:  
  
-   Eine erweiternde Konvertierung muss vorhanden sein, über den Datentyp jedes einzelnen Delegatparameters in den Datentyp des entsprechenden Parameters der Funktion zugewiesen oder `Sub`. Im folgenden Beispiel ist der Delegat `Del1` verfügt über einen Parameter einer `Integer`. Parameter `m` Ausdrücke müssen in der zugewiesenen Lambda-Ausdruck einen Datentyp, der für das eine erweiternde Konvertierung vorhanden ist `Integer`, z. B. `Long` oder `Double`.  
  
     [!code-vb[VbVbalrRelaxedDelegates#1](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_1.vb)]  
  
     [!code-vb[VbVbalrRelaxedDelegates#2](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_2.vb)]  
  
     Einschränkende Konvertierungen sind zulässig, nur, wenn `Option Strict` nastaven NA hodnotu `Off`.  
  
     [!code-vb[VbVbalrRelaxedDelegates#8](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_3.vb)]  
  
-   Eine erweiternde Konvertierung muss vorhanden sein, in die entgegengesetzte Richtung aus dem Rückgabetyp der Funktion zugewiesen oder `Sub` in den Rückgabetyp des Delegaten. In den folgenden Beispielen muss der Text der einzelnen zugewiesenen Lambda-Ausdrücke ausgewertet werden in einen Datentyp, der auf erweitert wird `Integer` , da der Rückgabetyp der `del1` ist `Integer`.  
  
     [!code-vb[VbVbalrRelaxedDelegates#3](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_4.vb)]  
  
 Wenn `Option Strict` nastaven NA hodnotu `Off`, wird die Einschränkung erweiternde in beide Richtungen entfernt wird.  
  
 [!code-vb[VbVbalrRelaxedDelegates#4](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_5.vb)]  
  
## <a name="omitting-parameter-specifications"></a>Parameterangaben auslassen  
 Lockere Delegaten ermöglichen außerdem vollständig Parameterangaben in der zugewiesenen Methode weglassen:  
  
 [!code-vb[VbVbalrRelaxedDelegates#5](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_6.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#6](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_7.vb)]  
  
 Beachten Sie, dass Sie nicht einige Parameter angeben und anderen weglassen.  
  
 [!code-vb[VbVbalrRelaxedDelegates#15](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_8.vb)]  
  
 Die Möglichkeit, Parameter auslassen, empfiehlt sich in einer Situation wie die Definition eines ereignishandlers, in denen mehrere komplexe Parameter beteiligt sind. Die Argumente für einige Ereignishandler werden nicht verwendet. Stattdessen greift der Handler direkt über den Zustand des Steuerelements auf dem das Ereignis registriert ist, und die Argumente ignoriert. Lockere Delegaten können Sie die Argumente in der diese Deklarationen, wenn keine Mehrdeutigkeiten auftreten zu lassen. Im folgenden Beispiel, die vollständig angegebene Methode `OnClick` kann wie folgt umgeschrieben werden `RelaxedOnClick`.  
  
```vb  
Sub OnClick(ByVal sender As Object, ByVal e As EventArgs) Handles b.Click  
    MessageBox.Show("Hello World from" + b.Text)  
End Sub  
  
Sub RelaxedOnClick() Handles b.Click  
    MessageBox.Show("Hello World from" + b.Text)  
End Sub  
```  
  
## <a name="addressof-examples"></a>AddressOf-Beispiele  
 Lambda-Ausdrücke werden in den vorherigen Beispielen verwendet, um die typbeziehungen vereinfachen finden Sie unter. Die lockerungen für die gleiche dürfen jedoch auf Zuweisungen von Delegaten, mit denen `AddressOf`, `Handles`, oder `AddHandler`.  
  
 Im folgenden Beispiel zu Funktionen `f1`, `f2`, `f3`, und `f4` können alle zugewiesen werden `Del1`.  
  
 [!code-vb[VbVbalrRelaxedDelegates#1](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_1.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#7](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_9.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#9](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_10.vb)]  
  
 Das folgende Beispiel ist nur gültig, wenn `Option Strict` nastaven NA hodnotu `Off`.  
  
 [!code-vb[VbVbalrRelaxedDelegates#14](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_11.vb)]  
  
## <a name="dropping-function-returns"></a>Löschen die Funktion zurück  
 Gelockerte delegatenkonvertierung können Sie eine Funktion zum Zuweisen einer `Sub` Delegaten effektiv ignoriert den Rückgabewert der Funktion. Allerdings kann nicht zugewiesen werden eine `Sub` auf eine zu delegierende Funktion. Im folgenden Beispiel ist die Adresse der Funktion `doubler` zugewiesen `Sub` Delegieren `Del3`.  
  
 [!code-vb[VbVbalrRelaxedDelegates#10](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_12.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#11](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_13.vb)]  
  
## <a name="see-also"></a>Siehe auch
- [Lambda-Ausdrücke](../../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [Erweiternde und eingrenzende Konvertierungen](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [Delegaten](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [Vorgehensweise: Übergeben von Prozeduren an eine andere Prozedur in Visual Basic](../../../../visual-basic/programming-guide/language-features/delegates/how-to-pass-procedures-to-another-procedure.md)
- [Lokaler Typrückschluss](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [Option Strict-Anweisung](../../../../visual-basic/language-reference/statements/option-strict-statement.md)
