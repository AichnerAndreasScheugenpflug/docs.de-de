---
title: 'Vorgehensweise: Festlegen einer Windows Forms-Schaltfläche als "Abbrechen"-Schaltfläche mithilfe des Designers'
ms.date: 03/30/2017
helpviewer_keywords:
- buttons [Windows Forms], cancel buttons
- Button control [Windows Forms], designating as cancel button
ms.assetid: 30e77d9c-d565-4ab5-a84a-62c043af8822
ms.openlocfilehash: 9d11528d7d7fed13f531faeb09f38c4564f970be
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520476"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-cancel-button-using-the-designer"></a>Vorgehensweise: Festlegen einer Windows Forms-Schaltfläche als "Abbrechen"-Schaltfläche mithilfe des Designers
Auf jedem Windows-Formular, Sie können festlegen, eine <xref:System.Windows.Forms.Button> Steuerelement die Schaltfläche "Abbrechen". Schaltfläche "Abbrechen" geklickt wird, wenn der Benutzer die ESC-Taste drückt, unabhängig davon, die welche anderen Formular auf das Steuerelement den Fokus besitzt. Eine solche Schaltfläche programmiert wird in der Regel dem Benutzer ermöglichen, schnell einen Vorgang beendet, ohne dass eine Aktion.  
  
> [!NOTE]
>  Je nach den aktiven Einstellungen oder der Version unterscheiden sich die Dialogfelder und Menübefehle auf Ihrem Bildschirm möglicherweise von den in der Hilfe beschriebenen. Klicken Sie im Menü **Extras** auf **Einstellungen importieren und exportieren** , um die Einstellungen zu ändern. Weitere Informationen finden Sie unter [Personalisieren von Visual Studio-IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-designate-the-cancel-button"></a>Um die Schaltfläche "Abbrechen" zu kennzeichnen.  
  
1.  Wählen Sie das Formular, das auf dem sich die Schaltfläche befindet.  
  
2.  In der **Eigenschaften** legen des Formulars <xref:System.Windows.Forms.Form.CancelButton%2A> Eigenschaft, um die <xref:System.Windows.Forms.Button> Name des Steuerelements.  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Windows.Forms.Form.CancelButton%2A>
- [Übersicht über das Button-Steuerelement](../../../../docs/framework/winforms/controls/button-control-overview-windows-forms.md)
- [Methoden zur Auswahl eines Button-Steuerelements in Windows Forms](../../../../docs/framework/winforms/controls/ways-to-select-a-windows-forms-button-control.md)
- [Vorgehensweise: Reagieren Sie auf eine Windows Forms-Schaltfläche geklickt](../../../../docs/framework/winforms/controls/how-to-respond-to-windows-forms-button-clicks.md)
- [Vorgehensweise: Definieren Sie eine Windows Forms-Schaltfläche als "Annehmen"-Schaltfläche mithilfe des Designers](../../../../docs/framework/winforms/controls/designate-a-wf-button-as-the-accept-button-using-the-designer.md)
- [Button-Steuerelement](../../../../docs/framework/winforms/controls/button-control-windows-forms.md)
