---
title: Mehrdimensionale Arrays – C#-Programmierhandbuch
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- arrays [C#], multidimensional
- multidimensional arrays [C#]
ms.assetid: 020ce02e-7dff-4273-8e53-bf0b33747232
ms.openlocfilehash: 4547bd94a0870dbb3955c4980361c8be0453616d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642411"
---
# <a name="multidimensional-arrays-c-programming-guide"></a><span data-ttu-id="21a2f-102">Mehrdimensionale Arrays (C#-Programmierhandbuch)</span><span class="sxs-lookup"><span data-stu-id="21a2f-102">Multidimensional Arrays (C# Programming Guide)</span></span>

<span data-ttu-id="21a2f-103">Arrays können mehr als eine Dimension aufweisen.</span><span class="sxs-lookup"><span data-stu-id="21a2f-103">Arrays can have more than one dimension.</span></span> <span data-ttu-id="21a2f-104">Die folgende Deklaration erstellt z.B. ein zweidimensionales Array mit vier Zeilen und zwei Spalten.</span><span class="sxs-lookup"><span data-stu-id="21a2f-104">For example, the following declaration creates a two-dimensional array of four rows and two columns.</span></span>  
  
 [!code-csharp[csProgGuideArrays#11](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_1.cs)]  
  
 <span data-ttu-id="21a2f-105">Die folgende Deklaration erstellt ein Array mit drei Dimensionen 4, 2 und 3.</span><span class="sxs-lookup"><span data-stu-id="21a2f-105">The following declaration creates an array of three dimensions, 4, 2, and 3.</span></span>  
  
 [!code-csharp[csProgGuideArrays#12](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_2.cs)]  
  
## <a name="array-initialization"></a><span data-ttu-id="21a2f-106">Arrayinitialisierung</span><span class="sxs-lookup"><span data-stu-id="21a2f-106">Array Initialization</span></span>

 <span data-ttu-id="21a2f-107">Sie können das Array wie im folgenden Beispiel gezeigt nach der Deklaration initialisieren.</span><span class="sxs-lookup"><span data-stu-id="21a2f-107">You can initialize the array upon declaration, as is shown in the following example.</span></span>  
  
 [!code-csharp[csProgGuideArrays#13](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_3.cs)]  
  
 <span data-ttu-id="21a2f-108">Sie können das Array auch ohne Angabe des Rangs initialisieren.</span><span class="sxs-lookup"><span data-stu-id="21a2f-108">You also can initialize the array without specifying the rank.</span></span>  
  
 [!code-csharp[csProgGuideArrays#14](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_4.cs)]  
  
 <span data-ttu-id="21a2f-109">Wenn Sie eine Arrayvariable ohne Initialisierung deklarieren möchten, müssen Sie der Variable mit dem Operator `new` ein Array zuweisen.</span><span class="sxs-lookup"><span data-stu-id="21a2f-109">If you choose to declare an array variable without initialization, you must use the `new` operator to assign an array to the variable.</span></span> <span data-ttu-id="21a2f-110">Die Verwendung von `new` wird im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="21a2f-110">The use of `new` is shown in the following example.</span></span>  
  
 [!code-csharp[csProgGuideArrays#15](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_5.cs)]  
  
 <span data-ttu-id="21a2f-111">Im folgende Beispiel wird einem bestimmten Arrayelement ein Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="21a2f-111">The following example assigns a value to a particular array element.</span></span>  
  
 [!code-csharp[csProgGuideArrays#16](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_6.cs)]  
  
 <span data-ttu-id="21a2f-112">Auf ähnliche Weise wird im folgenden Beispiel der Wert eines bestimmten Arrayelements abgerufen und der Variablen `elementValue` zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="21a2f-112">Similarly, the following example gets the value of a particular array element and assigns it to variable `elementValue`.</span></span>  
  
 [!code-csharp[csProgGuideArrays#42](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_7.cs)]  
  
 <span data-ttu-id="21a2f-113">Im folgenden Codebeispiel werden die Arrayelemente auf Standardwerte initialisiert (mit Ausnahme von verzweigten Arrays).</span><span class="sxs-lookup"><span data-stu-id="21a2f-113">The following code example initializes the array elements to default values (except for jagged arrays).</span></span>  
  
 [!code-csharp[csProgGuideArrays#17](../../../csharp/programming-guide/arrays/codesnippet/CSharp/multidimensional-arrays_8.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="21a2f-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21a2f-114">See also</span></span>

- [<span data-ttu-id="21a2f-115">C#-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="21a2f-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="21a2f-116">Arrays</span><span class="sxs-lookup"><span data-stu-id="21a2f-116">Arrays</span></span>](../../../csharp/programming-guide/arrays/index.md)
- [<span data-ttu-id="21a2f-117">Eindimensionale Arrays</span><span class="sxs-lookup"><span data-stu-id="21a2f-117">Single-Dimensional Arrays</span></span>](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)
- [<span data-ttu-id="21a2f-118">Verzweigte Arrays</span><span class="sxs-lookup"><span data-stu-id="21a2f-118">Jagged Arrays</span></span>](../../../csharp/programming-guide/arrays/jagged-arrays.md)
