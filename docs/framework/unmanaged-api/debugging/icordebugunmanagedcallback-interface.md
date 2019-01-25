---
title: ICorDebugUnmanagedCallback-Schnittstelle
ms.date: 03/30/2017
api_name:
- ICorDebugUnmanagedCallback
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugUnmanagedCallback
helpviewer_keywords:
- ICorDebugUnmanagedCallback interface [.NET Framework debugging]
ms.assetid: bc71cbca-7d73-40e5-84dd-2109fade3c2a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fd61c8133d9f155ae8e15bbc6aa90b2b9de1aadd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647666"
---
# <a name="icordebugunmanagedcallback-interface"></a><span data-ttu-id="c8d30-102">ICorDebugUnmanagedCallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c8d30-102">ICorDebugUnmanagedCallback Interface</span></span>
<span data-ttu-id="c8d30-103">Ermöglicht die Benachrichtigung über systemeigene Ereignisse, die nicht direkt auf die common Language Runtime (CLR) beziehen.</span><span class="sxs-lookup"><span data-stu-id="c8d30-103">Provides notification of native events that are not directly related to the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c8d30-104">Methoden</span><span class="sxs-lookup"><span data-stu-id="c8d30-104">Methods</span></span>  
  
|<span data-ttu-id="c8d30-105">Methode</span><span class="sxs-lookup"><span data-stu-id="c8d30-105">Method</span></span>|<span data-ttu-id="c8d30-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8d30-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c8d30-107">DebugEvent-Methode</span><span class="sxs-lookup"><span data-stu-id="c8d30-107">DebugEvent Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugunmanagedcallback-debugevent-method.md)|<span data-ttu-id="c8d30-108">Benachrichtigt den Debugger, dass ein systemeigenes Ereignis ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="c8d30-108">Notifies the debugger that a native event has been fired.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c8d30-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c8d30-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c8d30-110">Diese Schnittstelle kann weder computerübergreifend noch prozessübergreifend remote aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8d30-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c8d30-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8d30-111">Requirements</span></span>  
 <span data-ttu-id="c8d30-112">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c8d30-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c8d30-113">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c8d30-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c8d30-114">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c8d30-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c8d30-115">**.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c8d30-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c8d30-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8d30-116">See also</span></span>
- [<span data-ttu-id="c8d30-117">Debuggen von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c8d30-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
