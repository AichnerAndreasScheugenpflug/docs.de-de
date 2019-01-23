---
title: CorDebugIntercept-Enumeration
ms.date: 03/30/2017
api_name:
- CorDebugIntercept
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugIntercept
helpviewer_keywords:
- CorDebugIntercept enumeration [.NET Framework debugging]
ms.assetid: 3d5b642e-7ef2-428b-a5ae-509c35ed461a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d15f34c55f0ee261c65649e9d431944201c546f0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506029"
---
# <a name="cordebugintercept-enumeration"></a><span data-ttu-id="044e5-102">CorDebugIntercept-Enumeration</span><span class="sxs-lookup"><span data-stu-id="044e5-102">CorDebugIntercept Enumeration</span></span>
<span data-ttu-id="044e5-103">Gibt die Codetypen an, die schrittweise abgefangen werden können.</span><span class="sxs-lookup"><span data-stu-id="044e5-103">Indicates the types of code that can be intercepted (that is, stepped into).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="044e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="044e5-104">Syntax</span></span>  
  
```  
typedef enum CorDebugIntercept {  
    INTERCEPT_NONE                = 0x0,  
    INTERCEPT_CLASS_INIT          = 0x01,  
    INTERCEPT_EXCEPTION_FILTER    = 0x02,  
    INTERCEPT_SECURITY            = 0x04,  
    INTERCEPT_CONTEXT_POLICY      = 0x08,  
    INTERCEPT_INTERCEPTION        = 0x10,  
    INTERCEPT_ALL                 = 0xffff  
} CorDebugIntercept;  
```  
  
## <a name="members"></a><span data-ttu-id="044e5-105">Member</span><span class="sxs-lookup"><span data-stu-id="044e5-105">Members</span></span>  
  
|<span data-ttu-id="044e5-106">Member</span><span class="sxs-lookup"><span data-stu-id="044e5-106">Member</span></span>|<span data-ttu-id="044e5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="044e5-107">Description</span></span>|  
|------------|-----------------|  
|`INTERCEPT_NONE`|<span data-ttu-id="044e5-108">Kein Code kann abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="044e5-108">No code can be intercepted.</span></span>|  
|`INTERCEPT_CLASS_INIT`|<span data-ttu-id="044e5-109">Ein Konstruktor kann abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="044e5-109">A constructor can be intercepted.</span></span>|  
|`INTERCEPT_EXCEPTION_FILTER`|<span data-ttu-id="044e5-110">Ein Ausnahmefilter kann abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="044e5-110">An exception filter can be intercepted.</span></span>|  
|`INTERCEPT_SECURITY`|<span data-ttu-id="044e5-111">Code, der die Einhaltung von Sicherheitsrichtlinien erzwingt, kann abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="044e5-111">Code that enforces security can be intercepted.</span></span>|  
|`INTERCEPT_CONTEXT_POLICY`|<span data-ttu-id="044e5-112">Eine Kontextrichtlinie kann abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="044e5-112">A context policy can be intercepted.</span></span>|  
|`INTERCEPT_INTERCEPTION`|<span data-ttu-id="044e5-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="044e5-113">Not used.</span></span>|  
|`INTERCEPT_ALL`|<span data-ttu-id="044e5-114">Jeder Code kann abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="044e5-114">All code can be intercepted.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="044e5-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="044e5-115">Remarks</span></span>  
 <span data-ttu-id="044e5-116">Verwenden der [ICorDebugStepper:: SetInterceptMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setinterceptmask-method.md) Methode, um die Codetypen festzulegen, die abgefangen werden können.</span><span class="sxs-lookup"><span data-stu-id="044e5-116">Use the [ICorDebugStepper::SetInterceptMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setinterceptmask-method.md) method to establish the types of code that can be intercepted.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="044e5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="044e5-117">Requirements</span></span>  
 <span data-ttu-id="044e5-118">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="044e5-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="044e5-119">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="044e5-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="044e5-120">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="044e5-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="044e5-121">**.NET Framework-Versionen:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="044e5-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="044e5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="044e5-122">See also</span></span>
- [<span data-ttu-id="044e5-123">Debuggen von Enumerationen</span><span class="sxs-lookup"><span data-stu-id="044e5-123">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
