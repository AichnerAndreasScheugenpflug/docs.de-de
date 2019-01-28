---
title: -codepage (C#-Compileroptionen)
ms.date: 07/20/2015
f1_keywords:
- /codepage
helpviewer_keywords:
- /codepage compiler option [C#]
- codepage compiler option [C#]
- -codepage compiler option [C#]
ms.assetid: 75942989-b69a-4308-90a0-840c73d2c478
ms.openlocfilehash: 7cbd3ec1b2d134106c6c9429341f5603444dac27
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54693979"
---
# <a name="-codepage-c-compiler-options"></a><span data-ttu-id="1d7aa-102">-codepage (C#-Compileroptionen)</span><span class="sxs-lookup"><span data-stu-id="1d7aa-102">-codepage (C# Compiler Options)</span></span>
<span data-ttu-id="1d7aa-103">Diese Option gibt an, welche Codepage beim Kompilieren verwendet werden soll, wenn die erforderliche Seite nicht die aktuelle Standardcodepage für das System ist.</span><span class="sxs-lookup"><span data-stu-id="1d7aa-103">This option specifies which codepage to use during compilation if the required page is not the current default codepage for the system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1d7aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d7aa-104">Syntax</span></span>  
  
```console  
-codepage:id  
```  
  
## <a name="arguments"></a><span data-ttu-id="1d7aa-105">Argumente</span><span class="sxs-lookup"><span data-stu-id="1d7aa-105">Arguments</span></span>  
 `id`  
 <span data-ttu-id="1d7aa-106">Die ID der Codepage, die für alle Quellcodedateien in der Kompilierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d7aa-106">The id of the code page to use for all source code files in the compilation.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1d7aa-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1d7aa-107">Remarks</span></span>  
 <span data-ttu-id="1d7aa-108">Wenn Sie eine oder mehrere Quellcodedateien kompilieren, für die beim Erstellen nicht die Verwendung der Standardcodepage auf dem Computer festgelegt wurde, können Sie die Option **-codepage** verwenden, um anzugeben, welche Codepage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d7aa-108">If you compile one or more source code files that were not created to use the default code page on your computer, you can use the **-codepage** option to specify which code page should be used.</span></span> <span data-ttu-id="1d7aa-109">**-codepage** wirkt sich auf alle bei der Kompilierung verwendeten Quellcodedateien aus.</span><span class="sxs-lookup"><span data-stu-id="1d7aa-109">**-codepage** applies to all source code files in your compilation.</span></span>  
  
 <span data-ttu-id="1d7aa-110">Wenn die Quellcodedateien mit der auf dem Computer aktivierten Codepage oder mit UNICODE bzw. UTF-8 erstellt wurden, müssen Sie **-codepage** nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d7aa-110">If the source code files were created with the same codepage that is in effect on your computer or if the source code files were created with UNICODE or UTF-8, you need not use **-codepage**.</span></span>  
  
 <span data-ttu-id="1d7aa-111">Weitere Informationen darüber, wie ermittelt wird, welche Codeseiten auf dem System unterstützt werden, finden Sie unter [GetCPInfo](/windows/desktop/api/winnls/nf-winnls-getcpinfo).</span><span class="sxs-lookup"><span data-stu-id="1d7aa-111">See [GetCPInfo](/windows/desktop/api/winnls/nf-winnls-getcpinfo) for information on how to find which code pages are supported on your system.</span></span>  
  
 <span data-ttu-id="1d7aa-112">Diese Compileroption steht in Visual Studio nicht zur Verfügung und kann auch nicht programmgesteuert angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="1d7aa-112">This compiler option is unavailable in Visual Studio and cannot be changed programmatically.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d7aa-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d7aa-113">See also</span></span>

- [<span data-ttu-id="1d7aa-114">C#-Compileroptionen</span><span class="sxs-lookup"><span data-stu-id="1d7aa-114">C# Compiler Options</span></span>](../../../csharp/language-reference/compiler-options/index.md)
- [<span data-ttu-id="1d7aa-115">Verwalten von Projekt- und Projektmappeneigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d7aa-115">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
