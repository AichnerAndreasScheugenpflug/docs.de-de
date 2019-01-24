---
title: 'Vorgehensweise: Zuschneiden eines Bilds'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [WPF], cropping
- cropping images [WPF]
ms.assetid: c6bba109-c6e7-4cf8-bfe6-9cf8d01bb4fc
ms.openlocfilehash: fbd15ea6c5c47aa090829754402cc3a6926654d8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663965"
---
# <a name="how-to-crop-an-image"></a><span data-ttu-id="5b12e-102">Vorgehensweise: Zuschneiden eines Bilds</span><span class="sxs-lookup"><span data-stu-id="5b12e-102">How to: Crop an Image</span></span>
<span data-ttu-id="5b12e-103">Dieses Beispiel zeigt, wie Sie ein Bild mit Zuschneiden <xref:System.Windows.Media.Imaging.CroppedBitmap>.</span><span class="sxs-lookup"><span data-stu-id="5b12e-103">This example shows how to crop an image using <xref:System.Windows.Media.Imaging.CroppedBitmap>.</span></span>  
  
 <span data-ttu-id="5b12e-104"><xref:System.Windows.Media.Imaging.CroppedBitmap> Bei der Codierung einer zugeschnittenen Version eines Bilds wird in erster Linie, die sich in einer Datei speichern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b12e-104"><xref:System.Windows.Media.Imaging.CroppedBitmap> is primarily used when encoding a cropped version of an image to save out to a file.</span></span> <span data-ttu-id="5b12e-105">Zum Zuschneiden eines Bilds zu Anzeigezwecken finden Sie die [erstellen Sie einen Clip-Bereich](https://msdn.microsoft.com/library/56e4bed6-78d7-4292-b917-d72d0b3e4376) Thema.</span><span class="sxs-lookup"><span data-stu-id="5b12e-105">To crop an image for display purposes see the [Create a Clip Region](https://msdn.microsoft.com/library/56e4bed6-78d7-4292-b917-d72d0b3e4376) topic.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5b12e-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5b12e-106">Example</span></span>  
 <span data-ttu-id="5b12e-107">Die folgenden [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] definiert Ressourcen, die in den folgenden Beispielen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b12e-107">The following [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] defines resources used within the samples below.</span></span>  
  
 [!code-xaml[imageelementexample#CroppedXAML1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml1)]  
  
 <span data-ttu-id="5b12e-108">Das folgende Beispiel erstellt ein Image mit einem <xref:System.Windows.Media.Imaging.CroppedBitmap> als Quelle.</span><span class="sxs-lookup"><span data-stu-id="5b12e-108">The following example creates an image using a <xref:System.Windows.Media.Imaging.CroppedBitmap> as its source.</span></span>  
  
 [!code-xaml[imageelementexample#CroppedXAML2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml2)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp1)]
 [!code-vb[imageelementexample#CroppedCSharp1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp1)]  
  
 <span data-ttu-id="5b12e-109">Die <xref:System.Windows.Media.Imaging.CroppedBitmap> kann auch verwendet werden, als Quelle eines anderen <xref:System.Windows.Media.Imaging.CroppedBitmap>, das Zuschneiden zu verketten.</span><span class="sxs-lookup"><span data-stu-id="5b12e-109">The <xref:System.Windows.Media.Imaging.CroppedBitmap> can also be used as the source of another <xref:System.Windows.Media.Imaging.CroppedBitmap>, chaining the cropping.</span></span> <span data-ttu-id="5b12e-110">Beachten Sie, dass die <xref:System.Windows.Media.Imaging.CroppedBitmap.SourceRect%2A> verwendet Werte, die relativ zum zugeschnittenen Bitmap und nicht das erste Bild sind.</span><span class="sxs-lookup"><span data-stu-id="5b12e-110">Note that the <xref:System.Windows.Media.Imaging.CroppedBitmap.SourceRect%2A> uses values that are relative to the source cropped bitmap and not the initial image.</span></span>  
  
 [!code-xaml[imageelementexample#CroppedXAML3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml3)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp2)]
 [!code-vb[imageelementexample#CroppedCSharp2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp2)]  
  
## <a name="see-also"></a><span data-ttu-id="5b12e-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b12e-111">See also</span></span>
- [<span data-ttu-id="5b12e-112">Erstellen Sie einen Clip-Bereich</span><span class="sxs-lookup"><span data-stu-id="5b12e-112">Create a Clip Region</span></span>](https://msdn.microsoft.com/library/56e4bed6-78d7-4292-b917-d72d0b3e4376)
