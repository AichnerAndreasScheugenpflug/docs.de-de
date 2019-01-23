---
title: QualifierSet_GetNames-Funktion (Referenz zur nicht verwalteten API)
description: Die QualifierSet_GetNames-Funktion ruft die Namen der Qualifizierer aus einem Objekt oder die Eigenschaft ab.
ms.date: 11/06/2017
api_name:
- QualifierSet_GetNames
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- QualifierSet_GetNames
helpviewer_keywords:
- QualifierSet_GetNames function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2da6bc87a175851aa7b23b67075ce61e39f0b937
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54555091"
---
# <a name="qualifiersetgetnames-function"></a><span data-ttu-id="9c98a-103">QualifierSet_GetNames-Funktion</span><span class="sxs-lookup"><span data-stu-id="9c98a-103">QualifierSet_GetNames function</span></span>
<span data-ttu-id="9c98a-104">Ruft die Namen der alle Qualifizierer oder bestimmte Qualifizierer angegeben, die aus dem aktuellen Objekt oder eine Eigenschaft verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9c98a-104">Retrieves the names of all the qualifiers or of certain qualifiers that are available from the current object or property.</span></span> 

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="9c98a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c98a-105">Syntax</span></span>  
  
```  
HRESULT QualifierSet_GetNames (
   [in] int                  vFunc, 
   [in] IWbemQualifierSet*   ptr, 
   [in] LONG                 lFlags,
   [out] SAFEARRAY (BSTR)**  pstrNames
); 
```  

## <a name="parameters"></a><span data-ttu-id="9c98a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c98a-106">Parameters</span></span>

`vFunc`   
<span data-ttu-id="9c98a-107">[in] Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c98a-107">[in] This parameter is unused.</span></span>

`ptr`   
<span data-ttu-id="9c98a-108">[in] Ein Zeiger auf ein [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) Instanz.</span><span class="sxs-lookup"><span data-stu-id="9c98a-108">[in] A pointer to an [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) instance.</span></span>

`lFlags`   
<span data-ttu-id="9c98a-109">[in] Einer der folgenden Flags oder Werte, der angibt, welche Namen in der Enumeration einschließen.</span><span class="sxs-lookup"><span data-stu-id="9c98a-109">[in] One of the following flags or values that specifies which names to include in the enumeration.</span></span>

|<span data-ttu-id="9c98a-110">Konstante</span><span class="sxs-lookup"><span data-stu-id="9c98a-110">Constant</span></span>  |<span data-ttu-id="9c98a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="9c98a-111">Value</span></span>  |<span data-ttu-id="9c98a-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c98a-112">Description</span></span>  |
|---------|---------|---------|
|  | <span data-ttu-id="9c98a-113">0</span><span class="sxs-lookup"><span data-stu-id="9c98a-113">0</span></span> | <span data-ttu-id="9c98a-114">Die Namen aller Qualifizierer zurück</span><span class="sxs-lookup"><span data-stu-id="9c98a-114">Return the names of all qualifiers.</span></span> |
| `WBEM_FLAG_LOCAL_ONLY` | <span data-ttu-id="9c98a-115">0x10</span><span class="sxs-lookup"><span data-stu-id="9c98a-115">0x10</span></span> | <span data-ttu-id="9c98a-116">Nur die Namen der Qualifizierer an die current-Eigenschaft oder das Objekt bestimmte zurück.</span><span class="sxs-lookup"><span data-stu-id="9c98a-116">Return only the names of qualifiers specific to the current property or object.</span></span> <br/> <span data-ttu-id="9c98a-117">Für eine Eigenschaft: Nur die Qualifizierer, die spezifisch für die Eigenschaft (einschließlich Außerkraftsetzungen) und nicht die Qualifizierer, die aus der Definition der Klasse weitergegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="9c98a-117">For a property: Return only the qualifiers specific to the property (including overrides), and not those qualifiers propagated from the class definition.</span></span> <br/> <span data-ttu-id="9c98a-118">Für eine Instanz: Geben Sie nur instanzspezifischen Qualifizierer-Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="9c98a-118">For an instance: Return only instance-specific qualifier names.</span></span> <br/> <span data-ttu-id="9c98a-119">Für eine Klasse: Nur Qualifizierer an die abgeleitete Klasse Beiong bestimmte zurück.</span><span class="sxs-lookup"><span data-stu-id="9c98a-119">For a class: Return only qualifiers specific to the class beiong derived.</span></span>
|`WBEM_FLAG_PROPAGATED_ONLY` | <span data-ttu-id="9c98a-120">0x20</span><span class="sxs-lookup"><span data-stu-id="9c98a-120">0x20</span></span> | <span data-ttu-id="9c98a-121">Rückgabe, nur die Namen der Qualifizierer weitergegeben aus einem anderen Objekt.</span><span class="sxs-lookup"><span data-stu-id="9c98a-121">Return only the names of qualifiers propagated from another object.</span></span> <br/> <span data-ttu-id="9c98a-122">Für eine Eigenschaft: Rückgabe, nur die Qualifizierer weitergegeben für diese Eigenschaft aus der Klassendefinition und nicht die von der Eigenschaft selbst.</span><span class="sxs-lookup"><span data-stu-id="9c98a-122">For a property: Return only the qualifiers propagated to this property from the class definition, and not those from the property itself.</span></span> <br/> <span data-ttu-id="9c98a-123">Für eine Instanz: Rückgabe, nur diese Qualifizierer weitergegeben aus der Klassendefinition.</span><span class="sxs-lookup"><span data-stu-id="9c98a-123">For an instance: Return only those qualifiers propagated from the class definition.</span></span> <br/> <span data-ttu-id="9c98a-124">Für eine Klasse: Die Rückgabe nur die Namen dieser Qualifizierer von den übergeordneten Klassen geerbt.</span><span class="sxs-lookup"><span data-stu-id="9c98a-124">For a class: Return only those qualifier names inherited from the parent classes.</span></span> |

