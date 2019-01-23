---
title: 'Vorgehensweise: Drucken eines bildlauffähigen Formulars (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- entire form [Visual Basic], printing
- scrollable form [Visual Basic], printing
ms.assetid: 1196e1cf-b77f-4928-a3e4-85b51ba3787d
ms.openlocfilehash: 6cec75eae8046befeb37da39e0b788f045ff4149
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54552501"
---
# <a name="how-to-print-a-scrollable-form-visual-basic"></a>Vorgehensweise: Drucken eines bildlauffähigen Formulars (Visual Basic)
Mithilfe der <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> -Komponente können Sie schnell ein Bild eines Formulars drucken, ohne eine <xref:System.Drawing.Printing.PrintDocument> -Komponente zu verwenden. Standardmäßig wird nur der aktuell sichtbare Teil des Formulars gedruckt; wenn ein Benutzer die Größe des Formulars zur Laufzeit geändert hat, wird das Bild möglicherweise nicht wie beabsichtigt gedruckt. Die folgende Vorgehensweise veranschaulicht, wie der gesamte Clientbereich eines scrollbaren Formulars gedruckt wird, selbst wenn die Größe des Formulars geändert wurde.  
  
 Die PowerPack-Steuerelemente sind nicht mehr in Visual Studio enthalten, Sie können sie jedoch aus dem [Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=25169)herunterladen.  
  
### <a name="to-print-the-complete-client-area-of-a-scrollable-form"></a>So drucken Sie den vollständigen Clientbereich eines scrollbaren Formulars  
  
1.  Klicken Sie in der **Toolbox**auf die Registerkarte **Visual Basic PowerPacks** , und ziehen Sie dann die <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> -Komponente auf das Formular.  
  
     Die <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm> -Komponente wird der Komponentenleiste hinzugefügt.  
  
2.  Legen Sie im Fenster **Eigenschaften** die Eigenschaft <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> auf <xref:System.Drawing.Printing.PrintAction.PrintToPrinter>fest.  
  
3.  Fügen Sie den folgenden Code in die entsprechenden Ereignishandler (z. B. in der `Click` -Ereignishandler für ein **Drucken**`Button`).  
  
    ```  
    PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.Scrollable)  
    ```  
  
    > [!NOTE]
    >  Unter einigen Betriebssystemen werden von den <xref:System.Drawing.Graphics> -Methoden gezeichnete Text- oder Grafikelemente möglicherweise nicht ordnungsgemäß gedruckt. In diesem Fall kann der `Scrollable` -Parameter beim Drucken nicht verwendet werden.  
  
## <a name="see-also"></a>Siehe auch
- <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A>
- <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.Print%2A>
- [PrintForm-Komponente](../../../visual-basic/developing-apps/printing/printform-component.md)
- [Vorgehensweise: Drucken des Clientbereichs eines Formulars](../../../visual-basic/developing-apps/printing/how-to-print-the-client-area-of-a-form.md)
- [Vorgehensweise: Drucken von Client- und Nicht-Client-Bereichen eines Formulars](../../../visual-basic/developing-apps/printing/how-to-print-client-and-non-client-areas-of-a-form.md)
