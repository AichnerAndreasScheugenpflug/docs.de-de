---
title: 'Vorgehensweise: Hinzufügen eines Wasserzeichens zu einer TextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- displaying a background image inside a text box to aid user input [WPF]
- aid usability of a TextBox using a background image [WPF]
ms.assetid: df89bdd8-a0fb-45e0-b312-dd53332d01a8
ms.openlocfilehash: 1ab8c0f9274f4d461c9c2be04ec0aaca5e753c7d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54531131"
---
# <a name="how-to-add-a-watermark-to-a-textbox"></a>Vorgehensweise: Hinzufügen eines Wasserzeichens zu einer TextBox
Das folgende Beispiel zeigt, wie die Verwendbarkeit einer <xref:System.Windows.Controls.TextBox> durch ein erläuternde Hintergrundbild in der die <xref:System.Windows.Controls.TextBox> bis der Benutzer Text eingibt, an diesem Punkt das Bild wird entfernt. Darüber hinaus wird das Hintergrundbild erneut wiederhergestellt werden, wenn der Benutzer die Eingabe entfernt. Finden Sie in der folgenden Abbildung aus.  
  
 ![Ein Textfeld mit einem Hintergrundbild](../../../../docs/framework/wpf/controls/media/editing-textbox-using-background-image.png "Editing_TextBox_using_background_image")  
  
> [!NOTE]
>  Der Grund, ein Hintergrundbild wird in diesem Beispiel, sondern Sie einfach bearbeiten verwendet, die <xref:System.Windows.Controls.TextBox.Text%2A> Eigenschaft <xref:System.Windows.Controls.TextBox>, besteht darin, dass ein Hintergrundbild mit der Datenbindung nicht beeinträchtigt.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[TextBoxMiscSnippets_snip#TextBoxBackgroundExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/textbox_with_background_image.xaml#textboxbackgroundexamplewholepage)]  
  
 [!code-csharp[TextBoxMiscSnippets_snip#TextBoxBackgroundCodeExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/csharp/textbox_with_background_image.xaml.cs#textboxbackgroundcodeexamplewholepage)]
 [!code-vb[TextBoxMiscSnippets_snip#TextBoxBackgroundCodeExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextBoxMiscSnippets_snip/visualbasic/textbox_with_background_image.xaml.vb#textboxbackgroundcodeexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch
- [Übersicht über TextBox](../../../../docs/framework/wpf/controls/textbox-overview.md)
- [Übersicht über RichTextBox](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
