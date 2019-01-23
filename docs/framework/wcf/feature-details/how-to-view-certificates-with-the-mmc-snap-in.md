---
title: 'Vorgehensweise: Anzeigen von Zertifikaten mit dem MMC-Snap-in'
ms.date: 03/30/2017
helpviewer_keywords:
- certificates [WCF], viewing with the MMC snap-in
ms.assetid: 2b8782aa-ebb4-4ee7-974b-90299e356dc5
ms.openlocfilehash: 72fd6a1be2f33e1bfeb08fd43f3436627ee842e5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521581"
---
# <a name="how-to-view-certificates-with-the-mmc-snap-in"></a>Vorgehensweise: Anzeigen von Zertifikaten mit dem MMC-Snap-in
Ein allgemeiner Typ der Anmeldeinformationen ist das X.509-Zertifikat. Bei der Erstellung sicherer Dienste oder Clients können Sie ein Zertifikat angeben, das als Anmeldeinformation für Client oder Dienst über die Methoden wie beispielsweise <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential.SetCertificate%2A> verwendet wird. Die Methode erfordert diverse Parameter; beispielsweise den Speicherplatz des Zertifikats und eines Werts, der für die Suche eines Zertifikats verwendet wird. Die folgende Prozedur veranschaulicht, wie die Speicherplätze auf einem Computer untersucht werden, um ein entsprechendes Zertifikat zu suchen. Ein Beispiel für den Fingerabdruck des Zertifikats zu suchen, finden Sie unter [Vorgehensweise: Abrufen des Fingerabdrucks eines Zertifikats](../../../../docs/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate.md).  
  
### <a name="to-view-certificates-in-the-mmc-snap-in"></a>So zeigen Sie Zertifikate im MMC-Snap-In an  
  
1.  Öffnen Sie ein Eingabeaufforderungsfenster.  
  
2.  Typ `mmc` , und drücken Sie die EINGABETASTE. Beachten Sie, dass Sie in der Administratorrolle sein müssen, um Zertifikate im lokalen Computerspeicher anzuzeigen.  
  
3.  Auf der **Datei** Menü klicken Sie auf **Snap-In hinzufügen/entfernen**.  
  
4.  Klicken Sie auf **Hinzufügen**.  
  
5.  In der **Standalone-Snap-in hinzufügen** wählen Sie im Dialogfeld **Zertifikate**.  
  
6.  Klicken Sie auf **Hinzufügen**.  
  
7.  In der **Zertifikat-Snap-in** wählen Sie im Dialogfeld **Computerkonto** , und klicken Sie auf **Weiter**. Wählen Sie optional **eigenes Benutzerkonto** oder **-Dienstkonto**. Sind Sie kein Verwalter des Computers, können Sie Zertifikate nur für Ihr Benutzerkonto verwalten.  
  
8.  In der **Computer auswählen** Dialogfeld klicken Sie auf **Fertig stellen**.  
  
9. In der **Standalone-Snap-in hinzufügen** Dialogfeld klicken Sie auf **schließen**.  
  
10. Auf der **Snap-In hinzufügen/entfernen** Dialogfeld klicken Sie auf **OK**.  
  
11. In der **Konsolenstamm** Fenster, klicken Sie auf **Zertifikate (lokaler Computer)** um das Zertifikat anzuzeigen, die für den Computer werden gespeichert.  
  
12. Dies ist optional. Wiederholen Sie die Schritte 3 bis 6, um Zertifikate für Ihr Konto anzuzeigen. Klicken Sie in Schritt 7 anstelle **Computerkonto**, klicken Sie auf **eigenes Benutzerkonto** , und wiederholen Sie die Schritte 8 bis 10.  
  
13. Dies ist optional. Auf der **Datei** Menü klicken Sie auf **speichern** oder **speichern**. Speichern Sie die Konsolendatei zur späteren Wiederverwendung.  
  
## <a name="viewing-certificates-with-internet-explorer"></a>Anzeigen von Zertifikaten mit Internet Explorer  
 Darüber hinaus können Sie Zertifikate mit dem Internet Explorer ansehen, exportieren, importieren und löschen.  
  
#### <a name="to-view-certificates-with-internet-explorer"></a>So zeigen Sie Zertifikate mit dem Internet Explorer an  
  
1.  Klicken Sie in Internet Explorer auf **Tools**, klicken Sie dann auf **Internetoptionen** zum Anzeigen der **Internetoptionen** Dialogfeld.  
  
2.  Klicken Sie auf die **Content** Registerkarte.  
  
3.  Klicken Sie unter **Zertifikate**, klicken Sie auf **Zertifikate**.  
  
4.  Zum Anzeigen der Details eines Zertifikats, wählen Sie das Zertifikat aus, und klicken Sie auf **Ansicht**.  
  
## <a name="see-also"></a>Siehe auch
- [Arbeiten mit Zertifikaten](../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [Vorgehensweise: Erstellen von temporären Zertifikaten für die Verwendung während der Entwicklung](../../../../docs/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development.md)
- [Vorgehensweise: Abrufen des Fingerabdrucks eines Zertifikats](../../../../docs/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate.md)
