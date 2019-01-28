---
title: class-Schlüsselwort – C#-Referenz
ms.custom: seodec18
ms.date: 07/18/2017
f1_keywords:
- class_CSharpKeyword
- class
helpviewer_keywords:
- class keyword [C#]
ms.assetid: b95d8815-de18-4c3f-a8cc-a0a53bdf8690
ms.openlocfilehash: 83e7d278b38e17dac668b32687a368211399d437
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54652071"
---
# <a name="class-c-reference"></a>class (C#-Referenz)

Klassen werden mithilfe des Schlüsselworts `class` deklariert, wie im folgenden Beispiel dargestellt:

```csharp
class TestClass
{
    // Methods, properties, fields, events, delegates
    // and nested classes go here.
}
```

## <a name="remarks"></a>Hinweise

In C# ist nur die einfache Vererbung zulässig. Eine Klasse kann also Implementierungen aus nur einer Basisklasse erben. Es kann allerdings mehr als eine Schnittstelle implementiert werden. Die folgende Tabelle zeigt Beispiele für Klassenvererbung und Implementierung der Schnittstelle:

|Vererbung|Beispiel|
|-----------------|-------------|
|Keiner|`class ClassA { }`|
|Single|`class DerivedClass: BaseClass { }`|
|Keine, Implementierung von zwei Schnittstellen|`class ImplClass: IFace1, IFace2 { }`|
|Single, Implementierung einer Schnittstelle|`class ImplDerivedClass: BaseClass, IFace1 { }`|

Klassen, die Sie direkt innerhalb eines Namespace und nicht in anderen Klassen geschachtelt deklarieren, können entweder [public](../../../csharp/language-reference/keywords/public.md) oder [internal](../../../csharp/language-reference/keywords/internal.md) sein. Klassen sind standardmäßig `internal`.

Klassenmember, einschließlich geschachtelter Klassen, können [öffentlich](public.md), [intern geschützt](protected-internal.md), [geschützt](protected.md), [intern](internal.md), [privat geschützt](private.md) oder [privat](private-protected.md) sein. Member sind standardmäßig `private`.

Weitere Informationen finden Sie unter [Zugriffsmodifizierer](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).

Sie können generische Klassen deklarieren, die über Typparameter verfügen. Weitere Informationen finden Sie unter [Generische Klassen](../../../csharp/programming-guide/generics/generic-classes.md).

Eine Klasse kann Deklarationen der folgenden Member enthalten:

- [Konstruktoren](../../../csharp/programming-guide/classes-and-structs/constructors.md)

- [Konstanten](../../../csharp/programming-guide/classes-and-structs/constants.md)

- [Felder](../../../csharp/programming-guide/classes-and-structs/fields.md)

- [Finalizer](../../../csharp/programming-guide/classes-and-structs/destructors.md)

- [Methoden](../../../csharp/programming-guide/classes-and-structs/methods.md)

- [Eigenschaften](../../../csharp/programming-guide/classes-and-structs/properties.md)

- [Indexer](../../../csharp/programming-guide/indexers/index.md)

- [Operatoren](../../../csharp/programming-guide/statements-expressions-operators/operators.md)

- [Ereignisse](../../../csharp/programming-guide/events/index.md)

- [Delegaten](../../../csharp/programming-guide/delegates/index.md)

- [Klassen](../../../csharp/programming-guide/classes-and-structs/classes.md)

- [Schnittstellen](../../../csharp/programming-guide/interfaces/index.md)

- [Strukturen](../../../csharp/programming-guide/classes-and-structs/structs.md)

- [Enumerationen](../../../csharp/programming-guide/enumeration-types.md)

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt das Deklarieren von Klassenfeldern, Konstruktoren und Methoden. Darüber hinaus veranschaulicht es Objektinstanziierung und Ausgabe von Instanzdaten. In diesem Beispiel werden zwei Klassen deklariert. Die erste Klasse, `Child`, enthält zwei private Felder (`name` und `age`), zwei öffentliche Konstruktoren und eine öffentliche Methode. Die zweite Klasse, `StringTest`, enthält `Main`.

[!code-csharp[csrefKeywordsTypes#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#5)]

## <a name="comments"></a>Kommentare

Beachten Sie, dass im vorherigen Beispiel nur über die öffentliche Methode der Klasse `Child` auf die privaten Felder (`name` und `age`) zugegriffen werden kann. Sie können z.B. den Namen des untergeordneten Elements nicht aus der `Main`-Methode mit einer Anweisung wie folgt drucken:

```csharp
Console.Write(child1.name);   // Error
```

Zugriff auf private Member der `Child` von `Main` wäre nur möglich, wenn `Main` ein Member der Klasse wäre.

Typen, die innerhalb einer Klasse ohne Zugriffsmodifizierer deklariert werden, sind standardmäßig `private`, sodass die Datenmember in diesem Beispiel dennoch `private` wären, wenn das Schlüsselwort entfernt worden wäre.

Beachten Sie schließlich, dass für das Objekt, das mit dem Standardkonstruktor (`child3`) erstellt wurde, das Feld `age` standardmäßig auf Null (0) initialisiert wurde.

## <a name="c-language-specification"></a>C#-Sprachspezifikation

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Siehe auch

- [C#-Referenz](../../../csharp/language-reference/index.md)
- [C#-Programmierhandbuch](../../../csharp/programming-guide/index.md)
- [C#-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)
- [Verweistypen](../../../csharp/language-reference/keywords/reference-types.md)
