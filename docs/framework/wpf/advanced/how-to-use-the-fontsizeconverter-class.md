---
title: 'Vorgehensweise: Verwenden der FontSizeConverter-Klasse'
ms.date: 03/30/2017
helpviewer_keywords:
- FontSizeConverter objects [WPF]
- typography [WPF], FontSizeConverter objects
ms.assetid: 3b0592bd-7223-4860-a108-a5d72f3a9178
ms.openlocfilehash: 7cb76ad4ffe4b4574a48212240b852e1f2253088
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54741898"
---
# <a name="how-to-use-the-fontsizeconverter-class"></a>Vorgehensweise: Verwenden der FontSizeConverter-Klasse
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird gezeigt, wie zum Erstellen einer Instanz von <xref:System.Windows.FontSizeConverter> und mit, dass Sie um eine Schriftgröße zu ändern.  
  
 Das Beispiel definiert eine benutzerdefinierte Methode namens `changeSize` , der den Inhalt des konvertiert eine <xref:System.Windows.Controls.ListBoxItem>, wie definiert in einer separaten [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] -Datei, um eine Instanz von <xref:System.Double>, und später in eine <xref:System.String>. Diese Methode übergibt der <xref:System.Windows.Controls.ListBoxItem> auf eine <xref:System.Windows.FontSizeConverter> -Objekt, das konvertiert die <xref:System.Windows.Controls.ContentControl.Content%2A> von einer <xref:System.Windows.Controls.ListBoxItem> mit einer Instanz von <xref:System.Double>. Dieser Wert übergeben wird dann wieder als Wert für die <xref:System.Windows.Controls.TextBlock.FontSize%2A> Eigenschaft der <xref:System.Windows.Controls.TextBlock> Element.  
  
 Dieses Beispiel definiert auch eine zweite benutzerdefinierte Methode, die aufgerufen wird `changeFamily`. Diese Methode konvertiert die <xref:System.Windows.Controls.ContentControl.Content%2A> von der <xref:System.Windows.Controls.ListBoxItem> auf eine <xref:System.String>, und übergibt dann diesen Wert auf die <xref:System.Windows.Controls.TextBlock.FontFamily%2A> Eigenschaft der <xref:System.Windows.Controls.TextBlock> Element.  
  
 Dieses Beispiel wird nicht ausgeführt.  
  
 [!code-csharp[FontSizeConverter#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FontSizeConverter/CSharp/Window1.xaml.cs#1)]  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Windows.FontSizeConverter>
