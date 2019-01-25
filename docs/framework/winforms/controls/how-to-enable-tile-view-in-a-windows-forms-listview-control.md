---
title: 'Vorgehensweise: Aktivieren der Tile-Ansicht in ein ListView-Steuerelement in Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tile view feature
- tiling
- Windows Forms, controls
- ListView control [Windows Forms], tile view
ms.assetid: c20e67a3-2d94-413d-9fcf-ecbd0fe251da
ms.openlocfilehash: b51a314791180ea0f03f2eb0c5fbe8f897a0016d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629301"
---
# <a name="how-to-enable-tile-view-in-a-windows-forms-listview-control"></a><span data-ttu-id="ab9b6-102">Vorgehensweise: Aktivieren der Tile-Ansicht in ein ListView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ab9b6-102">How to: Enable Tile View in a Windows Forms ListView Control</span></span>
<span data-ttu-id="ab9b6-103">Mit der Funktion „Nebeneinanderanzeige„ des <xref:System.Windows.Forms.ListView>-Steuerelements können Sie eine visuelle Balance zwischen grafischen und textbasierten Daten herstellen.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-103">With the tile view feature of the <xref:System.Windows.Forms.ListView> control, you can provide a visual balance between graphical and textual information.</span></span> <span data-ttu-id="ab9b6-104">Die textbasierten Daten, die für ein Element in der Ansicht "Nebeneinander" angezeigt werden, sind die gleichen wie die Spalteninformationen, die für die Detailansicht definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-104">The textual information displayed for an item in tile view is the same as the column information defined for details view.</span></span> <span data-ttu-id="ab9b6-105">Die Ansicht "Nebeneinander" funktioniert in Kombination mit den Features "Gruppieren" oder "Einfügemarke" des <xref:System.Windows.Forms.ListView>-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-105">Tile view works in combination with either the grouping or insertion mark features in the <xref:System.Windows.Forms.ListView> control.</span></span>  
  
 <span data-ttu-id="ab9b6-106">Für die Ansicht "Nebeneinander" wird ein 32 x 32 Pixel großes Symbol mit mehreren Textzeilen verwendet, wie in den folgenden Abbildungen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-106">The tile view uses a 32 x 32 pixel icon and several lines of text, as shown in the following images.</span></span>  
  
 <span data-ttu-id="ab9b6-107">![Ansicht in einem ListView-Steuerelement "Nebeneinander"](../../../../docs/framework/winforms/controls/media/listviewtile.gif "ListViewTile")</span><span class="sxs-lookup"><span data-stu-id="ab9b6-107">![Tile View in a ListView Control](../../../../docs/framework/winforms/controls/media/listviewtile.gif "ListViewTile")</span></span>  
<span data-ttu-id="ab9b6-108">Symbole und Text der Ansicht "Nebeneinander"</span><span class="sxs-lookup"><span data-stu-id="ab9b6-108">Tile view icons and text</span></span>  
  
 <span data-ttu-id="ab9b6-109">Um die Ansicht "Nebeneinander" zu aktivieren, legen Sie die <xref:System.Windows.Forms.ListView.View%2A>-Eigenschaft auf <xref:System.Windows.Forms.View.Tile> fest.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-109">To enable tile view, set the <xref:System.Windows.Forms.ListView.View%2A> property to <xref:System.Windows.Forms.View.Tile>.</span></span> <span data-ttu-id="ab9b6-110">Sie können die Größe der Kacheln anpassen, indem Sie die <xref:System.Windows.Forms.ListView.TileSize%2A>-Eigenschaft festlegen, und Sie können die Anzahl der angezeigten Textzeilen festlegen, indem Sie die <xref:System.Windows.Forms.ListView.Columns%2A>-Auflistung anpassen.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-110">You can adjust the size of the tiles by setting the <xref:System.Windows.Forms.ListView.TileSize%2A> property, and the number of text lines displayed in the tile by adjusting the <xref:System.Windows.Forms.ListView.Columns%2A> collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ab9b6-111">Die Ansicht "Nebeneinander" steht unter [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] nur zur Verfügung, wenn die Anwendung die <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType>-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-111">The tile view is available only on [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] when your application calls the <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="ab9b6-112">Unter älteren Betriebssystemen hat Code in Bezug auf die Ansicht "Nebeneinander" keine Auswirkungen, und das <xref:System.Windows.Forms.ListView>-Steuerelement wird in der Ansicht "Große Symbole" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-112">On earlier operating systems, any code related to the tile view has no effect, and the <xref:System.Windows.Forms.ListView> control displays in the large icon view.</span></span> <span data-ttu-id="ab9b6-113">Weitere Informationen finden Sie unter <xref:System.Windows.Forms.ListView.View%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-113">For more information, see <xref:System.Windows.Forms.ListView.View%2A?displayProperty=nameWithType>.</span></span>  
  
