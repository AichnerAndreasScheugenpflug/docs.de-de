---
title: ISymUnmanagedReader::GetMethodByVersion-Methode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetMethodByVersion
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetMethodByVersion
helpviewer_keywords:
- ISymUnmanagedReader::GetMethodByVersion method [.NET Framework debugging]
- GetMethodByVersion method [.NET Framework debugging]
ms.assetid: 6ddb0631-4569-41b3-93e4-50fdfaa486dc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 531ed9a6d8805e22408f112c9e617705057468ff
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624214"
---
# <a name="isymunmanagedreadergetmethodbyversion-method"></a>ISymUnmanagedReader::GetMethodByVersion-Methode
Ruft ein Methodenobjekt des Symbolreaders, wenn ein Methodentoken und eine Versionsnummer für bearbeiten und kopieren. Versionsnummern beginnen bei 1 und werden jedes Mal inkrementiert, die als Ergebnis eines Vorgangs bearbeiten, und kopieren die Methode geändert wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT GetMethodByVersion (  
    [in]  mdMethodDef  token,  
    [in]  int  version,  
    [out, retval] ISymUnmanagedMethod** pRetVal);  
```  
  
#### <a name="parameters"></a>Parameter  
 `token`  
 [in] Das Methodentoken.  
  
 `version`  
 [in] Die Methodenversion.  
  
 `pRetVal`  
 [out] Ein Zeiger auf die zurückgegebene Schnittstelle.  
  
## <a name="return-value"></a>Rückgabewert  
 S_OK, wenn die Methode erfolgreich ist; andernfalls E_FAIL oder einen anderen Fehlercode.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Siehe auch
- [ISymUnmanagedReader-Schnittstelle](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
