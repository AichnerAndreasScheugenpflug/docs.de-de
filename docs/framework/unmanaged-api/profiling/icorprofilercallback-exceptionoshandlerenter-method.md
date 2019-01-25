---
title: ICorProfilerCallback::ExceptionOSHandlerEnter-Methode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionOSHandlerEnter
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionOSHandlerEnter
helpviewer_keywords:
- ExceptionOSHandlerEnter method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionOSHandlerEnter method [.NET Framework profiling]
ms.assetid: 09238b9b-9359-4780-89dc-2f5e4f57920e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7842e7a8f12a58aa56fd5be5674b183fc515f51b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54608448"
---
# <a name="icorprofilercallbackexceptionoshandlerenter-method"></a><span data-ttu-id="4379c-102">ICorProfilerCallback::ExceptionOSHandlerEnter-Methode</span><span class="sxs-lookup"><span data-stu-id="4379c-102">ICorProfilerCallback::ExceptionOSHandlerEnter Method</span></span>
<span data-ttu-id="4379c-103">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4379c-103">Not implemented.</span></span> <span data-ttu-id="4379c-104">Ein Profiler, der nicht verwaltete Ausnahmeinformationen benötigt, muss diese Informationen mithilfe anderer Methoden abrufen.</span><span class="sxs-lookup"><span data-stu-id="4379c-104">A profiler that needs unmanaged exception information must obtain this information through other means.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4379c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4379c-105">Syntax</span></span>  
  
```  
HRESULT ExceptionOSHandlerEnter(  
    [in] UINT_PTR __unused);  
```  
  
## <a name="requirements"></a><span data-ttu-id="4379c-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4379c-106">Requirements</span></span>  
 <span data-ttu-id="4379c-107">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4379c-107">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4379c-108">**Header:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="4379c-108">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="4379c-109">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4379c-109">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4379c-110">**.NET Framework-Versionen:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4379c-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4379c-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4379c-111">See also</span></span>
- [<span data-ttu-id="4379c-112">ICorProfilerCallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4379c-112">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
