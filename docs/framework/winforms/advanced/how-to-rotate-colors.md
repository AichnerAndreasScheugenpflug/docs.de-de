---
title: 'Vorgehensweise: Drehen von Farben'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], rotating
- examples [Windows Forms], rotating colors
ms.assetid: e2e4c300-159c-4f4a-9b56-103b0f7cbc05
ms.openlocfilehash: 6c4f41504911e94673707d99d804fad5b228599e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54503064"
---
# <a name="how-to-rotate-colors"></a><span data-ttu-id="517dc-102">Vorgehensweise: Drehen von Farben</span><span class="sxs-lookup"><span data-stu-id="517dc-102">How to: Rotate Colors</span></span>
<span data-ttu-id="517dc-103">Drehung in einer vierdimensionalen Farbraum ist schwierig, zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="517dc-103">Rotation in a four-dimensional color space is difficult to visualize.</span></span> <span data-ttu-id="517dc-104">Wir können es vorstellbar, stimmen zu einer der festen Farbkomponenten vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="517dc-104">We can make it easier to visualize rotation by agreeing to keep one of the color components fixed.</span></span> <span data-ttu-id="517dc-105">Nehmen wir an, dass in jedem die alpha-Komponente auf 1 festgesetzt (vollständig deckend) beibehalten.</span><span class="sxs-lookup"><span data-stu-id="517dc-105">Suppose we agree to keep the alpha component fixed at 1 (fully opaque).</span></span> <span data-ttu-id="517dc-106">Dann können wir einen dreidimensionalen Farbraum mit roten, grünen und blauen Achsen visualisieren, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="517dc-106">Then we can visualize a three-dimensional color space with red, green, and blue axes as shown in the following illustration.</span></span>  
  
 <span data-ttu-id="517dc-107">![Recoloring](../../../../docs/framework/winforms/advanced/media/recoloring03.gif "recoloring03")</span><span class="sxs-lookup"><span data-stu-id="517dc-107">![Recoloring](../../../../docs/framework/winforms/advanced/media/recoloring03.gif "recoloring03")</span></span>  
  
 <span data-ttu-id="517dc-108">Eine Farbe kann als ein Punkt im 3D-Raum betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="517dc-108">A color can be thought of as a point in 3-D space.</span></span> <span data-ttu-id="517dc-109">Beispielsweise wird der Punkt im Raum (1, 0, 0) darstellt, die Farbe Rot, und der Punkt im Raum (0, 1, 0) darstellt, die Farbe Grün.</span><span class="sxs-lookup"><span data-stu-id="517dc-109">For example, the point (1, 0, 0) in space represents the color red, and the point (0, 1, 0) in space represents the color green.</span></span>  
  
 <span data-ttu-id="517dc-110">Die folgende Abbildung zeigt was es bedeutet, die die Farbe (1, 0, 0) gedreht, über einen Winkel von 60 Grad in der Rot-Grün-Ebene.</span><span class="sxs-lookup"><span data-stu-id="517dc-110">The following illustration shows what it means to rotate the color (1, 0, 0) through an angle of 60 degrees in the Red-Green plane.</span></span> <span data-ttu-id="517dc-111">Drehung in einer Ebene Parallel zur Rot-Grün-Ebene kann als Drehung um die blauen Achse betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="517dc-111">Rotation in a plane parallel to the Red-Green plane can be thought of as rotation about the blue axis.</span></span>  
  
 <span data-ttu-id="517dc-112">![Recoloring](../../../../docs/framework/winforms/advanced/media/recoloring04.gif "recoloring04")</span><span class="sxs-lookup"><span data-stu-id="517dc-112">![Recoloring](../../../../docs/framework/winforms/advanced/media/recoloring04.gif "recoloring04")</span></span>  
  
 <span data-ttu-id="517dc-113">In der folgende Abbildung wird veranschaulicht, wie eine Farbmatrix zum Ausführen der Rotation zu jeder der drei Koordinatenachsen (Rot, Grün, Blau) initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="517dc-113">The following illustration shows how to initialize a color matrix to perform rotations about each of the three coordinate axes (red, green, blue).</span></span>  
  
 <span data-ttu-id="517dc-114">![Recoloring](../../../../docs/framework/winforms/advanced/media/recoloring05.gif "recoloring05")</span><span class="sxs-lookup"><span data-stu-id="517dc-114">![Recoloring](../../../../docs/framework/winforms/advanced/media/recoloring05.gif "recoloring05")</span></span>  
  
## <a name="example"></a><span data-ttu-id="517dc-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="517dc-115">Example</span></span>  
 <span data-ttu-id="517dc-116">Im folgenden Beispiel wird ein Bild, das alle eine Farbe ("1", "0", "0,6") und wendet eine Drehung um 60 Grad die blaue Achse an.</span><span class="sxs-lookup"><span data-stu-id="517dc-116">The following example takes an image that is all one color (1, 0, 0.6) and applies a 60-degree rotation about the blue axis.</span></span> <span data-ttu-id="517dc-117">Der Winkel der Drehung wird sich in einer Ebene überflüssig, die parallel zu der Rot-Grün-Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="517dc-117">The angle of the rotation is swept out in a plane that is parallel to the red-green plane.</span></span>  
  
 <span data-ttu-id="517dc-118">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das Bild Farben gedreht, auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="517dc-118">The following illustration shows the original image on the left and the color-rotated image on the right.</span></span>  
  
 <span data-ttu-id="517dc-119">![Drehen von Farben](../../../../docs/framework/winforms/advanced/media/colortrans5.png "colortrans5")</span><span class="sxs-lookup"><span data-stu-id="517dc-119">![Rotate Colors](../../../../docs/framework/winforms/advanced/media/colortrans5.png "colortrans5")</span></span>  
  
 <span data-ttu-id="517dc-120">Die folgende Abbildung zeigt eine Visualisierung der Color-Drehung, die in den folgenden Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="517dc-120">The following illustration shows a visualization of the color rotation performed in the following code.</span></span>  
  
 <span data-ttu-id="517dc-121">![Recoloring](../../../../docs/framework/winforms/advanced/media/recoloring06.gif "recoloring06")</span><span class="sxs-lookup"><span data-stu-id="517dc-121">![Recoloring](../../../../docs/framework/winforms/advanced/media/recoloring06.gif "recoloring06")</span></span>  
  
 [!code-csharp[System.Drawing.RotateColors#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RotateColors/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.RotateColors#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RotateColors/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="517dc-122">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="517dc-122">Compiling the Code</span></span>  
 <span data-ttu-id="517dc-123">Das obige Beispiel ist für die Verwendung mit Windows Forms konzipiert und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e`, ein Parameter von der <xref:System.Windows.Forms.Control.Paint> -Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="517dc-123">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="517dc-124">Ersetzen Sie dies `RotationInput.bmp` mit einer Bilddateinamen gültigen und Pfad auf Ihrem System.</span><span class="sxs-lookup"><span data-stu-id="517dc-124">Replace `RotationInput.bmp` with an image file name and path valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="517dc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="517dc-125">See also</span></span>
- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [<span data-ttu-id="517dc-126">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="517dc-126">Graphics and Drawing in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="517dc-127">Neufärben von Bildern</span><span class="sxs-lookup"><span data-stu-id="517dc-127">Recoloring Images</span></span>](../../../../docs/framework/winforms/advanced/recoloring-images.md)
