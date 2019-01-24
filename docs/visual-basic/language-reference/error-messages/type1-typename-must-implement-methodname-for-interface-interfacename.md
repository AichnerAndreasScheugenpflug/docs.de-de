---
title: '&lt;type1&gt;&#39;&lt;Typename&gt; &#39; müssen implementieren &#39; &lt;Methodname&gt; &#39; für Schnittstelle &#39; &lt;Schnittstellenname&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: ff9ffd50f7f21814d5e4c23fd8df50b12bf746f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642440"
---
# <a name="lttype1gt39lttypenamegt39-must-implement-39ltmethodnamegt39-for-interface-39ltinterfacenamegt39"></a><span data-ttu-id="8bfc6-102">&lt;type1&gt;&#39;&lt;Typename&gt; &#39; müssen implementieren &#39; &lt;Methodname&gt; &#39; für Schnittstelle &#39; &lt;Schnittstellenname&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="8bfc6-102">&lt;type1&gt;&#39;&lt;typename&gt;&#39; must implement &#39;&lt;methodname&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39;</span></span>
<span data-ttu-id="8bfc6-103">Eine Klasse oder Struktur vorgibt, eine Schnittstelle zu implementieren, ohne dass eine Prozedur, die von der Schnittstelle definierten implementiert.</span><span class="sxs-lookup"><span data-stu-id="8bfc6-103">A class or structure claims to implement an interface but does not implement a procedure defined by the interface.</span></span> <span data-ttu-id="8bfc6-104">Jeder Member der Schnittstelle muss implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="8bfc6-104">Every member of the interface must be implemented.</span></span>  
  
 <span data-ttu-id="8bfc6-105">**Fehler-ID:** BC30149</span><span class="sxs-lookup"><span data-stu-id="8bfc6-105">**Error ID:** BC30149</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="8bfc6-106">So beheben Sie diesen Fehler</span><span class="sxs-lookup"><span data-stu-id="8bfc6-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="8bfc6-107">Deklarieren Sie eine Prozedur mit dem gleichen Namen und die gleiche Signatur wie in der Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="8bfc6-107">Declare a procedure with the same name and signature as defined in the interface.</span></span> <span data-ttu-id="8bfc6-108">Müssen Sie mindestens die `End Function` oder `End Sub` Anweisung.</span><span class="sxs-lookup"><span data-stu-id="8bfc6-108">Be sure to include at least the `End Function` or `End Sub` statement.</span></span>  
  
2.  <span data-ttu-id="8bfc6-109">Hinzufügen einer `Implements` Klausel am Ende der `Function` oder `Sub` Anweisung.</span><span class="sxs-lookup"><span data-stu-id="8bfc6-109">Add an `Implements` clause to the end of the `Function` or `Sub` statement.</span></span> <span data-ttu-id="8bfc6-110">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8bfc6-110">For example:</span></span>  
  
    ```  
    Public Sub DoSomething() Implements IBaseInterface.DoSomething  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="8bfc6-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bfc6-111">See also</span></span>
- [<span data-ttu-id="8bfc6-112">Implements-Anweisung</span><span class="sxs-lookup"><span data-stu-id="8bfc6-112">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)
- [<span data-ttu-id="8bfc6-113">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8bfc6-113">Interfaces</span></span>](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
