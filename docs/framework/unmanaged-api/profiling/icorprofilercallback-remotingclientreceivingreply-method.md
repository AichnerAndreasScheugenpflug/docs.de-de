---
title: ICorProfilerCallback::RemotingClientReceivingReply-Methode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingClientReceivingReply
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingClientReceivingReply
helpviewer_keywords:
- ICorProfilerCallback::RemotingClientReceivingReply method [.NET Framework profiling]
- RemotingClientReceivingReply method [.NET Framework profiling]
ms.assetid: 15cfc300-8231-4ecb-9a04-19851c3eb484
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 313dd7526478377ca457d165de4b95e7e81d93f8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54599785"
---
# <a name="icorprofilercallbackremotingclientreceivingreply-method"></a>ICorProfilerCallback::RemotingClientReceivingReply-Methode
Benachrichtigt den Profiler, die der serverseitigen Teil eines Remoteaufrufs abgeschlossen ist und der Client nun empfängt sowie über die Antwort zu verarbeiten.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT RemotingClientReceivingReply(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);   
```  
  
#### <a name="parameters"></a>Parameter  
 `pCookie`  
 [in] Ein Wert, der entspricht, mit dem Wert im bereitgestellten [ICorProfilerCallback:: RemotingServerSendingReply](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingserversendingreply-method.md) unter diesen Bedingungen:  
  
-   Remoting-GUID-Cookies sind aktiv.  
  
-   Der Kanal ist erfolgreich, bei der Übermittlung der Nachricht.  
  
-   GUID-Cookies werden auf den serverseitigen Prozess aktiv.  
  
 Dies ermöglicht die einfache Kopplung von Remoting aufrufen.  
  
 `fIsAsync`  
 [in] Ein Wert, `true` , wenn der Aufruf asynchron; andernfalls ist `false`.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** CorProf.idl, CorProf.h  
  
 **Bibliothek:** CorGuids.lib  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch
- [ICorProfilerCallback-Schnittstelle](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
