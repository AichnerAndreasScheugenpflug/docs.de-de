---
title: ISymUnmanagedDocument::FindClosestLine-Methode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.FindClosestLine
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::FindClosestLine
helpviewer_keywords:
- FindClosestLine method [.NET Framework debugging]
- ISymUnmanagedDocument::FindClosestLine method [.NET Framework debugging]
ms.assetid: 628f2a04-e529-407d-841e-3b3da219a9cb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 96ad0e34bf638c378f37e317f790696c2ac7cb25
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54519696"
---
# <a name="isymunmanageddocumentfindclosestline-method"></a><span data-ttu-id="af4c1-102">ISymUnmanagedDocument::FindClosestLine-Methode</span><span class="sxs-lookup"><span data-stu-id="af4c1-102">ISymUnmanagedDocument::FindClosestLine Method</span></span>
<span data-ttu-id="af4c1-103">Gibt die nächste Zeile, die ein Sequenzpunkt ist, ausgehend von einer Zeile in diesem Dokument, das nicht unbedingt ein Sequenzpunkt zurück.</span><span class="sxs-lookup"><span data-stu-id="af4c1-103">Returns the closest line that is a sequence point, given a line in this document that may or may not be a sequence point.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="af4c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af4c1-104">Syntax</span></span>  
  
```  
HRESULT FindClosestLine(  
    [in]  ULONG32  line,  
    [out, retval] ULONG32*  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="af4c1-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="af4c1-105">Parameters</span></span>  
 `line`  
 <span data-ttu-id="af4c1-106">[in] Eine Zeile in diesem Dokument.</span><span class="sxs-lookup"><span data-stu-id="af4c1-106">[in] A line in this document.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="af4c1-107">[out] Ein Zeiger auf eine Variable, die Zeile empfängt.</span><span class="sxs-lookup"><span data-stu-id="af4c1-107">[out] A pointer to a variable that receives the line.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="af4c1-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af4c1-108">Return Value</span></span>  
 <span data-ttu-id="af4c1-109">S_OK, wenn die Methode erfolgreich ist; andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="af4c1-109">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="af4c1-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af4c1-110">See also</span></span>
- [<span data-ttu-id="af4c1-111">ISymUnmanagedDocument-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="af4c1-111">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
