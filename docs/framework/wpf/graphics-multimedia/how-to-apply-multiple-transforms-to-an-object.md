---
title: 'Vorgehensweise: Anwenden mehrerer Transformationen auf ein Objekt'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- grouping Transform objects [WPF]
- Transform objects [WPF], grouping
- graphics [WPF], grouping Transform objects
- TransformGroup [WPF]
ms.assetid: 98cd1921-12bc-4bf5-8193-529228fb7402
ms.openlocfilehash: dc9b7c052d9deb4d1167c813a6ce652c99983a9f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54649452"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a><span data-ttu-id="e2f4d-102">Vorgehensweise: Anwenden mehrerer Transformationen auf ein Objekt</span><span class="sxs-lookup"><span data-stu-id="e2f4d-102">How to: Apply Multiple Transforms to an Object</span></span>
<span data-ttu-id="e2f4d-103">Dieses Beispiel zeigt, wie Sie mit einem <xref:System.Windows.Media.TransformGroup> Gruppe zwei oder mehr <xref:System.Windows.Media.Transform> Objekte in einem einzigen zusammengesetzten <xref:System.Windows.Media.Transform>.</span><span class="sxs-lookup"><span data-stu-id="e2f4d-103">This example shows how to use a <xref:System.Windows.Media.TransformGroup> to group two or more <xref:System.Windows.Media.Transform> objects into a single composite <xref:System.Windows.Media.Transform>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e2f4d-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2f4d-104">Example</span></span>  
 <span data-ttu-id="e2f4d-105">Im folgenden Beispiel wird eine <xref:System.Windows.Media.TransformGroup> Anwenden einer <xref:System.Windows.Media.ScaleTransform> und ein <xref:System.Windows.Media.RotateTransform> auf eine <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="e2f4d-105">The following example uses a <xref:System.Windows.Media.TransformGroup> to apply a <xref:System.Windows.Media.ScaleTransform> and a <xref:System.Windows.Media.RotateTransform> to a <xref:System.Windows.Controls.Button>.</span></span>  
  
 [!code-xaml[Transforms_snip#MultipleTransformExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MultipleTransformExample.xaml#multipletransformexamplewholepage)]  
  
 [!code-csharp[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/MultipleTransformsExample.cs#multipletransformscodeexamplewholepage)]
 [!code-vb[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/MultipleTransformsExample.vb#multipletransformscodeexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="e2f4d-106">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2f4d-106">See also</span></span>
- <xref:System.Windows.UIElement.RenderTransform%2A>
- <xref:System.Windows.Media.TransformGroup>
- [<span data-ttu-id="e2f4d-107">Übersicht über Transformationen</span><span class="sxs-lookup"><span data-stu-id="e2f4d-107">Transforms Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
- [<span data-ttu-id="e2f4d-108">Beispiel für 2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="e2f4d-108">2-D Transforms Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=158252)
