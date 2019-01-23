---
title: IInstallReferenceEnum-Schnittstelle
ms.date: 03/30/2017
api_name:
- IInstallReferenceEnum
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceEnum
helpviewer_keywords:
- IInstallReferenceEnum interface [.NET Framework fusion]
ms.assetid: 2863b33b-a541-462c-bbe8-702a2832898e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2aed89008dd2fa86b38f243c8e7cca1bdda901e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54497773"
---
# <a name="iinstallreferenceenum-interface"></a><span data-ttu-id="c7f48-102">IInstallReferenceEnum-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c7f48-102">IInstallReferenceEnum Interface</span></span>
<span data-ttu-id="c7f48-103">Stellt einen Enumerator für die referenzierten Assemblys im globalen Assemblycache installiert.</span><span class="sxs-lookup"><span data-stu-id="c7f48-103">Represents an enumerator for the referenced assemblies installed in the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7f48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7f48-104">Syntax</span></span>  
  
```  
interface IInstallReferenceEnum : IUnknown {  
    HRESULT GetNextInstallReferenceItem (  
        [out] IInstallReferenceItem **ppRefItem,  
        [in]  DWORD dwFlags,  
        [in]  LPVOID pvReserved  
    );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c7f48-105">Methoden</span><span class="sxs-lookup"><span data-stu-id="c7f48-105">Methods</span></span>  
  
|<span data-ttu-id="c7f48-106">Methode</span><span class="sxs-lookup"><span data-stu-id="c7f48-106">Method</span></span>|<span data-ttu-id="c7f48-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7f48-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c7f48-108">GetNextInstallReferenceItem-Methode</span><span class="sxs-lookup"><span data-stu-id="c7f48-108">GetNextInstallReferenceItem Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-getnextinstallreferenceitem-method.md)|<span data-ttu-id="c7f48-109">Ruft einen Zeiger auf der nächste `IInstallReferenceItem` enthalten `IInstallReferenceEnum`.</span><span class="sxs-lookup"><span data-stu-id="c7f48-109">Gets a pointer to the next `IInstallReferenceItem` contained in this `IInstallReferenceEnum`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c7f48-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7f48-110">Requirements</span></span>  
 <span data-ttu-id="c7f48-111">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c7f48-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7f48-112">**Header:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="c7f48-112">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="c7f48-113">**.NET Framework-Versionen:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7f48-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7f48-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7f48-114">See also</span></span>
- [<span data-ttu-id="c7f48-115">Fusion-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c7f48-115">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [<span data-ttu-id="c7f48-116">IInstallReferenceItem-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c7f48-116">IInstallReferenceItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md)
