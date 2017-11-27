---
title: FunctionIDMapper2-Funktion
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: FunctionIDMapper2
api_location: mscorwks.dll
api_type: COM
f1_keywords: FunctionIDMapper2
helpviewer_keywords: FunctionIDMapper2 function [.NET Framework profiling]
ms.assetid: 466ad51b-8f0c-41d9-81f7-371aac3374cb
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 5da0acdd7622ad06879b57d8d4b2a9faeba10ca9
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/21/2017
---
# <a name="functionidmapper2-function"></a><span data-ttu-id="ad11e-102">FunctionIDMapper2-Funktion</span><span class="sxs-lookup"><span data-stu-id="ad11e-102">FunctionIDMapper2 Function</span></span>
<span data-ttu-id="ad11e-103">Benachrichtigt den Profiler, dass der angegebene Bezeichner einer Funktion einer alternativen ID zu verwendende zugeordnet werden kann die [FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md), [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md), und [FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md), oder[FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md), [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md), und [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) Rückrufe für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="ad11e-103">Notifies the profiler that the given identifier of a function may be remapped to an alternative ID to be used in the [FunctionEnter3](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md), [FunctionLeave3](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md), and [FunctionTailcall3](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md), or[FunctionEnter3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md), [FunctionLeave3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md), and [FunctionTailcall3WithInfo](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md) callbacks for that function.</span></span> <span data-ttu-id="ad11e-104">Mit `FunctionIDMapper2`kann der Profiler auch angeben, ob er Rückrufe für diese Funktion empfangen will.</span><span class="sxs-lookup"><span data-stu-id="ad11e-104">`FunctionIDMapper2` also enables the profiler to indicate whether it wants to receive callbacks for that function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad11e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad11e-105">Syntax</span></span>  
  
```  
UINT_PTR __stdcall FunctionIDMapper2 (  
    [in]  FunctionID  funcId,  
    [in]  void * clientData,  
    [out] BOOL       *pbHookFunction  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ad11e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad11e-106">Parameters</span></span>  
 `funcId`  
 <span data-ttu-id="ad11e-107">[in] Der Funktionsbezeichner, der neu zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad11e-107">[in] The function identifier to be remapped.</span></span>  
  
 `clientData`  
 <span data-ttu-id="ad11e-108">[in] Ein Zeiger auf Daten, mit denen Mehrdeutigkeiten zwischen Laufzeiten aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="ad11e-108">[in] A pointer to data that is used to disambiguate among runtimes.</span></span>  
  
 `pbHookFunction`  
 <span data-ttu-id="ad11e-109">[out] Ein Zeiger auf einen Wert, den der Profiler auf `true` festlegt, wenn er die Rückrufe `FunctionEnter3`, `FunctionLeave3` und `FunctionTailcall3` oder `FunctionEnter3WithInfo`, `FunctionLeave3WithInfo` und `FunctionTailcall3WithInfo` empfangen möchte. Andernfalls wird der Wert auf `false` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ad11e-109">[out] A pointer to a value that the profiler sets to `true` if it wants to receive `FunctionEnter3`, `FunctionLeave3`, and `FunctionTailcall3`, or `FunctionEnter3WithInfo`, `FunctionLeave3WithInfo`, and `FunctionTailcall3WithInfo` callbacks; otherwise, it sets this value to `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ad11e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad11e-110">Return Value</span></span>  
 <span data-ttu-id="ad11e-111">Der Profiler gibt einen Wert zurück, den das Ausführungsmodul als alternativen Funktionsbezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad11e-111">The profiler returns a value that the execution engine uses as an alternative function identifier.</span></span> <span data-ttu-id="ad11e-112">Der Rückgabewert darf nicht NULL sein, es sei denn, in `false` wird `pbHookFunction` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad11e-112">The return value cannot be null unless `false` is returned in `pbHookFunction`.</span></span> <span data-ttu-id="ad11e-113">Andernfalls führt ein Rückgabewert von NULL zu unvorhersehbaren Ergebnissen, einschließlich des möglichen Anhaltens des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="ad11e-113">Otherwise, a null return value produces unpredictable results, including possibly halting the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ad11e-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad11e-114">Remarks</span></span>  
 <span data-ttu-id="ad11e-115">Diese Methode erweitert die [FunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md) Funktion mit einem zusätzlichen Parameter, die zum Übergeben von Clientdaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad11e-115">This method extends the [FunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md) function with an additional parameter that is used to pass client data.</span></span> <span data-ttu-id="ad11e-116">Die Clientdaten werden verwendet, um Mehrdeutigkeiten zwischen Laufzeiten aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="ad11e-116">The client data is used to disambiguate among runtimes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ad11e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad11e-117">Requirements</span></span>  
 <span data-ttu-id="ad11e-118">**Plattformen:** finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ad11e-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ad11e-119">**Header:** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="ad11e-119">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="ad11e-120">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ad11e-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ad11e-121">**.NET Framework-Versionen:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ad11e-121">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad11e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad11e-122">See Also</span></span>  
 [<span data-ttu-id="ad11e-123">ICorProfilerInfo:: SetFunctionIDMapper</span><span class="sxs-lookup"><span data-stu-id="ad11e-123">ICorProfilerInfo::SetFunctionIDMapper</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setfunctionidmapper-method.md)  
 [<span data-ttu-id="ad11e-124">ICorProfilerInfo3:: Setfunctionidmapper2</span><span class="sxs-lookup"><span data-stu-id="ad11e-124">ICorProfilerInfo3::SetFunctionIDMapper2</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-setfunctionidmapper2-method.md)  
 [<span data-ttu-id="ad11e-125">FunctionEnter3</span><span class="sxs-lookup"><span data-stu-id="ad11e-125">FunctionEnter3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3-function.md)  
 [<span data-ttu-id="ad11e-126">FunctionLeave3</span><span class="sxs-lookup"><span data-stu-id="ad11e-126">FunctionLeave3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3-function.md)  
 [<span data-ttu-id="ad11e-127">FunctionTailcall3</span><span class="sxs-lookup"><span data-stu-id="ad11e-127">FunctionTailcall3</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3-function.md)  
 [<span data-ttu-id="ad11e-128">FunctionEnter3WithInfo</span><span class="sxs-lookup"><span data-stu-id="ad11e-128">FunctionEnter3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionenter3withinfo-function.md)  
 [<span data-ttu-id="ad11e-129">FunctionLeave3WithInfo</span><span class="sxs-lookup"><span data-stu-id="ad11e-129">FunctionLeave3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functionleave3withinfo-function.md)  
 [<span data-ttu-id="ad11e-130">FunctionTailcall3WithInfo</span><span class="sxs-lookup"><span data-stu-id="ad11e-130">FunctionTailcall3WithInfo</span></span>](../../../../docs/framework/unmanaged-api/profiling/functiontailcall3withinfo-function.md)  
 [<span data-ttu-id="ad11e-131">Profilerstellung für globale statische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad11e-131">Profiling Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-global-static-functions.md)