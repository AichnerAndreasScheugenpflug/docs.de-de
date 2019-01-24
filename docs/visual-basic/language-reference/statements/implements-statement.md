---
title: Implements-Anweisung (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Implements
- Implements
helpviewer_keywords:
- Implements statement [Visual Basic], syntax
- Implements statement [Visual Basic]
- interface implementation [Visual Basic], Implements statement
ms.assetid: 1fafb83f-f55a-4215-8ea9-681e8622613d
ms.openlocfilehash: cdcbe20157b9647040e3610d0632bd8e3fb9df65
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54681065"
---
# <a name="implements-statement"></a><span data-ttu-id="f4e64-102">Implements-Anweisung</span><span class="sxs-lookup"><span data-stu-id="f4e64-102">Implements Statement</span></span>
<span data-ttu-id="f4e64-103">Gibt an, mindestens eine weitere Schnittstellen oder Schnittstellenmember, die in der Klasse implementiert werden müssen oder Strukturdefinition, die in der sie angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f4e64-103">Specifies one or more interfaces, or interface members, that must be implemented in the class or structure definition in which it appears.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4e64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4e64-104">Syntax</span></span>  
  
```  
Implements interfacename [, ...]  
-or-  
Implements interfacename.interfacemember [, ...]  
```  
  
## <a name="parts"></a><span data-ttu-id="f4e64-105">Teile</span><span class="sxs-lookup"><span data-stu-id="f4e64-105">Parts</span></span>  
 `interfacename`  
 <span data-ttu-id="f4e64-106">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f4e64-106">Required.</span></span> <span data-ttu-id="f4e64-107">Eine Schnittstelle, deren Eigenschaften, Prozeduren und Ereignisse werden von den entsprechenden Elementen in der Klasse oder Struktur implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f4e64-107">An interface whose properties, procedures, and events are to be implemented by corresponding members in the class or structure.</span></span>  
  
 `interfacemember`  
 <span data-ttu-id="f4e64-108">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f4e64-108">Required.</span></span> <span data-ttu-id="f4e64-109">Der Member einer Schnittstelle, das implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="f4e64-109">The member of an interface that is being implemented.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f4e64-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f4e64-110">Remarks</span></span>  
 <span data-ttu-id="f4e64-111">Eine Schnittstelle ist eine Sammlung von Prototypen, die die Member (Eigenschaften, Prozeduren und Ereignisse) darstellen die Schnittstelle kapselt.</span><span class="sxs-lookup"><span data-stu-id="f4e64-111">An interface is a collection of prototypes representing the members (properties, procedures, and events) the interface encapsulates.</span></span> <span data-ttu-id="f4e64-112">Schnittstellen enthalten nur die Deklarationen für Member. implementieren diese Member, Klassen und Strukturen.</span><span class="sxs-lookup"><span data-stu-id="f4e64-112">Interfaces contain only the declarations for members; classes and structures implement these members.</span></span> <span data-ttu-id="f4e64-113">Weitere Informationen finden Sie unter [Schnittstellen](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span><span class="sxs-lookup"><span data-stu-id="f4e64-113">For more information, see [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span></span>  
  
 <span data-ttu-id="f4e64-114">Die `Implements` Anweisung muss unmittelbar folgen der `Class` oder `Structure` Anweisung.</span><span class="sxs-lookup"><span data-stu-id="f4e64-114">The `Implements` statement must immediately follow the `Class` or `Structure` statement.</span></span>  
  
 <span data-ttu-id="f4e64-115">Wenn Sie eine Schnittstelle implementieren, müssen Sie alle in der Schnittstelle deklarierten Member implementieren.</span><span class="sxs-lookup"><span data-stu-id="f4e64-115">When you implement an interface, you must implement all the members declared in the interface.</span></span> <span data-ttu-id="f4e64-116">Das auslassen jedes Element gilt ein Syntaxfehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f4e64-116">Omitting any member is considered to be a syntax error.</span></span> <span data-ttu-id="f4e64-117">Um einen einzelnen Member zu implementieren, geben Sie die [implementiert](../../../visual-basic/language-reference/statements/implements-clause.md) Schlüsselwort (unterscheidet sich von der `Implements` Anweisung) Wenn Sie das Element in der Klasse oder Struktur deklarieren.</span><span class="sxs-lookup"><span data-stu-id="f4e64-117">To implement an individual member, you specify the [Implements](../../../visual-basic/language-reference/statements/implements-clause.md) keyword (which is separate from the `Implements` statement) when you declare the member in the class or structure.</span></span> <span data-ttu-id="f4e64-118">Weitere Informationen finden Sie unter [Schnittstellen](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span><span class="sxs-lookup"><span data-stu-id="f4e64-118">For more information, see [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md).</span></span>  
  
 <span data-ttu-id="f4e64-119">Klassen können [Private](../../../visual-basic/language-reference/modifiers/private.md) Implementierungen von Eigenschaften und Prozeduren, aber diese Member sind nur durch umwandeln, die eine Instanz der implementierenden Klasse in eine Variable deklariert wird, der den Typ der Schnittstelle zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4e64-119">Classes can use [Private](../../../visual-basic/language-reference/modifiers/private.md) implementations of properties and procedures, but these members are accessible only by casting an instance of the implementing class into a variable declared to be of the type of the interface.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f4e64-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f4e64-120">Example</span></span>  
 <span data-ttu-id="f4e64-121">Das folgende Beispiel zeigt, wie Sie mit der `Implements` Anweisung, um die Member einer Schnittstelle zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="f4e64-121">The following example shows how to use the `Implements` statement to implement members of an interface.</span></span> <span data-ttu-id="f4e64-122">Es definiert eine Schnittstelle, die mit dem Namen `ICustomerInfo` mit einem Ereignis, eine Eigenschaft und einer Prozedur.</span><span class="sxs-lookup"><span data-stu-id="f4e64-122">It defines an interface named `ICustomerInfo` with an event, a property, and a procedure.</span></span> <span data-ttu-id="f4e64-123">Die Klasse `customerInfo` implementiert alle in der Schnittstelle definierten Member.</span><span class="sxs-lookup"><span data-stu-id="f4e64-123">The class `customerInfo` implements all the members defined in the interface.</span></span>  
  
 [!code-vb[VbVbalrStatements#33](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/implements-statement_1.vb)]  
  
 <span data-ttu-id="f4e64-124">Beachten Sie, dass die Klasse `customerInfo` verwendet die `Implements` Anweisung in einer separaten Quellcodezeile, um anzugeben, dass die Klasse, alle Member implementiert der `ICustomerInfo` Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f4e64-124">Note that the class `customerInfo` uses the `Implements` statement on a separate source code line to indicate that the class implements all the members of the `ICustomerInfo` interface.</span></span> <span data-ttu-id="f4e64-125">Klicken Sie dann auf jedes Element in der Klasse verwendet die `Implements` -Schlüsselwort als Teil der Element-Deklaration, um anzugeben, dass sie diesen Schnittstellenmember implementiert.</span><span class="sxs-lookup"><span data-stu-id="f4e64-125">Then each member in the class uses the `Implements` keyword as part of its member declaration to indicate that it implements that interface member.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f4e64-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f4e64-126">Example</span></span>  
 <span data-ttu-id="f4e64-127">Die beiden folgenden Verfahren zeigen, wie Sie die Schnittstelle implementiert, die im vorherigen Beispiel verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f4e64-127">The following two procedures show how you could use the interface implemented in the preceding example.</span></span> <span data-ttu-id="f4e64-128">Um die Implementierung zu testen, fügen Sie diese Prozeduren, um Ihr Projekt, und rufen die `testImplements` Verfahren.</span><span class="sxs-lookup"><span data-stu-id="f4e64-128">To test the implementation, add these procedures to your project and call the `testImplements` procedure.</span></span>  
  
 [!code-vb[VbVbalrStatements#34](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/implements-statement_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="f4e64-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4e64-129">See also</span></span>
- [<span data-ttu-id="f4e64-130">Implements</span><span class="sxs-lookup"><span data-stu-id="f4e64-130">Implements</span></span>](../../../visual-basic/language-reference/statements/implements-clause.md)
- [<span data-ttu-id="f4e64-131">Interface-Anweisung</span><span class="sxs-lookup"><span data-stu-id="f4e64-131">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)
- [<span data-ttu-id="f4e64-132">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f4e64-132">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
