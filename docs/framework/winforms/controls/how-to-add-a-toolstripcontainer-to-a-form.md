---
title: 'Vorgehensweise: Hinzufügen von ToolStripContainer zu einem Formular'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms], built-in rafting
- ToolStrip control [Windows Forms], built-in rafting
- ToolStripContainer control [Windows Forms], adding to Windows Forms
ms.assetid: d0f55095-a833-453e-be5a-644906d75d54
ms.openlocfilehash: 9aace854a9583268ef7aac6ac1f57534cfdfe1e6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515520"
---
# <a name="how-to-add-a-toolstripcontainer-to-a-form"></a><span data-ttu-id="238cb-102">Vorgehensweise: Hinzufügen von ToolStripContainer zu einem Formular</span><span class="sxs-lookup"><span data-stu-id="238cb-102">How to: Add a ToolStripContainer to a Form</span></span>
<span data-ttu-id="238cb-103">Sie können einer Windows Form programmgesteuert einen <xref:System.Windows.Forms.ToolStripContainer> hinzufügen und diesen mit Steuerelementen füllen.</span><span class="sxs-lookup"><span data-stu-id="238cb-103">You can programmatically add a <xref:System.Windows.Forms.ToolStripContainer> to a Windows Form and populate it with controls.</span></span>  
  
## <a name="example"></a><span data-ttu-id="238cb-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="238cb-104">Example</span></span>  
 <span data-ttu-id="238cb-105">Das folgende Codebeispiel zeigt, wie einer Windows Form ein <xref:System.Windows.Forms.ToolStripContainer> und ein <xref:System.Windows.Forms.ToolStrip> hinzugefügt wird, wie dem <xref:System.Windows.Forms.ToolStrip> Elemente hinzugefügt werden und wie der <xref:System.Windows.Forms.ToolStrip> zum <xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanel%2A> des <xref:System.Windows.Forms.ToolStripContainer> hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="238cb-105">The following code example demonstrates how to add a <xref:System.Windows.Forms.ToolStripContainer> and a <xref:System.Windows.Forms.ToolStrip> to a Windows Forms, how to add items to the <xref:System.Windows.Forms.ToolStrip>, and how to add the <xref:System.Windows.Forms.ToolStrip> to the <xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanel%2A> of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStripContainer2#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/system.windows.forms.toolstripcontainer2/cs/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStripContainer2#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/system.windows.forms.toolstripcontainer2/vb/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="238cb-106">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="238cb-106">Compiling the Code</span></span>  
 <span data-ttu-id="238cb-107">Für dieses Codebeispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="238cb-107">This code example requires:</span></span>  
  
-   <span data-ttu-id="238cb-108">Verweise auf die Assemblys "System.Drawing", "System.Text" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="238cb-108">References to the System.Drawing, System.Text, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="238cb-109">Informationen zum Erstellen dieses Beispiels über die Befehlszeile für Visual Basic oder Visual c# finden Sie unter [erstellen über die Befehlszeile](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) oder [Befehlszeile mit csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="238cb-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="238cb-110">Sie können auch in diesem Beispiel in Visual Studio erstellen, indem Sie den Code in ein neues Projekt einfügen.</span><span class="sxs-lookup"><span data-stu-id="238cb-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="238cb-111">Weitere Information finden Sie unter [How to: Kompilieren und Ausführen einer vollständigen Windows Forms-Codebeispiels mit Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)) oder [Dialogfeld "ToolStripContainer-Aufgaben"](https://msdn.microsoft.com/library/ms233647\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="238cb-111">See also [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)) or [ToolStripContainer Tasks Dialog Box](https://msdn.microsoft.com/library/ms233647\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="238cb-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="238cb-112">See also</span></span>
- <xref:System.Windows.Forms.ToolStripContainer>
- [<span data-ttu-id="238cb-113">ToolStripContainer-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="238cb-113">ToolStripContainer Control</span></span>](../../../../docs/framework/winforms/controls/toolstripcontainer-control.md)
- [<span data-ttu-id="238cb-114">ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="238cb-114">ToolStrip Control</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
