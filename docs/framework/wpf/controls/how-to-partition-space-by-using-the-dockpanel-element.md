---
title: 'Vorgehensweise: Aufteilen von Bereichen mithilfe des DockPanel-Elements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [WPF], DockPanel
- DockPanel control [WPF], partitioning space
- partitioning space [WPF]
ms.assetid: a219b9e5-b205-4438-89b5-0a137ac463ab
ms.openlocfilehash: 8b79b89e512ec9da27774188aeaeed8ebd5b1153
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577658"
---
# <a name="how-to-partition-space-by-using-the-dockpanel-element"></a>Vorgehensweise: Aufteilen von Bereichen mithilfe des DockPanel-Elements
Das folgende Beispiel erstellt eine einfache [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] Framework mit einer <xref:System.Windows.Controls.DockPanel> Element. Die <xref:System.Windows.Controls.DockPanel> teilt den verfügbaren Platz für seine untergeordneten Elemente.  
  
## <a name="example"></a>Beispiel  
 Dieses Beispiel verwendet die <xref:System.Windows.Controls.DockPanel.Dock%2A> -Eigenschaft, die eine angefügte Eigenschaft, um zwei identische anzudocken <xref:System.Windows.Controls.Border> Elemente an die <xref:System.Windows.Controls.Dock.Top> des aufgeteilten Bereichs. Eine dritte <xref:System.Windows.Controls.Border> Elements angedockt ist die <xref:System.Windows.Controls.Dock.Left>, dessen Breite auf 200 Pixel festgelegt. Eine vierte <xref:System.Windows.Controls.Border> angedockt ist die <xref:System.Windows.Controls.Dock.Bottom> des Bildschirms. Die letzte <xref:System.Windows.Controls.Border> Elements den verbleibenden Platz ausfüllt.  
  
 [!code-cpp[DockPanelOvwSample#1](../../../../samples/snippets/cpp/VS_Snippets_Wpf/DockPanelOvwSample/CPP/DockPanel_Ovw_Sample.cpp#1)]
 [!code-csharp[DockPanelOvwSample#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DockPanelOvwSample/CSharp/DockPanel_Ovw_Sample.cs#1)]
 [!code-vb[DockPanelOvwSample#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DockPanelOvwSample/VisualBasic/dockpanel_vb.vb#1)]
 [!code-xaml[DockPanelOvwSample#1](../../../../samples/snippets/xaml/VS_Snippets_Wpf/DockPanelOvwSample/XAML/default.xaml#1)]  
  
> [!NOTE]
>  Standardmäßig ist das letzte untergeordnete Element von einem <xref:System.Windows.Controls.DockPanel> Element füllt die verbleibenden verfügbaren Speicherplatz. Wenn Sie dieses Verhalten nicht wünschen, legen Sie `LastChildFill="False"` fest.  
  
 Die kompilierte Anwendung gibt eine neue Benutzeroberfläche aus, die folgendermaßen aussieht.  
  
 ![Ein typisches DockPanel-Szenario.](../../../../docs/framework/wpf/controls/media/panel-intro-dockpanel.PNG "Panel_intro_dockpanel")  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Windows.Controls.DockPanel>
- [Übersicht über Panel-Elemente](../../../../docs/framework/wpf/controls/panels-overview.md)
