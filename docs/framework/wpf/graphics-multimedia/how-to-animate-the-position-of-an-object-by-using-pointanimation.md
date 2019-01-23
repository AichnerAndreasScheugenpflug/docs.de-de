---
title: 'Vorgehensweise: Animieren der Position eines Objekts mit Punktanimation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], animation
- animation [WPF], PointAnimation
ms.assetid: 42310977-cc90-438a-8a47-0345898e01be
ms.openlocfilehash: e359e712f533c861a694c53848ca0eaeb289eb21
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54495552"
---
# <a name="how-to-animate-the-position-of-an-object-by-using-pointanimation"></a>Vorgehensweise: Animieren der Position eines Objekts mit Punktanimation
Dieses Beispiel zeigt, wie Sie mit der <xref:System.Windows.Media.Animation.PointAnimation> -Klasse zum Animieren eines Objekts entlang einer <xref:System.Windows.Shapes.Path>.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine Ellipse entlang einer <xref:System.Windows.Shapes.Path> von einem Punkt auf dem Bildschirm in eine andere. Im Beispiel wird die Position des animiert ein <xref:System.Windows.Media.EllipseGeometry> mit <xref:System.Windows.Media.Animation.PointAnimation> zum Animieren der <xref:System.Windows.Media.EllipseGeometry.Center%2A> Eigenschaft.  
  
 [!code-csharp[BasicAnimations_snip#PointAnimationWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/PointAnimationExample.cs#pointanimationwholepage)]
 [!code-vb[BasicAnimations_snip#PointAnimationWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/PointAnimationExample.vb#pointanimationwholepage)]  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Windows.Media.Animation.PointAnimation>
- <xref:System.Windows.Shapes.Path>
- <xref:System.Windows.Media.EllipseGeometry>
- <xref:System.Windows.Media.EllipseGeometry.Center%2A>
- [Übersicht über Animationen](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [Grafiken und Multimedia](../../../../docs/framework/wpf/graphics-multimedia/index.md)
- [Themen zu Vorgehensweisen](../../../../docs/framework/wpf/graphics-multimedia/graphics-how-to-topics.md)
- [Animations- und Zeitsteuerungssystem](https://msdn.microsoft.com/library/7d83765b-d5ae-41b1-b423-80206e1124aa)
- [Themen zu Vorgehensweisen](../../../../docs/framework/wpf/graphics-multimedia/animation-and-timing-how-to-topics.md)
