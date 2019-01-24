---
title: 'Generika – C#-Programmierhandbuch'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
  - 'C# language, generics'
  - 'generics [C#]'
ms.assetid: 75ea8509-a4ea-4e7a-a2b3-cf72482e9282
---
# <a name="generics-c-programming-guide"></a><span data-ttu-id="c6b1c-102">Generika (C#-Programmierhandbuch)</span><span class="sxs-lookup"><span data-stu-id="c6b1c-102">Generics (C# Programming Guide)</span></span>
<span data-ttu-id="c6b1c-103">Generika wurden zur Version 2.0 der Sprache C# und der Common Language Runtime (CLR) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c6b1c-103">Generics were added to version 2.0 of the C# language and the common language runtime (CLR).</span></span> <span data-ttu-id="c6b1c-104">Generika führen in .NET Framework das Konzept der Typparameter ein, wodurch Sie Klassen und Methoden entwerfen können, die die Spezialisierung einer oder mehr Typen verzögern können, bis die Klasse oder Methode vom Clientcode deklariert und instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="c6b1c-104">Generics introduce to the .NET Framework the concept of type parameters, which make it possible to design classes and methods that defer the specification of one or more types until the class or method is declared and instantiated by client code.</span></span> <span data-ttu-id="c6b1c-105">Indem Sie z.B. einen generischen Parameter „T“ verwenden, können Sie eine einzelne Klasse schreiben, die anderer Clientcode verwenden kann, ohne die Kosten und Risiken von Umwandlungen zur Laufzeit oder Boxingvorgängen einzugehen, wie folgendermaßen gezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="c6b1c-105">For example, by using a generic type parameter T you can write a single class that other client code can use without incurring the cost or risk of runtime casts or boxing operations, as shown here:</span></span>  
  
 [!code-csharp[csProgGuideGenerics#1](../../../csharp/programming-guide/generics/codesnippet/CSharp/index_1.cs)]  
  
## <a name="generics-overview"></a><span data-ttu-id="c6b1c-106">Übersicht über Generika</span><span class="sxs-lookup"><span data-stu-id="c6b1c-106">Generics Overview</span></span>  
  
-   <span data-ttu-id="c6b1c-107">Verwenden Sie Generika, um die Wiederverwendung von Code, Typsicherheit und Leistung zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="c6b1c-107">Use generic types to maximize code reuse, type safety, and performance.</span></span>  
  
-   <span data-ttu-id="c6b1c-108">Generika werden am häufigsten zur Erstellung von Auflistungsklassen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6b1c-108">The most common use of generics is to create collection classes.</span></span>  
  
-   <span data-ttu-id="c6b1c-109">Die Klassenbibliothek von .NET Framework enthält eine Reihe generischer Auflistungsklassen im <xref:System.Collections.Generic>-Namespace.</span><span class="sxs-lookup"><span data-stu-id="c6b1c-109">The .NET Framework class library contains several new generic collection classes in the <xref:System.Collections.Generic> namespace.</span></span> <span data-ttu-id="c6b1c-110">Diese sollten wenn möglich anstatt Klassen wie z.B. <xref:System.Collections.ArrayList> im <xref:System.Collections>-Namespace verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6b1c-110">These should be used whenever possible instead of classes such as <xref:System.Collections.ArrayList> in the <xref:System.Collections> namespace.</span></span>  
  
-   <span data-ttu-id="c6b1c-111">Sie können Ihre eigenen generischen Schnittstellen, Klassen, Methoden, Ereignisse und Delegaten erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6b1c-111">You can create your own generic interfaces, classes, methods, events and delegates.</span></span>  
  
-   <span data-ttu-id="c6b1c-112">Generische Klassen sind womöglich in der Aktivierung des Zugriffs auf Methoden für bestimmte Datentypen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="c6b1c-112">Generic classes may be constrained to enable access to methods on particular data types.</span></span>  
  
-   <span data-ttu-id="c6b1c-113">Informationen zu den Typen, die in einem generischen Datentyp verwendet werden, können zur Laufzeit unter Verwendung von Reflektion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c6b1c-113">Information on the types that are used in a generic data type may be obtained at run-time by using reflection.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="c6b1c-114">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="c6b1c-114">Related Sections</span></span>  
 <span data-ttu-id="c6b1c-115">Weitere Informationen finden Sie unter: </span><span class="sxs-lookup"><span data-stu-id="c6b1c-115">For more information:</span></span>  
  
-   [<span data-ttu-id="c6b1c-116">Einführung in Generika</span><span class="sxs-lookup"><span data-stu-id="c6b1c-116">Introduction to Generics</span></span>](../../../csharp/programming-guide/generics/introduction-to-generics.md)  
  
-   [<span data-ttu-id="c6b1c-117">Vorteile von Generika</span><span class="sxs-lookup"><span data-stu-id="c6b1c-117">Benefits of Generics</span></span>](../../../csharp/programming-guide/generics/benefits-of-generics.md)  
  
-   [<span data-ttu-id="c6b1c-118">Generische Typparameter</span><span class="sxs-lookup"><span data-stu-id="c6b1c-118">Generic Type Parameters</span></span>](../../../csharp/programming-guide/generics/generic-type-parameters.md)  
  
-   [<span data-ttu-id="c6b1c-119">Einschränkungen für Typparameter</span><span class="sxs-lookup"><span data-stu-id="c6b1c-119">Constraints on Type Parameters</span></span>](../../../csharp/programming-guide/generics/constraints-on-type-parameters.md)  
  
-   [<span data-ttu-id="c6b1c-120">Generische Klassen</span><span class="sxs-lookup"><span data-stu-id="c6b1c-120">Generic Classes</span></span>](../../../csharp/programming-guide/generics/generic-classes.md)  
  
-   [<span data-ttu-id="c6b1c-121">Generische Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c6b1c-121">Generic Interfaces</span></span>](../../../csharp/programming-guide/generics/generic-interfaces.md)  
  
-   [<span data-ttu-id="c6b1c-122">Generische Methoden</span><span class="sxs-lookup"><span data-stu-id="c6b1c-122">Generic Methods</span></span>](../../../csharp/programming-guide/generics/generic-methods.md)  
  
-   [<span data-ttu-id="c6b1c-123">Generische Delegate</span><span class="sxs-lookup"><span data-stu-id="c6b1c-123">Generic Delegates</span></span>](../../../csharp/programming-guide/generics/generic-delegates.md)  
  
-   [<span data-ttu-id="c6b1c-124">Unterschiede zwischen C++-Vorlagen und C#-Generika</span><span class="sxs-lookup"><span data-stu-id="c6b1c-124">Differences Between C++ Templates and C# Generics</span></span>](../../../csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics.md)  
  
-   [<span data-ttu-id="c6b1c-125">Generika und Reflexion</span><span class="sxs-lookup"><span data-stu-id="c6b1c-125">Generics and Reflection</span></span>](../../../csharp/programming-guide/generics/generics-and-reflection.md)  
  
-   [<span data-ttu-id="c6b1c-126">Generika zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="c6b1c-126">Generics in the Run Time</span></span>](../../../csharp/programming-guide/generics/generics-in-the-run-time.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="c6b1c-127">C#-Programmiersprachenspezifikation</span><span class="sxs-lookup"><span data-stu-id="c6b1c-127">C# Language Specification</span></span>  
 <span data-ttu-id="c6b1c-128">Weitere Informationen erhalten Sie unter [C#-Sprachspezifikation](~/_csharplang/spec/types.md#constructed-types).</span><span class="sxs-lookup"><span data-stu-id="c6b1c-128">For more information, see the [C# Language Specification](~/_csharplang/spec/types.md#constructed-types).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6b1c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6b1c-129">See also</span></span>

- <xref:System.Collections.Generic>
- [<span data-ttu-id="c6b1c-130">C#-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="c6b1c-130">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="c6b1c-131">Typen</span><span class="sxs-lookup"><span data-stu-id="c6b1c-131">Types</span></span>](../../../csharp/programming-guide/types/index.md)
- [<span data-ttu-id="c6b1c-132">\<typeparam></span><span class="sxs-lookup"><span data-stu-id="c6b1c-132">\<typeparam></span></span>](../../../csharp/programming-guide/xmldoc/typeparam.md)
- [<span data-ttu-id="c6b1c-133">\<typeparamref></span><span class="sxs-lookup"><span data-stu-id="c6b1c-133">\<typeparamref></span></span>](../../../csharp/programming-guide/xmldoc/typeparamref.md)
- [<span data-ttu-id="c6b1c-134">Generika in .NET</span><span class="sxs-lookup"><span data-stu-id="c6b1c-134">Generics in .NET</span></span>](../../../standard/generics/index.md)
