---
title: ICLRRuntimeInfo::GetInterface-Methode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.GetInterface
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::GetInterface
helpviewer_keywords:
- GetInterface method [.NET Framework hosting]
- ICLRRuntimeInfo::GetInterface method [.NET Framework hosting]
ms.assetid: cc7b0e5b-48c3-4509-8ebb-611ddb1f7ec2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 770901d5461d2092ce5f2862624a038caf03e1f7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54678659"
---
# <a name="iclrruntimeinfogetinterface-method"></a><span data-ttu-id="a43bf-102">ICLRRuntimeInfo::GetInterface-Methode</span><span class="sxs-lookup"><span data-stu-id="a43bf-102">ICLRRuntimeInfo::GetInterface Method</span></span>
<span data-ttu-id="a43bf-103">Lädt die CLR in den aktuellen Prozess und gibt Sie Common Language Runtime-Schnittstellenzeiger auf, wie z. B. [ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md), [ICLRStrongName](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md), und [IMetaDataDispenserEx](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md).</span><span class="sxs-lookup"><span data-stu-id="a43bf-103">Loads the CLR into the current process and returns runtime interface pointers, such as [ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md), [ICLRStrongName](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md), and [IMetaDataDispenserEx](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md).</span></span>  
  
 <span data-ttu-id="a43bf-104">Diese Methode ersetzt alle die `CorBindTo`\*-Funktionen in der [Hosten von CLR-Funktionen als veraltet markiert](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md) Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="a43bf-104">This method supersedes all the `CorBindTo`\* functions in the [Deprecated CLR Hosting Functions](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md) section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a43bf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a43bf-105">Syntax</span></span>  
  
