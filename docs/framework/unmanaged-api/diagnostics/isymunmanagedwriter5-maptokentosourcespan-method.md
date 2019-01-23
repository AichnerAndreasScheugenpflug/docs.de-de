---
title: ISymUnmanagedWriter5::MapTokenToSourceSpan-Methode
ms.date: 03/30/2017
ms.assetid: d0fbbf61-71c6-4fb1-8c9f-d619ca5d7d68
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 158ff204d57c3b08ced91d397ef71f24c5f44248
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499209"
---
# <a name="isymunmanagedwriter5maptokentosourcespan-method"></a><span data-ttu-id="e35ea-102">ISymUnmanagedWriter5::MapTokenToSourceSpan-Methode</span><span class="sxs-lookup"><span data-stu-id="e35ea-102">ISymUnmanagedWriter5::MapTokenToSourceSpan Method</span></span>
<span data-ttu-id="e35ea-103">Zuordnungen in die Zeile für die angegebene Quelle das angegebene Metadatentoken umfassen, in der angegebenen Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="e35ea-103">Maps the given metadata token to the given source line span in the specified source file.</span></span>  
  
 <span data-ttu-id="e35ea-104">Muss aufgerufen werden, zwischen den Aufrufen [OpenMapTokensToSourceSpans-Methode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) und [CloseMapTokensToSourceSpans-Methode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span><span class="sxs-lookup"><span data-stu-id="e35ea-104">Must be called between calls to [OpenMapTokensToSourceSpans Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) and [CloseMapTokensToSourceSpans Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e35ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e35ea-105">Syntax</span></span>  
  
```idl  
HRESULT MapTokenToSourceSpan(    [in] mdToken token,    [in] ISymUnmanagedDocumentWriter* document,    [in] ULONG32 line,    [in] ULONG32 column,    [in] ULONG32 endLine,    [in] ULONG32 endColumn);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e35ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e35ea-106">Parameters</span></span>  
  
|<span data-ttu-id="e35ea-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e35ea-107">Parameter</span></span>|<span data-ttu-id="e35ea-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e35ea-108">Description</span></span>|  
|---------------|-----------------|  
|`token`||  
|`document`||  
|`line`||  
|`column`||  
|`endLine`||  
|`endColumn`||  
  
## <a name="return-value"></a><span data-ttu-id="e35ea-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e35ea-109">Return Value</span></span>  
 <span data-ttu-id="e35ea-110">Gibt `HRESULT`zurück.</span><span class="sxs-lookup"><span data-stu-id="e35ea-110">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e35ea-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e35ea-111">Requirements</span></span>  
 <span data-ttu-id="e35ea-112">**Header:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e35ea-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e35ea-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e35ea-113">See also</span></span>
- [<span data-ttu-id="e35ea-114">ISymUnmanagedWriter5-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e35ea-114">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
