---
title: Debuggen von Strukturen
ms.date: 03/30/2017
helpviewer_keywords:
- unmanaged structures [.NET Framework], debugging
- debugging structures [.NET Framework]
- structures [.NET Framework debugging]
ms.assetid: 173ba2c2-ab34-49ae-b6a8-e5c49882bf05
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 23aa619d666f2e0b9eb67ab4cf8d4f92761865d3
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2019
ms.locfileid: "54415324"
---
# <a name="debugging-structures"></a>Debuggen von Strukturen
In diesem Abschnitt werden die nicht verwalteten Strukturen beschrieben, die die Debug-API verwendet.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [CLR_DEBUGGING_VERSION-Struktur](../../../../docs/framework/unmanaged-api/debugging/clr-debugging-version-structure.md)  
 Definiert die Produktversion der Common Language Runtime (CLR) zu Debugzwecken.  
  
 [CodeChunkInfo-Struktur1](../../../../docs/framework/unmanaged-api/debugging/codechunkinfo-structure.md)  
 Stellt einen einzelnen Codeabschnitt im Speicher dar.  
  
 [CorDebugBlockingObject-Struktur](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md)  
 Definiert ein Objekt, das einen Thread blockiert, sowie die Ursache, weshalb der Thread blockiert ist.  
  
 [CorDebugEHClause-Struktur](../../../../docs/framework/unmanaged-api/debugging/cordebugehclause-structure.md)  
 Stellt eine Ausnahmebehandlung (Exception Handling, EH)-Klausel für einen bestimmten Intermediate Language (IL)-Codeabschnitt dar.  
  
 [CorDebugExceptionObjectStackFrame-Struktur](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md)  
 Stellt Stapelrahmeninformationen von einem Ausnahmeobjekt dar.  
  
 [CorDebugExceptionObjectStackFrame-Struktur](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md)  
 Maps eine [!INCLUDE[wrt](../../../../includes/wrt-md.md)] GUID dem entsprechenden [ICorDebugType](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-interface.md) Objekt.  
  
 COR_ACTIVE_FUNCTION  
 Enthält Informationen zu den Funktionen, die aktuell in den Rahmen eines Threads aktiv sind.  
  
 [COR_ARRAY_LAYOUT-Struktur](../../../../docs/framework/unmanaged-api/debugging/cor-array-layout-structure.md)  
 Bietet Informationen zum Layout eines Arrayobjekts im Speicher.  
  
 COR_DEBUG_IL_TO_NATIVE_MAP  
 Enthält die Offsets, die genutzt werden, um Microsoft Intermediate Language (MSIL)-Code nativem Code zuzuordnen.  
  
 COR_DEBUG_STEP_RANGE  
 Enthält die Offsetinformationen für einen Codebereich.  
  
 [COR_FIELD-Struktur](../../../../docs/framework/unmanaged-api/debugging/cor-field-structure.md)  
 Bietet Informationen zu einem Feld in einem Objekt.  
  
 [COR_GC_REFERENCE-Struktur](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md)  
 Enthält Informationen zu einem Objekt, das speicherbereinigt werden soll.  
  
 [COR_HEAPINFO-Struktur](../../../../docs/framework/unmanaged-api/debugging/cor-heapinfo-structure.md)  
 Liefert allgemeine Informationen zum Garbage Collection-Heap, auch zu dessen Aufzählbarkeit.  
  
 [COR_HEAPOBJECT-Struktur](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md)  
 Stellt Informationen zu einem Objekt auf dem verwalteten Heap bereit.  
  
 COR_IL_MAP  
 Gibt Änderungen im relativen Offset einer Funktion an.  
  
 [COR_SEGMENT-Struktur](../../../../docs/framework/unmanaged-api/debugging/cor-segment-structure.md)  
 Enthält Informationen zu einem Bereich des Arbeitsspeichers im verwalteten Heap.  
  
 [COR_TYPEID-Struktur](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md)  
 Enthält einen Typbezeichner.  
  
 [COR_TYPE_LAYOUT-Struktur](../../../../docs/framework/unmanaged-api/debugging/cor-type-layout-structure.md)  
 Bietet Informationen zum Layout eines Objekts im Speicher.  
  
 COR_VERSION  
 Speichert die standardmäßige vierstellige Versionsnummer der Common Language Runtime.  
  
 [StackTrace_SimpleContext-Struktur](../../../../docs/framework/unmanaged-api/debugging/stacktrace-simplecontext-structure.md)  
 Stellt einen einfachen Kontext bereit, der statt einer vollständigen `CONTEXT`-Struktur verwendet werden kann.

 [CLRDATA_ADDRESS_RANGE Struktur](../../../../docs/framework/unmanaged-api/debugging/clrdata-address-range-structure.md) ein Adressbereichs definiert.
 
 [CLRDATA_IL_ADDRESS_MAP Struktur](../../../../docs/framework/unmanaged-api/debugging/clrdata-il-address-map-structure.md) definiert eine IL-Adresszuordnung
 
 [DacpGetModuleAddress Struktur](../../../../docs/framework/unmanaged-api/debugging/dacpgetmoduleaddress-structure.md) definiert der Container für eine Anforderung zum modulimport Adresse.

  
## <a name="related-sections"></a>Verwandte Abschnitte  
 [Debuggen von Co-Klassen](../../../../docs/framework/unmanaged-api/debugging/debugging-coclasses.md)  
  
 [Debuggen von Schnittstellen](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
  
 [Debuggen von globalen statischen Funktionen](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)  
  
 [Debuggen von Enumerationen](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)  
  
 [Debuggen](../../../../docs/framework/unmanaged-api/debugging/index.md)
