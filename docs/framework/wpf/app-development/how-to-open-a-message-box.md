---
title: 'Vorgehensweise: Öffnen eines Meldungsfelds'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- message boxes [WPF], opening
- opening message boxes [WPF]
ms.assetid: acaad17f-af43-4eca-a004-f1c9e7c6f292
ms.openlocfilehash: 1bde7c4f794ca7e3b01490db8e918b06b5074bcf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54739731"
---
# <a name="how-to-open-a-message-box"></a>Vorgehensweise: Öffnen eines Meldungsfelds
Dieses Beispiel zeigt, wie ein Meldungsfeld geöffnet wird.  
  
## <a name="example"></a>Beispiel  
 Ein Meldungsfeld wird eine vorgefertigte modales Dialogfeld für die Anzeige von Informationen für Benutzer. Ein Meldungsfeld wird geöffnet, durch Aufrufen der statischen <xref:System.Windows.MessageBox.Show%2A> Methode der <xref:System.Windows.MessageBox> Klasse. Wenn <xref:System.Windows.MessageBox.Show%2A> wird aufgerufen, wird die Meldung übergeben mit einem String-Parameter. Mehrere Überladungen der <xref:System.Windows.MessageBox.Show%2A> können Sie konfigurieren, wie ein Meldungsfeld angezeigt wird (siehe <xref:System.Windows.MessageBox>).  
  
 [!code-csharp[MessageBoxSnippets#MessageBoxShow1CODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/MessageBoxSnippets/CSharp/Show1Window.xaml.cs#messageboxshow1code)]
 [!code-vb[MessageBoxSnippets#MessageBoxShow1CODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/MessageBoxSnippets/visualbasic/show1window.xaml.vb#messageboxshow1code)]  
  
## <a name="see-also"></a>Siehe auch
- [MessageBox-Beispiel](https://go.microsoft.com/fwlink/?LinkID=160023)
