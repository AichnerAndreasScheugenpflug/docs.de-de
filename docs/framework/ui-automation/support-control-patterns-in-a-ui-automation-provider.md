---
title: Unterstützung von Steuerelementmustern in einem Benutzeroberflächenautomatisierungs-Anbieter
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- control patterns, supporting in UI Automation provider
- UI Automation, supporting control patterns in provider
ms.assetid: 0d635c35-ffa8-4dc8-bbc9-12fcd5445776
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: 76340438de505cb8297c6a303defe7c33bbb5726
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54691709"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a>Unterstützung von Steuerelementmustern in einem Benutzeroberflächenautomatisierungs-Anbieter
> [!NOTE]
>  Diese Dokumentation ist für .NET Framework-Entwickler vorgesehen, die die verwalteten [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]-Klassen verwenden möchten, die im <xref:System.Windows.Automation>-Namespace definiert sind. Die neuesten Informationen zu [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], finden Sie unter [Windows-Automatisierungs-API: Benutzeroberflächenautomatisierung](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 In diesem Thema wird erläutert, wie Sie ein oder mehrere Steuerelementmuster in einem Benutzeroberflächenautomatisierungs-Anbieter implementieren, damit Clientanwendungen Steuerelemente ändern und Daten von Steuerelementen abrufen können.  
  
### <a name="support-control-patterns"></a>Unterstützung von Steuerelementmustern  
  
1.  Implementieren Sie die entsprechenden Schnittstellen für die Steuerelementmuster, die vom Element unterstützt werden sollen, z. B. <xref:System.Windows.Automation.Provider.IInvokeProvider> für <xref:System.Windows.Automation.InvokePattern>.  
  
2.  Geben Sie das Objekt, das die Implementierung der einzelnen Steuerelementschnittstellen enthält, in der Implementierung von <xref:System.Windows.Automation.Provider.IRawElementProviderSimple.GetPatternProvider%2A?displayProperty=nameWithType>zurück  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine Implementierung von <xref:System.Windows.Automation.Provider.ISelectionProvider> für ein benutzerdefiniertes Einzelauswahl-Listenfeld dargestellt. Die Implementierung gibt drei Eigenschaften zurück und ruft das aktuell ausgewählte Element ab.  
  
 [!code-csharp[UIAFragmentProvider_snip#119](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAFragmentProvider_snip/CSharp/ListPattern.cs#119)]
 [!code-vb[UIAFragmentProvider_snip#119](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAFragmentProvider_snip/VisualBasic/ListPattern.vb#119)]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird eine Implementierung von <xref:System.Windows.Automation.Provider.IRawElementProviderSimple.GetPatternProvider%2A> dargestellt, die die <xref:System.Windows.Automation.Provider.ISelectionProvider>implementierende Klasse zurückgibt. Die meisten Listenfeld-Steuerelemente unterstützt andere Muster auch, aber in diesem Beispiel wird ein null-Verweis (`Nothing` in Microsoft Visual Basic .NET) für alle anderen Musterbezeichner zurückgegeben wird.  
  
 [!code-csharp[UIAFragmentProvider_snip#120](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAFragmentProvider_snip/CSharp/ListFragment.cs#120)]
 [!code-vb[UIAFragmentProvider_snip#120](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAFragmentProvider_snip/VisualBasic/ListFragment.vb#120)]  
  
## <a name="see-also"></a>Siehe auch
- [Übersicht über die Benutzeroberflächenautomatisierungs-Anbieter](../../../docs/framework/ui-automation/ui-automation-providers-overview.md)
- [Server-Side UI Automation Provider Implementation](../../../docs/framework/ui-automation/server-side-ui-automation-provider-implementation.md)(Implementierung eines serverseitigen Benutzeroberflächenautomatisierungs-Anbieter)
