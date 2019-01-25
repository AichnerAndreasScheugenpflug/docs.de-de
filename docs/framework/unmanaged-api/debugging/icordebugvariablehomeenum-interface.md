---
title: ICorDebugVariableHomeEnum-Schnittstelle
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHomeEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHomeEnum
helpviewer_keywords:
- ICorDebugVariableHomeEnum interface [.NET Framework debugging]
ms.assetid: c312ae6d-c8dc-48d6-9f1e-ead515c88fdf
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 43f63e09c654c7aab9f1da0db7587a92bee4fb79
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54632035"
---
# <a name="icordebugvariablehomeenum-interface"></a>ICorDebugVariableHomeEnum-Schnittstelle
Stellt einen Enumerator für die lokalen Variablen und Argumente in einer Funktion an.  
  
## <a name="methods"></a>Methoden  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[Next-Methode](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md)|Ruft die angegebene Anzahl von [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) -Instanzen, die Informationen über die lokalen Variablen und Argumente in einer Funktion enthalten.|  
  
## <a name="remarks"></a>Hinweise  
 Die `ICorDebugVariableHomeEnum` -Schnittstelle implementiert, die ICorDebugEnum-Schnittstelle.  
  
 Ein `ICorDebugVariableHomeEnum` Instanz wird mit aufgefüllt [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) Instanzen durch Aufrufen der [ICorDebugCode4::EnumerateVariableHomes](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-enumeratevariablehomes-method.md) Methode. Jede [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) Instanzen in der Auflistung darstellt, eine lokale Variable oder ein Argument in einer Funktion. Die [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) Objekte in der Auflistung aufgelistet werden können, durch den Aufruf der [ICorDebugVariableHomeEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md) Methode.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** CorDebug.idl, CorDebug.h  
  
 **Bibliothek:** CorGuids.lib  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch
- [ICorDebugVariableHome-Schnittstelle](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)
- [Debuggen von Schnittstellen](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
