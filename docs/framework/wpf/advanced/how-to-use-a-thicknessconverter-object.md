---
title: 'Vorgehensweise: Verwenden eines ThicknessConverter-Objekts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- border thickness [WPF]
- ThicknessConverter objects [WPF]
ms.assetid: 52682194-d7fd-499c-8005-73fcc84e7b2c
ms.openlocfilehash: 22215a155f4a204e3edeebc464413d5718290bb4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577070"
---
# <a name="how-to-use-a-thicknessconverter-object"></a><span data-ttu-id="f10d5-102">Vorgehensweise: Verwenden eines ThicknessConverter-Objekts</span><span class="sxs-lookup"><span data-stu-id="f10d5-102">How to: Use a ThicknessConverter Object</span></span>
## <a name="example"></a><span data-ttu-id="f10d5-103">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f10d5-103">Example</span></span>  
 <span data-ttu-id="f10d5-104">In diesem Beispiel wird gezeigt, wie zum Erstellen einer Instanz von <xref:System.Windows.ThicknessConverter> und um die Breite eines Rahmens zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f10d5-104">This example shows how to create an instance of <xref:System.Windows.ThicknessConverter> and use it to change the thickness of a border.</span></span>  
  
 <span data-ttu-id="f10d5-105">Das Beispiel definiert eine benutzerdefinierte Methode namens `changeThickness`; diese Methode zuerst konvertiert den Inhalt der ein <xref:System.Windows.Controls.ListBoxItem>, wie definiert in einer separaten [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] -Datei, um eine Instanz von <xref:System.Windows.Thickness>, und konvertiert Sie den Inhalt in einem späteren Zeitpunkt eine <xref:System.String>.</span><span class="sxs-lookup"><span data-stu-id="f10d5-105">The example defines a custom method called `changeThickness`; this method first converts the contents of a <xref:System.Windows.Controls.ListBoxItem>, as defined in a separate [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file, to an instance of <xref:System.Windows.Thickness>, and later converts the content into a <xref:System.String>.</span></span> <span data-ttu-id="f10d5-106">Diese Methode übergibt der <xref:System.Windows.Controls.ListBoxItem> auf eine <xref:System.Windows.ThicknessConverter> -Objekt, das konvertiert die <xref:System.Windows.Controls.ContentControl.Content%2A> von einer <xref:System.Windows.Controls.ListBoxItem> mit einer Instanz von <xref:System.Windows.Thickness>.</span><span class="sxs-lookup"><span data-stu-id="f10d5-106">This method passes the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.Windows.ThicknessConverter> object, which converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of a <xref:System.Windows.Controls.ListBoxItem> to an instance of <xref:System.Windows.Thickness>.</span></span> <span data-ttu-id="f10d5-107">Dieser Wert übergeben wird dann wieder als Wert für die <xref:System.Windows.Controls.Border.BorderThickness%2A> Eigenschaft der <xref:System.Windows.Controls.Border>.</span><span class="sxs-lookup"><span data-stu-id="f10d5-107">This value is then passed back as the value of the <xref:System.Windows.Controls.Border.BorderThickness%2A> property of the <xref:System.Windows.Controls.Border>.</span></span>  
  
 <span data-ttu-id="f10d5-108">Dieses Beispiel wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f10d5-108">This example does not run.</span></span>  
  
 [!code-csharp[ThicknessConverter#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ThicknessConverter/CSharp/Window1.xaml.cs#1)]
 [!code-vb[ThicknessConverter#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ThicknessConverter/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="f10d5-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f10d5-109">See also</span></span>
- <xref:System.Windows.Thickness>
- <xref:System.Windows.ThicknessConverter>
- <xref:System.Windows.Controls.Border>
- [<span data-ttu-id="f10d5-110">Vorgehensweise: Ändern Sie die Margin-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f10d5-110">How to: Change the Margin Property</span></span>](https://msdn.microsoft.com/library/8a313efd-5f99-4097-b4c1-8fa49d8379a2)
- [<span data-ttu-id="f10d5-111">Vorgehensweise: Konvertieren Sie ein ListBoxItem in einen neuen Typ von Daten</span><span class="sxs-lookup"><span data-stu-id="f10d5-111">How to: Convert a ListBoxItem to a new Data Type</span></span>](https://msdn.microsoft.com/library/7a080b88-184e-4b27-bb61-d42bafba9727)
- [<span data-ttu-id="f10d5-112">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="f10d5-112">Panels Overview</span></span>](../../../../docs/framework/wpf/controls/panels-overview.md)
