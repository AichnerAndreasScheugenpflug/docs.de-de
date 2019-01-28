---
title: 'Vorgehensweise: Schreiben eines Kopierkonstruktors – C#-Programmierhandbuch'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# Language, copy constructor
- copy constructor [C#]
ms.assetid: fba899b5-fc41-428e-a745-3ebdbf37990a
ms.openlocfilehash: 252e66229b75c545c85aa175267ea267c138a087
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54573123"
---
# <a name="how-to-write-a-copy-constructor-c-programming-guide"></a><span data-ttu-id="350fd-102">Vorgehensweise: Schreiben eines Kopierkonstruktors (C#-Programmierhandbuch)</span><span class="sxs-lookup"><span data-stu-id="350fd-102">How to: Write a Copy Constructor (C# Programming Guide)</span></span>
<span data-ttu-id="350fd-103">C# stellt keinen Kopierkonstruktor für Objekte bereit. Sie können jedoch selbst einen schreiben.</span><span class="sxs-lookup"><span data-stu-id="350fd-103">C# doesn't provide a copy constructor for objects, but you can write one yourself.</span></span>  
  
## <a name="example"></a><span data-ttu-id="350fd-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="350fd-104">Example</span></span>  
 <span data-ttu-id="350fd-105">Im folgenden Beispiel wird von der `Person`-[Klasse](../../../csharp/language-reference/keywords/class.md) ein Kopierkonstruktor definiert, der eine Instanz von `Person` als sein Argument annimmt.</span><span class="sxs-lookup"><span data-stu-id="350fd-105">In the following example, the `Person`[class](../../../csharp/language-reference/keywords/class.md) defines a copy constructor that takes, as its argument, an instance of `Person`.</span></span> <span data-ttu-id="350fd-106">Die Werte der Eigenschaften des Arguments werden den Eigenschaften der neuen Instanz von `Person` zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="350fd-106">The values of the properties of the argument are assigned to the properties of the new instance of `Person`.</span></span> <span data-ttu-id="350fd-107">Der Code enthält einen alternativen Kopierkonstruktor, der die `Name`- und `Age`-Eigenschaften der Instanz sendet, die Sie in den Instanzenkonstruktor der Klasse kopieren möchten.</span><span class="sxs-lookup"><span data-stu-id="350fd-107">The code contains an alternative copy constructor that sends the `Name` and `Age` properties of the instance that you want to copy to the instance constructor of the class.</span></span>  
  
 [!code-csharp[csProgGuideObjects#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-write-a-copy-constructor_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="350fd-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="350fd-108">See also</span></span>

- <xref:System.ICloneable>
- [<span data-ttu-id="350fd-109">C#-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="350fd-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="350fd-110">Klassen und Strukturen</span><span class="sxs-lookup"><span data-stu-id="350fd-110">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)
- [<span data-ttu-id="350fd-111">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="350fd-111">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)
- [<span data-ttu-id="350fd-112">Finalizer</span><span class="sxs-lookup"><span data-stu-id="350fd-112">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)
