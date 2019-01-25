---
title: ETW-Konfliktereignisse
ms.date: 03/30/2017
helpviewer_keywords:
- contention events [.NET Framework]
- ETW, contention events (CLR)
ms.assetid: 6933e753-2f2a-425b-ae84-42138c957d76
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 90beb1487581ff4c031d6f10fb613430207dc026
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54575566"
---
# <a name="contention-etw-events"></a><span data-ttu-id="0d8e4-102">ETW-Konfliktereignisse</span><span class="sxs-lookup"><span data-stu-id="0d8e4-102">Contention ETW Events</span></span>
<span data-ttu-id="0d8e4-103">Konfliktereignisse werden immer dann ausgelöst, wenn es Konflikte bei <xref:System.Threading.Monitor?displayProperty=nameWithType>-Sperren oder nativen Sperren gibt, die von der Laufzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-103">Contention events are raised whenever there is contention for <xref:System.Threading.Monitor?displayProperty=nameWithType> locks or native locks used by the runtime.</span></span> <span data-ttu-id="0d8e4-104">Konflikte treten auf, wenn ein Thread auf eine Sperre wartet, während ein anderer Thread die Sperre besitzt.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-104">Contention occurs when a thread is waiting for a lock while another thread possesses the lock.</span></span>  
  
 <span data-ttu-id="0d8e4-105">Die folgende Tabelle zeigt das Schlüsselwort, unter dem Konfliktereignisse ausgelöst werden, und die Ebene der Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-105">The following table shows the keyword under which contention events are raised, and the level of the events.</span></span> <span data-ttu-id="0d8e4-106">(Weitere Informationen finden Sie unter [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="0d8e4-106">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="0d8e4-107">Schlüsselwort zum Auslösen des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="0d8e4-107">Keyword for raising the event</span></span>|<span data-ttu-id="0d8e4-108">Ebene</span><span class="sxs-lookup"><span data-stu-id="0d8e4-108">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="0d8e4-109">`ContentionKeyword` (0x4000)</span><span class="sxs-lookup"><span data-stu-id="0d8e4-109">`ContentionKeyword` (0x4000)</span></span>|<span data-ttu-id="0d8e4-110">Information (4)</span><span class="sxs-lookup"><span data-stu-id="0d8e4-110">Informational (4)</span></span>|  
  
 <span data-ttu-id="0d8e4-111">Die folgende Tabelle zeigt die Ereignisinformationen an.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-111">The following table shows event information.</span></span>  
  
|<span data-ttu-id="0d8e4-112">event</span><span class="sxs-lookup"><span data-stu-id="0d8e4-112">Event</span></span>|<span data-ttu-id="0d8e4-113">Ereignis-ID</span><span class="sxs-lookup"><span data-stu-id="0d8e4-113">Event ID</span></span>|<span data-ttu-id="0d8e4-114">Wird ausgelöst, wenn</span><span class="sxs-lookup"><span data-stu-id="0d8e4-114">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`ContentionStart_V1`|<span data-ttu-id="0d8e4-115">81</span><span class="sxs-lookup"><span data-stu-id="0d8e4-115">81</span></span>|<span data-ttu-id="0d8e4-116">Konflikt startet.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-116">Contention starts.</span></span> <span data-ttu-id="0d8e4-117">Dieses Ereignis enthält die Spinzeit vor dem Abruf einer Sperre eines Threads nicht. Dies wird nur ausgelöst, wenn der Thread darauf wartet, eine Sperre abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-117">This event does not include the amount of spinning time before a thread waits to acquire a lock; it is raised only when the thread waits to acquire a lock.</span></span>|  
|`ContentionStop`|<span data-ttu-id="0d8e4-118">81</span><span class="sxs-lookup"><span data-stu-id="0d8e4-118">81</span></span>|<span data-ttu-id="0d8e4-119">Konflikt endet.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-119">Contention ends.</span></span>|  
  
 <span data-ttu-id="0d8e4-120">In der folgenden Tabelle finden Sie die Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-120">The following table shows event data.</span></span>  
  
|<span data-ttu-id="0d8e4-121">Feldname</span><span class="sxs-lookup"><span data-stu-id="0d8e4-121">Field name</span></span>|<span data-ttu-id="0d8e4-122">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0d8e4-122">Data type</span></span>|<span data-ttu-id="0d8e4-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d8e4-123">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="0d8e4-124">Flags</span><span class="sxs-lookup"><span data-stu-id="0d8e4-124">Flags</span></span>|<span data-ttu-id="0d8e4-125">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="0d8e4-125">win:UInt8</span></span>|<span data-ttu-id="0d8e4-126">0 für verwaltet. 1 für nativ.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-126">0 for managed; 1 for native.</span></span>|  
|<span data-ttu-id="0d8e4-127">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="0d8e4-127">ClrInstanceID</span></span>|<span data-ttu-id="0d8e4-128">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="0d8e4-128">win:UInt16</span></span>|<span data-ttu-id="0d8e4-129">Eindeutige ID für die Instanz von CLR.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-129">Unique ID for the instance of CLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0d8e4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d8e4-130">See also</span></span>
- [<span data-ttu-id="0d8e4-131">CLR-ETW-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="0d8e4-131">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
