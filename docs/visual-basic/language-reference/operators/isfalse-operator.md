---
title: IsFalse-Operator (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.isfalse
helpviewer_keywords:
- AndAlso operator [Visual Basic]
- IsFalse operator [Visual Basic]
ms.assetid: 37fc9dbf-e5cc-4570-b93f-7213447974df
ms.openlocfilehash: ec8d7bcd2f4ca3fb1c74f4edcf6ec8af78fd144d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54740419"
---
# <a name="isfalse-operator-visual-basic"></a>IsFalse-Operator (Visual Basic)
Bestimmt, ob ein Ausdruck ist `False`.  
  
 Sie können nicht aufrufen `IsFalse` explizit in Ihrem Code, aber die Visual Basic Compiler können sie zum Generieren von Code aus `AndAlso` Klauseln. Wenn Sie eine Klasse oder Struktur definieren und verwenden Sie dann auf eine Variable dieses Typs in eine `AndAlso` -Klausel, müssen Sie definieren `IsFalse` für diese Klasse oder Struktur.  
  
 Der Compiler betrachtet die `IsFalse` und `IsTrue` Operatoren als eine *zueinander passendes Paar*. Dies bedeutet, dass wenn Sie einen dieser definieren, Sie auch die anderen Knoten definieren müssen.  
  
> [!NOTE]
>  Die `IsFalse` Operator möglich *überladen*, was bedeutet, dass eine Klasse oder Struktur sein Verhalten definieren kann, wenn der Operand den Typ der Klasse oder Struktur hat. Wenn Ihr Code dieser Operator für diese eine Klasse oder Struktur verwendet, achten Sie darauf, dass Sie verstehen, dass das neu definierte Verhalten. Weitere Informationen finden Sie unter [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Beispiel  
 Das folgende Codebeispiel definiert die Gliederung einer Struktur, die Definitionen für enthält die `IsFalse` und `IsTrue` Operatoren.  
  
 [!code-vb[VbVbalrOperators#28](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/isfalse-operator_1.vb)]  
  
## <a name="see-also"></a>Siehe auch
- [IsTrue-Operator](../../../visual-basic/language-reference/operators/istrue-operator.md)
- [Vorgehensweise: Definieren eines Operators](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [AndAlso-Operator](../../../visual-basic/language-reference/operators/andalso-operator.md)
