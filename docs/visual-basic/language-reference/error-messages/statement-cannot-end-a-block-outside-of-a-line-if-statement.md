---
title: Eine Anweisung kann keinen Block außerhalb einer "If"-Zeilenanweisung beenden.
ms.date: 07/20/2015
f1_keywords:
- vbc32005
- bc32005
helpviewer_keywords:
- BC32005
ms.assetid: 4039f51b-e0ee-4789-a89b-45d06de06b5d
ms.openlocfilehash: 0cee52f0ca00395d93c469aae6498fd3793f1085
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266311"
---
# <a name="statement-cannot-end-a-block-outside-of-a-line-if-statement"></a>Eine Anweisung kann keinen Block außerhalb einer "If"-Zeilenanweisung beenden.
Einem einzeiligen `If` -Anweisung enthält mehrere Anweisungen, getrennt durch Doppelpunkte (:), von denen eine `End` -Anweisung für einen Kontrollblock außerhalb der einzeiligen `If`. Einzeilige `If` Anweisungen verwenden Sie nicht die `End If` Anweisung.  
  
 **Fehler-ID:** BC32005  
  
## <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Verschieben der einzeilige `If` Anweisung außerhalb der Kontrollblock mit der `End If` Anweisung.  
  
## <a name="see-also"></a>Siehe auch
- [If...Then...Else-Anweisung](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
