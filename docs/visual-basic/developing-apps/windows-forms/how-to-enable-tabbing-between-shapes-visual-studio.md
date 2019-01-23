---
title: 'Vorgehensweise: Aktivieren Sie die TAB-Taste zwischen Formen (Visual Studio)'
ms.date: 07/20/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Line control [Visual Basic], implementing tabbing
- Shape control [Visual Basic], implementing tabbing
ms.assetid: 09731b34-3900-4fcb-a9df-ce5280328433
ms.openlocfilehash: c47d94317008af57907b747e53bd13ae7ca229f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498280"
---
# <a name="how-to-enable-tabbing-between-shapes-visual-studio"></a><span data-ttu-id="b22ad-102">Vorgehensweise: Aktivieren Sie die TAB-Taste zwischen Formen (Visual Studio)</span><span class="sxs-lookup"><span data-stu-id="b22ad-102">How to: Enable Tabbing Between Shapes (Visual Studio)</span></span>
<span data-ttu-id="b22ad-103">Linien-und Formensteuerelemente keine `TabStop` oder `TabIndex` Eigenschaften, aber Sie können trotzdem aktivieren TAB-Taste zwischen ihnen.</span><span class="sxs-lookup"><span data-stu-id="b22ad-103">Line and shape controls do not have `TabStop` or `TabIndex` properties, but you can still enable tabbing among them.</span></span> <span data-ttu-id="b22ad-104">Im folgenden Beispiel wird sowohl die STRG-Taste und die TAB-Taste drücken zwischen Formen Registerkarte durch Drücken der TAB-Taste zwischen den Schaltflächen Registerkarte wird.</span><span class="sxs-lookup"><span data-stu-id="b22ad-104">In the following example, pressing both the CTRL and the TAB keys will tab between shapes; pressing only the TAB key will tab between the buttons.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b22ad-105">Auf Ihrem Computer werden möglicherweise andere Namen oder Speicherorte für die Benutzeroberflächenelemente von Visual Studio angezeigt als die in den folgenden Anweisungen aufgeführten.</span><span class="sxs-lookup"><span data-stu-id="b22ad-105">Your computer might show different names or locations for some of the Visual Studio user interface elements in the following instructions.</span></span> <span data-ttu-id="b22ad-106">Diese Elemente sind von der jeweiligen Visual Studio-Version und den verwendeten Einstellungen abhängig.</span><span class="sxs-lookup"><span data-stu-id="b22ad-106">The Visual Studio edition that you have and the settings that you use determine these elements.</span></span> <span data-ttu-id="b22ad-107">Weitere Informationen finden Sie unter [Personalisieren von Visual Studio-IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="b22ad-107">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
## <a name="to-enable-tabbing-among-shapes"></a><span data-ttu-id="b22ad-108">So aktivieren Sie die TAB-Taste zwischen Formen</span><span class="sxs-lookup"><span data-stu-id="b22ad-108">To enable tabbing among shapes</span></span>  
  
1.  <span data-ttu-id="b22ad-109">Ziehen Sie drei <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> -Steuerelemente und zwei <xref:System.Windows.Forms.Button> -Steuerelemente aus der **Toolbox** zu einem Formular.</span><span class="sxs-lookup"><span data-stu-id="b22ad-109">Drag three <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape> controls and two <xref:System.Windows.Forms.Button> controls from the **Toolbox** to a form.</span></span>  
  
2.  <span data-ttu-id="b22ad-110">In der **Code-Editor**, Hinzufügen einer `Imports` oder `using` -Anweisung am Anfang des Moduls:</span><span class="sxs-lookup"><span data-stu-id="b22ad-110">In the **Code Editor**, add an `Imports` or `using` statement at the top of the module:</span></span>  
  
```vb  
Imports Microsoft.VisualBasic.PowerPacks  
```  
  
```csharp  
using Microsoft.VisualBasic.PowerPacks;  
```  

3.  <span data-ttu-id="b22ad-111">Fügen Sie den folgenden Code in einer Prozedur an:</span><span class="sxs-lookup"><span data-stu-id="b22ad-111">Add the following code in an event procedure:</span></span>  
  
[!code-csharp[VbPowerPacksTabbing#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-enable-tabbing-between-shapes-visual-studio_1.cs)]
[!code-vb[VbPowerPacksTabbing#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-enable-tabbing-between-shapes-visual-studio_1.vb)]  
  
4.  <span data-ttu-id="b22ad-112">Fügen Sie den folgenden Code in die `Button1_PreviewKeyDown` Ereignisprozedur:</span><span class="sxs-lookup"><span data-stu-id="b22ad-112">Add the following code in the `Button1_PreviewKeyDown` event procedure:</span></span>  
  
[!code-csharp[VbPowerPacksTabbing#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-enable-tabbing-between-shapes-visual-studio_2.cs)]
[!code-vb[VbPowerPacksTabbing#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-enable-tabbing-between-shapes-visual-studio_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="b22ad-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b22ad-113">See also</span></span>
- [<span data-ttu-id="b22ad-114">Vorgehensweise: Zeichnen von Formen mit dem OvalShape-Steuerelement und dem RectangleShape-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b22ad-114">How to: Draw Shapes with the OvalShape and RectangleShape Controls</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)
- [<span data-ttu-id="b22ad-115">Vorgehensweise: Zeichnen von Linien mit dem LineShape-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b22ad-115">How to: Draw Lines with the LineShape Control</span></span>](../../../visual-basic/developing-apps/windows-forms/how-to-draw-lines-with-the-lineshape-control-visual-studio.md)
- [<span data-ttu-id="b22ad-116">Einführung in das Line-Steuerelement und das Shape-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b22ad-116">Introduction to the Line and Shape Controls</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-line-and-shape-controls-visual-studio.md)
