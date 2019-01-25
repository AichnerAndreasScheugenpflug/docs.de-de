---
title: 'Vorgehensweise: Ausführen einer parametrisierten gespeicherten Prozedur mithilfe von EntityCommand'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 4f5639bf-bb7f-4982-bb1d-c7caa4348888
ms.openlocfilehash: 11894decbb81192eb68c680149bbe9f7398f0203
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587809"
---
# <a name="how-to-execute-a-parameterized-stored-procedure-using-entitycommand"></a>Vorgehensweise: Ausführen einer parametrisierten gespeicherten Prozedur mithilfe von EntityCommand
In diesem Thema wird beschrieben, wie eine parametrisierte gespeicherte Prozedur mithilfe der <xref:System.Data.EntityClient.EntityCommand>-Klasse ausgeführt wird.  
  
### <a name="to-run-the-code-in-this-example"></a>So führen Sie den Code in diesem Beispiel aus  
  
1.  Hinzufügen der [Modell "School"](https://msdn.microsoft.com/library/859a9587-81ea-4a45-9bc0-f8d330e1adac) zu Ihrem Projekt und Konfigurieren Ihres Projekts zur Verwendung der [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]. Weitere Informationen finden Sie unter [Vorgehensweise: Verwenden des Assistenten für Entity Data Model](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d).  
  
2.  Fügen Sie der Codepage Ihrer Anwendung die folgenden `using`-Anweisungen (`Imports` in Visual Basic) hinzu:  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
3.  Importieren Sie die gespeicherte `GetStudentGrades`-Prozedur, und geben Sie `CourseGrade`-Entitäten als Rückgabetyp an. Informationen zum Importieren einer gespeicherten Prozedur finden Sie unter [Vorgehensweise: Importieren einer gespeicherten Prozedur](https://msdn.microsoft.com/library/24e68bf4-bd6d-428d-bc35-92d7b8e3736d).  
  
## <a name="example"></a>Beispiel  
 Der folgenden Code führt die gespeicherte `GetStudentGrades`-Prozedur aus. Dabei ist `StudentId` ein erforderlicher Parameter. Die Ergebnisse werden dann von einer <xref:System.Data.EntityClient.EntityDataReader> gelesen.  
  
 [!code-csharp[DP EntityServices Concepts#StoredProcWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#storedprocwithentitycommand)]
 [!code-vb[DP EntityServices Concepts#StoredProcWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#storedprocwithentitycommand)]  
  
## <a name="see-also"></a>Siehe auch
- [EntityClient-Anbieter für Entity Framework](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)