### <a name="to-set-tile-view-programmatically"></a><span data-ttu-id="ab9b6-114">So legen Sie die Ansicht "Nebeneinander" programmgesteuert fest</span><span class="sxs-lookup"><span data-stu-id="ab9b6-114">To set tile view programmatically</span></span>  
  
1.  <span data-ttu-id="ab9b6-115">Verwenden Sie die <xref:System.Windows.Forms.View>-Enumeration des <xref:System.Windows.Forms.ListView>-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-115">Use the <xref:System.Windows.Forms.View> enumeration of the <xref:System.Windows.Forms.ListView> control.</span></span>  
  
    ```vb  
    ListView1.View = View.Tile  
    ```  
  
    ```csharp  
    listView1.View = View.Tile;  
    ```  
  
## <a name="example"></a><span data-ttu-id="ab9b6-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ab9b6-116">Example</span></span>  
 <span data-ttu-id="ab9b6-117">Die folgenden vollständigen Codebeispiele zeigen die Ansicht "Nebeneinander" mit Kacheln, die so geändert wurden, dass drei Textzeilen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-117">The following complete code example demonstrates Tile view with tiles modified to show three lines of text.</span></span> <span data-ttu-id="ab9b6-118">Die Kachelgröße wurde angepasst, um Zeilenumbrüche zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-118">The tile size has been adjusted to prevent line-wrapping.</span></span>  
  
 [!code-cpp[System.Windows.Forms.ListView.Tiling#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/CPP/listviewtilingexample.cpp#1)]
 [!code-csharp[System.Windows.Forms.ListView.Tiling#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/CS/listviewtilingexample.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.Tiling#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/VB/listviewtilingexample.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ab9b6-119">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="ab9b6-119">Compiling the Code</span></span>  
 <span data-ttu-id="ab9b6-120">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ab9b6-120">This example requires:</span></span>  
  
-   <span data-ttu-id="ab9b6-121">Verweise auf die Assemblys "System" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="ab9b6-121">References to the System and System.Windows.Forms assemblies.</span></span>  
  
-   <span data-ttu-id="ab9b6-122">Eine Symboldatei mit Namen "book.ico", die sich im selben Verzeichnis befinden wie die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-122">An icon file named book.ico in the same directory as the executable file.</span></span>  
  
 <span data-ttu-id="ab9b6-123">Informationen zum Erstellen dieses Beispiels über die Befehlszeile für Visual Basic oder Visual c# finden Sie unter [erstellen über die Befehlszeile](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) oder [Befehlszeile mit csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="ab9b6-123">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="ab9b6-124">Sie können auch in diesem Beispiel in Visual Studio erstellen, indem Sie den Code in ein neues Projekt einfügen.</span><span class="sxs-lookup"><span data-stu-id="ab9b6-124">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="ab9b6-125">Weitere Informationen hierzu finden Sie auch unter [Gewusst wie: Kompilieren und Ausführen einer vollständigen Windows Forms-Codebeispiels mit Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="ab9b6-125">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab9b6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab9b6-126">See also</span></span>
- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.TileSize%2A>
- [<span data-ttu-id="ab9b6-127">ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ab9b6-127">ListView Control</span></span>](../../../../docs/framework/winforms/controls/listview-control-windows-forms.md)
- [<span data-ttu-id="ab9b6-128">Übersicht über das ListView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ab9b6-128">ListView Control Overview</span></span>](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)
- [<span data-ttu-id="ab9b6-129">Windows XP-Features und Windows Forms-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="ab9b6-129">Windows XP Features and Windows Forms Controls</span></span>](https://msdn.microsoft.com/library/bc7fab94-fce9-4bf1-a8ad-a5837c91c3c0)
