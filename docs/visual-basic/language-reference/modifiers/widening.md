---
title: Widening (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.widening
helpviewer_keywords:
- conversions [Visual Basic], type
- type conversion [Visual Basic]
- conversions [Visual Basic], data type
- Widening keyword [Visual Basic]
- data type conversion [Visual Basic]
ms.assetid: 646ae263-94d3-40a2-b0cc-64f619292f56
ms.openlocfilehash: 3b9d1ec15c6c2000fb0842abe25848f853cdf986
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54703707"
---
# <a name="widening-visual-basic"></a>Widening (Visual Basic)
Gibt an, dass ein Konvertierungsoperator (`CType`) konvertiert Sie eine Klasse oder Struktur in einen Typ, der alle möglichen Werte der ursprünglichen Klasse oder Struktur enthalten kann.  
  
## <a name="converting-with-the-widening-keyword"></a>Konvertierung mit dem Widening-Schlüsselwort  
 Konvertierungsprozedur muss angegeben werden `Public Shared` zusätzlich zu `Widening`.  
  
 Erweiternde Konvertierungen immer erfolgreich, zur Laufzeit und verursachen keine Daten verloren gehen. Beispiele sind `Single` zu `Double`, `Char` zu `String`, und einen abgeleiteten Typ in den Basistyp. Die letzte Konvertierung ist erweiternde, weil der abgeleitete Typ alle Member des Basistyps enthält und daher eine Instanz des Basistyps.  
  
 Der konsumierenden Code keine Verwendung `CType` für erweiternde Konvertierungen, auch wenn `Option Strict` ist `On`.  
  
 Die `Widening` -Schlüsselwort kann in diesem Kontext verwendet werden:  
  
 [Operator-Anweisung](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 Definitionen von erweiternde und eingrenzende Konvertierungsoperatoren, z. B. finden Sie unter [Vorgehensweise: Definieren eines Konvertierungsoperators](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md).  
  
## <a name="see-also"></a>Siehe auch
- [Operator-Anweisung](../../../visual-basic/language-reference/statements/operator-statement.md)
- [Narrowing](../../../visual-basic/language-reference/modifiers/narrowing.md)
- [Erweiternde und eingrenzende Konvertierungen](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [Vorgehensweise: Definieren eines Operators](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [CType-Funktion](../../../visual-basic/language-reference/functions/ctype-function.md)
- [Option Strict-Anweisung](../../../visual-basic/language-reference/statements/option-strict-statement.md)
- [Vorgehensweise: Definieren eines Konvertierungsoperators](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
