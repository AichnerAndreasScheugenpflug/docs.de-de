---
title: 'Exemplarische Vorgehensweise: Einbetten von Typinformationen aus Microsoft Office-Assemblys in Visual Studio (C#)'
ms.date: 07/20/2015
ms.assetid: 3320e866-01f1-4b7f-8932-049a7b2d2a9b
ms.openlocfilehash: 20ed45b1796062973a1d4a9bcaa86782655d3867
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732699"
---
# <a name="walkthrough-embedding-type-information-from-microsoft-office-assemblies-in-visual-studio-c"></a><span data-ttu-id="5901d-102">Exemplarische Vorgehensweise: Einbetten von Typinformationen aus Microsoft Office-Assemblys in Visual Studio (C#)</span><span class="sxs-lookup"><span data-stu-id="5901d-102">Walkthrough: Embedding Type Information from Microsoft Office Assemblies in Visual Studio (C#)</span></span>
<span data-ttu-id="5901d-103">Wenn Sie Typinformationen in eine Anwendung einbetten, die auf COM-Objekte verweist, ist die Verwendung einer primären Interopassembly (PIA) nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5901d-103">If you embed type information in an application that references COM objects, you can eliminate the need for a primary interop assembly (PIA).</span></span> <span data-ttu-id="5901d-104">Darüber hinaus wird die Anwendung durch die eingebetteten Typinformationen versionsunabhängig.</span><span class="sxs-lookup"><span data-stu-id="5901d-104">Additionally, the embedded type information enables you to achieve version independence for your application.</span></span> <span data-ttu-id="5901d-105">Ihr Programm kann daher für Typen aus unterschiedlichen Versionen einer COM-Bibliothek geschrieben werden; eine versionsspezifische PIA ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5901d-105">That is, your program can be written to use types from multiple versions of a COM library without requiring a specific PIA for each version.</span></span> <span data-ttu-id="5901d-106">Dies ist ein allgemeines Szenario für Anwendungen, die Objekte aus Microsoft Office-Bibliotheken verwenden.</span><span class="sxs-lookup"><span data-stu-id="5901d-106">This is a common scenario for applications that use objects from Microsoft Office libraries.</span></span> <span data-ttu-id="5901d-107">Mithilfe von eingebetteten Typinformationen kann ein Build eines Programms verschiedene Versionen von Microsoft Office auf unterschiedlichen Computern verwenden, ohne dass das Programm oder die PIA für jede Version von Microsoft Office erneut bereitgestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5901d-107">Embedding type information enables the same build of a program to work with different versions of Microsoft Office on different computers without the need to redeploy either the program or the PIA for each version of Microsoft Office.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
## <a name="prerequisites"></a><span data-ttu-id="5901d-108">Erforderliche Komponenten</span><span class="sxs-lookup"><span data-stu-id="5901d-108">Prerequisites</span></span>  
 <span data-ttu-id="5901d-109">Für diese exemplarische Vorgehensweise wird Folgendes vorausgesetzt:</span><span class="sxs-lookup"><span data-stu-id="5901d-109">This walkthrough requires the following:</span></span>  
  
-   <span data-ttu-id="5901d-110">Ein Computer, auf dem Visual Studio und Microsoft Excel installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5901d-110">A computer on which Visual Studio and Microsoft Excel are installed.</span></span>  
  
-   <span data-ttu-id="5901d-111">Ein zweiter Computer, auf dem .NET Framework 4 oder höher und eine andere Version von Excel installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5901d-111">A second computer on which the .NET Framework 4 or higher and a different version of Excel are installed.</span></span>  
  
##  <a name="BKMK_createapp"></a> <span data-ttu-id="5901d-112">So erstellen Sie eine Anwendung, die mit mehreren Versionen von Microsoft Office kompatibel ist</span><span class="sxs-lookup"><span data-stu-id="5901d-112">To create an application that works with multiple versions of Microsoft Office</span></span>  
  
1.  <span data-ttu-id="5901d-113">Starten Sie Visual Studio auf einem Computer, auf dem Excel installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5901d-113">Start Visual Studio on a computer on which Excel is installed.</span></span>  
  
2.  <span data-ttu-id="5901d-114">Wählen Sie im Menü **Datei** die Optionsfolge **Neu**, **Projekt**aus.</span><span class="sxs-lookup"><span data-stu-id="5901d-114">On the **File** menu, choose **New**, **Project**.</span></span>  
  
