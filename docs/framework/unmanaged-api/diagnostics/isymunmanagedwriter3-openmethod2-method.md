---
title: ISymUnmanagedWriter3::OpenMethod2-Methode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter3.OpenMethod2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter3::OpenMethod2
helpviewer_keywords:
- ISymUnmanagedWriter3::OpenMethod2 method [.NET Framework debugging]
- OpenMethod2 method [.NET Framework debugging]
ms.assetid: 025e358c-448f-4423-a2f2-57acf437c8a5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b641f463eb9b664597b4806a6353278e8027d5b8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54709103"
---
# <a name="isymunmanagedwriter3openmethod2-method"></a><span data-ttu-id="70f5e-102">ISymUnmanagedWriter3::OpenMethod2-Methode</span><span class="sxs-lookup"><span data-stu-id="70f5e-102">ISymUnmanagedWriter3::OpenMethod2 Method</span></span>
<span data-ttu-id="70f5e-103">Öffnet eine Methode, und bietet die echten Abschnittoffset im Bild.</span><span class="sxs-lookup"><span data-stu-id="70f5e-103">Opens a method and provides its real section offset in the image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70f5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70f5e-104">Syntax</span></span>  
  
```  
HRESULT OpenMethod2(   
    [in] mdMethodDef method,  
    [in] ULONG32 isect,  
    [in] ULONG32 offset);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="70f5e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="70f5e-105">Parameters</span></span>  
 `method`  
 <span data-ttu-id="70f5e-106">[in] Das Metadatentoken für die Methode, die geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="70f5e-106">[in] The metadata token for the method to be opened.</span></span>  
  
 `isect`  
 <span data-ttu-id="70f5e-107">[in] Der Abschnittoffset im Bild.</span><span class="sxs-lookup"><span data-stu-id="70f5e-107">[in] The section offset in the image.</span></span>  
  
 `offset`  
 <span data-ttu-id="70f5e-108">[in] Der Offset im Bild.</span><span class="sxs-lookup"><span data-stu-id="70f5e-108">[in] The offset in the image.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="70f5e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70f5e-109">Return Value</span></span>  
 <span data-ttu-id="70f5e-110">S_OK, wenn die Methode erfolgreich ist; andernfalls E_FAIL oder einen anderen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="70f5e-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="70f5e-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70f5e-111">Requirements</span></span>  
 <span data-ttu-id="70f5e-112">**Header:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="70f5e-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70f5e-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70f5e-113">See also</span></span>
- [<span data-ttu-id="70f5e-114">ISymUnmanagedWriter3-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="70f5e-114">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
- [<span data-ttu-id="70f5e-115">OpenMethod-Methode</span><span class="sxs-lookup"><span data-stu-id="70f5e-115">OpenMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)
