---
title: Modellieren und Zuordnen
ms.date: 03/30/2017
ms.assetid: ec8a9515-3708-4cde-a688-4d8e6975f150
ms.openlocfilehash: 847d518710b21df714343b541401ff7fc8443fb3
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/07/2019
ms.locfileid: "55828305"
---
# <a name="modeling-and-mapping"></a>Modellieren und Zuordnen
In [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] können Sie das konzeptionelle Modell, das Speichermodell und die Zuordnung zwischen beiden auf die Weise definieren, die der Anwendung am besten entspricht. Entity Data Model-Tools in Visual Studio können Sie erstellen ein. [Edmx-Datei](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100)) aus einer Datenbank oder einem grafischen Modell und aktualisieren Sie dann die Datei, wenn die Datenbank oder das Modell ändert.  
  
 Ab Entity Framework 4.1 können Sie ein Modell anhand der Code First-Entwicklung auch programmgesteuert erstellen. Es gibt zwei verschiedene Szenarien für die Code First-Entwicklung. In beiden Fällen definiert der Entwickler ein Modell, indem er .NET Framework-Klassendefinitionen codiert und dann optional zusätzliche Zuordnungen oder Konfigurationen mithilfe von Datenanmerkungen oder der Fluent-API angibt.  
  
 Weitere Informationen finden Sie unter [erstellen und Zuordnen eines konzeptionellen Modells](https://go.microsoft.com/fwlink/?LinkId=235016).  
  
 Sie können auch den EDM-Generator, der in enthalten ist das [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)]. EdmGen.exe generiert die CSDL-, SSDL- und MSL-Dateien aus einer vorhandenen Datenquelle. Sie können Modell- und Zuordnungsinhalte auch manuell erstellen. Weitere Informationen finden Sie unter [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md).
