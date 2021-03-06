---
title: 'Vorgehensweise: Hinzufügen und Entfernen von Elementen mit dem ListView-Steuerelement in Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView control [Windows Forms], populating
- list views [Windows Forms], adding list items
- ListView control [Windows Forms], adding list items
ms.assetid: 1b35a80a-edd8-495f-a807-a28c4aae52c6
ms.openlocfilehash: 7a4083d54ea85ff7a2e18f7e448f2b967317ac25
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54544522"
---
# <a name="how-to-add-and-remove-items-with-the-windows-forms-listview-control"></a>Vorgehensweise: Hinzufügen und Entfernen von Elementen mit dem ListView-Steuerelement in Windows Forms
Beim Hinzufügen eines Elements zu einer Windows Forms <xref:System.Windows.Forms.ListView> -Steuerelement besteht aus in erster Linie das Element angeben, und Eigenschaften zuweisen. Hinzufügen oder Entfernen von Elementen kann jederzeit erfolgen.  
  
### <a name="to-add-items-programmatically"></a>Elemente programmgesteuert hinzuzufügen.  
  
1.  Verwenden der <xref:System.Windows.Forms.ListView.ListViewItemCollection.Add%2A> Methode der <xref:System.Windows.Forms.ListView.Items%2A> Eigenschaft.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#11)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#11)]  
  
### <a name="to-remove-items-programmatically"></a>Das programmgesteuerte Entfernen von Elementen  
  
1.  Verwenden der <xref:System.Windows.Forms.ListView.ListViewItemCollection.RemoveAt%2A> oder <xref:System.Windows.Forms.ListView.ListViewItemCollection.Clear%2A> Methode der <xref:System.Windows.Forms.ListView.Items%2A> Eigenschaft. Die <xref:System.Windows.Forms.ListView.ListViewItemCollection.RemoveAt%2A> -Methode entfernt ein einzelnes Element; die <xref:System.Windows.Forms.ListView.ListViewItemCollection.Clear%2A> -Methode entfernt alle Elemente aus der Liste.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#12](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#12)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#12](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#12)]  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Windows.Forms.ListView>
- [ListView-Steuerelement](../../../../docs/framework/winforms/controls/listview-control-windows-forms.md)
- [Übersicht über das ListView-Steuerelement](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)
