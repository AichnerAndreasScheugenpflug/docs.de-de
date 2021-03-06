---
title: ICorDebugFunction-Schnittstelle1
ms.date: 03/30/2017
api_name:
- ICorDebugFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction
helpviewer_keywords:
- ICorDebugFunction interface [.NET Framework debugging]
ms.assetid: 783faea9-8083-41c1-b04a-51a81ac4c8f3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b810ce8634781438faccac25f96442624a78ea0a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676769"
---
# <a name="icordebugfunction-interface1"></a>ICorDebugFunction-Schnittstelle1
Stellt eine verwaltete Funktion oder Methode dar.  
  
## <a name="methods"></a>Methoden  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[CreateBreakpoint-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-createbreakpoint-method.md)|Erstellt einen Haltepunkt am Anfang dieser Funktion.|  
|[GetClass-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getclass-method.md)|Ruft ein ICorDebugClass-Objekt, das die Klasse darstellt, die, der diese Funktion ein Member ist.|  
|[GetCurrentVersionNumber-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getcurrentversionnumber-method.md)|Ruft die Versionsnummer der letzten Änderung dieser Funktion ab.|  
|[GetILCode-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getilcode-method.md)|Ruft die Microsoft intermediate Language (MSIL)-Code für diese Funktion ab.|  
|[GetLocalVarSigToken-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getlocalvarsigtoken-method.md)|Ruft den Metadatentoken für die Signatur der lokalen Variablen der Funktion, die von diesem dargestellt wird `ICorDebugFunction` Instanz.|  
|[GetModule-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getmodule-method.md)|Ruft das Modul, in dem diese Funktion definiert ist.|  
|[GetNativeCode-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-getnativecode-method.md)|Ruft den systemeigenen Code für diese Funktion ab.|  
|[GetToken-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction-gettoken-method.md)|Ruft den Metadatentoken für diese Funktion.|  
  
## <a name="remarks"></a>Hinweise  
 Die `ICorDebugFunction` Schnittstelle stellt eine Funktion mit generischen Typparametern keine dar. Z. B. eine `ICorDebugFunction` Instanz darstellen würde `Func<T>` , nicht jedoch `Func<string>`. Rufen Sie [ICorDebugILFrame2:: EnumerateTypeParameters](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe2-enumeratetypeparameters-method.md) um die generischen Typparameter zu erhalten.  
  
 Die Beziehung zwischen einer Methode Metadatentoken `mdMethodDef`, und einer Methode `ICorDebugFunction` Objekt ist abhängig davon, ob bearbeiten und Fortfahren für die Funktion zulässig ist:  
  
-   Wenn Bearbeiten und Fortfahren wird für die Funktion nicht zulässig, besteht eine direkte Beziehung zwischen der `ICorDebugFunction` Objekt und die `mdMethodDef` token. D. h. die Funktion verfügt über eine `ICorDebugFunction` Objekt und eine `mdMethodDef` token.  
  
-   Wenn Bearbeiten und Fortfahren für die Funktion zulässig ist, besteht eine n: 1 Beziehung zwischen der `ICorDebugFunction` Objekt und die `mdMethodDef` token. Also möglicherweise die Funktion viele Instanzen des `ICorDebugFunction`, einen für jede Version der Funktion, aber nur eine `mdMethodDef` token.  
  
> [!NOTE]
>  Diese Schnittstelle kann weder computerübergreifend noch prozessübergreifend remote aufgerufen werden.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** CorDebug.idl, CorDebug.h  
  
 **Bibliothek:**  CorGuids.lib  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch
- [Debuggen von Schnittstellen](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
