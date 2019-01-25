---
title: ICLRDataTarget3-Schnittstelle
ms.date: 03/30/2017
api_name:
- ICLRDataTarget3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: d2711bdf-64b3-404c-a0c3-01ba4907f703
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 974abb123c4c11f6bb512431cea5cc6460a5c55a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54654739"
---
# <a name="iclrdatatarget3-interface"></a><span data-ttu-id="46328-102">ICLRDataTarget3-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="46328-102">ICLRDataTarget3 Interface</span></span>
<span data-ttu-id="46328-103">Eine Unterklasse von [ICLRDataTarget2](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md) , Zugriff auf Informationen über die Ausnahme bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="46328-103">A subclass of [ICLRDataTarget2](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md) that provides access to exception information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="46328-104">Methoden</span><span class="sxs-lookup"><span data-stu-id="46328-104">Methods</span></span>  
  
|<span data-ttu-id="46328-105">Methode</span><span class="sxs-lookup"><span data-stu-id="46328-105">Method</span></span>|<span data-ttu-id="46328-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46328-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="46328-107">GetExceptionRecord-Methode</span><span class="sxs-lookup"><span data-stu-id="46328-107">GetExceptionRecord Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionrecord-method.md)|<span data-ttu-id="46328-108">Wird durch die Common Language Runtime (CLR)- Datenzugriffsdienste aufgerufen, um den Ausnahmedatensatz abzurufen, der dem Zielprozess zugordnet ist.</span><span class="sxs-lookup"><span data-stu-id="46328-108">Called by the common language runtime (CLR) data access services to retrieve the exception record associated with the target process.</span></span>|  
|[<span data-ttu-id="46328-109">GetExceptionContextRecord-Methode</span><span class="sxs-lookup"><span data-stu-id="46328-109">GetExceptionContextRecord Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptioncontextrecord-method.md)|<span data-ttu-id="46328-110">Wird durch die CLR-Datenzugriffsdienste aufgerufen, um den Kontextdatensatz abzurufen, der dem Zielprozess zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="46328-110">Called by the CLR data access services to retrieve the context record associated with the target process.</span></span>|  
|[<span data-ttu-id="46328-111">GetExceptionThreadID-Methode</span><span class="sxs-lookup"><span data-stu-id="46328-111">GetExceptionThreadID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionthreadid-method.md)|<span data-ttu-id="46328-112">Wird durch die CLR-Datenzugriffsdienste aufgerufen, um die ID des Threads abzurufen, der die Ausnahme ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="46328-112">Called by the CLR data access services to get the ID of the thread that threw the exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="46328-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="46328-113">Remarks</span></span>  
 <span data-ttu-id="46328-114">Der API-Client (d. h. der Debugger) muss diese Schnittstelle in einer für den jeweiligen Zielprozess geeigneten Form implementieren.</span><span class="sxs-lookup"><span data-stu-id="46328-114">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="46328-115">So hätte ein Liveprozess z. B. eine andere Implementierung als ein Speicherabbild.</span><span class="sxs-lookup"><span data-stu-id="46328-115">For example, a live process would have an implementation different from that of a memory dump.</span></span> <span data-ttu-id="46328-116">Das Ziel unterstützt möglicherweise keine Änderung seiner Arbeitsspeicherbereiche.</span><span class="sxs-lookup"><span data-stu-id="46328-116">The target may not support modification of its memory regions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46328-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46328-117">Requirements</span></span>  
 <span data-ttu-id="46328-118">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="46328-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46328-119">**Header:** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="46328-119">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="46328-120">**Bibliothek:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46328-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46328-121">**.NET Framework-Versionen:** [!INCLUDE[v451_update](../../../../includes/v451-update-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46328-121">**.NET Framework Versions:** [!INCLUDE[v451_update](../../../../includes/v451-update-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46328-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46328-122">See also</span></span>
- [<span data-ttu-id="46328-123">ICLRDataTarget-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="46328-123">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
- [<span data-ttu-id="46328-124">ICLRDataTarget2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="46328-124">ICLRDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md)
- [<span data-ttu-id="46328-125">Debuggen von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="46328-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
