---
title: '&lt;exception&gt; – C#-Programmierhandbuch'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- exception
- <exception>
helpviewer_keywords:
- <exception> C# XML tag
- exception C# XML tag
ms.assetid: dd73aac5-3c74-4fcf-9498-f11bff3a2f3c
ms.openlocfilehash: 1d48d9c05e23154ee98d077af5f43c80b4dbe2fe
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54588110"
---
# <a name="ltexceptiongt-c-programming-guide"></a><span data-ttu-id="2c824-102">&lt;exception&gt; (C#-Programmierhandbuch)</span><span class="sxs-lookup"><span data-stu-id="2c824-102">&lt;exception&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="2c824-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c824-103">Syntax</span></span>  
  
```xml  
<exception cref="member">description</exception>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2c824-104">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c824-104">Parameters</span></span>  
 <span data-ttu-id="2c824-105">cref = " `member`"</span><span class="sxs-lookup"><span data-stu-id="2c824-105">cref = " `member`"</span></span>  
 <span data-ttu-id="2c824-106">Ein Verweis auf eine Ausnahme, die von der aktuellen Kompilierungsumgebung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2c824-106">A reference to an exception that is available from the current compilation environment.</span></span> <span data-ttu-id="2c824-107">Der Compiler prüft, ob die angegebene Ausnahme vorhanden ist, und übersetzt in der Ausgabe-XML `member` in den kanonischen Elementnamen.</span><span class="sxs-lookup"><span data-stu-id="2c824-107">The compiler checks that the given exception exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="2c824-108">`member` muss in doppelte Anführungszeichen (" ") gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="2c824-108">`member` must appear within double quotation marks (" ").</span></span>  
  
 <span data-ttu-id="2c824-109">Weitere Informationen zum Erstellen von cref-Verweisen auf einen generischen Typ finden Sie unter [\<see](../../../csharp/programming-guide/xmldoc/see.md).</span><span class="sxs-lookup"><span data-stu-id="2c824-109">For more information on how to create a cref reference to a generic type, see [\<see>](../../../csharp/programming-guide/xmldoc/see.md).</span></span>  
  
 `description`  
 <span data-ttu-id="2c824-110">Eine Beschreibung der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="2c824-110">A description of the exception.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2c824-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c824-111">Remarks</span></span>  
 <span data-ttu-id="2c824-112">Mit dem Tag \<exception> können Sie angeben, welche Ausnahmen ausgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="2c824-112">The \<exception> tag lets you specify which exceptions can be thrown.</span></span> <span data-ttu-id="2c824-113">Dieses Tag kann für Definitionen für Methoden, Eigenschaften, Ereignisse und Indexer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c824-113">This tag can be applied to definitions for methods, properties, events, and indexers.</span></span>  
  
 <span data-ttu-id="2c824-114">Dokumentationskommentare werden zu einer Datei verarbeitet, indem sie mit [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="2c824-114">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
 <span data-ttu-id="2c824-115">Weitere Informationen zur Behandlung von Ausnahmen finden Sie unter [Ausnahmen und Ausnahmebehandlung](../../../csharp/programming-guide/exceptions/index.md).</span><span class="sxs-lookup"><span data-stu-id="2c824-115">For more information about exception handling, see [Exceptions and Exception Handling](../../../csharp/programming-guide/exceptions/index.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2c824-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2c824-116">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#4](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/exception_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="2c824-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c824-117">See also</span></span>

- [<span data-ttu-id="2c824-118">C#-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="2c824-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="2c824-119">Empfohlene Tags für Dokumentationskommentare</span><span class="sxs-lookup"><span data-stu-id="2c824-119">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
