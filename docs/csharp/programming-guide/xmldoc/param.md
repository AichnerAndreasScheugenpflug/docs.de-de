---
title: <param> – C#-Programmierhandbuch
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- param
- <param>
helpviewer_keywords:
- <param> C# XML tag
- param C# XML tag
ms.assetid: 46d329b1-5b84-4537-9e17-73ca97313e4e
ms.openlocfilehash: 3f1099da6a43ed7f48389a16e3be6a3b6b98a148
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271576"
---
# <a name="param-c-programming-guide"></a><span data-ttu-id="e239a-102">\<param> (C#-Programmierhandbuch)</span><span class="sxs-lookup"><span data-stu-id="e239a-102">\<param> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="e239a-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="e239a-103">Syntax</span></span>  
  
```xml  
<param name="name">description</param>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e239a-104">Parameter</span><span class="sxs-lookup"><span data-stu-id="e239a-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="e239a-105">Der Name eines Methodenparameters.</span><span class="sxs-lookup"><span data-stu-id="e239a-105">The name of a method parameter.</span></span> <span data-ttu-id="e239a-106">Setzen Sie den Namen in doppelte Anführungszeichen (" ").</span><span class="sxs-lookup"><span data-stu-id="e239a-106">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="e239a-107">Eine Beschreibung für den Parameter</span><span class="sxs-lookup"><span data-stu-id="e239a-107">A description for the parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e239a-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e239a-108">Remarks</span></span>  
 <span data-ttu-id="e239a-109">Das \<param>-Tag sollte im Kommentar für eine Methodendeklaration verwendet werden, um einen der Methodenparameter zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e239a-109">The \<param> tag should be used in the comment for a method declaration to describe one of the parameters for the method.</span></span> <span data-ttu-id="e239a-110">Um mehrere Parameter zu dokumentieren, verwenden Sie mehrere \<param>-Tags.</span><span class="sxs-lookup"><span data-stu-id="e239a-110">To document multiple parameters, use multiple \<param> tags.</span></span>  
  
 <span data-ttu-id="e239a-111">Der Text für den \<param>-Tag wird in IntelliSense, dem Objektkatalog, und im Webbericht für Codekommentare angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e239a-111">The text for the \<param> tag will be displayed in IntelliSense, the Object Browser, and in the Code Comment Web Report.</span></span>  
  
 <span data-ttu-id="e239a-112">Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="e239a-112">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e239a-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e239a-113">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#1](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/param_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="e239a-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e239a-114">See also</span></span>

- [<span data-ttu-id="e239a-115">C#-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="e239a-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="e239a-116">Empfohlene Tags für Dokumentationskommentare</span><span class="sxs-lookup"><span data-stu-id="e239a-116">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
