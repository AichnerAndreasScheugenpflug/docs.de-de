---
title: 'Vorgehensweise: Navigieren Sie durch ein DataSet mit dem BindingNavigator-Steuerelement in Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- datasets [Windows Forms], moving through
- BindingNavigator control [Windows Forms], moving through datasets
- examples [Windows Forms], BindingNavigator control
ms.assetid: 146d97be-3d97-400e-accb-860bbf47729d
ms.openlocfilehash: df11a525ab6491cf12b4ffb63c276f39cae0e44e
ms.sourcegitcommit: af0a22a4eb11bbcd33baec49150d551955b50a16
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2019
ms.locfileid: "56260709"
---
# <a name="how-to-move-through-a-dataset-with-the-windows-forms-bindingnavigator-control"></a>Vorgehensweise: Navigieren Sie durch ein DataSet mit dem BindingNavigator-Steuerelement in Windows Forms
Wenn Sie datengesteuerte Anwendungen erstellen, müssen Sie oft Auflistungen von Daten für Benutzer anzeigen. Das <xref:System.Windows.Forms.BindingNavigator>-Steuerelement in Verbindung mit der <xref:System.Windows.Forms.BindingSource>-Komponente stellt eine bequeme und erweiterbare Lösung bereit, um eine Auflistung zu durchlaufen und Elemente nacheinander anzuzeigen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird veranschaulicht, wie Sie ein <xref:System.Windows.Forms.BindingNavigator>-Steuerelement verwenden, um Daten zu durchlaufen. Das Dataset befindet sich in <xref:System.Data.DataView>, die an ein <xref:System.Windows.Forms.TextBox>-Steuerelement mit einer <xref:System.Windows.Forms.BindingSource>-Komponente gebunden ist.  
  
> [!NOTE]
>  Das Speichern vertraulicher Informationen (z. B. eines Kennworts) innerhalb der Verbindungszeichenfolge kann die Sicherheit einer Anwendung beeinträchtigen. Der Zugriff auf eine Datenbank lässt sich mithilfe der Windows-Authentifizierung (wird auch als integrierte Sicherheit bezeichnet) sicherer steuern. Weitere Informationen finden Sie unter [Protecting Connection Information (Schützen von Verbindungsinformationen)](../../../../docs/framework/data/adonet/protecting-connection-information.md).  
  
 [!code-csharp[System.Windows.Forms.DataNavigator#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataNavigator/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataNavigator#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataNavigator/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
-   Verweise auf die Assemblys "System", "System.Data", "System.Drawing", "System.Windows.Forms" und "System.Xml".  
  
 Informationen zum Erstellen dieses Beispiels über die Befehlszeile für Visual Basic oder Visual c# finden Sie unter [erstellen über die Befehlszeile](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) oder [Befehlszeile mit csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Sie können auch in diesem Beispiel in Visual Studio erstellen, indem Sie den Code in ein neues Projekt einfügen.  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Windows.Forms.BindingSource>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [BindingNavigator-Steuerelement](../../../../docs/framework/winforms/controls/bindingnavigator-control-windows-forms.md)
- [BindingSource-Komponente](../../../../docs/framework/winforms/controls/bindingsource-component.md)
- [Vorgehensweise: Binden eines Windows Forms-Steuerelements an einen Typ](../../../../docs/framework/winforms/controls/how-to-bind-a-windows-forms-control-to-a-type.md)
