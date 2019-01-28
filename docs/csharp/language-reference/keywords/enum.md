---
title: enum-Schlüsselwort – C#-Referenz
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- enum
- enum_CSharpKeyword
helpviewer_keywords:
- enum keyword [C#]
ms.assetid: bbeb9a0f-e9b3-41ab-b0a6-c41b1a08974c
ms.openlocfilehash: 768d8da320022a686f2ecfe5222880eccacee7dd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54727637"
---
# <a name="enum-c-reference"></a><span data-ttu-id="b0ddf-102">enum (C#-Referenz)</span><span class="sxs-lookup"><span data-stu-id="b0ddf-102">enum (C# Reference)</span></span>

<span data-ttu-id="b0ddf-103">Das Schlüsselwort `enum` wird zum Deklarieren einer Enumeration verwendet. Dies ist ein eigener Typ, der aus einer Gruppe benannter Konstanten besteht, die Enumeratorliste genannt wird.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-103">The `enum` keyword is used to declare an enumeration, a distinct type that consists of a set of named constants called the enumerator list.</span></span>  

<span data-ttu-id="b0ddf-104">In der Regel ist es am besten, eine Enumeration direkt innerhalb eines Namespaces so zu definieren, dass alle Klassen im Namespace auf gleiche Weise darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-104">Usually it is best to define an enum directly within a namespace so that all classes in the namespace can access it with equal convenience.</span></span> <span data-ttu-id="b0ddf-105">Eine Enumeration kann aber auch innerhalb einer Klasse oder einer Struktur geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-105">However, an enum can also be nested within a class or struct.</span></span>

<span data-ttu-id="b0ddf-106">Der erste Enumerator hat standardmäßig den Wert 0. Der Wert jedes nachfolgenden Enumerators wird um 1 erhöht.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-106">By default, the first enumerator has the value 0, and the value of each successive enumerator is increased by 1.</span></span> <span data-ttu-id="b0ddf-107">In der folgenden Enumeration gilt z. B.: `Sat` ist `0`, `Sun` ist `1`, `Mon` ist `2`usw.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-107">For example, in the following enumeration, `Sat` is `0`, `Sun` is `1`, `Mon` is `2`, and so forth.</span></span>

```csharp
enum Day {Sat, Sun, Mon, Tue, Wed, Thu, Fri};
```

<span data-ttu-id="b0ddf-108">Enumeratoren können mithilfe von Initialisierern die Standardwerte überschreiben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-108">Enumerators can use initializers to override the default values, as shown in the following example.</span></span>

```csharp
enum Day {Sat=1, Sun, Mon, Tue, Wed, Thu, Fri};
```

<span data-ttu-id="b0ddf-109">In dieser Enumeration wird erzwungen, dass die Abfolge von Elementen mit `1` und nicht mit `0`beginnt.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-109">In this enumeration, the sequence of elements is forced to start from `1` instead of `0`.</span></span> <span data-ttu-id="b0ddf-110">Allerdings wird das Einfügen einer Konstanten mit dem Wert 0 empfohlen.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-110">However, including a constant that has the value of 0 is recommended.</span></span> <span data-ttu-id="b0ddf-111">Weitere Informationen finden Sie unter [Enumerationstypen](../../programming-guide/enumeration-types.md).</span><span class="sxs-lookup"><span data-stu-id="b0ddf-111">For more information, see [Enumeration Types](../../programming-guide/enumeration-types.md).</span></span>

<span data-ttu-id="b0ddf-112">Jeder Enumerationstyp hat einen zugrunde liegenden Typ, bei dem es sich um jeden ganzzahligen Typ außer [char](char.md) handeln kann.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-112">Every enumeration type has an underlying type, which can be any integral type except [char](char.md).</span></span> <span data-ttu-id="b0ddf-113">Der zugrunde liegende Standardtyp von Enumerationselementen ist [int](int.md). Um eine Enumeration eines anderen ganzzahligen Typs, z. B. [byte](byte.md)zu deklarieren, setzen Sie einen Doppelpunkt hinter dem Bezeichner, auf den der Typ folgt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-113">The default underlying type of enumeration elements is [int](int.md). To declare an enum of another integral type, such as [byte](byte.md), use a colon after the identifier followed by the type, as shown in the following example.</span></span>

```csharp
enum Day : byte {Sat=1, Sun, Mon, Tue, Wed, Thu, Fri};
```

<span data-ttu-id="b0ddf-114">Die zulässigen Typen für eine Enumeration sind [byte](byte.md), [sbyte](sbyte.md), [short](short.md), [ushort](ushort.md), [int](int.md), [uint](uint.md), [long](long.md) und [ulong](ulong.md).</span><span class="sxs-lookup"><span data-stu-id="b0ddf-114">The approved types for an enum are [byte](byte.md), [sbyte](sbyte.md), [short](short.md), [ushort](ushort.md), [int](int.md), [uint](uint.md), [long](long.md), or [ulong](ulong.md).</span></span>

<span data-ttu-id="b0ddf-115">Der Variablen eines Enumerationstyps kann jeder Wert im Bereich des zugrunde liegenden Typs zugewiesen werden. Die Werte sind nicht auf benannte Konstanten beschränkt.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-115">A variable of an enumeration type can be assigned any value in the range of the underlying type; the values are not limited to the named constants.</span></span>

<span data-ttu-id="b0ddf-116">Der Standardwert von `enum E` ist der Wert, der vom Ausdruck `(E)0`erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-116">The default value of an `enum E` is the value produced by the expression `(E)0`.</span></span>

> [!NOTE]
> <span data-ttu-id="b0ddf-117">Namen von Enumeratoren dürfen keine Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-117">An enumerator cannot contain white space in its name.</span></span>

<span data-ttu-id="b0ddf-118">Der zugrunde liegende Typ gibt an, wie viel Speicher für jeden Enumerator reserviert wird.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-118">The underlying type specifies how much storage is allocated for each enumerator.</span></span> <span data-ttu-id="b0ddf-119">Eine explizite Typumwandlung ist jedoch erforderlich, um einen `enum` -Typ in einen ganzzahligen Typ zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-119">However, an explicit cast is necessary to convert from `enum` type to an integral type.</span></span> <span data-ttu-id="b0ddf-120">Durch die folgende Anweisung wird der `Sun` -Enumerator beispielsweise einer Variablen des Typs [int](int.md) zugewiesen. Dabei erfolgt für die Konvertierung von `enum` in `int`eine Typumwandlung.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-120">For example, the following statement assigns the enumerator `Sun` to a variable of the type [int](int.md) by using a cast to convert from `enum` to `int`.</span></span>

```csharp
int x = (int)Day.Sun;
```

<span data-ttu-id="b0ddf-121">Wenn <xref:System.FlagsAttribute?displayProperty=nameWithType> auf eine Enumeration mit Elementen angewendet wird, die mit einer bitweisen `OR` -Operation kombiniert werden können, beeinflusst das Attribut das Verhalten von `enum` bei der Verwendung bestimmter Tools.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-121">When you apply <xref:System.FlagsAttribute?displayProperty=nameWithType> to an enumeration that contains elements that can be combined with a bitwise `OR` operation, the attribute affects the behavior of the `enum` when it is used with some tools.</span></span> <span data-ttu-id="b0ddf-122">Solche Änderungen sind bei Verwendung von Tools wie den Methoden der <xref:System.Console> -Klasse und der Ausdrucksauswertung zu beobachten.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-122">You can notice these changes when you use tools such as the <xref:System.Console> class methods and the Expression Evaluator.</span></span> <span data-ttu-id="b0ddf-123">(Siehe das dritte Beispiel.)</span><span class="sxs-lookup"><span data-stu-id="b0ddf-123">(See the third example.)</span></span>

## <a name="robust-programming"></a><span data-ttu-id="b0ddf-124">Stabile Programmierung</span><span class="sxs-lookup"><span data-stu-id="b0ddf-124">Robust programming</span></span>

<span data-ttu-id="b0ddf-125">Wie bei Konstanten werden zur Kompilierzeit alle Verweise auf die einzelnen Werte einer Enumeration in numerische Literale konvertiert.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-125">Just as with any constant, all references to the individual values of an enum are converted to numeric literals at compile time.</span></span> <span data-ttu-id="b0ddf-126">Dies kann, wie unter [Konstanten](../../programming-guide/classes-and-structs/constants.md) beschrieben, zu möglichen Versionsproblemen führen.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-126">This can create potential versioning issues as described in [Constants](../../programming-guide/classes-and-structs/constants.md).</span></span>

<span data-ttu-id="b0ddf-127">Das Zuweisen zusätzlicher Werte zu neuen Enumerationsversionen oder das Ändern der Werte von Enumerationsmembern in einer neuen Version kann für abhängigen Quellcode Probleme verursachen.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-127">Assigning additional values to new versions of enums, or changing the values of the enum members in a new version, can cause problems for dependent source code.</span></span> <span data-ttu-id="b0ddf-128">Enumerationswerte werden oft in [switch](switch.md) -Anweisungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-128">Enum values often are used in [switch](switch.md) statements.</span></span> <span data-ttu-id="b0ddf-129">Wenn dem `enum` -Typ weitere Elemente hinzugefügt wurden, kann der Standardabschnitt der „switch“-Anweisung unerwartet ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-129">If additional elements have been added to the `enum` type, the default section of the switch statement can be selected unexpectedly.</span></span>

<span data-ttu-id="b0ddf-130">Falls andere Entwickler Ihren Code verwenden, sollten Sie Richtlinien festlegen, die angeben, wie deren Code reagieren soll, wenn `enum` -Typen neue Elemente hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-130">If other developers use your code, you should provide guidelines about how their code should react if new elements are added to any `enum` types.</span></span>

## <a name="example"></a><span data-ttu-id="b0ddf-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b0ddf-131">Example</span></span>

<span data-ttu-id="b0ddf-132">Im folgenden Beispiel wird die Enumeration `Day`deklariert.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-132">In the following example, an enumeration, `Day`, is declared.</span></span> <span data-ttu-id="b0ddf-133">Zwei Enumeratoren werden explizit in ganze Zahlen konvertiert und „Integer“-Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-133">Two enumerators are explicitly converted to integer and assigned to integer variables.</span></span>

[!code-csharp[csrefKeywordsTypes#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#10)]

## <a name="example"></a><span data-ttu-id="b0ddf-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b0ddf-134">Example</span></span>

<span data-ttu-id="b0ddf-135">Im folgenden Beispiel wird die Basistypoption verwendet, um ein `enum` zu deklarieren, dessen Member den Typ `long`haben.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-135">In the following example, the base-type option is used to declare an `enum` whose members are of type `long`.</span></span> <span data-ttu-id="b0ddf-136">Beachten Sie, dass obwohl der Enumeration der Typ `long`zugrunde liegt, die Enumerationsmember noch explizit mithilfe einer Typumwandlung in den Typ `long` umgewandelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-136">Notice that even though the underlying type of the enumeration is `long`, the enumeration members still must be explicitly converted to type `long` by using a cast.</span></span>

[!code-csharp[csrefKeywordsTypes#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#11)]

## <a name="example"></a><span data-ttu-id="b0ddf-137">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b0ddf-137">Example</span></span>

<span data-ttu-id="b0ddf-138">Im folgenden Codebeispiel werden die Verwendung des <xref:System.FlagsAttribute?displayProperty=nameWithType> -Attributs in einer `enum` -Deklaration und seine Wirkung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b0ddf-138">The following code example illustrates the use and effect of the <xref:System.FlagsAttribute?displayProperty=nameWithType> attribute on an `enum` declaration.</span></span>

[!code-csharp[csrefKeywordsTypes#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#12)]

## <a name="comments"></a><span data-ttu-id="b0ddf-139">Kommentare</span><span class="sxs-lookup"><span data-stu-id="b0ddf-139">Comments</span></span>

<span data-ttu-id="b0ddf-140">Wenn Sie `Flags`entfernen, werden im Beispiel die folgenden Werte angezeigt:</span><span class="sxs-lookup"><span data-stu-id="b0ddf-140">If you remove `Flags`, the example displays the following values:</span></span>

`5`

`5`

## <a name="c-language-specification"></a><span data-ttu-id="b0ddf-141">C#-Sprachspezifikation</span><span class="sxs-lookup"><span data-stu-id="b0ddf-141">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="b0ddf-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0ddf-142">See also</span></span>

- [<span data-ttu-id="b0ddf-143">C#-Referenz</span><span class="sxs-lookup"><span data-stu-id="b0ddf-143">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="b0ddf-144">Enumerationstypen</span><span class="sxs-lookup"><span data-stu-id="b0ddf-144">Enumeration Types</span></span>](../../programming-guide/enumeration-types.md)
- [<span data-ttu-id="b0ddf-145">C#-Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0ddf-145">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="b0ddf-146">Tabelle ganzzahliger Typen</span><span class="sxs-lookup"><span data-stu-id="b0ddf-146">Integral Types Table</span></span>](integral-types-table.md)
- [<span data-ttu-id="b0ddf-147">Tabelle integrierter Typen</span><span class="sxs-lookup"><span data-stu-id="b0ddf-147">Built-In Types Table</span></span>](built-in-types-table.md)
- [<span data-ttu-id="b0ddf-148">Tabelle für implizite numerische Konvertierungen</span><span class="sxs-lookup"><span data-stu-id="b0ddf-148">Implicit Numeric Conversions Table</span></span>](implicit-numeric-conversions-table.md)
- [<span data-ttu-id="b0ddf-149">Tabelle für explizite numerische Konvertierungen</span><span class="sxs-lookup"><span data-stu-id="b0ddf-149">Explicit Numeric Conversions Table</span></span>](explicit-numeric-conversions-table.md)
- [<span data-ttu-id="b0ddf-150">Benennungskonventionen für Enumerationen</span><span class="sxs-lookup"><span data-stu-id="b0ddf-150">Enum Naming Conventions</span></span>](../../../standard/design-guidelines/names-of-classes-structs-and-interfaces.md#naming-enumerations)
