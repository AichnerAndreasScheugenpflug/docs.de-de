---
title: ICorProfilerCallback::ExceptionSearchFunctionLeave-Methode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionSearchFunctionLeave
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionSearchFunctionLeave
helpviewer_keywords:
- ExceptionSearchFunctionLeave method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionSearchFunctionLeave method [.NET Framework profiling]
ms.assetid: 01de7ac6-0aad-42ef-bf93-50737667b0a4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6d20aa04b292fd29b60d68b844ef410258d90d31
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54546581"
---
# <a name="icorprofilercallbackexceptionsearchfunctionleave-method"></a><span data-ttu-id="ceab2-102">ICorProfilerCallback::ExceptionSearchFunctionLeave-Methode</span><span class="sxs-lookup"><span data-stu-id="ceab2-102">ICorProfilerCallback::ExceptionSearchFunctionLeave Method</span></span>
<span data-ttu-id="ceab2-103">Benachrichtigt den Profiler, dass die Suchphase der Ausnahmebehandlung Suche in einer Funktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ceab2-103">Notifies the profiler that the search phase of exception handling has finished searching a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ceab2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ceab2-104">Syntax</span></span>  
  
```  
HRESULT ExceptionSearchFunctionLeave();  
```  
  
## <a name="requirements"></a><span data-ttu-id="ceab2-105">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ceab2-105">Requirements</span></span>  
 <span data-ttu-id="ceab2-106">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ceab2-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ceab2-107">**Header:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ceab2-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ceab2-108">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ceab2-108">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ceab2-109">**.NET Framework-Versionen:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ceab2-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ceab2-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ceab2-110">See also</span></span>
- [<span data-ttu-id="ceab2-111">ICorProfilerCallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ceab2-111">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="ceab2-112">ExceptionSearchFunctionEnter-Methode</span><span class="sxs-lookup"><span data-stu-id="ceab2-112">ExceptionSearchFunctionEnter Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfunctionenter-method.md)
