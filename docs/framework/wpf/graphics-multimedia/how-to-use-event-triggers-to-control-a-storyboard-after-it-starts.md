---
title: 'Vorgehensweise: Verwenden von Ereignistriggern zum Steuern eines Storyboards nach dessen Start'
ms.date: 03/30/2017
helpviewer_keywords:
- triggers [WPF], controlling Storyboards
- event triggers [WPF], controlling Storyboards
- Storyboards [WPF], controlling after start
ms.assetid: 3b115594-6a93-4972-b24d-61aa16f1c15f
ms.openlocfilehash: e4cfaf2352c3cca2b67a8e6a5d4c933399583e5a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663647"
---
# <a name="how-to-use-event-triggers-to-control-a-storyboard-after-it-starts"></a>Vorgehensweise: Verwenden von Ereignistriggern zum Steuern eines Storyboards nach dessen Start
Dieses Beispiel zeigt, wie Sie steuern eine <xref:System.Windows.Media.Animation.Storyboard> nachdem es gestartet wurde. Starten einer <xref:System.Windows.Media.Animation.Storyboard> mit [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], verwenden Sie <xref:System.Windows.Media.Animation.BeginStoryboard>, das verteilt der Animationen an die Objekte und Eigenschaften, die sie animieren, und klicken Sie dann das Storyboard gestartet wird. Wenn Sie geben <xref:System.Windows.Media.Animation.BeginStoryboard> einen Namen durch Angabe der <xref:System.Windows.Media.Animation.BeginStoryboard.Name%2A> -Eigenschaft, Sie machen es ein steuerbares Storyboard. Sie können das Storyboard dann interaktiv steuern, nachdem es gestartet wurde.  
  
 Verwenden Sie die folgenden Storyboard Aktionen zusammen mit <xref:System.Windows.EventTrigger> Objekte zum Steuern eines Storyboards.  
  
-   <xref:System.Windows.Media.Animation.PauseStoryboard>: Hält das Storyboard an.  
  
-   <xref:System.Windows.Media.Animation.ResumeStoryboard>: Setzt ein angehaltenes Storyboard fort.  
  
-   <xref:System.Windows.Media.Animation.SetStoryboardSpeedRatio>: Ändert die Geschwindigkeit des Storyboards.  
  
-   <xref:System.Windows.Media.Animation.SkipStoryboardToFill>: Setzt ein Storyboard an das Ende seines Füllbereichs, sofern vorhanden.  
  
-   <xref:System.Windows.Media.Animation.StopStoryboard>: Hält das Storyboard an.  
  
-   <xref:System.Windows.Media.Animation.RemoveStoryboard>: Entfernt das Storyboard, das Freigeben von Ressourcen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird die Aktionen des steuerbaren Storyboards zum interaktiven Steuern eines Storyboards.  
  
 **Hinweis**: Ein Beispiel zum Steuern eines Storyboards mithilfe von Code finden Sie unter [steuern Sie ein Storyboard nach es beginnt mithilfe von einem interaktiven Methoden](../../../../docs/framework/wpf/graphics-multimedia/how-to-control-a-storyboard-after-it-starts.md).  
  
 [!code-xaml[timingbehaviors_snip#ControlStoryboardExampleUsingWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/ControlStoryboardExample.xaml#controlstoryboardexampleusingwholepage)]  
  
 Weitere Beispiele finden Sie unter den [Beispielsammlung](https://go.microsoft.com/fwlink/?LinkID=159969).  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Windows.Media.Animation.ResumeStoryboard>
- <xref:System.Windows.Media.Animation.SetStoryboardSpeedRatio>
- <xref:System.Windows.Media.Animation.SkipStoryboardToFill>
- <xref:System.Windows.Media.Animation.PauseStoryboard>
- <xref:System.Windows.Media.Animation.StopStoryboard>
- <xref:System.Windows.Media.Animation.SeekStoryboard>
- [Interaktives Steuern eines Storyboards, nachdem es gestartet wurde](../../../../docs/framework/wpf/graphics-multimedia/how-to-control-a-storyboard-after-it-starts.md)
- [Übersicht über Animationen](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [Übersicht über Storyboards](../../../../docs/framework/wpf/graphics-multimedia/storyboards-overview.md)
