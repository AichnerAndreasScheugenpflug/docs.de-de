---
title: ICorDebugManagedCallback::UnloadModule-Methode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugManagedCallback.UnloadModule
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugManagedCallback::UnloadModule
helpviewer_keywords:
- ICorDebugManagedCallback::UnloadModule method [.NET Framework debugging]
- UnloadModule method [.NET Framework debugging]
ms.assetid: b12bfcd9-1e29-48bf-9a3d-44bfae5df5e8
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 509206045164a35d9740c7369f8d7c90f1b2b0e0
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugmanagedcallbackunloadmodule-method"></a><span data-ttu-id="31e92-102">ICorDebugManagedCallback::UnloadModule-Methode</span><span class="sxs-lookup"><span data-stu-id="31e92-102">ICorDebugManagedCallback::UnloadModule Method</span></span>
<span data-ttu-id="31e92-103">Benachrichtigt den Debugger, dass ein common Language Runtime-Modul (DLL) entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="31e92-103">Notifies the debugger that a common language runtime module (DLL) has been unloaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="31e92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31e92-104">Syntax</span></span>  
  
```  
HRESULT UnloadModule (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugModule     *pModule  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="31e92-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="31e92-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="31e92-106">[in] Ein Zeiger auf ein ICorDebugAppDomain-Objekt, das die Anwendungsdomäne darstellt, die das Modul enthält.</span><span class="sxs-lookup"><span data-stu-id="31e92-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contained the module.</span></span>  
  
 `pModule`  
 <span data-ttu-id="31e92-107">[in] Ein Zeiger auf ein ICorDebugModule-Objekt, das Modul darstellt.</span><span class="sxs-lookup"><span data-stu-id="31e92-107">[in] A pointer to an ICorDebugModule object that represents the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="31e92-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31e92-108">Remarks</span></span>  
 <span data-ttu-id="31e92-109">Das Modul muss nach diesem Aufruf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31e92-109">The module should not be used after this call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="31e92-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31e92-110">Requirements</span></span>  
 <span data-ttu-id="31e92-111">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="31e92-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="31e92-112">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="31e92-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="31e92-113">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="31e92-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="31e92-114">**.NET Framework-Versionen:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="31e92-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="31e92-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31e92-115">See Also</span></span>  
 [<span data-ttu-id="31e92-116">LoadModule-Methode</span><span class="sxs-lookup"><span data-stu-id="31e92-116">LoadModule Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-loadmodule-method.md)  
 [<span data-ttu-id="31e92-117">ICorDebugManagedCallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="31e92-117">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)