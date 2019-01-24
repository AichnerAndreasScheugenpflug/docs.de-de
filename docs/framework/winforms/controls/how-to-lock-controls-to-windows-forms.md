---
title: 'Vorgehensweise: Steuerelemente Sperren zu Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, locking
- controls [Windows Forms], locking
ms.assetid: 94efe0d2-c14e-4d14-b903-63ea9b07e290
ms.openlocfilehash: a59e5997104b9438681702d460dd8f6937df41b0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54741456"
---
# <a name="how-to-lock-controls-to-windows-forms"></a><span data-ttu-id="9a535-102">Vorgehensweise: Steuerelemente Sperren zu Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9a535-102">How to: Lock Controls to Windows Forms</span></span>
<span data-ttu-id="9a535-103">Wenn Sie die Benutzeroberfläche (UI) Ihrer Windows-Anwendung entwerfen, können Sie die Steuerelemente sperren, sobald sie die richtige Position sind, damit Sie nicht versehentlich zu verschieben oder deren Größe ändern, wenn Sie andere Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="9a535-103">When you design the user interface (UI) of your Windows application, you can lock the controls once they are positioned correctly, so that you do not inadvertently move or resize them when setting other properties.</span></span>  
  
 <span data-ttu-id="9a535-104">Darüber hinaus sperren und entsperren Sie alle Steuerelemente im Formular gleichzeitig angezeigt werden, die bei Formularen mit zahlreichen Steuerelementen hilfreich sind, oder Sie können einzelne Steuerelemente entsperren.</span><span class="sxs-lookup"><span data-stu-id="9a535-104">Additionally, you can lock and unlock all the controls on the form at once, which is helpful for forms with many controls, or you can unlock individual controls.</span></span> <span data-ttu-id="9a535-105">Nachdem Sie alle Steuerelemente platziert haben, Sie möchten diese auf dem Formular, Sperren Sie diese um fehlerhafte Bewegung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="9a535-105">Once you have placed all the controls where you want them on the form, lock them all in place to prevent erroneous movement.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9a535-106">Je nach den aktiven Einstellungen oder der Version unterscheiden sich die Dialogfelder und Menübefehle auf Ihrem Bildschirm möglicherweise von den in der Hilfe beschriebenen.</span><span class="sxs-lookup"><span data-stu-id="9a535-106">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="9a535-107">Klicken Sie im Menü **Extras** auf **Einstellungen importieren und exportieren** , um die Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9a535-107">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="9a535-108">Weitere Informationen finden Sie unter [Personalisieren von Visual Studio-IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="9a535-108">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-lock-a-control"></a><span data-ttu-id="9a535-109">Um ein Steuerelement zu sperren.</span><span class="sxs-lookup"><span data-stu-id="9a535-109">To lock a control</span></span>  
  
1.  <span data-ttu-id="9a535-110">In der **Eigenschaften** Fenster, klicken Sie auf die **gesperrt** Eigenschaft, und wählen `true`.</span><span class="sxs-lookup"><span data-stu-id="9a535-110">In the **Properties** window, click the **Locked** property and select `true`.</span></span> <span data-ttu-id="9a535-111">(Mit durch Doppelklicken auf den Namen wird die Einstellung der Eigenschaft.)</span><span class="sxs-lookup"><span data-stu-id="9a535-111">(Double-clicking the name toggles the property setting.)</span></span>  
  
     <span data-ttu-id="9a535-112">Alternativ klicken Sie auf das Steuerelement, und wählen Sie **Steuerelemente sperren**.</span><span class="sxs-lookup"><span data-stu-id="9a535-112">Alternatively, right-click the control and choose **Lock Controls**.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="9a535-113">Steuerelemente Sperren verhindert werden, die auf eine neue Größe oder Position auf der Entwurfsoberfläche gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="9a535-113">Locking controls prevents them from being dragged to a new size or location on the design surface.</span></span> <span data-ttu-id="9a535-114">Sie können jedoch weiterhin ändern die Größe oder Position der Steuerelemente von der **Eigenschaften** Fenster oder im Code.</span><span class="sxs-lookup"><span data-stu-id="9a535-114">However, you can still change the size or location of controls by means of the **Properties** window or in code.</span></span>  
  
### <a name="to-lock-all-the-controls-on-a-form"></a><span data-ttu-id="9a535-115">Um alle Steuerelemente in einem Formular zu sperren.</span><span class="sxs-lookup"><span data-stu-id="9a535-115">To lock all the controls on a form</span></span>  
  
1.  <span data-ttu-id="9a535-116">Von der **Format** Menü wählen **Steuerelemente sperren**.</span><span class="sxs-lookup"><span data-stu-id="9a535-116">From the **Format** menu, choose **Lock Controls**.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="9a535-117">Mit diesem Befehl sperrt auch die Größe des Formulars auf, da ein Formular ein Steuerelement handelt.</span><span class="sxs-lookup"><span data-stu-id="9a535-117">This command locks the form's size as well, because a form is a control.</span></span>  
  
### <a name="to-unlock-all-locked-controls-on-a-form"></a><span data-ttu-id="9a535-118">Um alle gesperrten Steuerelemente in einem Formular zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="9a535-118">To unlock all locked controls on a form</span></span>  
  
1.  <span data-ttu-id="9a535-119">Von der **Format** Menü wählen **Steuerelemente sperren**.</span><span class="sxs-lookup"><span data-stu-id="9a535-119">From the **Format** menu, choose **Lock Controls**.</span></span>  
  
     <span data-ttu-id="9a535-120">Alle zuvor gesperrten Steuerelemente im Formular sind jetzt entsperrt.</span><span class="sxs-lookup"><span data-stu-id="9a535-120">All previously locked controls on the form are now unlocked.</span></span>  
  
### <a name="to-unlock-locked-controls-individually"></a><span data-ttu-id="9a535-121">Um gesperrte Steuerelemente einzeln zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="9a535-121">To unlock locked controls individually</span></span>  
  
1.  <span data-ttu-id="9a535-122">In der **Eigenschaften** Fenster, klicken Sie auf die **gesperrt** Eigenschaft, und wählen `false`.</span><span class="sxs-lookup"><span data-stu-id="9a535-122">In the **Properties** window, click the **Locked** property and select `false`.</span></span> <span data-ttu-id="9a535-123">(Mit durch Doppelklicken auf den Namen wird die Einstellung der Eigenschaft.)</span><span class="sxs-lookup"><span data-stu-id="9a535-123">(Double-clicking the name toggles the property setting.)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a535-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a535-124">See also</span></span>
- [<span data-ttu-id="9a535-125">Windows Forms-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9a535-125">Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/index.md)
- [<span data-ttu-id="9a535-126">Anordnen von Steuerelementen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9a535-126">Arranging Controls on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/arranging-controls-on-windows-forms.md)
- [<span data-ttu-id="9a535-127">Beschriften einzelner Steuerelemente für Windows Forms und Konfigurieren von Shortcuts für diese Elemente</span><span class="sxs-lookup"><span data-stu-id="9a535-127">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](../../../../docs/framework/winforms/controls/labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [<span data-ttu-id="9a535-128">Windows Forms-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9a535-128">Controls to Use on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)
- [<span data-ttu-id="9a535-129">Windows Forms-Steuerelemente nach Funktion</span><span class="sxs-lookup"><span data-stu-id="9a535-129">Windows Forms Controls by Function</span></span>](../../../../docs/framework/winforms/controls/windows-forms-controls-by-function.md)
