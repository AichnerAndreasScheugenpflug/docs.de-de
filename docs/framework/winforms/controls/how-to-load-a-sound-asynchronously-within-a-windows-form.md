---
title: 'Vorgehensweise: Laden eines Sounds asynchron in einem Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- SoundPlayer class [Windows Forms], loading sounds asynchronously
- sounds [Windows Forms], loading on separate threads
- threading [Windows Forms], sounds
ms.assetid: 3b6a9296-1d5e-4d52-a4ba-94366d6fe302
ms.openlocfilehash: ed1257a942eb990c9b0c6427d264013e3324326b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54523674"
---
# <a name="how-to-load-a-sound-asynchronously-within-a-windows-form"></a><span data-ttu-id="540ca-102">Vorgehensweise: Laden eines Sounds asynchron in einem Windows Form</span><span class="sxs-lookup"><span data-stu-id="540ca-102">How to: Load a Sound Asynchronously within a Windows Form</span></span>
<span data-ttu-id="540ca-103">Im folgenden Codebeispiel wird ein Sound aus einer URL asynchron geladen und anschließend auf einem neuen Thread abgespielt.</span><span class="sxs-lookup"><span data-stu-id="540ca-103">The following code example asynchronously loads a sound from an URL and then plays it on a new thread.</span></span>  
  
## <a name="example"></a><span data-ttu-id="540ca-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="540ca-104">Example</span></span>  
 [!code-csharp[System.Media.SoundPlayer.LoadAsync#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Media.SoundPlayer.LoadAsync/CS/Form1.cs#1)]
 [!code-vb[System.Media.SoundPlayer.LoadAsync#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Media.SoundPlayer.LoadAsync/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="540ca-105">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="540ca-105">Compiling the Code</span></span>  
 <span data-ttu-id="540ca-106">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="540ca-106">This example requires:</span></span>  
  
-   <span data-ttu-id="540ca-107">Verweise auf die Assemblys "System" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="540ca-107">References to the System and System.Windows.Forms assemblies.</span></span>  
  
-   <span data-ttu-id="540ca-108">Ersetzen Sie den Dateinamen `"http://www.tailspintoys.com/sounds/stop.wav"` durch einen gültigen Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="540ca-108">That you replace the file name `"http://www.tailspintoys.com/sounds/stop.wav"` with a valid file name.</span></span>  
  
 <span data-ttu-id="540ca-109">Informationen zum Erstellen dieses Beispiels über die Befehlszeile für Visual Basic oder Visual c# finden Sie unter [erstellen über die Befehlszeile](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) oder [Befehlszeile mit csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="540ca-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="540ca-110">Sie können auch in diesem Beispiel in Visual Studio erstellen, indem Sie den Code in ein neues Projekt einfügen.</span><span class="sxs-lookup"><span data-stu-id="540ca-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="540ca-111">Weitere Informationen hierzu finden Sie auch unter [Gewusst wie: Kompilieren und Ausführen einer vollständigen Windows Forms-Codebeispiels mit Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="540ca-111">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="540ca-112">Stabile Programmierung</span><span class="sxs-lookup"><span data-stu-id="540ca-112">Robust Programming</span></span>  
 <span data-ttu-id="540ca-113">Dateioperationen sollten in entsprechende Ausnahmebehandlungsblöcke eingeschlossen sein.</span><span class="sxs-lookup"><span data-stu-id="540ca-113">File operations should be enclosed within appropriate exception-handling blocks.</span></span>  
  
 <span data-ttu-id="540ca-114">Die folgenden Bedingungen können einen Ausnahmefehler verursachen:</span><span class="sxs-lookup"><span data-stu-id="540ca-114">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="540ca-115">Der Pfadname ist falsch formatiert.</span><span class="sxs-lookup"><span data-stu-id="540ca-115">The path name is malformed.</span></span> <span data-ttu-id="540ca-116">Er enthält beispielsweise unzulässige Zeichen oder besteht nur aus Leerzeichen (<xref:System.ArgumentException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="540ca-116">For example, it contains characters that are not valid or is only white space (<xref:System.ArgumentException> class).</span></span>  
  
-   <span data-ttu-id="540ca-117">Der Pfad ist schreibgeschützt (<xref:System.IO.IOException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="540ca-117">The path is read-only (<xref:System.IO.IOException> class).</span></span>  
  
-   <span data-ttu-id="540ca-118">Der Pfadname ist `Nothing` (<xref:System.ArgumentNullException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="540ca-118">The path name is `Nothing` (<xref:System.ArgumentNullException> class).</span></span>  
  
-   <span data-ttu-id="540ca-119">Der Pfadname ist zu lang (<xref:System.IO.PathTooLongException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="540ca-119">The path name is too long (<xref:System.IO.PathTooLongException> class).</span></span>  
  
-   <span data-ttu-id="540ca-120">Der Pfad ist ungültig (<xref:System.IO.DirectoryNotFoundException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="540ca-120">The path is not valid (<xref:System.IO.DirectoryNotFoundException> class).</span></span>  
  
-   <span data-ttu-id="540ca-121">Der Pfad besteht nur aus einem Doppelpunkt ":" (<xref:System.NotSupportedException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="540ca-121">The path is only a colon ":" (<xref:System.NotSupportedException> class).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="540ca-122">.NET Framework-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="540ca-122">.NET Framework Security</span></span>  
 <span data-ttu-id="540ca-123">Beurteilen Sie den Inhalt der Datei nicht anhand des Dateinamens.</span><span class="sxs-lookup"><span data-stu-id="540ca-123">Do not make decisions about the contents of the file based on the name of the file.</span></span> <span data-ttu-id="540ca-124">Bei der Datei `Form1.vb` handelt es sich zum Beispiel nicht unbedingt um eine Visual Basic-Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="540ca-124">For example, the file `Form1.vb` may not be a Visual Basic source file.</span></span> <span data-ttu-id="540ca-125">Überprüfen Sie alle Eingaben, bevor Sie die Daten in der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="540ca-125">Verify all inputs before using the data in your application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="540ca-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="540ca-126">See also</span></span>
- <xref:System.Media.SoundPlayer.LoadAsync%2A>
- <xref:System.Media.SoundPlayer.LoadCompleted>
- <xref:System.Media.SoundPlayer.Play%2A>
- [<span data-ttu-id="540ca-127">Vorgehensweise: Wiedergabe von Sound in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="540ca-127">How to: Play a Sound from a Windows Form</span></span>](../../../../docs/framework/winforms/controls/how-to-play-a-sound-from-a-windows-form.md)