3.  <span data-ttu-id="5901d-115">Überprüfen Sie, ob im Dialogfeld **Neues Projekt** im Bereich **Projekttypen** der Eintrag **Windows** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="5901d-115">In the **New Project** dialog box, in the **Project Types** pane, make sure that **Windows** is selected.</span></span> <span data-ttu-id="5901d-116">Wählen Sie im Bereich **Vorlagen** die Option **Konsolenanwendung** aus.</span><span class="sxs-lookup"><span data-stu-id="5901d-116">Select **Console Application** in the **Templates** pane.</span></span> <span data-ttu-id="5901d-117">Geben Sie im Feld **Name** `CreateExcelWorkbook` ein, und wählen Sie dann die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5901d-117">In the **Name** box, enter `CreateExcelWorkbook`, and then choose the **OK** button.</span></span> <span data-ttu-id="5901d-118">Das neue Projekt wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="5901d-118">The new project is created.</span></span>  
  
4.  <span data-ttu-id="5901d-119">Öffnen Sie im **Projektmappen-Explorer** das Kontextmenü für den Ordner **Verweise**, und wählen Sie dann **Verweis hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5901d-119">In **Solution Explorer**, open the shortcut menu for the **References** folder and then choose **Add Reference**.</span></span>  
  
5.  <span data-ttu-id="5901d-120">Wählen Sie auf der Registerkarte **.NET** die aktuellste Version von `Microsoft.Office.Interop.Excel` aus.</span><span class="sxs-lookup"><span data-stu-id="5901d-120">On the **.NET** tab, choose the most recent version of `Microsoft.Office.Interop.Excel`.</span></span> <span data-ttu-id="5901d-121">Beispiel: **Microsoft.Office.Interop.Excel 14.0.0.0**.</span><span class="sxs-lookup"><span data-stu-id="5901d-121">For example, **Microsoft.Office.Interop.Excel 14.0.0.0**.</span></span> <span data-ttu-id="5901d-122">Klicken Sie auf die Schaltfläche **OK** .</span><span class="sxs-lookup"><span data-stu-id="5901d-122">Choose the **OK** button.</span></span>  
  
6.  <span data-ttu-id="5901d-123">Wählen Sie in der Liste der Verweise für das **CreateExcelWorkbook**-Projekt den Verweis für `Microsoft.Office.Interop.Excel` aus, den Sie im vorherigen Schritt hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="5901d-123">In the list of references for the **CreateExcelWorkbook** project, select the reference for `Microsoft.Office.Interop.Excel` that you added in the previous step.</span></span> <span data-ttu-id="5901d-124">Vergewissern Sie sich, dass die `Embed Interop Types`-Eigenschaft im Fester **Eigenschaften** auf `True` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5901d-124">In the **Properties** window, make sure that the `Embed Interop Types` property is set to `True`.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="5901d-125">Die in dieser exemplarischen Vorgehensweise erstellte Anwendung kann aufgrund der eingebetteten Interop-Typinformationen mit verschiedenen Versionen von Microsoft Office ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5901d-125">The application created in this walkthrough runs with different versions of Microsoft Office because of the embedded interop type information.</span></span> <span data-ttu-id="5901d-126">Wenn die `Embed Interop Types`-Eigenschaft auf `False` festgelegt ist, müssen Sie eine PIA für jede Version von Microsoft Office einschließen, mit der die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5901d-126">If the `Embed Interop Types` property is set to `False`, you must include a PIA for each version of Microsoft Office that the application will run with.</span></span>  
  
7.  <span data-ttu-id="5901d-127">Öffnen Sie die Datei **Program.cs**.</span><span class="sxs-lookup"><span data-stu-id="5901d-127">Open the **Program.cs** file.</span></span> <span data-ttu-id="5901d-128">Ersetzen Sie den Code in der Datei durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="5901d-128">Replace the code in the file with the following code:</span></span>  
  
    ```csharp  
    using System;  
    using System.Collections.Generic;  
    using System.Linq;  
    using System.Text;  
    using System.IO;  
    using Excel = Microsoft.Office.Interop.Excel;  
  
    namespace CreateExcelWorkbook  
    {  
        class Program  
        {  
            static void Main(string[] args)  
            {  
                int[] values = {4, 6, 18, 2, 1, 76, 0, 3, 11};  
  
                CreateWorkbook(values, @"C:\SampleFolder\SampleWorkbook.xls");  
            }  
  
            static void CreateWorkbook(int[] values, string filePath)  
            {  
                Excel.Application excelApp = null;  
                Excel.Workbook wkbk;  
                Excel.Worksheet sheet;  
  
                try  
                {  
                        // Start Excel and create a workbook and worksheet.  
                        excelApp = new Excel.Application();  
                        wkbk = excelApp.Workbooks.Add();  
                        sheet = wkbk.Sheets.Add() as Excel.Worksheet;  
                        sheet.Name = "Sample Worksheet";  
  
                        // Write a column of values.  
                        // In the For loop, both the row index and array index start at 1.  
                        // Therefore the value of 4 at array index 0 is not included.  
                        for (int i = 1; i < values.Length; i++)  
                        {  
                            sheet.Cells[i, 1] = values[i];  
                        }  
  
                        // Suppress any alerts and save the file. Create the directory   
                        // if it does not exist. Overwrite the file if it exists.  
                        excelApp.DisplayAlerts = false;  
                        string folderPath = Path.GetDirectoryName(filePath);  
                        if (!Directory.Exists(folderPath))  
                        {  
                            Directory.CreateDirectory(folderPath);  
                        }  
                        wkbk.SaveAs(filePath);  
                }  
                catch  
                {  
                }  
                finally  
                {  
                    sheet = null;  
                    wkbk = null;  
  
                    // Close Excel.  
                    excelApp.Quit();  
                    excelApp = null;  
                }  
            }  
        }  
    }  
    ```  
  
