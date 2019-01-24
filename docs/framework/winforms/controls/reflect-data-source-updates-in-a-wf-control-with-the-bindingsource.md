---
title: 'Vorgehensweise: Datenquellenaktualisierungen Sie in einem Windows Forms-Steuerelement mit der BindingSource-Komponente'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- data binding [Windows Forms], updating
- BindingSource component [Windows Forms], updating data binding
- examples [Windows Forms], BindingSource component
- data sources [Windows Forms], updating
- BindingSource component [Windows Forms], examples
ms.assetid: bd8bd9b2-af8a-4f11-a3d5-54eecbe2400b
ms.openlocfilehash: c08df86596eef23ca4706333cbfa333427fcad0e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614340"
---
# <a name="how-to-reflect-data-source-updates-in-a-windows-forms-control-with-the-bindingsource"></a><span data-ttu-id="b3f3c-102">Vorgehensweise: Datenquellenaktualisierungen Sie in einem Windows Forms-Steuerelement mit der BindingSource-Komponente</span><span class="sxs-lookup"><span data-stu-id="b3f3c-102">How to: Reflect Data Source Updates in a Windows Forms Control with the BindingSource</span></span>
<span data-ttu-id="b3f3c-103">Wenn Sie an Daten gebundene Steuerelemente verwenden, müssen Sie manchmal auf Änderungen in der Datenquelle reagieren, wenn die Datenquelle keine Ereignisse für Listenänderungen auslöst.</span><span class="sxs-lookup"><span data-stu-id="b3f3c-103">When you use data-bound controls, you sometimes have to respond to changes in the data source when the data source does not raise list-changed events.</span></span> <span data-ttu-id="b3f3c-104">Wenn Sie die <xref:System.Windows.Forms.BindingSource> Komponente zum Binden Ihrer Datenquelle an ein Windows Forms-Steuerelement verwenden, können Sie das Steuerelement benachrichtigen, dass sich Ihre Datenquelle geändert hat, indem Sie die Methode <xref:System.Windows.Forms.BindingSource.ResetBindings%2A> aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b3f3c-104">When you use the <xref:System.Windows.Forms.BindingSource> component to bind your data source to a Windows Forms control, you can notify the control that your data source has changed by calling the <xref:System.Windows.Forms.BindingSource.ResetBindings%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b3f3c-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b3f3c-105">Example</span></span>  
 <span data-ttu-id="b3f3c-106">Das folgende Codebeispiel veranschaulicht die Verwendung der Methode <xref:System.Windows.Forms.BindingSource.ResetBindings%2A>, um ein gebundenes Steuerelement über eine Aktualisierung in der Datenquelle zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="b3f3c-106">The following code example demonstrates using the <xref:System.Windows.Forms.BindingSource.ResetBindings%2A> method to notify a bound control about an update in the data source.</span></span>  
  
 [!code-cpp[System.Windows.Forms.DataConnector.ResetBindings#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetBindings/CPP/form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.DataConnector.ResetBindings#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetBindings/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataConnector.ResetBindings#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetBindings/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="b3f3c-107">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="b3f3c-107">Compiling the Code</span></span>  
 <span data-ttu-id="b3f3c-108">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b3f3c-108">This example requires:</span></span>  
  
-   <span data-ttu-id="b3f3c-109">Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="b3f3c-109">References to the System, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="b3f3c-110">Informationen zum Erstellen dieses Beispiels über die Befehlszeile für Visual Basic oder Visual c# finden Sie unter [erstellen über die Befehlszeile](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) oder [Befehlszeile mit csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="b3f3c-110">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="b3f3c-111">Sie können auch in diesem Beispiel in Visual Studio erstellen, indem Sie den Code in ein neues Projekt einfügen.</span><span class="sxs-lookup"><span data-stu-id="b3f3c-111">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="b3f3c-112">Weitere Informationen hierzu finden Sie auch unter [Gewusst wie: Kompilieren und Ausführen einer vollständigen Windows Forms-Codebeispiels mit Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="b3f3c-112">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3f3c-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3f3c-113">See also</span></span>
- <xref:System.Windows.Forms.BindingNavigator>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="b3f3c-114">BindingSource-Komponente</span><span class="sxs-lookup"><span data-stu-id="b3f3c-114">BindingSource Component</span></span>](../../../../docs/framework/winforms/controls/bindingsource-component.md)
- [<span data-ttu-id="b3f3c-115">Vorgehensweise: Binden eines Windows Forms-Steuerelements an einen Typ</span><span class="sxs-lookup"><span data-stu-id="b3f3c-115">How to: Bind a Windows Forms Control to a Type</span></span>](../../../../docs/framework/winforms/controls/how-to-bind-a-windows-forms-control-to-a-type.md)
