---
title: PNRP in der Anwendungsentwicklung
ms.date: 03/30/2017
ms.assetid: 265615d6-4423-4b5d-8626-752e456f4f4e
ms.openlocfilehash: 93dd65100e19f16c6597374cbab1e10d6a759562
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54736545"
---
# <a name="pnrp-in-application-development"></a>PNRP in der Anwendungsentwicklung
In Windows Vista können Netzwerkanwendungen über eine vereinfachte PNRP-Anwendungsprogrammierschnittstelle (application programming interface – API) auf Funktionen zur Veröffentlichung und Auflösung von Namen zugreifen.  
  
## <a name="implementing-the-peer-name-resolution-protocol"></a>Implementieren des Peer Name Resolution-Protokolls  
 Bei der vereinfachten PNRP-API werden Clouds nicht explizit für die Namens- und Adressregistrierung angegeben. Die PNRP-Komponente bestimmt automatisch, welchen passenden Clouds beigetreten werden soll und welche Adressen in diesen veröffentlicht werden sollen.  
  
 Für die sehr stark vereinfachte PNRP-Namensauflösung in Windows Vista werden PNRP-Namen nun in die Windows Sockets-Funktion getaddrinfo() integriert. Namen lassen sich mithilfe von PNRP in eine IPv6-Adresse aufzulösen. Dazu können Anwendungen mit der Funktion getaddrinfo() den vollqualifizierten Domänennamen (Fully Qualified Domain Name – FQDN) „name-prnp.net“ verwenden. „name“ steht hier für den aufzulösenden Peernamen. Die Domain „pnrp.net“ ist in Windows Vista für die Auflösung von PNRP-Namen reserviert.  
  
 Die Nachrichtenübergabe zwischen Peer-zu-Peer-Anwendungen wird weiterhin von der zu Grunde liegenden Architektur übernommen, z.B. PeerChannel oder der WCF-Funktion für [umfangreiche Daten und Streaming](https://go.microsoft.com/fwlink/?LinkID=179652).  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Net.PeerToPeer>
