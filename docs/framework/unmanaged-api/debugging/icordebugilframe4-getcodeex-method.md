---
title: ICorDebugILFrame4::GetCodeEx-Methode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugILFrame4.GetLocalVariableEx
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: aeda0e42-29ee-4ca8-9f21-ac4641677a62
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5574b457925506f3178af7c636a834fad4fdd15e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54502455"
---
# <a name="icordebugilframe4getcodeex-method"></a>ICorDebugILFrame4::GetCodeEx-Methode
[Wird nur in .NET Framework 4.5.2 und neueren Versionen unterstützt]  
  
 Ruft einen Zeiger auf den Code ab, der vom Stapelrahmen ausgeführt wird.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT GetCodeEx(  
   [in] ILCodeKind flags,   
   [out] ICorDebugCode **ppCode  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `flags`  
 [in] Ein [ILCodeKind](../../../../docs/framework/unmanaged-api/debugging/ilcodekind-enumeration.md) -Enumerationsmember, der angibt, ob die intermediate Language (IL), die von der Profiler ReJIT-Anfrage definiert, die im Rahmen enthalten ist.  
  
 `ppCode`  
 [out] Ein Zeiger auf die Adresse ein "ICorDebugCode"-Objekt, das den Code darstellt, den diesen Stapelrahmen ausgeführt wird.  
  
## <a name="remarks"></a>Hinweise  
 Diese Methode ähnelt der [ICorDebugFrame:: GetCode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcode-method.md) -Methode, mit dem Unterschied, dass sie optional auf Code von der Profiler ReJIT-Anfrage definiert zugreift. Beim Aufruf dieser Methode eine `flags` Wert `ILCODE_ORIGINAL_IL` entspricht dem Aufruf [GetCode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcode-method.md); Wenn die Methode instrumentiert ist, die IL nicht zugegriffen werden. `ILCODE_REJIT_IL` ermöglicht dem Debugger auf den IL-Code durch der Profiler ReJIT-Anfrage definiert. Wenn die IL nicht instrumentiert wurde, `ppCode` ist **null**, und die Methode gibt `S_OK`.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** CorDebug.idl, CorDebug.h  
  
 **Bibliothek:** CorGuids.lib  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch
- [ICorDebugILFrame4-Schnittstelle](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-interface.md)
- [Debuggen von Schnittstellen](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [ReJIT: Einen Leitfaden zur Vorgehensweise](https://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)
