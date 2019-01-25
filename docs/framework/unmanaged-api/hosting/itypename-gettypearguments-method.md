---
title: ITypeName::GetTypeArguments-Methode
ms.date: 03/30/2017
api_name:
- ITypeName.GetTypeArguments
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetTypeArguments
helpviewer_keywords:
- ITypeName::GetTypeArguments method [.NET Framework hosting]
- GetTypeArguments method [.NET Framework hosting]
ms.assetid: 638d77df-ff9c-40d9-88ee-930f5f87ada1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9c6d89372bd9c1e10412832e91dc7660dfe6bbfd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732452"
---
# <a name="itypenamegettypearguments-method"></a><span data-ttu-id="8947d-102">ITypeName::GetTypeArguments-Methode</span><span class="sxs-lookup"><span data-stu-id="8947d-102">ITypeName::GetTypeArguments Method</span></span>
<span data-ttu-id="8947d-103">Diese Methode unterstützt die .NET Framework-Infrastruktur und ist nicht für eine direkte Verwendung im Code vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="8947d-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8947d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8947d-104">Syntax</span></span>  
  
```  
HRESULT GetTypeArguments (  
    [in] DWORD           count,  
    [out] ITypeName**    rgpArguments,  
    [out, retval] DWORD* pCount  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="8947d-105">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8947d-105">Requirements</span></span>  
 <span data-ttu-id="8947d-106">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8947d-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8947d-107">**Header:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8947d-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8947d-108">**Bibliothek:** Als Ressource in MSCorEE.dll enthalten</span><span class="sxs-lookup"><span data-stu-id="8947d-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8947d-109">**.NET Framework-Versionen:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8947d-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8947d-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8947d-110">See also</span></span>
- [<span data-ttu-id="8947d-111">Hosten von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8947d-111">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
