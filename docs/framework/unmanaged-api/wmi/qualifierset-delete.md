---
title: QualifierSet_Delete-Funktion (Referenz zur nicht verwalteten API)
description: Die Funktion QualifierSet_Delete Löscht einen Qualifizierer anhand des Namens.
ms.date: 11/06/2017
api_name:
- QualifierSet_Delete
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- QualifierSet_Delete
helpviewer_keywords:
- QualifierSet_Delete function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 860295a3d10acd67f5fb7665a7213dc90e4a4829
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54713165"
---
# <a name="qualifiersetdelete-function"></a><span data-ttu-id="4e9b8-103">QualifierSet_Delete-Funktion</span><span class="sxs-lookup"><span data-stu-id="4e9b8-103">QualifierSet_Delete function</span></span>
<span data-ttu-id="4e9b8-104">Löscht einen angegebenen Qualifizierer anhand des Namens.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-104">Deletes a specified qualifier by name.</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="4e9b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e9b8-105">Syntax</span></span>  
  
```  
HRESULT QualifierSet_Delete (
   [in] int                  vFunc, 
   [in] IWbemQualifierSet*   ptr, 
   [in] LPCWSTR              wszName
); 
```  

## <a name="parameters"></a><span data-ttu-id="4e9b8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e9b8-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="4e9b8-107">[in] Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-107">[in] This parameter is unused.</span></span>

`ptr`   
<span data-ttu-id="4e9b8-108">[in] Ein Zeiger auf ein [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) Instanz.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-108">[in] A pointer to an [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) instance.</span></span>

`wszName`   
<span data-ttu-id="4e9b8-109">[in] Der Name des Qualifizierers löschen.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-109">[in] The name of the qualifier to delete.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e9b8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e9b8-110">Return value</span></span>

<span data-ttu-id="4e9b8-111">Die folgenden Werte, die von dieser Funktion zurückgegebenen werden definiert, der *WbemCli.h* Header-Datei, und Sie können definieren sie als Konstanten in Ihrem Code:</span><span class="sxs-lookup"><span data-stu-id="4e9b8-111">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="4e9b8-112">Konstante</span><span class="sxs-lookup"><span data-stu-id="4e9b8-112">Constant</span></span>  |<span data-ttu-id="4e9b8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4e9b8-113">Value</span></span>  |<span data-ttu-id="4e9b8-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e9b8-114">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="4e9b8-115">0x80041008</span><span class="sxs-lookup"><span data-stu-id="4e9b8-115">0x80041008</span></span> | <span data-ttu-id="4e9b8-116">Der `wszName`-Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-116">The `wszName` parameter is not valid.</span></span> |
|`WBEM_E_INVALID_OPERATION` | <span data-ttu-id="4e9b8-117">0x80041016</span><span class="sxs-lookup"><span data-stu-id="4e9b8-117">0x80041016</span></span> | <span data-ttu-id="4e9b8-118">Das Löschen dieses Qualifizierers ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-118">Deleting this qualifier is illegal.</span></span> |
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="4e9b8-119">0x80041002</span><span class="sxs-lookup"><span data-stu-id="4e9b8-119">0x80041002</span></span> | <span data-ttu-id="4e9b8-120">Der angegebene Qualifizierer wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-120">The specified qualifier was not found.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="4e9b8-121">0</span><span class="sxs-lookup"><span data-stu-id="4e9b8-121">0</span></span> | <span data-ttu-id="4e9b8-122">Der Funktionsaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-122">The function call was successful.</span></span>  |
| `WBEM_S_RESET_TO_DEFAULT` | <span data-ttu-id="4e9b8-123">0x40002</span><span class="sxs-lookup"><span data-stu-id="4e9b8-123">0x40002</span></span> | <span data-ttu-id="4e9b8-124">Lokale Überschreibung gelöscht wurden, und der ursprüngliche Qualifizierer vom übergeordneten Objekt wurde Bereich fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-124">The local override was deleted and the original qualifier from the parent object has resumed scope.</span></span> |

## <a name="remarks"></a><span data-ttu-id="4e9b8-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4e9b8-125">Remarks</span></span>

<span data-ttu-id="4e9b8-126">Diese Funktion umschließt einen Aufruf der [IWbemQualifierSet::Delete](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-delete) Methode.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-126">This function wraps a call to the [IWbemQualifierSet::Delete](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-delete) method.</span></span>

<span data-ttu-id="4e9b8-127">Aufgrund der Regeln zur Weitergabe Qualifizierer kann ein bestimmter Qualifizierer von einem anderen Objekt geerbt und wurden lediglich in die aktuelle Klasse oder Instanz überschrieben.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-127">Due to qualifier propagation rules, a particular qualifier may have been inherited from another object and merely overridden in the current class or instance.</span></span> <span data-ttu-id="4e9b8-128">In diesem Fall die `QualifierSet_Delete` Methode setzt den Qualifizierer auf den ursprünglichen geerbten Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-128">In this case, the `QualifierSet_Delete` method resets the qualifier to its original inherited value.</span></span> <span data-ttu-id="4e9b8-129">In diesem Fall die Funktion gibt den Statuscode zurück `WBEM_S_RESET_TO_DEFAULT`.</span><span class="sxs-lookup"><span data-stu-id="4e9b8-129">The function in this case returns the status code `WBEM_S_RESET_TO_DEFAULT`.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e9b8-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e9b8-130">Requirements</span></span>  
 <span data-ttu-id="4e9b8-131">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4e9b8-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4e9b8-132">**Header:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="4e9b8-132">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="4e9b8-133">**.NET Framework-Versionen:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="4e9b8-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e9b8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e9b8-134">See also</span></span>
- [<span data-ttu-id="4e9b8-135">WMI und Leistungsindikatoren (Referenz zur nicht verwalteten API)</span><span class="sxs-lookup"><span data-stu-id="4e9b8-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