```  
HRESULT GetInterface(  
[in]  REFCLSID rclsid,  
[in]  REFIID   riid,  
[out, iid_is(riid), retval] LPVOID *ppUnk);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a43bf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a43bf-106">Parameters</span></span>  
 `rclsid`  
 <span data-ttu-id="a43bf-107">[in] Die CLSID-Schnittstelle für die Co-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a43bf-107">[in] The CLSID interface for the coclass.</span></span>  
  
 `riid`  
 <span data-ttu-id="a43bf-108">[in] Die IID der angeforderten `rclsid` Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a43bf-108">[in] The IID of the requested `rclsid` interface.</span></span>  
  
 `ppUnk`  
 <span data-ttu-id="a43bf-109">[out] Ein Zeiger auf die Schnittstelle abgefragt.</span><span class="sxs-lookup"><span data-stu-id="a43bf-109">[out] A pointer to the queried interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a43bf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a43bf-110">Return Value</span></span>  
 <span data-ttu-id="a43bf-111">Diese Methode gibt die folgenden spezifischen HRESULTs sowie HRESULT-Fehler zurück, die Methodenfehler anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a43bf-111">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="a43bf-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a43bf-112">HRESULT</span></span>|<span data-ttu-id="a43bf-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a43bf-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a43bf-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="a43bf-114">S_OK</span></span>|<span data-ttu-id="a43bf-115">Die Methode wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a43bf-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="a43bf-116">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="a43bf-116">E_POINTER</span></span>|<span data-ttu-id="a43bf-117">`ppUnk` ist NULL.</span><span class="sxs-lookup"><span data-stu-id="a43bf-117">`ppUnk` is null.</span></span>|  
|<span data-ttu-id="a43bf-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="a43bf-118">E_OUTOFMEMORY</span></span>|<span data-ttu-id="a43bf-119">Es ist nicht genügend Arbeitsspeicher verfügbar, um die Anforderung zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="a43bf-119">Not enough memory is available to handle the request.</span></span>|  
|<span data-ttu-id="a43bf-120">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span><span class="sxs-lookup"><span data-stu-id="a43bf-120">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span></span>|<span data-ttu-id="a43bf-121">Eine andere Runtime wurde bereits an das ältere CLR-Version 2-Aktivierungsrichtlinie gebunden.</span><span class="sxs-lookup"><span data-stu-id="a43bf-121">A different runtime was already bound to the legacy CLR version 2 activation policy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a43bf-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a43bf-122">Remarks</span></span>  
 <span data-ttu-id="a43bf-123">Diese Methode bewirkt, dass die CLR geladen, aber nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a43bf-123">This method causes the CLR to be loaded but not initialized.</span></span>  
  
 <span data-ttu-id="a43bf-124">Die folgende Tabelle zeigt die unterstützten Kombinationen für `rclsid` und `riid`.</span><span class="sxs-lookup"><span data-stu-id="a43bf-124">The following table shows the supported combinations for `rclsid` and `riid`.</span></span>  
  
|`rclsid`|`riid`|  
|--------------|------------|  
|<span data-ttu-id="a43bf-125">CLSID_CorMetaDataDispenser</span><span class="sxs-lookup"><span data-stu-id="a43bf-125">CLSID_CorMetaDataDispenser</span></span>|<span data-ttu-id="a43bf-126">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span><span class="sxs-lookup"><span data-stu-id="a43bf-126">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span></span>|  
|<span data-ttu-id="a43bf-127">CLSID_CorMetaDataDispenserRuntime</span><span class="sxs-lookup"><span data-stu-id="a43bf-127">CLSID_CorMetaDataDispenserRuntime</span></span>|<span data-ttu-id="a43bf-128">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span><span class="sxs-lookup"><span data-stu-id="a43bf-128">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span></span>|  
|<span data-ttu-id="a43bf-129">CLSID_CorRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="a43bf-129">CLSID_CorRuntimeHost</span></span>|<span data-ttu-id="a43bf-130">IID_ICorRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="a43bf-130">IID_ICorRuntimeHost</span></span>|  
|<span data-ttu-id="a43bf-131">CLSID_CLRRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="a43bf-131">CLSID_CLRRuntimeHost</span></span>|<span data-ttu-id="a43bf-132">IID_ICLRRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="a43bf-132">IID_ICLRRuntimeHost</span></span>|  
|<span data-ttu-id="a43bf-133">CLSID_TypeNameFactory</span><span class="sxs-lookup"><span data-stu-id="a43bf-133">CLSID_TypeNameFactory</span></span>|<span data-ttu-id="a43bf-134">IID_ITypeNameFactory</span><span class="sxs-lookup"><span data-stu-id="a43bf-134">IID_ITypeNameFactory</span></span>|  
|<span data-ttu-id="a43bf-135">CLSID_CLRDebuggingLegacy</span><span class="sxs-lookup"><span data-stu-id="a43bf-135">CLSID_CLRDebuggingLegacy</span></span>|<span data-ttu-id="a43bf-136">IID_ICorDebug</span><span class="sxs-lookup"><span data-stu-id="a43bf-136">IID_ICorDebug</span></span>|  
|||  
|<span data-ttu-id="a43bf-137">CLSID_CLRStrongName</span><span class="sxs-lookup"><span data-stu-id="a43bf-137">CLSID_CLRStrongName</span></span>|<span data-ttu-id="a43bf-138">IID_ICLRStrongName</span><span class="sxs-lookup"><span data-stu-id="a43bf-138">IID_ICLRStrongName</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a43bf-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a43bf-139">Requirements</span></span>  
 <span data-ttu-id="a43bf-140">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a43bf-140">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a43bf-141">**Header:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="a43bf-141">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="a43bf-142">**Bibliothek:** Als Ressource in MSCorEE.dll enthalten</span><span class="sxs-lookup"><span data-stu-id="a43bf-142">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a43bf-143">**.NET Framework-Versionen:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a43bf-143">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a43bf-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a43bf-144">See also</span></span>
- [<span data-ttu-id="a43bf-145">ICLRRuntimeInfo-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a43bf-145">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)
- [<span data-ttu-id="a43bf-146">Hosten von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a43bf-146">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="a43bf-147">Hosting</span><span class="sxs-lookup"><span data-stu-id="a43bf-147">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
