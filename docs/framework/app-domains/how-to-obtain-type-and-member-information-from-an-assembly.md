---
title: 'Vorgehensweise: Abrufen von Typ- und Memberinformationen aus einer Assembly'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- obtaining assembly information
- assemblies [.NET Framework], obtaining information from
ms.assetid: 348ae651-ccda-4f13-8eda-19e8337e9438
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ef3fbb7af3097a67cb39f0c3b2ee294b86f0600e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701598"
---
# <a name="how-to-obtain-type-and-member-information-from-an-assembly"></a><span data-ttu-id="0b0d9-102">Vorgehensweise: Abrufen von Typ- und Memberinformationen aus einer Assembly</span><span class="sxs-lookup"><span data-stu-id="0b0d9-102">How to: Obtain Type and Member Information from an Assembly</span></span>
<span data-ttu-id="0b0d9-103">Der <xref:System.Reflection>-Namespace enthält viele Methoden zum Abrufen von Informationen aus einer Assembly.</span><span class="sxs-lookup"><span data-stu-id="0b0d9-103">The <xref:System.Reflection> namespace contains many methods for obtaining information from an assembly.</span></span> <span data-ttu-id="0b0d9-104">In diesem Abschnitt wird eine dieser Methoden veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="0b0d9-104">This section demonstrates one of these methods.</span></span> <span data-ttu-id="0b0d9-105">Weitere Informationen finden Sie unter [Reflection Overview (Übersicht über Reflektion)](../../../docs/framework/reflection-and-codedom/reflection.md).</span><span class="sxs-lookup"><span data-stu-id="0b0d9-105">For additional information, see [Reflection Overview](../../../docs/framework/reflection-and-codedom/reflection.md).</span></span>  
  
 <span data-ttu-id="0b0d9-106">In folgendem Beispiel werden Typ- und Memberinformationen aus einer Assembly abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0b0d9-106">The following example obtains type and member information from an assembly.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0b0d9-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0b0d9-107">Example</span></span>  
 [!code-cpp[Conceptual.Types.ViewInfo#8](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.types.viewinfo/cpp/source6.cpp#8)]
 [!code-csharp[Conceptual.Types.ViewInfo#8](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.types.viewinfo/cs/source6.cs#8)]
 [!code-vb[Conceptual.Types.ViewInfo#8](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.types.viewinfo/vb/source6.vb#8)]  
  
## <a name="see-also"></a><span data-ttu-id="0b0d9-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b0d9-108">See also</span></span>
- [<span data-ttu-id="0b0d9-109">Programming with Application Domains (Programmieren mit Anwendungsdomänen)</span><span class="sxs-lookup"><span data-stu-id="0b0d9-109">Programming with Application Domains</span></span>](./application-domains.md#programming-with-application-domains)
- [<span data-ttu-id="0b0d9-110">Reflexion</span><span class="sxs-lookup"><span data-stu-id="0b0d9-110">Reflection</span></span>](../../../docs/framework/reflection-and-codedom/reflection.md)
- [<span data-ttu-id="0b0d9-111">Verwenden von Anwendungsdomänen</span><span class="sxs-lookup"><span data-stu-id="0b0d9-111">Using Application Domains</span></span>](../../../docs/framework/app-domains/use.md)
