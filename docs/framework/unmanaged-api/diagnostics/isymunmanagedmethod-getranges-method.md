---
title: ISymUnmanagedMethod::GetRanges-Methode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetRanges
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetRanges
helpviewer_keywords:
- ISymUnmanagedMethod::GetRanges method [.NET Framework debugging]
- GetRanges method [.NET Framework debugging]
ms.assetid: a85283d8-379c-417a-9736-ddeeef9bcf50
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b6afe0f0d8780a93a7d98f24a11bb67ef65ebf63
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604274"
---
# <a name="isymunmanagedmethodgetranges-method"></a><span data-ttu-id="f8274-102">ISymUnmanagedMethod::GetRanges-Methode</span><span class="sxs-lookup"><span data-stu-id="f8274-102">ISymUnmanagedMethod::GetRanges Method</span></span>
<span data-ttu-id="f8274-103">Gibt bei Angabe einer Position in einem Dokument ein Array von Start- / Endoffsetpaaren, die entsprechen, die den Bereichen Microsoft intermediate Language (MSIL), die die Position innerhalb dieser Methode abgedeckt werden.</span><span class="sxs-lookup"><span data-stu-id="f8274-103">Given a position in a document, returns an array of start and end offset pairs that correspond to the ranges of Microsoft intermediate language (MSIL) that the position covers within this method.</span></span> <span data-ttu-id="f8274-104">Das Array ist ein Array von ganzen Zahlen und weist das Format ["Start", "End", "Start", "Ende"].</span><span class="sxs-lookup"><span data-stu-id="f8274-104">The array is an array of integers and has the format [start, end, start, end].</span></span> <span data-ttu-id="f8274-105">Die Anzahl der Bereichspaare ist die Länge des Arrays geteilt durch 2.</span><span class="sxs-lookup"><span data-stu-id="f8274-105">The number of range pairs is the length of the array divided by 2.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8274-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8274-106">Syntax</span></span>  
  
```  
HRESULT GetRanges(  
    [in]  ISymUnmanagedDocument* document,  
    [in]  ULONG32                line,  
    [in]  ULONG32                column,  
    [in]  ULONG32                cRanges,  
    [out] ULONG32                *pcRanges,  
    [out, size_is(cRanges),  
        length_is(*pcRanges)] ULONG32 ranges[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f8274-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8274-107">Parameters</span></span>  
 `document`  
 <span data-ttu-id="f8274-108">[in] Das Dokument, für das der Offset angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="f8274-108">[in] The document for which the offset is requested.</span></span>  
  
 `line`  
 <span data-ttu-id="f8274-109">[in] Die Dokumentzeile, die den Bereichen entspricht.</span><span class="sxs-lookup"><span data-stu-id="f8274-109">[in] The document line corresponding to the ranges.</span></span>  
  
 `column`  
 <span data-ttu-id="f8274-110">[in] Die Dokumentspalte, die den Bereichen entspricht.</span><span class="sxs-lookup"><span data-stu-id="f8274-110">[in] The document column corresponding to the ranges.</span></span>  
  
 `cRanges`  
 <span data-ttu-id="f8274-111">[in] Die Größe des `ranges`-Arrays.</span><span class="sxs-lookup"><span data-stu-id="f8274-111">[in] The size of the `ranges` array.</span></span>  
  
 `pcRanges`  
 <span data-ttu-id="f8274-112">[out] Ein Zeiger auf eine `ULONG32` , empfängt die Größe des Puffers erforderlich, um die Bereiche enthalten.</span><span class="sxs-lookup"><span data-stu-id="f8274-112">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the ranges.</span></span>  
  
 `ranges`  
 <span data-ttu-id="f8274-113">[out] Ein Zeiger auf den Puffer, der die Bereiche empfängt.</span><span class="sxs-lookup"><span data-stu-id="f8274-113">[out] A pointer to the buffer that receives the ranges.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f8274-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8274-114">Return Value</span></span>  
 <span data-ttu-id="f8274-115">S_OK, wenn die Methode erfolgreich ist; andernfalls E_FAIL oder einen anderen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="f8274-115">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8274-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8274-116">Requirements</span></span>  
 <span data-ttu-id="f8274-117">**Header:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f8274-117">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8274-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8274-118">See also</span></span>
- [<span data-ttu-id="f8274-119">ISymUnmanagedMethod-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f8274-119">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
