---
title: ICorProfilerCallback2::FinalizeableObjectQueued-Methode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.FinalizeableObjectQueued
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::FinalizeableObjectQueued
helpviewer_keywords:
- FinalizeableObjectQueued method [.NET Framework profiling]
- ICorProfilerCallback2::FinalizeableObjectQueued method [.NET Framework profiling]
ms.assetid: 92d76893-683c-475d-9996-5bff03cdb10f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9b8a952bb2827d1946787f15151887fa25b8da52
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54733726"
---
# <a name="icorprofilercallback2finalizeableobjectqueued-method"></a>ICorProfilerCallback2::FinalizeableObjectQueued-Methode
Benachrichtigt Sie den Profiler, dass ein Objekt mit einem Finalizer an den Finalizerthread für die Ausführung von in die Warteschlange gestellt hat seine `Finalize` Methode.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT FinalizeableObjectQueued(  
    [in] DWORD finalizerFlags,  
    [in] ObjectID objectID);  
```  
  
#### <a name="parameters"></a>Parameter  
 `finalizerFlags`  
 [in] Der Wert der [COR_PRF_FINALIZER_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-finalizer-flags-enumeration.md) Enumeration, die Aspekte des Finalizers beschreibt.  
  
 `objectID`  
 [in] Die ID des Objekts, das in die Warteschlange gestellt wurde.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** CorProf.idl, CorProf.h  
  
 **Bibliothek:** CorGuids.lib  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch
- [ICorProfilerCallback-Schnittstelle](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [ICorProfilerCallback2-Schnittstelle](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
