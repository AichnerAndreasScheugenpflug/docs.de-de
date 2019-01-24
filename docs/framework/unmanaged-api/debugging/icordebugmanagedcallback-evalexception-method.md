---
title: ICorDebugManagedCallback::EvalException-Methode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.EvalException
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::EvalException
helpviewer_keywords:
- EvalException method [.NET Framework debugging]
- ICorDebugManagedCallback::EvalException method [.NET Framework debugging]
ms.assetid: d6036345-18a3-45c1-a302-b1c6f2dced9b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1705b9d77d0d91196201d713cceb0ccf0f8635a8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54728014"
---
# <a name="icordebugmanagedcallbackevalexception-method"></a><span data-ttu-id="ed029-102">ICorDebugManagedCallback::EvalException-Methode</span><span class="sxs-lookup"><span data-stu-id="ed029-102">ICorDebugManagedCallback::EvalException Method</span></span>
<span data-ttu-id="ed029-103">Benachrichtigt den Debugger, dass eine Auswertung mit einem Ausnahmefehler beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ed029-103">Notifies the debugger that an evaluation has terminated with an unhandled exception.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed029-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed029-104">Syntax</span></span>  
  
```  
HRESULT EvalException (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread,  
    [in] ICorDebugEval      *pEval  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ed029-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed029-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="ed029-106">[in] Ein Zeiger auf ein ICorDebugAppDomain-Objekt, das die Anwendungsdomäne darstellt, in dem die Auswertung beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ed029-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain in which the evaluation terminated.</span></span>  
  
 `pThread`  
 <span data-ttu-id="ed029-107">[in] Ein Zeiger auf ein ICorDebugThread-Objekt, das den Thread darstellt, in dem die Auswertung beendet.</span><span class="sxs-lookup"><span data-stu-id="ed029-107">[in] A pointer to an ICorDebugThread object that represents the thread in which the evaluation terminated.</span></span>  
  
 `pEval`  
 <span data-ttu-id="ed029-108">[in] Ein Zeiger auf ein ICorDebugEval-Objekt, das den Code darstellt, der die Auswertung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed029-108">[in] A pointer to an ICorDebugEval object that represents the code that performed the evaluation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ed029-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed029-109">Requirements</span></span>  
 <span data-ttu-id="ed029-110">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ed029-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ed029-111">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ed029-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ed029-112">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ed029-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ed029-113">**.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ed029-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed029-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed029-114">See also</span></span>
- [<span data-ttu-id="ed029-115">ICorDebugManagedCallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ed029-115">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
