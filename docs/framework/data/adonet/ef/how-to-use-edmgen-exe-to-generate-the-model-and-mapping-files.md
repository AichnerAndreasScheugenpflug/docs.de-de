---
title: 'Vorgehensweise: Verwenden von EdmGen.exe zum Generieren von Modell- und Zuordnungsdateien'
ms.date: 03/30/2017
ms.assetid: 40db462d-2fd2-4cc1-ad86-d280403e63fa
ms.openlocfilehash: 340ef0b20c25ca76df51085592e53849c6bf7a12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610152"
---
# <a name="how-to-use-edmgenexe-to-generate-the-model-and-mapping-files"></a>Vorgehensweise: Verwenden von EdmGen.exe zum Generieren von Modell- und Zuordnungsdateien
In diesem Thema wird veranschaulicht, wie das Tool EDM-Generator (EdmGen.exe) verwendet wird, um die folgenden Dateien auf der Grundlage der Datenbank "School" zu generieren:  
  
-   Ein konzeptionelles Modell (eine CSDL-Datei).  
  
-   Ein Speichermodell (eine SSDL-Datei).  
  
-   Die Zuordnung zwischen dem konzeptionellen Modell und dem Speichermodell (eine MSL-Datei).  
  
-   Code auf Objektebene für Visual Basic oder C#.  
  
-   Ansichtsdateien.  
  
 Wenn das Tool EdmGen.exe mit dem Befehl /mode:FullGeneration aufgerufen wird, werden die oben aufgeführten Dateien generiert. Weitere Informationen zu den Befehlen in EdmGen.exe finden Sie unter [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md).  
  
 Wenn Sie mithilfe von EdmGen.exe generieren von Modell- und Zuordnungsdateien, noch müssen Sie so konfigurieren Sie Ihre Visual Studio-Projekt für die Verwendung der [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]. Weitere Informationen finden Sie unter [Vorgehensweise: Manuelles Konfigurieren eines Entity Framework-Projekts](https://msdn.microsoft.com/library/73f6ae1d-b3b2-4577-aebd-ad5a75954e9e).  
  
> [!NOTE]
>  Ein mithilfe von EdmGen.exe erstelltes konzeptionelles Modell enthält alle Objekte der Datenbank. Sie können mithilfe des Entity Data Model-Assistenten ein konzeptionelles Modell erstellen, das nur bestimmte Objekte enthält. Weitere Informationen finden Sie unter [Vorgehensweise: Verwenden des Assistenten für Entity Data Model](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d).  
  
### <a name="to-generate-the-school-model-for-a-visual-basic-project-using-edmgenexe"></a>So erstellen Sie mithilfe von 'EdmGen.exe' das Modell 'School' für ein Visual Basic-Projekt  
  
1.  Erstellen der Datenbank "School". Weitere Informationen finden Sie unter [Erstellen der Beispieldatenbank "School"](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).  
  
2.  Führen Sie an der Eingabeaufforderung den folgenden Befehl ohne Zeilenumbrüche aus:  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:fullgeneration   
    /c:"Data Source=%datasourceserver%; Initial Catalog=School; Integrated Security=SSPI"   
    /project:School /entitycontainer:SchoolEntities /namespace:SchoolModel /language:VB  
    ```  
  
### <a name="to-generate-the-school-model-for-a-c-project-using-edmgenexe"></a>So erstellen Sie mithilfe von 'EdmGen.exe' das Modell 'School' für ein C#-Projekt  
  
1.  Erstellen der Datenbank "School". Weitere Informationen finden Sie unter [Erstellen der Beispieldatenbank "School"](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).  
  
2.  Führen Sie an der Eingabeaufforderung den folgenden Befehl ohne Zeilenumbrüche aus:  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:fullgeneration   
    /c:"Data Source=%datasourceserver%; Initial Catalog=School; Integrated Security=SSPI"   
    /project:School /entitycontainer:SchoolEntities /namespace:SchoolModel /language:CSharp  
    ```  
  
## <a name="see-also"></a>Siehe auch
- [Modellieren und Zuordnen](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md)
- [Vorgehensweise: Manuelles Konfigurieren eines Entity Framework-Projekts](https://msdn.microsoft.com/library/73f6ae1d-b3b2-4577-aebd-ad5a75954e9e)
- [Vorgehensweise: Vorgenerieren von Ansichten zur Verbesserung der Abfrageleistung](https://msdn.microsoft.com/library/b18a9d16-e10b-4043-ba91-b632f85a2579)
- [ADO.NET Entity Data Model Tools (ADO.NET Entity Data Model-Tools)](https://msdn.microsoft.com/library/91076853-0881-421b-837a-f582f36be527)
- [Vorgehensweise: Verwenden von EdmGen.exe zum Überprüfen von Modell- und Zuordnungsdateien](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-validate-model-and-mapping-files.md)
