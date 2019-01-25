---
title: 'Vorgehensweise: Zeichnen von Text mit GDI'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- GDI [Windows Forms], drawing text [Windows Forms]
- text [Windows Forms], drawing with TextRenderer
- drawing [Windows Forms], text
- Windows Forms, drawing text with GDI
ms.assetid: 2a19fe5d-2ace-451c-94db-01cb1118ef7b
ms.openlocfilehash: 3cb67f01f145a55e4e8a68642a37ad287ee94b1a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54685921"
---
# <a name="how-to-draw-text-with-gdi"></a><span data-ttu-id="51464-102">Vorgehensweise: Zeichnen von Text mit GDI</span><span class="sxs-lookup"><span data-stu-id="51464-102">How to: Draw Text with GDI</span></span>
<span data-ttu-id="51464-103">Mit der <xref:System.Windows.Forms.TextRenderer.DrawText%2A> -Methode in der die <xref:System.Windows.Forms.TextRenderer> -Klasse, die Sie zugreifen können [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)] Funktionen zum Zeichnen von Text in einem Formular oder Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="51464-103">With the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> method in the <xref:System.Windows.Forms.TextRenderer> class, you can access [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)] functionality for drawing text on a form or control.</span></span> [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)] <span data-ttu-id="51464-104">Rendern von Text in der Regel bietet, eine bessere Leistung und genauere Messung als Text [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)].</span><span class="sxs-lookup"><span data-stu-id="51464-104">text rendering typically offers better performance and more accurate text measuring than [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)].</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="51464-105">Die <xref:System.Windows.Forms.TextRenderer.DrawText%2A> Methoden der <xref:System.Windows.Forms.TextRenderer> Klasse werden zum Drucken nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51464-105">The <xref:System.Windows.Forms.TextRenderer.DrawText%2A> methods of the <xref:System.Windows.Forms.TextRenderer> class are not supported for printing.</span></span> <span data-ttu-id="51464-106">Beim Drucken, verwenden Sie immer die <xref:System.Drawing.Graphics.DrawString%2A> Methoden der <xref:System.Drawing.Graphics> Klasse.</span><span class="sxs-lookup"><span data-stu-id="51464-106">When printing, always use the <xref:System.Drawing.Graphics.DrawString%2A> methods of the <xref:System.Drawing.Graphics> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="51464-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="51464-107">Example</span></span>  
 <span data-ttu-id="51464-108">Im folgenden Codebeispiel wird veranschaulicht, wie zum Zeichnen von Text auf mehrere Zeilen in einem Rechteck mithilfe der <xref:System.Windows.Forms.TextRenderer.DrawText%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="51464-108">The following code example demonstrates how to draw text on multiple lines within a rectangle using the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> method.</span></span>  
  
 [!code-csharp[System.Windows.Forms.TextRendererExamples#7](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TextRendererExamples/CS/Form1.cs#7)]
 [!code-vb[System.Windows.Forms.TextRendererExamples#7](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TextRendererExamples/VB/Form1.vb#7)]  
  
 <span data-ttu-id="51464-109">Zum Rendern von Text mit der <xref:System.Windows.Forms.TextRenderer> -Klasse, die Sie benötigen ein <xref:System.Drawing.IDeviceContext>, z. B. eine <xref:System.Drawing.Graphics> und ein <xref:System.Drawing.Font>, einen Speicherort zum Zeichnen von Text und die Farbe, in denen es gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51464-109">To render text with the <xref:System.Windows.Forms.TextRenderer> class, you need an <xref:System.Drawing.IDeviceContext>, such as a <xref:System.Drawing.Graphics> and a <xref:System.Drawing.Font>, a location to draw the text, and the color in which it should be drawn.</span></span> <span data-ttu-id="51464-110">Optional können Sie angeben, die textformatierung, die mithilfe der <xref:System.Windows.Forms.TextFormatFlags> Enumeration.</span><span class="sxs-lookup"><span data-stu-id="51464-110">Optionally, you can specify the text formatting by using the <xref:System.Windows.Forms.TextFormatFlags> enumeration.</span></span>  
  
 <span data-ttu-id="51464-111">Weitere Informationen zum Abrufen einer <xref:System.Drawing.Graphics>, finden Sie unter [Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen](../../../../docs/framework/winforms/advanced/how-to-create-graphics-objects-for-drawing.md).</span><span class="sxs-lookup"><span data-stu-id="51464-111">For more information about obtaining a <xref:System.Drawing.Graphics>, see [How to: Create Graphics Objects for Drawing](../../../../docs/framework/winforms/advanced/how-to-create-graphics-objects-for-drawing.md).</span></span> <span data-ttu-id="51464-112">Weitere Informationen zum Erstellen einer <xref:System.Drawing.Font>, finden Sie unter [Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten](../../../../docs/framework/winforms/advanced/how-to-construct-font-families-and-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="51464-112">For more information about constructing a <xref:System.Drawing.Font>, see [How to: Construct Font Families and Fonts](../../../../docs/framework/winforms/advanced/how-to-construct-font-families-and-fonts.md).</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="51464-113">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="51464-113">Compiling the Code</span></span>  
 <span data-ttu-id="51464-114">Das vorherige Codebeispiel ist für die Verwendung mit Windows Forms konzipiert und erfordert die <xref:System.Windows.Forms.PaintEventArgs> `e`, d.h. ein Parameter vom <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="51464-114">The preceding code example is designed for use with Windows Forms, and it requires the <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51464-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51464-115">See also</span></span>
- <xref:System.Windows.Forms.TextRenderer>
- <xref:System.Drawing.Font>
- <xref:System.Drawing.Color>
- <xref:System.Drawing.Color>
- [<span data-ttu-id="51464-116">Verwenden von Schriftarten und Text</span><span class="sxs-lookup"><span data-stu-id="51464-116">Using Fonts and Text</span></span>](../../../../docs/framework/winforms/advanced/using-fonts-and-text.md)
