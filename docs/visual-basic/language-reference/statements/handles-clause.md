---
title: Handles-Klausel (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- Handles
- vb.Handles
helpviewer_keywords:
- Handles keyword [Visual Basic]
ms.assetid: 1b051c0e-f499-42f6-acb5-6f4f27824b40
ms.openlocfilehash: 45fa54d7f7a3e167ffe0545cc3edf6a24900b2b3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54492961"
---
# <a name="handles-clause-visual-basic"></a><span data-ttu-id="357a5-102">Handles-Klausel (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="357a5-102">Handles Clause (Visual Basic)</span></span>
<span data-ttu-id="357a5-103">Deklariert, dass eine Prozedur ein angegebenes Ereignis behandelt.</span><span class="sxs-lookup"><span data-stu-id="357a5-103">Declares that a procedure handles a specified event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="357a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="357a5-104">Syntax</span></span>  
  
```  
proceduredeclaration Handles eventlist  
```  
  
## <a name="parts"></a><span data-ttu-id="357a5-105">Teile</span><span class="sxs-lookup"><span data-stu-id="357a5-105">Parts</span></span>  
 `proceduredeclaration`  
 <span data-ttu-id="357a5-106">Die `Sub`-Prozedurdeklaration für die Prozedur, die das Ereignis verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="357a5-106">The `Sub` procedure declaration for the procedure that will handle the event.</span></span>  
  
 `eventlist`  
 <span data-ttu-id="357a5-107">Listet die Ereignisse für `proceduredeclaration` für die Verarbeitung auf, durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="357a5-107">List of the events for `proceduredeclaration` to handle, separated by commas.</span></span> <span data-ttu-id="357a5-108">Die Ereignisse müssen durch die Basisklasse für die aktuelle Klasse oder durch ein mithilfe des Schlüsselworts `WithEvents` deklariertes Objekt ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="357a5-108">The events must be raised by either the base class for the current class, or by an object declared using the `WithEvents` keyword.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="357a5-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="357a5-109">Remarks</span></span>  
 <span data-ttu-id="357a5-110">Verwenden Sie das `Handles` -Schlüsselwort am Ende der Prozedurdeklaration, damit sie Ereignisse verarbeitet, die durch eine mithilfe des Schlüsselworts `WithEvents` deklarierte Objektvariable ausgelöst wurden.</span><span class="sxs-lookup"><span data-stu-id="357a5-110">Use the `Handles` keyword at the end of a procedure declaration to cause it to handle events raised by an object variable declared using the `WithEvents` keyword.</span></span> <span data-ttu-id="357a5-111">Das Schlüsselwort `Handles` kann zudem in einer abgeleiteten Klasse verwendet werden, um Ereignisse aus einer Basisklasse zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="357a5-111">The `Handles` keyword can also be used in a derived class to handle events from a base class.</span></span>  
  
 <span data-ttu-id="357a5-112">Mit dem Schlüsselwort `Handles` und der Anweisung `AddHandler` können Sie angeben, dass diese bestimmten Prozeduren bestimmte Ereignisse verarbeiten. Es bestehen jedoch keine Unterschiede.</span><span class="sxs-lookup"><span data-stu-id="357a5-112">The `Handles` keyword and the `AddHandler` statement both allow you to specify that particular procedures handle particular events, but there are differences.</span></span> <span data-ttu-id="357a5-113">Verwenden Sie das Schlüsselwort `Handles`, wenn Sie eine Prozedur definieren, um anzugeben, dass sie ein bestimmtes Ereignis verarbeitet. </span><span class="sxs-lookup"><span data-stu-id="357a5-113">Use the `Handles` keyword when defining a procedure to specify that it handles a particular event.</span></span> <span data-ttu-id="357a5-114">Die Anweisung `AddHandler` verbindet Prozeduren zur Laufzeit mit Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="357a5-114">The `AddHandler` statement connects procedures to events at run time.</span></span> <span data-ttu-id="357a5-115">Weitere Informationen finden Sie unter [AddHandler-Anweisung](../../../visual-basic/language-reference/statements/addhandler-statement.md).</span><span class="sxs-lookup"><span data-stu-id="357a5-115">For more information, see [AddHandler Statement](../../../visual-basic/language-reference/statements/addhandler-statement.md).</span></span>  
  
 <span data-ttu-id="357a5-116">Für benutzerdefinierte Ereignisse ruft die Anwendung die `AddHandler`-Zugriffsmethode des Ereignisses auf, wenn die Prozedur als ein Ereignishandler hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="357a5-116">For custom events, the application invokes the event's `AddHandler` accessor when it adds the procedure as an event handler.</span></span> <span data-ttu-id="357a5-117">Weitere Informationen zu benutzerdefinierten Ereignissen finden Sie unter [Event-Anweisung](../../../visual-basic/language-reference/statements/event-statement.md).</span><span class="sxs-lookup"><span data-stu-id="357a5-117">For more information on custom events, see [Event Statement](../../../visual-basic/language-reference/statements/event-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="357a5-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="357a5-118">Example</span></span>  
 [!code-vb[VbVbalrEvents#2](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/handles-clause_1.vb)]  
  
 <span data-ttu-id="357a5-119">Im folgenden Beispiel wird gezeigt, wie eine abgeleitete Klasse die `Handles`-Anweisung zum Verarbeiten eines Ereignisses aus einer Basisklasse verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="357a5-119">The following example demonstrates how a derived class can use the `Handles` statement to handle an event from a base class.</span></span>  
  
 [!code-vb[VbVbalrEvents#3](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/handles-clause_2.vb)]  
  
## <a name="example"></a><span data-ttu-id="357a5-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="357a5-120">Example</span></span>  
 <span data-ttu-id="357a5-121">Das folgende Beispiel enthält zwei Tastenereignishandler für ein **WPF-Anwendung** Projekt.</span><span class="sxs-lookup"><span data-stu-id="357a5-121">The following example contains two button event handlers for a **WPF Application** project.</span></span>  
  
 [!code-vb[VbVbalrEvents#41](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/handles-clause_3.vb)]  
  
## <a name="example"></a><span data-ttu-id="357a5-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="357a5-122">Example</span></span>  
 <span data-ttu-id="357a5-123">Das folgende Beispiel entspricht dem vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="357a5-123">The following example is equivalent to the previous example.</span></span> <span data-ttu-id="357a5-124">Die `eventlist` in der `Handles`-Klausel enthält die Ereignisse für beide Tasten.</span><span class="sxs-lookup"><span data-stu-id="357a5-124">The `eventlist` in the `Handles` clause contains the events for both buttons.</span></span>  
  
 [!code-vb[VbVbalrEvents#42](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/handles-clause_4.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="357a5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="357a5-125">See also</span></span>
- [<span data-ttu-id="357a5-126">WithEvents</span><span class="sxs-lookup"><span data-stu-id="357a5-126">WithEvents</span></span>](../../../visual-basic/language-reference/modifiers/withevents.md)
- [<span data-ttu-id="357a5-127">AddHandler-Anweisung</span><span class="sxs-lookup"><span data-stu-id="357a5-127">AddHandler Statement</span></span>](../../../visual-basic/language-reference/statements/addhandler-statement.md)
- [<span data-ttu-id="357a5-128">RemoveHandler-Anweisung</span><span class="sxs-lookup"><span data-stu-id="357a5-128">RemoveHandler Statement</span></span>](../../../visual-basic/language-reference/statements/removehandler-statement.md)
- [<span data-ttu-id="357a5-129">Event-Anweisung</span><span class="sxs-lookup"><span data-stu-id="357a5-129">Event Statement</span></span>](../../../visual-basic/language-reference/statements/event-statement.md)
- [<span data-ttu-id="357a5-130">RaiseEvent-Anweisung</span><span class="sxs-lookup"><span data-stu-id="357a5-130">RaiseEvent Statement</span></span>](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
- [<span data-ttu-id="357a5-131">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="357a5-131">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
