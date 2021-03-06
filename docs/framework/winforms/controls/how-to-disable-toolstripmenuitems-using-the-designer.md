---
title: 'Vorgehensweise: Deaktivieren von ToolStripMenuItems mithilfe des Designers'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], disabling in designer
- MenuStrip control [Windows Forms], disabling menu items in designer
- menu items [Windows Forms], disabling
- menus [Windows Forms], disabling items
ms.assetid: 985e311e-7d67-4205-b5a3-d045b68a4a03
ms.openlocfilehash: e4506da2fd41a78ff8f8643a630abc4992fc5a87
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54644988"
---
# <a name="how-to-disable-toolstripmenuitems-using-the-designer"></a>Vorgehensweise: Deaktivieren von ToolStripMenuItems mithilfe des Designers
Können Sie einschränken oder erweitern die Befehle, die ein Benutzer aktivieren und Deaktivieren von Menüelementen in Benutzeraktivitäten herstellen kann. Menüelemente sind standardmäßig aktiviert, wenn sie erstellt wurden, aber dies die angepasst werden kann, über die <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> Eigenschaft. Sie können diese Eigenschaft zur Entwurfszeit im Bearbeiten der **Eigenschaften** Fenster oder programmgesteuert, indem sie im Code festlegen. Weitere Informationen finden Sie unter [Vorgehensweise: Deaktivieren von ToolStripMenuItems](../../../../docs/framework/winforms/controls/how-to-disable-toolstripmenuitems.md).  
  
> [!NOTE]
>  Je nach den aktiven Einstellungen oder der Version unterscheiden sich die Dialogfelder und Menübefehle auf Ihrem Bildschirm möglicherweise von den in der Hilfe beschriebenen. Klicken Sie im Menü **Extras** auf **Einstellungen importieren und exportieren** , um die Einstellungen zu ändern. Weitere Informationen finden Sie unter [Personalisieren von Visual Studio-IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-disable-a-menu-item-at-design-time"></a>So deaktivieren Sie ein Menüelement zur Entwurfszeit  
  
1.  Mit dem Menüelement, auf das Formular ausgewählt haben, legen Sie die <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> Eigenschaft `false`.  
  
    > [!TIP]
    >  Deaktivieren das erste oder der obersten Ebene Menüelement in einem Menü, deaktiviert alle Menüelemente im Menü enthalten. Ebenso wird beim Deaktivieren eines Menüelements, das über Untermenüelemente verfügt die Untermenüelemente deaktiviert. Wenn alle Befehle in einem bestimmten Menü für den Benutzer nicht verfügbar sind, gilt die guten Programmierstil, ausgeblendet und deaktiviert das gesamte Menü, wie dies führt zu eine sauberen-Benutzeroberfläche. Sie sollten auch deaktivieren Sie im Menü wie ausblenden, die nur Zugriff auf einen Menübefehl über eine Tastenkombination nicht verhindert wird. Legen Sie die <xref:System.Windows.Forms.ToolStripItem.Visible%2A> Eigenschaft eines Elements zum Menü der obersten Ebene `false` das gesamte Menü ausblenden.  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [Vorgehensweise: Ausblenden von ToolStripMenuItems](../../../../docs/framework/winforms/controls/how-to-hide-toolstripmenuitems.md)
- [Übersicht über das MenuStrip-Steuerelement](../../../../docs/framework/winforms/controls/menustrip-control-overview-windows-forms.md)
