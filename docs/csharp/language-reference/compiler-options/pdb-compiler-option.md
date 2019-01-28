---
title: -pdb (C#-Compileroptionen)
ms.date: 07/20/2015
f1_keywords:
- /pdb
helpviewer_keywords:
- -pdb compiler option [C#]
- pdb compiler option [C#]
- /pdb compiler option [C#]
ms.assetid: e9d0f96a-5b75-45d6-9765-92538dd5f823
ms.openlocfilehash: b0a566931ac76a3adb191f423a497bc446e280c8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54575501"
---
# <a name="-pdb-c-compiler-options"></a><span data-ttu-id="c3fa2-102">-pdb (C#-Compileroptionen)</span><span class="sxs-lookup"><span data-stu-id="c3fa2-102">-pdb (C# Compiler Options)</span></span>
<span data-ttu-id="c3fa2-103">Die Compileroption **-pdb** gibt den Namen und Speicherort der Debugsymboldatei an.</span><span class="sxs-lookup"><span data-stu-id="c3fa2-103">The **-pdb** compiler option specifies the name and location of the debug symbols file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c3fa2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3fa2-104">Syntax</span></span>  
  
```console  
-pdb:filename  
```  
  
## <a name="arguments"></a><span data-ttu-id="c3fa2-105">Argumente</span><span class="sxs-lookup"><span data-stu-id="c3fa2-105">Arguments</span></span>  
 `filename`  
 <span data-ttu-id="c3fa2-106">Der Name und Speicherort der Debugsymboldatei</span><span class="sxs-lookup"><span data-stu-id="c3fa2-106">The name and location of the debug symbols file.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c3fa2-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c3fa2-107">Remarks</span></span>  
 <span data-ttu-id="c3fa2-108">Wenn Sie [-debug (C#-Compileroptionen)](../../../csharp/language-reference/compiler-options/debug-compiler-option.md) angeben, erstellt der Compiler eine PDB-Datei im gleichen Verzeichnis, in dem der Compiler die Ausgabedatei (.exe oder .dll) mit einem Dateinamen erstellt, der mit dem Namen der Ausgabedatei identisch ist.</span><span class="sxs-lookup"><span data-stu-id="c3fa2-108">When you specify [-debug (C# Compiler Options)](../../../csharp/language-reference/compiler-options/debug-compiler-option.md), the compiler will create a .pdb file in the same directory where the compiler will create the output file (.exe or .dll) with a file name that is the same as the name of the output file.</span></span>  
  
 <span data-ttu-id="c3fa2-109">Mit **-pdb** können Sie einen Dateinamen und -speicherort für die PDB-Datei angeben, die nicht dem Standard entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c3fa2-109">**-pdb** allows you to specify a non-default file name and location for the .pdb file.</span></span>  
  
 <span data-ttu-id="c3fa2-110">Diese Compileroption kann weder in der Visual Studio-Entwicklungsumgebung festgelegt werden, noch kann sie programmgesteuert geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c3fa2-110">This compiler option cannot be set in the Visual Studio development environment, nor can it be changed programmatically.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c3fa2-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c3fa2-111">Example</span></span>  
 <span data-ttu-id="c3fa2-112">Kompilieren Sie `t.cs`, und erstellen Sie eine PDB-Datei mit dem Namen „tt.pdb“:</span><span class="sxs-lookup"><span data-stu-id="c3fa2-112">Compile `t.cs` and create a .pdb file called tt.pdb:</span></span>  
  
```console  
csc -debug -pdb:tt t.cs  
```  
  
## <a name="see-also"></a><span data-ttu-id="c3fa2-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3fa2-113">See also</span></span>

- [<span data-ttu-id="c3fa2-114">C#-Compileroptionen</span><span class="sxs-lookup"><span data-stu-id="c3fa2-114">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
- [<span data-ttu-id="c3fa2-115">Verwalten von Projekt- und Projektmappeneigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3fa2-115">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
