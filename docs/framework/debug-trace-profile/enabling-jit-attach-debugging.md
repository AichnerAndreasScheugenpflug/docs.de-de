---
title: Aktivieren von JIT-attach Debugging
ms.date: 03/30/2017
helpviewer_keywords:
- JIT-attach debugging
- debugging [.NET Framework], JIT-attach debugging
ms.assetid: f91fc5f7-de5a-4f23-b6ac-f450e63c662e
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d4630e6d02b0137021765f954ab0dae19f2f6199
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2019
ms.locfileid: "56093982"
---
# <a name="enabling-jit-attach-debugging"></a>Aktivieren von JIT-attach Debugging
Mit „JIT-attach Debugging“ wird das Anfügen eines Debuggers an einen Prozess beim Auftreten von Fehlern beschrieben. Es kann auch von bestimmten Methoden oder Funktionen ausgelöst werden.  
  
 JIT-attach Debugging wird bei den folgenden Fehlerzuständen verwendet:  
  
-   bei Ausnahmefehlern (im nativen und im verwalteten Code)  
  
-   bei der <xref:System.Environment.FailFast%2A?displayProperty=nameWithType>-Methode oder [RaiseFailFastException](https://go.microsoft.com/fwlink/?LinkId=182107)-Funktion (Windows 7-Produktfamilie)  
  
-   bei schwerwiegenden Laufzeitfehlern  
  
 JIT-attach Debugging wird auch durch Aufrufen der folgenden Methoden und Funktionen ausgelöst:  
  
-   <xref:System.Diagnostics.Debugger.Launch%2A?displayProperty=nameWithType> -Methode.  
  
-   <xref:System.Diagnostics.Debugger.Break%2A?displayProperty=nameWithType> -Methode.  
  
-   [DebugBreak](https://go.microsoft.com/fwlink/?LinkId=182106)-Funktion (Win32)  
  
 Vor [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)] stellte .NET Framework separate Registrierungsschlüssel zur Verhaltenssteuerung von nativen und verwalteten Debuggern bereit. Beginnend mit der [!INCLUDE[net_v40_short](../../../includes/net-v40-short-md.md)], ist die Steuerung unter einem einzelnen Registrierungsschlüssel konsolidiert: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\Current Version\AeDebug. Mit den Werten, die Sie für diesen Schlüssel festlegen können, bestimmen Sie, ob ein Debugger aufgerufen wird. Außerdem können Sie festlegen, ob in diesem Fall ein Dialogfeld angezeigt werden soll, das eine Benutzereingabe erfordert. Informationen zum Festlegen dieses Registrierungsschlüssels finden Sie unter [Konfigurieren des automatischen Debuggens](https://go.microsoft.com/fwlink/?LinkId=181767).  
  
## <a name="see-also"></a>Siehe auch
- [Debuggen, Ablaufverfolgung und Profilerstellung](../../../docs/framework/debug-trace-profile/index.md)
- [Erleichtern des Debuggens für ein Abbild](../../../docs/framework/debug-trace-profile/making-an-image-easier-to-debug.md)
