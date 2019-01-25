---
title: 'Vorgehensweise: Animieren einer Eigenschaft ohne Storyboard'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- non-Storyboard animation
- local animation [WPF]
- animation [WPF], non-Storyboard (local)
ms.assetid: d411db70-4df7-487d-82bc-95a7c1b2e7f8
ms.openlocfilehash: f2cb3533010579f912da62cb2f7fe28d982890c7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54678134"
---
# <a name="how-to-animate-a-property-without-using-a-storyboard"></a>Vorgehensweise: Animieren einer Eigenschaft ohne Storyboard
Dieses Beispiel zeigt eine Möglichkeit, eine Animation auf eine Eigenschaft anwenden, ohne eine <xref:System.Windows.Media.Animation.Storyboard>.  
  
> [!NOTE]
>  Diese Funktionalität ist in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] nicht verfügbar. Informationen über das Animieren einer Eigenschaft in [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] finden Sie unter [Vorgehensweise: Animieren einer Eigenschaft unter Verwendung eines Storyboards](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-property-by-using-a-storyboard.md).  
  
 Um eine lokale Animation auf eine Eigenschaft anzuwenden, verwenden die <xref:System.Windows.UIElement.BeginAnimation%2A> Methode. Diese Methode akzeptiert zwei Parameter: eine <xref:System.Windows.DependencyProperty> , der angibt, die zu animierende Eigenschaft, und die Animation, auf die Eigenschaft angewendet.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt, wie Sie die Breite und Hintergrundfarbe Farbe Animieren einer <xref:System.Windows.Controls.Button>.  
  
 [!code-cpp[animateproperty#11](../../../../samples/snippets/cpp/VS_Snippets_Wpf/animateproperty/CPP/LocalAnimationExample.cpp#11)]
 [!code-csharp[animateproperty#11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/animateproperty/CSharp/LocalAnimationExample.cs#11)]
 [!code-vb[animateproperty#11](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/animateproperty/VisualBasic/LocalAnimationExample.vb#11)]  
  
 Eine Reihe von Animationsklassen in die <xref:System.Windows.Media.Animation> Namespace, die für das Animieren von verschiedenen Eigenschaften vorhanden sind. Weitere Informationen über das Animieren von Eigenschaften finden Sie unter [Übersicht über Animationen](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md). Weitere Informationen über Abhängigkeitseigenschaften (der Eigenschaftentyp, der in diesen Beispielen verwendet wird) und ihre Funktionen finden Sie unter [Übersicht über Abhängigkeitseigenschaften](../../../../docs/framework/wpf/advanced/dependency-properties-overview.md).  
  
 Es gibt andere Möglichkeiten für Animationen ohne <xref:System.Windows.Media.Animation.Storyboard> Objekte; Weitere Informationen finden Sie unter [Eigenschaft Techniken-Übersicht über Animationen](../../../../docs/framework/wpf/graphics-multimedia/property-animation-techniques-overview.md).  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Windows.Media.Animation.AnimationTimeline>
- <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A>
- <xref:System.Windows.Media.Animation>
- <xref:System.Windows.Media.Animation.Storyboard>
- [Übersicht über die Verfahren zur Animation von Eigenschaften](../../../../docs/framework/wpf/graphics-multimedia/property-animation-techniques-overview.md)
- [Übersicht über Animationen](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
