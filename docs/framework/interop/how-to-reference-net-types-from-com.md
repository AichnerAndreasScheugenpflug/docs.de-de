---
title: 'Vorgehensweise: Verweisen auf .NET-Typen in COM'
ms.date: 03/30/2017
dev_langs:
- cpp
helpviewer_keywords:
- importing type library
- COM interop, referencing .NET types
- interoperation with unmanaged code, referencing .NET types
- referencing .NET types
- interoperation with unmanaged code, importing type library
- type libraries
- COM interop, importing type library
ms.assetid: 54917f6f-cb18-4103-b622-856b55da93f3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9826f8af06693fdff0d5bea75cfa3f2586faa4f6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54582122"
---
# <a name="how-to-reference-net-types-from-com"></a>Vorgehensweise: Verweisen auf .NET-Typen in COM
Hinsichtlich Clientcode und Servercode bestehen kaum Unterschiede zwischen COM und .NET Framework. Microsoft Visual Basic-Clients können ein .NET-Objekt im Objektkatalog anzeigen. Dort werden Objektmethoden und –syntax sowie Eigenschaften und Felder in gleicher Weise angegeben wie für ein beliebiges anderes COM-Objekt.  
  
 Der Prozess zum Importieren einer Typbibliothek ist etwas komplizierter für C++-Clients, obwohl dieselben Tools verwendet werden wie beim Exportieren von Metadaten in eine COM-Typbibliothek. Zum Verweisen auf .NET-Objektmember von einem nicht verwalteten C++-Client aus verweisen Sie auf die TLB-Datei (die mit Tlbexp.exe erstellt wurde) mit der **#import**-Anweisung. Zum Verweisen auf eine Typbibliothek von C++ müssen Sie entweder die **raw_interfaces_only**-Option angeben oder die Definitionen in die Basisklassenbibliothek Mscorlib.tlb importieren.  
  
### <a name="to-import-a-library"></a>So importieren Sie eine Bibliothek  
  
-   Geben Sie die **raw_interfaces_only**-Option in der **#import**-Anweisung an. Beispiel:  
  
    ```cpp  
    #import "..\LoanLib\LoanLib.tlb" raw_interfaces_only  
    ```  
  
     - oder -   
  
-   Schließen Sie eine #import-Direktive für Mscorlib.tlb ein. Beispiel:  
  
    ```cpp  
    #import "mscorlib.tlb"  
    #import "..\LoanLib\LoanLib.tlb"  
    ```  
  
## <a name="see-also"></a>Siehe auch
- [Verfügbarmachen von .NET Framework-Komponenten in COM](exposing-dotnet-components-to-com.md)
- [Registrieren von Assemblys bei COM](registering-assemblies-with-com.md)
- [Aufrufen eines .NET-Objekts](https://msdn.microsoft.com/library/40c9626c-aea6-4bad-b8f0-c1de462efd33(v=vs.100))
- [Deploying an Application for COM Access (Bereitstellen einer Anwendung für COM-Zugriff)](https://msdn.microsoft.com/library/fb63564c-c1b9-4655-a094-a235625882ce(v=vs.100))
