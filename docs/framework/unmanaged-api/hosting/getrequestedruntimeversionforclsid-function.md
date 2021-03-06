---
title: GetRequestedRuntimeVersionForCLSID-Funktion
ms.date: 03/30/2017
api_name:
- GetRequestedRuntimeVersionForCLSID
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetRequestedRuntimeVersionForCLSID
helpviewer_keywords:
- GetRequestedRuntimeVersionForCLSID function [.NET Framework hosting]
ms.assetid: 5bb12f9a-0612-434b-b4ed-2db636a20bec
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2e00bc95dd9b54d5451da65cefbfff13395e467f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54511958"
---
# <a name="getrequestedruntimeversionforclsid-function"></a>GetRequestedRuntimeVersionForCLSID-Funktion
Ruft die entsprechende Version zur common Language Runtime (CLR) für die Klasse mit dem angegebenen `CLSID`.  
  
 Diese Funktion ist in [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)] veraltet.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT GetRequestedRuntimeVersionForCLSID (  
    [in]  REFCLSID   rclsid,   
    [out]  LPWSTR     pVersion,   
    [in]  DWORD      cchBuffer,   
    [out] DWORD*     dwLength,   
    [in]  CLSID_RESOLUTION_FLAGS dwResolutionFlags  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `rclsid`  
 [in]  Die `CLSID` der Komponente.  
  
 `pVersion`  
 [out]  Ein Puffer, der die Versionsnummer-Zeichenfolge nach dem erfolgreichen Abschluss enthält.  
  
 `cchBuffer`  
 [in]  Die Größe in Breitzeichen, der die `pVersion` Puffer.  
  
 `dwLength`  
 [out] Die Länge des zurückgegebenen Puffers in Bytes.  
  
 `dwResolutionFlags`  
 [in]  Einer der CLSID_RESOLUTION_FLAGS-Werte. Die folgenden Werte werden unterstützt:  
  
-   CLSID_RESOLUTION_DEFAULT: (0 x 0) gibt an, dass die Interop-Standardverhalten verwendet werden soll.  
  
-   CLSID_RESOLUTION_REGISTERED: (0 x 1) gibt an, die die Registrierung durchsucht werden soll, und Shimrichtlinie angewendet werden soll.  
  
## <a name="return-value"></a>Rückgabewert  
  
|HRESULT|Beschreibung|  
|-------------|-----------------|  
|S_OK|Die Funktion wurde erfolgreich zurückgegeben.|  
|E_INVALIDARG|Einer der Parameter hat einen ungültigen Typ oder Format.|  
|ERROR_INSUFFICIENT_BUFFER|Die `pVersion` Puffer ist nicht groß genug für die gesamte Versionszeichenfolge.|  
|REGDB_E_CLASSNOTREG|Es gibt keine Klasse, die mit dem angegebenen registriert `CLSID`.|  
|E_POINTER|`dwLength` null ist, oder `cchBuffer` ist groß genug für die Versionszeichenfolge, aber `pVersion` ist null.|  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** MSCorEE.h  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch
- [Veraltete CLR-Hostingfunktionen](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
