---
title: System.ServiceModel.Channels.FailedAcceptFromPool
ms.date: 03/30/2017
ms.assetid: d535b1b5-ee58-45e8-b400-7d9570f4eb9a
ms.openlocfilehash: 093a76a0157948520c2f0d8bf6145b6f78966906
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54695464"
---
# <a name="systemservicemodelchannelsfailedacceptfrompool"></a>System.ServiceModel.Channels.FailedAcceptFromPool
Fehler beim Versuch, eine gepoolte Verbindung erneut zu verwenden. Ein weiterer Versuch wird innerhalb des angegebenen Timeouts unternommen.  
  
## <a name="description"></a>Beschreibung  
 Diese Informationsablaufverfolgung gibt an, dass während des Versuchs, eine zusammengeführte Verbindung wiederzuverwenden, ein Fehler aufgetreten ist Dies kann geschehen, weil die zusammengeführte Verbindung nicht kompatibel, nicht bereit oder noch immer aktiv war. Weitere Versuche, andere zusammengeführte Verbindungen wiederzuverwenden werden innerhalb des gegebenen Timeout unternommen, und eine neue Verbindung wird für den Fall erstellt, dass keine verwendbaren Verbindungen gefunden werden können.  
  
## <a name="see-also"></a>Siehe auch
- [Ablaufverfolgung](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [Verwenden der Ablaufverfolgung zum Beheben von Anwendungsfehlern](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [Verwaltung und Diagnose](../../../../../docs/framework/wcf/diagnostics/index.md)