<span data-ttu-id="9c98a-125">`pstrNames` [out] Ein neues `SAFEARRAY` , die den angeforderten Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="9c98a-125">`pstrNames` [out] A new `SAFEARRAY` that contains the requested names.</span></span> <span data-ttu-id="9c98a-126">Das Array kann 0 Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="9c98a-126">The array can have 0 elements.</span></span> <span data-ttu-id="9c98a-127">Wenn ein Fehler auftritt, ein neues `SAFEARRAY` wird nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c98a-127">If an error occurs, a new `SAFEARRAY` is not returned.</span></span>

## <a name="return-value"></a><span data-ttu-id="9c98a-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c98a-128">Return value</span></span>

<span data-ttu-id="9c98a-129">Die folgenden Werte, die von dieser Funktion zurückgegebenen werden definiert, der *WbemCli.h* Header-Datei, und Sie können definieren sie als Konstanten in Ihrem Code:</span><span class="sxs-lookup"><span data-stu-id="9c98a-129">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="9c98a-130">Konstante</span><span class="sxs-lookup"><span data-stu-id="9c98a-130">Constant</span></span>  |<span data-ttu-id="9c98a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9c98a-131">Value</span></span>  |<span data-ttu-id="9c98a-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c98a-132">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="9c98a-133">0x80041008</span><span class="sxs-lookup"><span data-stu-id="9c98a-133">0x80041008</span></span> | <span data-ttu-id="9c98a-134">Ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9c98a-134">A parameter is not valid.</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="9c98a-135">0x80041006</span><span class="sxs-lookup"><span data-stu-id="9c98a-135">0x80041006</span></span> | <span data-ttu-id="9c98a-136">Es ist nicht genügend Arbeitsspeicher zur Verfügung, um eine neue Enumeration beginnen.</span><span class="sxs-lookup"><span data-stu-id="9c98a-136">Not enough memory is available to begin a new enumeration.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="9c98a-137">0</span><span class="sxs-lookup"><span data-stu-id="9c98a-137">0</span></span> | <span data-ttu-id="9c98a-138">Der Funktionsaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9c98a-138">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="9c98a-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c98a-139">Remarks</span></span>

<span data-ttu-id="9c98a-140">Diese Funktion umschließt einen Aufruf der [IWbemQualifierSet::GetNames](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-getnames) Methode.</span><span class="sxs-lookup"><span data-stu-id="9c98a-140">This function wraps a call to the [IWbemQualifierSet::GetNames](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-getnames) method.</span></span>

<span data-ttu-id="9c98a-141">Nachdem Sie die Namen des Qualifizierers abgerufen haben, können Sie jede Qualifizierer anhand des Namens zugreifen, durch den Aufruf der [QualifierSet_Get](qualifierset-get.md) Funktion.</span><span class="sxs-lookup"><span data-stu-id="9c98a-141">Once you've retrieved the qualifier names, you can access each qualifier by name by calling the [QualifierSet_Get](qualifierset-get.md) function.</span></span> 

<span data-ttu-id="9c98a-142">Es ist kein Fehler für ein bestimmtes Objekt auf 0 (null) Qualifizierer enthalten, also die Anzahl der Zeichenfolgen in `pstrNames` bei der Rückgabe "0" sein, obwohl die Funktion gibt `WBEM_S_NO_ERROR`.</span><span class="sxs-lookup"><span data-stu-id="9c98a-142">It is not an error for a given object to have zero qualifiers, so the number of strings in `pstrNames` on return can be 0, even though the function returns `WBEM_S_NO_ERROR`.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c98a-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c98a-143">Requirements</span></span>  
 <span data-ttu-id="9c98a-144">**Plattformen:** Weitere Informationen finden Sie unter [Systemanforderungen](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9c98a-144">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9c98a-145">**Header:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="9c98a-145">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="9c98a-146">**.NET Framework-Versionen:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="9c98a-146">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c98a-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c98a-147">See also</span></span>
- [<span data-ttu-id="9c98a-148">WMI und Leistungsindikatoren (Referenz zur nicht verwalteten API)</span><span class="sxs-lookup"><span data-stu-id="9c98a-148">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
