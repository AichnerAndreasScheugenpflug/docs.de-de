---
title: 'Vorgehensweise: Verhindern des Anfügens einer untergeordneten Aufgabe an die übergeordnete Aufgabe'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tasks, preventing attachments
ms.assetid: c0fb85d4-9e80-4905-9f65-29acc54201c4
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7506a57e29b7942bd06141baa2d2b048ed998214
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/11/2019
ms.locfileid: "54221530"
---
# <a name="how-to-prevent-a-child-task-from-attaching-to-its-parent"></a>Vorgehensweise: Verhindern des Anfügens einer untergeordneten Aufgabe an die übergeordnete Aufgabe
Dieses Dokument veranschaulicht, wie das Anfügen einer untergeordneten Aufgabe an die übergeordnete Aufgabe verhindert wird. Sie sollten verhindern, dass eine untergeordnete Aufgabe an ihre übergeordnete Aufgabe angefügt wird, wenn Sie eine Komponente aufrufen, die von einem Drittanbieter geschrieben wurde und auch Aufgaben verwendet. So kann z.B. eine Drittanbieterkomponente bei Verwendung der <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent?displayProperty=nameWithType>-Option zum Erstellen eines <xref:System.Threading.Tasks.Task>- oder <xref:System.Threading.Tasks.Task%601>-Objekts Probleme im Code verursachen, wenn sie lange ausgeführt wird oder eine unbehandelte Ausnahme auslöst.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden die Auswirkungen der Verwendung der Standardoptionen mit den Auswirkungen verglichen, die es mit sich bringt, zu verhindern, dass eine untergeordnete Aufgabe dem übergeordneten Element angefügt wird. Im Beispiel wird ein <xref:System.Threading.Tasks.Task>-Objekt erstellt, das einen Aufruf an eine Drittanbieterbibliothek richtet, die auch ein <xref:System.Threading.Tasks.Task>-Objekt verwendet. Die Drittanbieterbibliothek verwendet die <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent>-Option zum Erstellen des <xref:System.Threading.Tasks.Task>-Objekts. Die Anwendung verwendet die <xref:System.Threading.Tasks.TaskCreationOptions.DenyChildAttach?displayProperty=nameWithType>-Option zum Erstellen der übergeordneten Aufgabe. Diese Option weist die Runtime an, die <xref:System.Threading.Tasks.TaskCreationOptions.AttachedToParent>-Spezifikation in untergeordneten Aufgaben zu entfernen.  
  
 [!code-csharp[TPL_DenyChildAttach#1](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_denychildattach/cs/denychildattach.cs#1)]
 [!code-vb[TPL_DenyChildAttach#1](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_denychildattach/vb/denychildattach.vb#1)]  
  
 Da eine übergeordnete Aufgabe nicht beendet wird, ehe alle untergeordneten Aufgaben abgeschlossen sind, kann eine untergeordnete Aufgabe mit langer Laufzeit zu einer Verschlechterung der Leistung der gesamten Anwendung führen. Wenn die Anwendung in diesem Beispiel die Standardoptionen verwendet, um die übergeordnete Aufgabe zu erstellen, muss die untergeordnete Aufgabe vor der übergeordneten Aufgabe beendet werden. Wenn die Anwendung die <xref:System.Threading.Tasks.TaskCreationOptions.DenyChildAttach?displayProperty=nameWithType>-Option verwendet, wird das untergeordnete Element nicht dem übergeordneten angefügt. Aus diesem Grund kann die Anwendung zusätzliche Aufgaben ausführen, nachdem die übergeordnete Aufgabe abgeschlossen ist, und vorher muss sie auf das Beenden der untergeordneten Aufgabe warten.  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Kopieren Sie den Beispielcode, und fügen Sie ihn in ein Visual Studio-Projekt ein, oder fügen Sie ihn in eine Datei namens `DenyChildAttach.cs` ein (`DenyChildAttach.vb` für Visual Basic), und führen Sie dann den folgenden Befehl in einer Developer-Eingabeaufforderung für Visual Studio aus.  
  
 Visual C#  
  
 **csc.exe DenyChildAttach.cs**  
  
 Visual Basic  
  
 **vbc.exe DenyChildAttach.vb**  
  
## <a name="robust-programming"></a>Stabile Programmierung  
  
## <a name="see-also"></a>Siehe auch

- [Aufgabenbasierte asynchrone Programmierung](../../../docs/standard/parallel-programming/task-based-asynchronous-programming.md)
