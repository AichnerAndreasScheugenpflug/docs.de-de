---
title: IMetaDataImport::GetNativeCallConvFromSig-Methode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetNativeCallConvFromSig
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetNativeCallConvFromSig
helpviewer_keywords:
- GetNativeCallConvFromSig method [.NET Framework metadata]
- IMetaDataImport::GetNativeCallConvFromSig method [.NET Framework metadata]
ms.assetid: 50e04026-4d4a-47d9-96c1-f4677d6d938b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 752dcf90f790d6403c37fcee377c35656b655b36
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491065"
---
# <a name="imetadataimportgetnativecallconvfromsig-method"></a>IMetaDataImport::GetNativeCallConvFromSig-Methode
Ruft die native Aufrufkonvention für die Methode ab, die durch den angegebenen Signaturzeiger dargestellt wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT GetNativeCallConvFromSig (  
   [in]  void const  *pvSig,  
   [in]  ULONG       cbSig,  
   [out] ULONG       *pCallConv  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pvSig`  
 [in] Ein Zeiger auf die Metadatensignatur der Methode, die Aufrufkonvention für zurück.  
  
 `cbSig`  
 [in] Die Größe in Bytes der `pvSig`.  
  
 `pCallConv`  
 [out] Ein Zeiger auf die systemeigene Aufrufkonvention.  
  
## <a name="requirements"></a>Anforderungen  
 **Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Header:** Cor.h  
  
 **Bibliothek:** Als Ressource in MsCorEE.dll enthalten  
  
 **.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Runtime.InteropServices.CallingConvention>
- [IMetaDataImport-Schnittstelle](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2-Schnittstelle](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
