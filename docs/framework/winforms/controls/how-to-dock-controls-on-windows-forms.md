---
title: 'Vorgehensweise: Andocken von Steuerelementen in Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], docking
- Explorer-style applications [Windows Forms], creating
- Windows Forms controls, filling client area
ms.assetid: bc11f2e4-e90a-4830-b0e2-f43b6e2b8bec
ms.openlocfilehash: f4a9d3bcf7f9db1634da2b2f06177c05061af28e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54733544"
---
# <a name="how-to-dock-controls-on-windows-forms"></a>Vorgehensweise: Andocken von Steuerelementen in Windows Forms
Sie können Andocken von Steuerelementen an den Rändern des Formulars oder Sie geben Sie im Container des Steuerelements (ein Formular oder ein Container-Steuerelement). Beispielsweise Windows-Explorer angedockt seine <xref:System.Windows.Forms.TreeView> Steuerelement auf der linken Seite des Fensters und die zugehörige <xref:System.Windows.Forms.ListView> Steuerelement auf die rechte Seite des Fensters. Verwenden der <xref:System.Windows.Forms.Control.Dock%2A> -Eigenschaft für alle sichtbaren Windows Forms-Steuerelemente, um den Andockmodus zu definieren.  
  
> [!NOTE]
>  Steuerelemente werden in umgekehrter Z-Reihenfolge angedockt.  
  
 Die <xref:System.Windows.Forms.Control.Dock%2A> -Eigenschaft interagiert mit der <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft. Weitere Informationen finden Sie unter [Übersicht über die AutoSize-Eigenschaft](../../../../docs/framework/winforms/controls/autosize-property-overview.md).  
  
### <a name="to-dock-a-control"></a>So docken Sie ein Steuerelement an  
  
1.  Wählen Sie das Steuerelement, das Sie andocken möchten.  
  
2.  Klicken Sie im Eigenschaftenfenster auf den Pfeil rechts neben der <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft.  
  
     Ein Editor wird mit einer Reihe von Feldern, die darstellt, die Kanten und der Mitte des Formulars angezeigt.  
  
3.  Klicken Sie auf die Schaltfläche ", die den Rand des Formulars darstellt, in dem das Steuerelement angedockt werden soll. Klicken Sie auf das mittlere Feld, um den Inhalt des Steuerelements Formular oder Containersteuerelement zu füllen. Klicken Sie auf **(keine)** zum Andocken zu deaktivieren.  
  
     Das Steuerelement wird automatische größenanpassung die Grenzen der verankerten Kante.  
  
    > [!NOTE]
    >  Geerbte Steuerelemente muss `Protected` angedockt werden kann. Um die Zugriffsebene eines Steuerelements zu ändern, legen Sie dessen **Modifizierer** Eigenschaft im Eigenschaftenfenster angezeigt.  
  
## <a name="see-also"></a>Siehe auch
- [Windows Forms-Steuerelemente](../../../../docs/framework/winforms/controls/index.md)
- [Anordnen von Steuerelementen in Windows Forms](../../../../docs/framework/winforms/controls/arranging-controls-on-windows-forms.md)
- [Beschriften einzelner Steuerelemente für Windows Forms und Konfigurieren von Shortcuts für diese Elemente](../../../../docs/framework/winforms/controls/labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [Windows Forms-Steuerelemente](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)
- [Windows Forms-Steuerelemente nach Funktion](../../../../docs/framework/winforms/controls/windows-forms-controls-by-function.md)
- [Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem FlowLayoutPanel-Steuerelement](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem TableLayoutPanel-Steuerelement](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [Übersicht über die AutoSize-Eigenschaft](../../../../docs/framework/winforms/controls/autosize-property-overview.md)
- [Vorgehensweise: Verankern von Steuerelementen in Windows Forms](../../../../docs/framework/winforms/controls/how-to-anchor-controls-on-windows-forms.md)
