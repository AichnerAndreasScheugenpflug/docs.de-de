---
title: ICorProfilerInfo3::GetAppDomainsContainingModule-Methode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.GetAppDomainsContainingModule Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::GetAppDomainsContainingModule
helpviewer_keywords:
- GetAppDomainsContainingModule method [.NET Framework profiling]
- ICorProfilerInfo3::GetAppDomainsContainingModule method [.NET Framework profiling]
ms.assetid: 603b3881-ea94-4dca-95cd-91eebac873a0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 343834492776fdb09a68210fb80138ec2c588773
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54741151"
---
# <a name="icorprofilerinfo3getappdomainscontainingmodule-method"></a>ICorProfilerInfo3::GetAppDomainsContainingModule-Methode
Ruft die Bezeichner der Anwendungsdomänen ab, in denen das angegebene Modul geladen wurde.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT GetAppDomainsContainingModule(  
            [in] ModuleID moduleId,  
            [in] ULONG32 cAppDomainIds,  
            [out] ULONG32 *pcAppDomainIds,  
            [out, size_is(cAppDomainIds), length_is(*pcAppDomainIds)]  
                    AppDomainID appDomainIds[]);  
```  
  
#### <a name="parameters"></a>Parameter  
 `moduleId`  
 [in] Die ID des geladenen Moduls.  
  
 `cAppDomainIds`  
 [in] Die Größe des `appDomainIds`-Arrays.  
  
 `pcAppDomainIds`  
 [out] Ein Zeiger auf die Gesamtzahl von zurückgegebenen Elementen.  
  
 `appDomainIds`  
 [out] Ein Array von ID-Werten der Anwendungsdomänen.  
  
## <a name="remarks"></a>Hinweise  
 Die Methode verwendet vom Aufrufer reservierte Puffer.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** CorProf.idl, CorProf.h  
  
 **Bibliothek:** CorGuids.lib  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch
- [ICorProfilerFunctionEnum-Schnittstelle](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md)
- [ICorProfilerInfo3-Schnittstelle](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [Profilerstellungsschnittstellen](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [Profilerstellung](../../../../docs/framework/unmanaged-api/profiling/index.md)
