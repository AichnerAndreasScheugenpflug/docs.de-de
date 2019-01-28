---
title: Zugriffsdomäne – C#-Referenz
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- accessibility domain [C#]
ms.assetid: 8af779c1-275b-44be-a864-9edfbca71bcc
ms.openlocfilehash: 241fe7714bfd3dd3fd37f7ac83a836f89b4951bf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54605577"
---
# <a name="accessibility-domain-c-reference"></a><span data-ttu-id="427c9-102">Zugriffsdomäne (C#-Referenz)</span><span class="sxs-lookup"><span data-stu-id="427c9-102">Accessibility Domain (C# Reference)</span></span>
<span data-ttu-id="427c9-103">Die Zugriffsdomäne eines Members gibt an, in welche Teile des Programms ein Member verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="427c9-103">The accessibility domain of a member specifies in which program sections a member can be referenced.</span></span> <span data-ttu-id="427c9-104">Wenn der Member in einem anderen Typ geschachtelt ist, wird seine Zugriffsdomäne sowohl durch das [Zugriffslevel](../../../csharp/language-reference/keywords/accessibility-levels.md) des Members als auch durch die Zugriffsdomäne des direkt enthaltenden Typs bestimmt.</span><span class="sxs-lookup"><span data-stu-id="427c9-104">If the member is nested within another type, its accessibility domain is determined by both the [accessibility level](../../../csharp/language-reference/keywords/accessibility-levels.md) of the member and the accessibility domain of the immediately containing type.</span></span>  
  
 <span data-ttu-id="427c9-105">Die Zugriffsdomäne eines Typs der obersten Ebene ist mindestens der Programmtext des Projekts, in dem er deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="427c9-105">The accessibility domain of a top-level type is at least the program text of the project that it is declared in.</span></span> <span data-ttu-id="427c9-106">Das bedeutet, dass die Domäne alle Quelldateien des Projekts enthält.</span><span class="sxs-lookup"><span data-stu-id="427c9-106">That is, the domain includes all of the source files of this project.</span></span> <span data-ttu-id="427c9-107">Die Zugriffsdomäne eines geschachtelten Typs ist mindestens der Programmtext des Typs, in dem er deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="427c9-107">The accessibility domain of a nested type is at least the program text of the type in which it is declared.</span></span> <span data-ttu-id="427c9-108">Das bedeutet, dass die Domäne der Typkörper ist, der alle geschachtelten Typen enthält.</span><span class="sxs-lookup"><span data-stu-id="427c9-108">That is, the domain is the type body, which includes all nested types.</span></span> <span data-ttu-id="427c9-109">Die Zugriffsdomäne eines geschachtelten Typs geht nie über die des enthaltenden Typs hinaus.</span><span class="sxs-lookup"><span data-stu-id="427c9-109">The accessibility domain of a nested type never exceeds that of the containing type.</span></span> <span data-ttu-id="427c9-110">Diese Konzepte werden im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="427c9-110">These concepts are demonstrated in the following example.</span></span>  
  
## <a name="example"></a><span data-ttu-id="427c9-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="427c9-111">Example</span></span>  
 <span data-ttu-id="427c9-112">Dieses Beispiel enthält einen Typ der obersten Ebene `T1`, und zwei geschachtelte Klassen `M1` und `M2`.</span><span class="sxs-lookup"><span data-stu-id="427c9-112">This example contains a top-level type, `T1`, and two nested classes, `M1` and `M2`.</span></span> <span data-ttu-id="427c9-113">Die Klassen enthalten Felder mit unterschiedlichen deklarierten Zugriffen.</span><span class="sxs-lookup"><span data-stu-id="427c9-113">The classes contain fields that have different declared accessibilities.</span></span> <span data-ttu-id="427c9-114">In der `Main`-Methode folgt jeder Anweisung ein Kommentar, der die Zugriffsdomäne jedes Members angibt.</span><span class="sxs-lookup"><span data-stu-id="427c9-114">In the `Main` method, a comment follows each statement to indicate the accessibility domain of each member.</span></span> <span data-ttu-id="427c9-115">Beachten Sie, dass die Anweisungen, die versuchen, auf die Member zu verweisen, auf die nicht zugegriffen werden kann, auskommentiert werden. Wenn Sie die Compilerfehler anzeigen möchten, die durch Verweisen auf einen Member verursacht werden, auf den nicht zugegriffen werden kann, entfernen Sie die Kommentare nacheinander.</span><span class="sxs-lookup"><span data-stu-id="427c9-115">Notice that the statements that try to reference the inaccessible members are commented out. If you want to see the compiler errors caused by referencing an inaccessible member, remove the comments one at a time.</span></span>  
  
[!code-csharp[csrefKeywordsModifiers#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#4)]
  
## <a name="c-language-specification"></a><span data-ttu-id="427c9-116">C#-Programmiersprachenspezifikation</span><span class="sxs-lookup"><span data-stu-id="427c9-116">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="427c9-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="427c9-117">See also</span></span>
- [<span data-ttu-id="427c9-118">C#-Referenz</span><span class="sxs-lookup"><span data-stu-id="427c9-118">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="427c9-119">C#-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="427c9-119">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="427c9-120">C#-Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="427c9-120">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
- [<span data-ttu-id="427c9-121">Zugriffsmodifizierer</span><span class="sxs-lookup"><span data-stu-id="427c9-121">Access Modifiers</span></span>](../../../csharp/language-reference/keywords/access-modifiers.md)
- [<span data-ttu-id="427c9-122">Zugriffsebenen</span><span class="sxs-lookup"><span data-stu-id="427c9-122">Accessibility Levels</span></span>](../../../csharp/language-reference/keywords/accessibility-levels.md)
- [<span data-ttu-id="427c9-123">Einschränkungen bei der Verwendung von Zugriffsebenen</span><span class="sxs-lookup"><span data-stu-id="427c9-123">Restrictions on Using Accessibility Levels</span></span>](../../../csharp/language-reference/keywords/restrictions-on-using-accessibility-levels.md)
- [<span data-ttu-id="427c9-124">Zugriffsmodifizierer</span><span class="sxs-lookup"><span data-stu-id="427c9-124">Access Modifiers</span></span>](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)
- [<span data-ttu-id="427c9-125">public</span><span class="sxs-lookup"><span data-stu-id="427c9-125">public</span></span>](../../../csharp/language-reference/keywords/public.md)
- [<span data-ttu-id="427c9-126">private</span><span class="sxs-lookup"><span data-stu-id="427c9-126">private</span></span>](../../../csharp/language-reference/keywords/private.md)
- [<span data-ttu-id="427c9-127">protected</span><span class="sxs-lookup"><span data-stu-id="427c9-127">protected</span></span>](../../../csharp/language-reference/keywords/protected.md)
- [<span data-ttu-id="427c9-128">internal</span><span class="sxs-lookup"><span data-stu-id="427c9-128">internal</span></span>](../../../csharp/language-reference/keywords/internal.md)
