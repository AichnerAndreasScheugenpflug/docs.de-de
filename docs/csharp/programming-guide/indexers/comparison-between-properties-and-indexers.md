---
title: Vergleich zwischen Eigenschaften und Indexern – C#-Programmierhandbuch
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- properties [C#], vs. indexers
- indexers [C#], vs. properties
ms.assetid: 3358a89f-44a0-4a4d-bf8c-07237a90af39
ms.openlocfilehash: 41b27905edb8a0e00a6af5a4cce38988161326d0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54537724"
---
# <a name="comparison-between-properties-and-indexers-c-programming-guide"></a><span data-ttu-id="f38b8-102">Vergleich zwischen Eigenschaften und Indexern (C#-Programmierhandbuch)</span><span class="sxs-lookup"><span data-stu-id="f38b8-102">Comparison Between Properties and Indexers (C# Programming Guide)</span></span>
<span data-ttu-id="f38b8-103">Indexer sind wie Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f38b8-103">Indexers are like properties.</span></span> <span data-ttu-id="f38b8-104">Mit Ausnahme der in der folgenden Tabelle aufgeführten Unterschiede gelten alle für Eigenschaftenaccessoren definierten Regeln auch für Indexeraccessoren.</span><span class="sxs-lookup"><span data-stu-id="f38b8-104">Except for the differences shown in the following table, all the rules that are defined for property accessors apply to indexer accessors also.</span></span>  
  
|<span data-ttu-id="f38b8-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f38b8-105">Property</span></span>|<span data-ttu-id="f38b8-106">Indexer</span><span class="sxs-lookup"><span data-stu-id="f38b8-106">Indexer</span></span>|  
|--------------|-------------|  
|<span data-ttu-id="f38b8-107">Damit können Methoden wie allgemein zugängliche Datenmember aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f38b8-107">Allows methods to be called as if they were public data members.</span></span>|<span data-ttu-id="f38b8-108">Damit können Elemente einer internen Auflistung eines Objekts durch die Anwendung der Arraynotation auf das Objekt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f38b8-108">Allows elements of an internal collection of an object to be accessed by using array notation on the object itself.</span></span>|  
|<span data-ttu-id="f38b8-109">Der Zugriff erfolgt über einen einfachen Namen.</span><span class="sxs-lookup"><span data-stu-id="f38b8-109">Accessed through a simple name.</span></span>|<span data-ttu-id="f38b8-110">Der Zugriff erfolgt über einen Index.</span><span class="sxs-lookup"><span data-stu-id="f38b8-110">Accessed through an index.</span></span>|  
|<span data-ttu-id="f38b8-111">Kann ein statischer Member oder ein Instanzmember sein.</span><span class="sxs-lookup"><span data-stu-id="f38b8-111">Can be a static or an instance member.</span></span>|<span data-ttu-id="f38b8-112">Muss ein Instanzmember sein.</span><span class="sxs-lookup"><span data-stu-id="f38b8-112">Must be an instance member.</span></span>|  
|<span data-ttu-id="f38b8-113">Ein [get](../../../csharp/language-reference/keywords/get.md)-Accessor einer Eigenschaft weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="f38b8-113">A [get](../../../csharp/language-reference/keywords/get.md) accessor of a property has no parameters.</span></span>|<span data-ttu-id="f38b8-114">Ein `get`-Accessor eines Indexers hat dieselbe Liste formaler Parameter wie der Indexer.</span><span class="sxs-lookup"><span data-stu-id="f38b8-114">A `get` accessor of an indexer has the same formal parameter list as the indexer.</span></span>|  
|<span data-ttu-id="f38b8-115">Ein [set](../../../csharp/language-reference/keywords/set.md)-Accessor einer Eigenschaft enthält den impliziten `value`-Parameter.</span><span class="sxs-lookup"><span data-stu-id="f38b8-115">A [set](../../../csharp/language-reference/keywords/set.md) accessor of a property contains the implicit `value` parameter.</span></span>|<span data-ttu-id="f38b8-116">Ein `set`-Accessor eines Indexers enthält neben dem [value](../../../csharp/language-reference/keywords/value.md)-Parameter auch dieselbe Liste formaler Parameter wie der Indexer.</span><span class="sxs-lookup"><span data-stu-id="f38b8-116">A `set` accessor of an indexer has the same formal parameter list as the indexer, and also to the [value](../../../csharp/language-reference/keywords/value.md) parameter.</span></span>|  
|<span data-ttu-id="f38b8-117">Unterstützt Kurzsyntax mit [Auto-Implemented Properties (Automatisch implementierte Eigenschaften)](../../../csharp/programming-guide/classes-and-structs/auto-implemented-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f38b8-117">Supports shortened syntax with [Auto-Implemented Properties](../../../csharp/programming-guide/classes-and-structs/auto-implemented-properties.md).</span></span>|<span data-ttu-id="f38b8-118">Unterstützt keine Kurzsyntax.</span><span class="sxs-lookup"><span data-stu-id="f38b8-118">Does not support shortened syntax.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f38b8-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f38b8-119">See also</span></span>

- [<span data-ttu-id="f38b8-120">C#-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="f38b8-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="f38b8-121">Indexer</span><span class="sxs-lookup"><span data-stu-id="f38b8-121">Indexers</span></span>](../../../csharp/programming-guide/indexers/index.md)
- [<span data-ttu-id="f38b8-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f38b8-122">Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/properties.md)
