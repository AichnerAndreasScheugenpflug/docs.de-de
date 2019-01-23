---
title: ICorDebugMutableDataTarget-Schnittstelle
ms.date: 03/30/2017
ms.assetid: 14aad5b3-84ab-4bbc-94e3-1eb92e258d10
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f63343b43481d1d91d1db30cd2ace3214c5590a9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54492298"
---
# <a name="icordebugmutabledatatarget-interface"></a><span data-ttu-id="0b7c1-102">ICorDebugMutableDataTarget-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0b7c1-102">ICorDebugMutableDataTarget Interface</span></span>
<span data-ttu-id="0b7c1-103">Erweitert die [ICorDebugDataTarget](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-interface.md) Schnittstelle, um änderbare Datenziele zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0b7c1-103">Extends the [ICorDebugDataTarget](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-interface.md) interface to support mutable data targets.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0b7c1-104">Methoden</span><span class="sxs-lookup"><span data-stu-id="0b7c1-104">Methods</span></span>  
  
|<span data-ttu-id="0b7c1-105">Methode</span><span class="sxs-lookup"><span data-stu-id="0b7c1-105">Method</span></span>|<span data-ttu-id="0b7c1-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b7c1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0b7c1-107">ContinueStatusChanged-Methode</span><span class="sxs-lookup"><span data-stu-id="0b7c1-107">ContinueStatusChanged Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmutabledatatarget-continuestatuschanged-method.md)|<span data-ttu-id="0b7c1-108">Ändert den Fortsetzungsstatus für das ausstehende Debugereignis für den angegebenen Thread.</span><span class="sxs-lookup"><span data-stu-id="0b7c1-108">Changes the continuation status for the outstanding debug event on the specified thread.</span></span>|  
|[<span data-ttu-id="0b7c1-109">SetThreadContext-Methode</span><span class="sxs-lookup"><span data-stu-id="0b7c1-109">SetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmutabledatatarget-setthreadcontext-method.md)|<span data-ttu-id="0b7c1-110">Legt den Kontext (Registerwerte) für einen Thread fest.</span><span class="sxs-lookup"><span data-stu-id="0b7c1-110">Sets the context (register values) for a thread.</span></span>|  
|[<span data-ttu-id="0b7c1-111">WriteVirtual-Methode</span><span class="sxs-lookup"><span data-stu-id="0b7c1-111">WriteVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmutabledatatarget-writevirtual-method.md)|<span data-ttu-id="0b7c1-112">Schreibt Speicher in den Prozessadressraum.</span><span class="sxs-lookup"><span data-stu-id="0b7c1-112">Writes memory into the target process address space.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0b7c1-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b7c1-113">Remarks</span></span>  
 <span data-ttu-id="0b7c1-114">Diese Erweiterung die [ICorDebugDataTarget](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-interface.md) Schnittstelle kann implementiert werden, von Debugtools, die den Zielprozess (z. B. zum Ausführen von invasivem Livedebuggen) ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="0b7c1-114">This extension to the [ICorDebugDataTarget](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-interface.md) interface can be implemented by debugging tools that wish to modify the target process (for example, to perform live invasive debugging).</span></span>  
  
 <span data-ttu-id="0b7c1-115">Alle diese Methoden sind insofern optional, als keine auf einer Untersuchung des Kerns basierende Debugfunktionen verloren geht, wenn diese Schnittstelle nicht implementiert oder wird oder keine Aufrufe dieser Methoden stattfinden.</span><span class="sxs-lookup"><span data-stu-id="0b7c1-115">All of these methods are optional in the sense that no core inspection-based debugging functionality is lost by not implementing this interface or by the failure of calls to these methods.</span></span>  <span data-ttu-id="0b7c1-116">Jeder Fehler `HRESULT` von diesen Methoden wird als `HRESULT` aus dem ICorDebug-Methodenaufruf verteilt.</span><span class="sxs-lookup"><span data-stu-id="0b7c1-116">Any failure `HRESULT` from these methods will propagate out as the `HRESULT` from the ICorDebug method call.</span></span>  
  
 <span data-ttu-id="0b7c1-117">Beachten Sie, dass ein einzelner ICorDebug-Methodenaufruf ggf. zu mehreren Mutationen führt. Es ist kein Mechanismus zum Sicherstellen vorhanden, dass zugehörige Mutationen transaktional angewendet werden (alle oder keine).</span><span class="sxs-lookup"><span data-stu-id="0b7c1-117">Note that a single ICorDebug method call may result in multiple mutations, and that there is no mechanism for ensuring related mutations are applied transactionally (all-or-none).</span></span>  <span data-ttu-id="0b7c1-118">Dies bedeutet, dass bei einem Fehler einer Mutation, nachdem andere Mutationen (für den gleichen ICorDebug-Aufruf) erfolgreich ausgeführt wurden, der Zielprozess in einem inkonsistenten Zustand verbleiben kann, und das Debuggen wird ggf. unzuverlässig.</span><span class="sxs-lookup"><span data-stu-id="0b7c1-118">This means that if a mutation fails after others (for the same ICorDebug call) have succeeded, the target process may be left in an inconsistent state and debugging may become unreliable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0b7c1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b7c1-119">Requirements</span></span>  
 <span data-ttu-id="0b7c1-120">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0b7c1-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0b7c1-121">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0b7c1-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0b7c1-122">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0b7c1-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0b7c1-123">**.NET Framework-Versionen:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0b7c1-123">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b7c1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b7c1-124">See also</span></span>
- [<span data-ttu-id="0b7c1-125">Debuggen von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0b7c1-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="0b7c1-126">Debuggen</span><span class="sxs-lookup"><span data-stu-id="0b7c1-126">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
