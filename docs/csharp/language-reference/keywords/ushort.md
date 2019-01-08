---
title: ushort-Schlüsselwort – C#-Referenz
ms.custom: seodec18
ms.date: 03/14/2017
f1_keywords:
- ushort
- ushort_CSharpKeyword
helpviewer_keywords:
- ushort keyword [C#]
ms.assetid: 1a7dbaae-b7a0-4111-872a-c88a6d3981ac
ms.openlocfilehash: 934e25576a8a24c176a54ec6af984459b513fe5a
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2018
ms.locfileid: "53614457"
---
# <a name="ushort-c-reference"></a>ushort (C#-Referenz)

Das Schlüsselwort `ushort` kennzeichnet einen ganzzahligen Datentyp, der Werte anhand der Größe und des Bereichs speichert, die in der folgenden Tabelle gezeigt werden.

|Typ|Bereich|Größe|.NET-Typ|
|----------|-----------|----------|-------------------------|
|`ushort`|0 bis 65.535|16-Bit-Ganzzahl ohne Vorzeichen|<xref:System.UInt16?displayProperty=nameWithType>|

## <a name="literals"></a>Literale

Sie können eine `ushort`-Variable deklarieren und initialisieren, indem Sie ihr ein Dezimalliteral, ein hexadezimales Literal oder (ab C# 7.0) ein binäres Literal zuweisen. Wenn sich das Ganzzahlliteral außerhalb des Bereichs von `ushort` befindet (sprich, wenn es kleiner als <xref:System.UInt16.MinValue?displayProperty=nameWithType> oder größer als <xref:System.UInt16.MaxValue?displayProperty=nameWithType> ist) tritt ein Kompilierfehler auf.

Im folgenden Beispiel werden Ganzzahlen wie 65.034, die als dezimale, hexadezimale und binäre Literale dargestellt werden, implizit aus [int](int.md) in `ushort`-Werte konvertiert.

[!code-csharp[UShort](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UShort)]

> [!NOTE]
> Verwenden Sie das Präfix `0x` oder `0X` zum Kennzeichnen eines hexadezimalen Literals und das Präfix `0b` oder `0B` zum Kennzeichnen eines binären Literals. Dezimale Literale haben kein Präfix.

Mit C# 7.0 wurde eine Reihe von Features zur Verbesserung der Lesbarkeit hinzugefügt:

- C# 7.0 lässt die Verwendung des Unterstrichs (`_`) als Zifferntrennzeichen zu.
- C# 7.2 lässt die Verwendung von `_` als Zifferntrennzeichen nach dem Präfix für ein binäres oder hexadezimales Literal zu. Dezimalliterale dürfen keinen vorangestellten Unterstrich aufweisen.

Im Folgenden werden einige Beispiele veranschaulicht.

[!code-csharp[UShort](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UShortS)]

## <a name="compiler-overload-resolution"></a>Überladungsauflösung des Compiler

Beim Aufrufen überladener Methoden muss eine Typumwandlung durchgeführt werden. Betrachten Sie z.B. die folgenden überladenen Methoden, die die Parameter `ushort` und [int](int.md) verwenden:

```csharp
public static void SampleMethod(int i) {}
public static void SampleMethod(ushort s) {}
```

Die Verwendung der `ushort`-Umwandlung gewährleistet, dass der richtige Typ aufgerufen wird, wie z.B.:

```csharp
// Calls the method with the int parameter:
SampleMethod(5);
// Calls the method with the ushort parameter:
SampleMethod((ushort)5);
```

## <a name="conversions"></a>Konvertierungen

Es gibt eine vordefinierte implizite Konvertierung von `ushort` in [int](int.md), [uint](uint.md) [long](long.md), [ulong](ulong.md), [float](float.md), [double](double.md) oder [decimal](decimal.md).

Es gibt eine vordefinierte implizite Konvertierung von [byte](byte.md) oder [char](char.md) in `ushort`. Andernfalls muss eine Umwandlung verwendet werden, um eine explizite Konvertierung durchzuführen. Betrachten Sie z.B. die folgenden beiden `ushort`-Variablen `x` und `y`:

```csharp
ushort x = 5, y = 12;
```

Die folgende Zuweisungsanweisung erzeugt einen Kompilierfehler, da der arithmetische Ausdruck auf der rechten Seite des Zuweisungsoperators standardmäßig `int` ergibt.

```csharp
ushort z = x + y;   // Error: conversion from int to ushort
```

Verwenden Sie eine Umwandlung, um dieses Problem zu lösen:

```csharp
ushort z = (ushort)(x + y);   // OK: explicit conversion
```

Es ist jedoch möglich, die folgenden Anweisungen zu verwenden, bei denen die Zielvariable über dieselbe oder eine größere Speichergröße verfügt:

```csharp
int m = x + y;
long n = x + y;
```

Beachten Sie auch, dass es keine implizite Konvertierung von Gleitkomma-Datentypen zu `ushort` gibt. Die folgende Anweisung erzeugt z.B. einen Compilerfehler, außer es wird eine explizite Umwandlung verwendet:

```csharp
// Error -- no implicit conversion from double:
ushort x = 3.0;
// OK -- explicit conversion:
ushort y = (ushort)3.0;
```

Informationen zu arithmetischen Ausdrücken mit ganzzahligen und Gleitkommatypen finden Sie unter [float](float.md) und [double](double.md).

Weitere Informationen zu impliziten numerischen Konvertierungsregeln finden Sie in der [Tabelle für implizite numerische Konvertierungen](implicit-numeric-conversions-table.md).

## <a name="c-language-specification"></a>C#-Sprachspezifikation

Weitere Informationen finden Sie unter [Intregrale Datentypen](~/_csharplang/spec/types.md#integral-types) in der [C#-Sprachspezifikation](../language-specification/index.md). Die Sprachspezifikation ist die verbindliche Quelle für die Syntax und Verwendung von C#.

## <a name="see-also"></a>Siehe auch

- <xref:System.UInt16>
- [C#-Referenz](../index.md)
- [C#-Programmierhandbuch](../../programming-guide/index.md)
- [C#-Schlüsselwörter](index.md)
- [Tabelle ganzzahliger Typen](integral-types-table.md)
- [Tabelle integrierter Typen](built-in-types-table.md)
- [Tabelle für implizite numerische Konvertierungen](implicit-numeric-conversions-table.md)
- [Tabelle für explizite numerische Konvertierungen](explicit-numeric-conversions-table.md)