8.  <span data-ttu-id="5901d-129">Speichern Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="5901d-129">Save the project.</span></span>  
  
9. <span data-ttu-id="5901d-130">Drücken Sie STRG+F5, um das Projekt zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5901d-130">Press CTRL+F5 to build and run the project.</span></span> <span data-ttu-id="5901d-131">Überprüfen Sie, ob eine Excel-Arbeitsmappe an dem Speicherort erstellt wurde, der im Beispielcode angegebenen ist: C:\SampleFolder\SampleWorkbook.xls.</span><span class="sxs-lookup"><span data-stu-id="5901d-131">Verify that an Excel workbook has been created at the location specified in the example code: C:\SampleFolder\SampleWorkbook.xls.</span></span>  
  
##  <a name="BKMK_publishapp"></a> <span data-ttu-id="5901d-132">So veröffentlichen Sie die Anwendung auf einem Computer, auf dem eine andere Version von Microsoft Office installiert ist</span><span class="sxs-lookup"><span data-stu-id="5901d-132">To publish the application to a computer on which a different version of Microsoft Office is installed</span></span>  
  
1.  <span data-ttu-id="5901d-133">Öffnen Sie das Projekt, das Sie in dieser exemplarischen Vorgehensweise erstellt haben, in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5901d-133">Open the project created by this walkthrough in Visual Studio.</span></span>  
  
2.  <span data-ttu-id="5901d-134">Wählen Sie im Menü **Erstellen** die Option **CreateExcelWorkbook veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="5901d-134">On the **Build** menu, choose **Publish CreateExcelWorkbook**.</span></span> <span data-ttu-id="5901d-135">Führen Sie die Schritte des Webpublishing-Assistenten aus, um eine installierbare Version der Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5901d-135">Follow the steps of the Publish Wizard to create an installable version of the application.</span></span> <span data-ttu-id="5901d-136">Weitere Informationen finden Sie unter [Veröffentlichungs-Assistent (Office-Entwicklung in Visual Studio)](/visualstudio/vsto/publish-wizard-office-development-in-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="5901d-136">For more information, see [Publish Wizard (Office Development in Visual Studio)](/visualstudio/vsto/publish-wizard-office-development-in-visual-studio).</span></span>  
  
3.  <span data-ttu-id="5901d-137">Installieren Sie die Anwendung auf einem Computer, auf dem .NET Framework 4 oder höher und eine andere Version von Excel installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5901d-137">Install the application on a computer on which the .NET Framework 4 or higher and a different version of Excel are installed.</span></span>  
  
4.  <span data-ttu-id="5901d-138">Führen Sie das installierte Programm aus, sobald die Installation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5901d-138">When the installation is finished, run the installed program.</span></span>  
  
5.  <span data-ttu-id="5901d-139">Überprüfen Sie, ob eine Excel-Arbeitsmappe an dem Speicherort erstellt wurde, der im Beispielcode angegebenen ist: C:\SampleFolder\SampleWorkbook.xls.</span><span class="sxs-lookup"><span data-stu-id="5901d-139">Verify that an Excel workbook has been created at the location specified in the sample code: C:\SampleFolder\SampleWorkbook.xls.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5901d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5901d-140">See also</span></span>

- [<span data-ttu-id="5901d-141">Exemplarische Vorgehensweise: Einbetten von Typen aus verwalteten Assemblys in Visual Studio (C#)</span><span class="sxs-lookup"><span data-stu-id="5901d-141">Walkthrough: Embedding Types from Managed Assemblies in Visual Studio (C#)</span></span>](../../../../csharp/programming-guide/concepts/assemblies-gac/walkthrough-embedding-types-from-managed-assemblies-in-visual-studio.md)
- [<span data-ttu-id="5901d-142">-link (C#-Compileroptionen)</span><span class="sxs-lookup"><span data-stu-id="5901d-142">/link (C# Compiler Options)</span></span>](../../../../csharp/language-reference/compiler-options/link-compiler-option.md)
