---
title: 'Gewusst wie: Iterieren von Dateiverzeichnissen mit PLINQ'
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- PLINQ queries, how to iterate directories
ms.assetid: 354e8ce3-35c4-431c-99ca-7661d1f3901b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d48f6df1e0e7680d2706c73c33dc817e1feaf1d5
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2018
ms.locfileid: "45689326"
---
# <a name="how-to-iterate-file-directories-with-plinq"></a>Gewusst wie: Iterieren von Dateiverzeichnissen mit PLINQ
Dieses Beispiel zeigt zwei einfache Möglichkeiten, um Vorgänge für Dateiverzeichnisse zu parallelisieren. Die erste Abfrage füllt mit der <xref:System.IO.Directory.GetFiles%2A>-Methode ein Array von Dateinamen in einem Verzeichnis und allen Unterverzeichnissen. Diese Methode erzeugt keine Rückgabe, solange nicht das gesamte Array aufgefüllt ist, und daher kann am Anfang des Vorgangs eine Wartezeit auftreten. Sobald das Array aufgefüllt ist, kann PLINQ es jedoch sehr schnell parallel verarbeiten.  
  
 Die zweite Abfrage verwendet die statische <xref:System.IO.Directory.EnumerateDirectories%2A>- und <xref:System.IO.DirectoryInfo.EnumerateFiles%2A>-Methode, die sofort beginnen, Ergebnisse zurückzugeben. Dieser Ansatz kann bei Iterationen über umfangreiche Verzeichnisstrukturen schneller sein, obwohl die Verarbeitungszeit im Vergleich zum ersten Beispiel von vielen Faktoren abhängen kann.  
  
> [!WARNING]
>  Diese Beispiele sollen die Nutzung darstellen und werden möglicherweise nicht schneller ausgeführt als die entsprechende sequenzielle LINQ to Objects-Abfrage. Weitere Informationen finden Sie unter [Grundlagen zur Beschleunigung in PLINQ](../../../docs/standard/parallel-programming/understanding-speedup-in-plinq.md).  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt die Iteration über Dateiverzeichnisse in einfachen Szenarien, wenn Sie Zugriff auf alle Verzeichnisse in der Struktur haben, die Dateien nicht sehr groß und die Zugriffszeiten nicht beachtlich sind. Bei diesem Ansatz tritt zu Anfang eine Wartezeit auf, während das Dateinamenarray konstruiert wird.  
  
 [!code-csharp[PLINQ#33](../../../samples/snippets/csharp/VS_Snippets_Misc/plinq/cs/plinqfileiteration.cs#33)]  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt die Iteration über Dateiverzeichnisse in einfachen Szenarien, wenn Sie Zugriff auf alle Verzeichnisse in der Struktur haben, die Dateien nicht sehr groß und die Zugriffszeiten nicht beachtlich sind. Dieser Ansatz erzeugt Ergebnisse schneller als das vorherige Beispiel.  
  
 [!code-csharp[PLINQ#34](../../../samples/snippets/csharp/VS_Snippets_Misc/plinq/cs/plinqfileiteration.cs#34)]  
  
 Achten Sie bei Verwendung von <xref:System.IO.Directory.GetFiles%2A> darauf, dass Sie über ausreichende Berechtigungen für alle Verzeichnisse in der Struktur verfügen. Andernfalls wird eine Ausnahme ausgelöst, und es werden keine Ergebnisse zurückgegeben. Bei Verwendung von <xref:System.IO.Directory.EnumerateDirectories%2A> in einer PLINQ-Abfrage ist es schwierig, E/A-Ausnahmen auf eine ordnungsgemäße Weise zu behandeln, die Ihnen erlaubt, die Iteration fortzusetzen. Wenn der Code E/A- oder nicht autorisierten Zugriff betreffende Ausnahmen behandeln muss, sollten Sie den in [Gewusst wie: Iteration über Dateiverzeichnisse der Parallel-Klasse](../../../docs/standard/parallel-programming/how-to-iterate-file-directories-with-the-parallel-class.md) beschriebenen Ansatz erwägen.  
  
 Wenn E/A-Wartezeit ein Problem ist, z.B. bei Datei-E/A über ein Netzwerk, erwägen Sie die Verwendung einer der in [TPL und herkömmliche asynchrone .NET Framework-Programmierung](../../../docs/standard/parallel-programming/tpl-and-traditional-async-programming.md) und in diesem [Blogbeitrag](https://blogs.msdn.microsoft.com/pfxteam/2009/08/04/parallel-extensions-and-io/) beschriebenen asynchronen E/A-Techniken.  
  
## <a name="see-also"></a>Siehe auch

- [Parallel LINQ (PLINQ) (Paralleles LINQ (PLINQ))](../../../docs/standard/parallel-programming/parallel-linq-plinq.md)
