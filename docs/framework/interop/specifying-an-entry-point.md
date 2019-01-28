---
title: Angeben eines Einstiegspunktes
ms.date: 03/30/2017
helpviewer_keywords:
- EntryPoint field
- platform invoke, attribute fields
- attribute fields in platform invoke, EntryPoint
ms.assetid: d1247f08-0965-416a-b978-e0b50652dfe3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c278eca421020bea4f36f87eb6c8a9a8ba7d2a43
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54658285"
---
# <a name="specifying-an-entry-point"></a>Angeben eines Einstiegspunktes
Ein Einstiegspunkt identifiziert die Position einer Funktion in einer DLL. In einem verwalteten Projekt wird diese Funktion vom ursprünglichen Namen oder vom Ordinaleinstiegspunkt einer Zielfunktion über die Grenzen der Interoperation hinaus identifiziert. Außerdem können Sie dem Einstiegspunkt einen anderen Namen zuordnen und damit die Funktion umbenennen.  
  
 Aus folgenden Gründen kann es sinnvoll sein, eine DLL-Funktion umzubenennen:  
  
-   Um keine API-Funktionsnamen zu verwenden, die zwischen Groß- und Kleinschreibung unterscheiden.  
  
-   Um die Konventionen vorhandener Namensstandards einzuhalten.  
  
-   Um Funktionen aufzunehmen, die verschiedene Datentypen verwenden (indem mehrere Versionen derselben DLL-Funktion deklariert werden).  
  
-   Um die Verwendung von APIs zu vereinfachen, die ANSI- und Unicode-Versionen enthalten.  
  
 In diesem Abschnitt wird das Umbenennen einer DLL-Funktion in verwaltetem Code veranschaulicht.  
  
## <a name="renaming-a-function-in-visual-basic"></a>Umbenennen einer Funktion in Visual Basic  
 Visual Basic verwendet das **Function**-Schlüsselwort in der **Declare**-Anweisung, um das<xref:System.Runtime.InteropServices.DllImportAttribute.EntryPoint?displayProperty=nameWithType>-Feld festzulegen. Das folgende Beispiel zeigt eine Basisdeklaration.  
  
```vb  
Imports System.Runtime.InteropServices  
  
Public Class Win32  
    Declare Auto Function MessageBox Lib "user32.dll" _  
       (ByVal hWnd As Integer, ByVal txt As String,_  
       ByVal caption As String, ByVal Typ As Integer) As Integer  
End Class  
```  
  
 Sie können den **MessageBox**-Einstiegspunkt durch **MsgBox** ersetzen, indem Sie das **Alias**-Schlüsselwort wie im folgenden Beispiel dargestellt in die Definition aufnehmen. In beiden Beispielen erübrigt sich aufgrund des **Auto**-Schlüsselwortes die Angabe der Zeichensatzversion des Einstiegspunktes. Weitere Informationen zum Auswählen eines Zeichensatzes finden Sie unter [Angeben eines Zeichensatzes](../../../docs/framework/interop/specifying-a-character-set.md).  
  
```vb  
Imports System.Runtime.InteropServices  
  
Public Class Win32  
    Declare Auto Function MsgBox Lib "user32.dll" _  
       Alias "MessageBox" (ByVal hWnd As Integer, ByVal txt As String,_  
       ByVal caption As String, ByVal Typ As Integer) As Integer  
End Class  
```  
  
## <a name="renaming-a-function-in-c-and-c"></a>Umbenennen einer Funktion in C# und C++  
 Sie können das <xref:System.Runtime.InteropServices.DllImportAttribute.EntryPoint?displayProperty=nameWithType>-Feld verwenden, um eine DLL-Funktion nach Name oder Ordinalzahl anzugeben. Wenn der Name der Funktion in der Methodendefinition mit dem Einstiegspunkt in der DLL übereinstimmt, müssen Sie die Funktion nicht explizit mit dem **EntryPoint**-Feld identifizieren. Andernfalls verwenden Sie eine der folgenden Attributformen zur Angabe eines Namens oder einer Ordinalzahl:  
  
```  
[DllImport("dllname", EntryPoint="Functionname")]  
[DllImport("dllname", EntryPoint="#123")]  
```  
  
 Hinweis: Für eine Ordinalzahl müssen Sie das Pfundzeichen (#) als Präfix verwenden.  
  
 Im folgenden Beispiel wird veranschaulicht, wie Sie im Code **MessageBoxA** mit **MsgBox** ersetzen, indem Sie das **EntryPoint**-Feld verwenden.  
  
```csharp  
using System.Runtime.InteropServices;  
  
public class Win32 {  
    [DllImport("user32.dll", EntryPoint="MessageBoxA")]  
    public static extern int MsgBox(int hWnd, String text, String caption,  
                                    uint type);  
}  
```  
  
```cpp  
using namespace System::Runtime::InteropServices;  
  
typedef void* HWND;  
[DllImport("user32", EntryPoint="MessageBoxA")]  
extern "C" int MsgBox(HWND hWnd,  
                      String*  pText,  
                      String*  pCaption,  
                      unsigned int uType);  
```  
  
## <a name="see-also"></a>Siehe auch
- <xref:System.Runtime.InteropServices.DllImportAttribute>
- [Creating Prototypes in Managed Code (Erstellen von Prototypen in verwaltetem Code)](../../../docs/framework/interop/creating-prototypes-in-managed-code.md)
- [Beispiele für Plattformaufrufe](../../../docs/framework/interop/platform-invoke-examples.md)
- [Marshallen von Daten mit Plattformaufruf](../../../docs/framework/interop/marshaling-data-with-platform-invoke.md)
