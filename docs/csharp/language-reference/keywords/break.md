---
title: break-Anweisung – C#-Referenz
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- break
- break_CSharpKeyword
helpviewer_keywords:
- break keyword [C#]
ms.assetid: be2571ed-efb0-4965-b122-81e5b09db0b9
ms.openlocfilehash: 18be5171329dd43c419e977a1799e2e72c32404d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54727572"
---
# <a name="break-c-reference"></a>break (C#-Referenz)

Die `break`-Anweisung beendet die Ausführung der nächsten einschließenden Schleife oder [switch](../../../csharp/language-reference/keywords/switch.md)-Anweisung, in der sie angezeigt wird. Das Steuerelement wird an die Anweisung übergeben, die auf die beendete Anweisung folgt, falls vorhanden.

## <a name="example"></a>Beispiel

In diesem Beispiel enthält die Bedingungsanweisung einen Indikator, der normalerweise zum Zählen von 1 bis 100 verwendet wird. Allerdings beendet die `break`-Anweisung die Schleife nach 4 Durchgängen.

[!code-csharp[csrefKeywordsJump#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#1)]

## <a name="example"></a>Beispiel

In diesem Beispiel wird die `break`-Anweisung verwendet, um aus einer inneren geschachtelten Schleife auszubrechen und die Steuerung an die äußere Schleife zurückzugeben.

[!code-csharp[csrefKeywordsJump#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#7)]

## <a name="example"></a>Beispiel

In diesem Beispiel wird die Verwendung von `break` in einer [switch](../../../csharp/language-reference/keywords/switch.md)-Anweisung veranschaulicht.

[!code-csharp[csrefKeywordsJump#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#2)]

Bei Eingabe von `4` sähe die Ausgabe wie folgt aus:

```console
Enter your selection (1, 2, or 3): 4
Sorry, invalid selection.
```

## <a name="c-language-specification"></a>C#-Sprachspezifikation

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Siehe auch

- [C#-Referenz](../../../csharp/language-reference/index.md)
- [C#-Programmierhandbuch](../../../csharp/programming-guide/index.md)
- [C#-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)
- [switch](../../../csharp/language-reference/keywords/switch.md)
- [Sprunganweisungen](../../../csharp/language-reference/keywords/jump-statements.md)
- [Iterationsanweisungen](../../../csharp/language-reference/keywords/iteration-statements.md)
