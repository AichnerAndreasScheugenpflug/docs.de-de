---
title: ICorDebugLoadedModule-Schnittstelle
ms.date: 03/30/2017
ms.assetid: 34be6369-2e75-4a95-a538-3b29ac97cf6d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f8f3a881a1beceb7d4aa35e2bd9a5e9e5419a391
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654866"
---
# <a name="icordebugloadedmodule-interface"></a><span data-ttu-id="f167a-102">ICorDebugLoadedModule-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f167a-102">ICorDebugLoadedModule Interface</span></span>
<span data-ttu-id="f167a-103">Stellt Informationen zu einem geladenen Modul bereit.</span><span class="sxs-lookup"><span data-stu-id="f167a-103">Provides information about a loaded module.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f167a-104">Methoden</span><span class="sxs-lookup"><span data-stu-id="f167a-104">Methods</span></span>  
  
|<span data-ttu-id="f167a-105">Methode</span><span class="sxs-lookup"><span data-stu-id="f167a-105">Method</span></span>|<span data-ttu-id="f167a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f167a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f167a-107">GetBaseAddress-Methode</span><span class="sxs-lookup"><span data-stu-id="f167a-107">GetBaseAddress Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-getbaseaddress-method.md)|<span data-ttu-id="f167a-108">Ruft die Basisadresse für das geladene Modul ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f167a-108">Gets the base address of the loaded module.</span></span>|  
|[<span data-ttu-id="f167a-109">GetName-Methode</span><span class="sxs-lookup"><span data-stu-id="f167a-109">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-getname-method.md)|<span data-ttu-id="f167a-110">Ruft den Namen des geladenen Moduls ab.</span><span class="sxs-lookup"><span data-stu-id="f167a-110">Gets the name of the loaded module.</span></span>|  
|[<span data-ttu-id="f167a-111">GetSize-Methode</span><span class="sxs-lookup"><span data-stu-id="f167a-111">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-getsize-method.md)|<span data-ttu-id="f167a-112">Ruft die Größe des geladenen Moduls in Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="f167a-112">Gets the size in bytes of the loaded module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f167a-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f167a-113">Remarks</span></span>  
 <span data-ttu-id="f167a-114">Die `ICorDebugLoadedModule`-Schnittstelle wird von einem Debugger implementiert und von den CLR-Debugschnittstellen verwendet, um Informationen vom Debugger zum geladenen Modul zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f167a-114">The `ICorDebugLoadedModule` interface is implemented by a debugger and is used by the CLR debugging interfaces to get information about the loaded module from the debugger.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f167a-115">Diese Schnittstelle ist nur in Verbindung mit .NET Native verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f167a-115">This interface is available with .NET Native only.</span></span> <span data-ttu-id="f167a-116">Wenn Sie diese Schnittstelle für ICorDebug-Szenarien außerhalb von .NET Native implementieren, ignoriert die Common Language Runtime diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f167a-116">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f167a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f167a-117">Requirements</span></span>  
 <span data-ttu-id="f167a-118">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f167a-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f167a-119">**Header:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f167a-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f167a-120">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f167a-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f167a-121">**.NET Framework-Versionen:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f167a-121">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f167a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f167a-122">See also</span></span>
- [<span data-ttu-id="f167a-123">Debuggen von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f167a-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="f167a-124">Debuggen</span><span class="sxs-lookup"><span data-stu-id="f167a-124">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
