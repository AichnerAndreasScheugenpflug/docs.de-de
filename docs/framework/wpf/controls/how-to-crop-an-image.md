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
# <a name="how-to-crop-an-image"></a>Vorgehensweise: Zuschneiden eines Bilds
Dieses Beispiel zeigt, wie Sie ein Bild mit Zuschneiden <xref:System.Windows.Media.Imaging.CroppedBitmap>.  
  
 <xref:System.Windows.Media.Imaging.CroppedBitmap> Bei der Codierung einer zugeschnittenen Version eines Bilds wird in erster Linie, die sich in einer Datei speichern verwendet werden. Zum Zuschneiden eines Bilds zu Anzeigezwecken finden Sie die [erstellen Sie einen Clip-Bereich](https://msdn.microsoft.com/library/56e4bed6-78d7-4292-b917-d72d0b3e4376) Thema.  
  
## <a name="example"></a>Beispiel  
 Die folgenden [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] definiert Ressourcen, die in den folgenden Beispielen verwendet.  
  
 [!code-xaml[imageelementexample#CroppedXAML1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml1)]  
  
 Das folgende Beispiel erstellt ein Image mit einem <xref:System.Windows.Media.Imaging.CroppedBitmap> als Quelle.  
  
 [!code-xaml[imageelementexample#CroppedXAML2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml2)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp1)]
 [!code-vb[imageelementexample#CroppedCSharp1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp1)]  
  
 Die <xref:System.Windows.Media.Imaging.CroppedBitmap> kann auch verwendet werden, als Quelle eines anderen <xref:System.Windows.Media.Imaging.CroppedBitmap>, das Zuschneiden zu verketten. Beachten Sie, dass die <xref:System.Windows.Media.Imaging.CroppedBitmap.SourceRect%2A> verwendet Werte, die relativ zum zugeschnittenen Bitmap und nicht das erste Bild sind.  
  
 [!code-xaml[imageelementexample#CroppedXAML3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml#croppedxaml3)]  
  
 [!code-csharp[imageelementexample#CroppedCSharp2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImageElementExample/CSharp/CroppedImageExample.xaml.cs#croppedcsharp2)]
 [!code-vb[imageelementexample#CroppedCSharp2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImageElementExample/VB/CroppedImageExample.xaml.vb#croppedcsharp2)]  
  
## <a name="see-also"></a>Siehe auch
- [Erstellen Sie einen Clip-Bereich](https://msdn.microsoft.com/library/56e4bed6-78d7-4292-b917-d72d0b3e4376)
