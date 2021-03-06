---
title: 'Vorgehensweise: Fügen Sie mehrerer Gruppen von Einstellungen zur Anwendung hinzuC#'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], multiple sets
- application settings [Windows Forms], C#
ms.assetid: 45007ac6-cf07-4be7-bc38-3f0ef962faf9
ms.openlocfilehash: 5496d370890e019ae2b31835c95a9988f8d9bc18
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54559410"
---
# <a name="how-to-add-multiple-sets-of-settings-to-your-application-in-c"></a>Vorgehensweise: Fügen Sie mehrerer Gruppen von Einstellungen zur Anwendung hinzuC# #
In einigen Fällen empfiehlt es sich um mehrere Gruppen von Einstellungen in einer Anwendung zu erhalten. Z. B. Wenn Sie eine Anwendung entwickeln, muss eine bestimmte Gruppe von Einstellungen häufig ändern, kann es sein es ratsam, alle in einer einzelnen Datei trennen, damit die Datei ersetzt werden kann, global, lassen andere Einstellungen sind nicht betroffen. Visual Studio können Sie mehrere Sätze von Einstellungen zu Ihrem Projekt hinzufügen. Weitere Gruppen von Einstellungen können über das Properties.Settings-Objekt zugegriffen werden.  
  
### <a name="to-add-an-additional-set-of-setting-to-your-application"></a>Hinzufügen ein zusätzlichen Satzes von Einstellung für Ihre Anwendung  
  
1.  Wählen Sie im Menü **Projekt** die Option **Neues Element hinzufügen** aus. Das Dialogfeld **Neues Element hinzufügen** wird angezeigt.  
  
2.  In der **neues Element hinzufügen** wählen Sie im Dialogfeld **Einstellungsdatei**, geben Sie einen Namen für die Datei, und klicken Sie auf **hinzufügen** Ihrer Projektmappe eine neue Datei hinzu.  
  
3.  In **Projektmappen-Explorer**, ziehen Sie die neue Einstellungsdatei in die **Eigenschaften** Ordner. Dadurch werden die neuen Einstellungen in Code verfügbar sein.  
  
4.  Fügen Sie hinzu und verwenden Sie Einstellungen in dieser Datei, wie jeder anderen Einstellungsdatei. Sie können diese Gruppe von Einstellungen über das Properties.Settings-Objekt zugreifen.  
  
## <a name="see-also"></a>Siehe auch
- [Verwenden von Anwendungseinstellungen und Benutzereinstellungen](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)
- [Übersicht über Anwendungseinstellungen](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
