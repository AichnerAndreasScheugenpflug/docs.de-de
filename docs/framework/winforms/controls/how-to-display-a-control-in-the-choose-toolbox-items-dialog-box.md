---
title: 'Vorgehensweise: Anzeigen eines Steuerelements in der Toolbox-Elemente-Dialogfeld "auswählen"'
ms.date: 03/30/2017
helpviewer_keywords:
- global assembly cache [Windows Forms], Choose Toolbox Items dialog box
- AssemblyFoldersEx [Windows Forms], Choose Toolbox Items dialog box
- controls [Windows Forms], display in Choose Toolbox Items dialog box
- assembly folder registration [Windows Forms], Choose Toolbox Items dialog box
- Choose Toolbox Items dialog box [Windows Forms], display control
ms.assetid: 01ef6eba-d044-40f0-951d-78eff7ebd9a9
ms.openlocfilehash: 56dad16b7a0bd8f0e7423b4a70e7173578150cbe
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520450"
---
# <a name="how-to-display-a-control-in-the-choose-toolbox-items-dialog-box"></a>Vorgehensweise: Anzeigen eines Steuerelements in der Toolbox-Elemente-Dialogfeld "auswählen"
Beim Entwickeln und Verteilen von Steuerelementen, sollten Sie die Steuerelemente angezeigt werden die **Toolboxelemente** dieses Dialogfeld wird angezeigt, wenn Sie mit der rechten Maustaste die **Toolbox** , und wählen Sie  **Wählen Sie Elemente aus**. Sie können das Steuerelement in diesem Dialogfeld angezeigt werden, mithilfe der Registrierungsvorgang "AssemblyFoldersEx" aktivieren.  
  
### <a name="to-display-your-control-in-the-choose-toolbox-items-dialog-box"></a>Das Steuerelement im Dialogfeld "Toolboxelemente auswählen" angezeigt.  
  
-   Installieren Sie die Steuerelementassembly im globalen Assemblycache. Weitere Informationen finden Sie unter [Vorgehensweise: Installieren einer Assembly im globalen Assemblycache](../../../../docs/framework/app-domains/how-to-install-an-assembly-into-the-gac.md)  
  
     - oder -   
  
-   Registrieren Sie Ihr Steuerelement und seine zugehörigen Entwurfszeitassemblys mithilfe der Registrierungsvorgang "AssemblyFoldersEx" ein. "AssemblyFoldersEx" ist ein Registrierungsspeicherort, in dem Drittanbieter Pfade für jede Version des Frameworks speichern, die sie unterstützen. Design-Time-Lösung kann an diesem Registrierungsspeicherort Verweisassemblys suchen Suchen. Das Registrierungsskript kann die Steuerelemente angeben, die in der Toolbox angezeigt werden sollen. Weitere Informationen finden Sie unter [Bereitstellen von einem benutzerdefinierten Steuerelement und während der Entwurfszeit-Assemblys (Visual Studio 2013)](https://msdn.microsoft.com/library/96158eb0-b691-4ae1-9e7b-3c65a1b798cb).  
  
## <a name="see-also"></a>Siehe auch
- [Dialogfeld „Toolboxelemente auswählen“ (Visual Studio)](https://msdn.microsoft.com/library/bd07835f-18a8-433e-bccc-7141f65263bb)
- [Bereitstellen eines benutzerdefinierten Steuerelements und während der Entwurfszeit-Assemblys (Visual Studio 2013)](https://msdn.microsoft.com/library/96158eb0-b691-4ae1-9e7b-3c65a1b798cb)
- [Entwickeln von Windows Forms-Steuerelementen zur Entwurfszeit](../../../../docs/framework/winforms/controls/developing-windows-forms-controls-at-design-time.md)
- [Vorgehensweise: Installieren einer Assembly im globalen Assemblycache](../../../../docs/framework/app-domains/how-to-install-an-assembly-into-the-gac.md)
- [Exemplarische Vorgehensweise: Automatisches Füllen der Toolbox mit benutzerdefinierten Komponenten](../../../../docs/framework/winforms/controls/walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
