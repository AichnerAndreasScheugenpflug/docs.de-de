---
title: Namen von Typmembern
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- events [.NET Framework], names
- methods [.NET Framework], names
- type members
- properties [.NET Framework], names
- fields, names
- field names
- names [.NET Framework], type members
- members [.NET Framework], type
ms.assetid: af5a0903-36af-4c2a-b848-cf959affeaa5
author: KrzysztofCwalina
ms.openlocfilehash: 7cf98b8ed1957352f357c7a9d580b4fd567a1634
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54576940"
---
# <a name="names-of-type-members"></a><span data-ttu-id="97738-102">Namen von Typmembern</span><span class="sxs-lookup"><span data-stu-id="97738-102">Names of Type Members</span></span>
<span data-ttu-id="97738-103">Typen bestehen aus Membern: Methoden, Eigenschaften, Ereignisse, Konstruktoren und Felder.</span><span class="sxs-lookup"><span data-stu-id="97738-103">Types are made of members: methods, properties, events, constructors, and fields.</span></span> <span data-ttu-id="97738-104">In den folgenden Abschnitten werden die Richtlinien zum Benennen von Typmembern beschrieben.</span><span class="sxs-lookup"><span data-stu-id="97738-104">The following sections describe guidelines for naming type members.</span></span>  
  
## <a name="names-of-methods"></a><span data-ttu-id="97738-105">Namen von Methoden</span><span class="sxs-lookup"><span data-stu-id="97738-105">Names of Methods</span></span>  
 <span data-ttu-id="97738-106">Da Methoden das Ausführen von Aktionen ermöglichen, erfordern die Entwurfsrichtlinien, dass Methodennamen Verben oder Verbalphrasen sind.</span><span class="sxs-lookup"><span data-stu-id="97738-106">Because methods are the means of taking action, the design guidelines require that method names be verbs or verb phrases.</span></span> <span data-ttu-id="97738-107">Mit dieser Richtlinie ist es auch möglich, Methodennamen von Eigenschafts- und Typnamen zu unterscheiden, die Nominal- oder Adjektivphrasen sind.</span><span class="sxs-lookup"><span data-stu-id="97738-107">Following this guideline also serves to distinguish method names from property and type names, which are noun or adjective phrases.</span></span>  
  
 <span data-ttu-id="97738-108">**✓ DO**: Geben Sie Methodennamen an, die Verben oder Verbalphrasen sind.</span><span class="sxs-lookup"><span data-stu-id="97738-108">**✓ DO** give methods names that are verbs or verb phrases.</span></span>  
  
```  
public class String {  
    public int CompareTo(...);  
    public string[] Split(...);  
    public string Trim();  
}  
```  
  
## <a name="names-of-properties"></a><span data-ttu-id="97738-109">Namen von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="97738-109">Names of Properties</span></span>  
 <span data-ttu-id="97738-110">Anders als andere Member sollten Eigenschaften mit Substantivphrasen oder Adjektivnamen benannt werden.</span><span class="sxs-lookup"><span data-stu-id="97738-110">Unlike other members, properties should be given noun phrase or adjective names.</span></span> <span data-ttu-id="97738-111">Das liegt daran, dass eine Eigenschaft auf Daten verweist, und der Name der Eigenschaft gibt dies wieder.</span><span class="sxs-lookup"><span data-stu-id="97738-111">That is because a property refers to data, and the name of the property reflects that.</span></span> <span data-ttu-id="97738-112">Für Eigenschaftsnamen wird immer PascalCasing verwendet.</span><span class="sxs-lookup"><span data-stu-id="97738-112">PascalCasing is always used for property names.</span></span>  
  
 <span data-ttu-id="97738-113">**✓ DO**: Benennen Sie Eigenschaften mit einem Nomen, einer Nominalphrase oder einem Adjektiv.</span><span class="sxs-lookup"><span data-stu-id="97738-113">**✓ DO** name properties using a noun, noun phrase, or adjective.</span></span>  
  
 <span data-ttu-id="97738-114">**X DO NOT**: Nutzen Sie keine Eigenschaften, die mit dem Namen von „Get“-Methoden übereinstimmen, so wie in folgendem Beispiel dargestellt:</span><span class="sxs-lookup"><span data-stu-id="97738-114">**X DO NOT** have properties that match the name of "Get" methods as in the following example:</span></span>  
  
 `public string TextWriter { get {...} set {...} }`  
 `public string GetTextWriter(int value) { ... }`  
  
 <span data-ttu-id="97738-115">Dieses Muster gibt normalerweise an, dass die Eigenschaft eigentlich eine Methode sein soll.</span><span class="sxs-lookup"><span data-stu-id="97738-115">This pattern typically indicates that the property should really be a method.</span></span>  
  
 <span data-ttu-id="97738-116">**✓ DO**: Benennen Sie Sammlungseigenschaften mit einer Phrase im Plural, mit dem die Elemente in der Sammlung beschrieben werden, anstatt mit einer Phrase im Singular, gefolgt von „List“ oder „Collection“.</span><span class="sxs-lookup"><span data-stu-id="97738-116">**✓ DO** name collection properties with a plural phrase describing the items in the collection instead of using a singular phrase followed by "List" or "Collection."</span></span>  
  
 <span data-ttu-id="97738-117">**✓ DO**: Benennen Sie boolesche Eigenschaften mit einem positiven Ausdruck (`CanSeek` anstelle von `CantSeek`).</span><span class="sxs-lookup"><span data-stu-id="97738-117">**✓ DO** name Boolean properties with an affirmative phrase (`CanSeek` instead of `CantSeek`).</span></span> <span data-ttu-id="97738-118">Optional können Sie auch booleschen Eigenschaften „Is,“, „Can,“ oder „Has,“ voranstellen, jedoch nur, wo es Sinn ergibt.</span><span class="sxs-lookup"><span data-stu-id="97738-118">Optionally, you can also prefix Boolean properties with "Is," "Can," or "Has," but only where it adds value.</span></span>  
  
 <span data-ttu-id="97738-119">**✓ CONSIDER**: Ziehen Sie in Betracht, einer Eigenschaft den gleichen Namen wie ihrem Typ zu geben.</span><span class="sxs-lookup"><span data-stu-id="97738-119">**✓ CONSIDER** giving a property the same name as its type.</span></span>  
  
 <span data-ttu-id="97738-120">Die folgende Eigenschaft ruft ordnungsgemäß einen Enumerationswert namens `Color` ab und legt ihn fest. Die Eigenschaft heißt also `Color`:</span><span class="sxs-lookup"><span data-stu-id="97738-120">For example, the following property correctly gets and sets an enum value named `Color`, so the property is named `Color`:</span></span>  
  
```  
public enum Color {...}  
public class Control {  
    public Color Color { get {...} set {...} }  
}  
```  
  
## <a name="names-of-events"></a><span data-ttu-id="97738-121">Namen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="97738-121">Names of Events</span></span>  
 <span data-ttu-id="97738-122">Ereignisse beziehen sich immer auf Aktionen, also entweder auf eine Aktion, die gerade passiert oder eine, die in der Vergangenheit liegt.</span><span class="sxs-lookup"><span data-stu-id="97738-122">Events always refer to some action, either one that is happening or one that has occurred.</span></span> <span data-ttu-id="97738-123">Deshalb werden Ereignisse mit Verben benannt (wie Methoden auch), und die Verbkonjugation wird genutzt, um den Zeitpunkt anzugeben, wann das Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="97738-123">Therefore, as with methods, events are named with verbs, and verb tense is used to indicate the time when the event is raised.</span></span>  
  
 <span data-ttu-id="97738-124">**✓ DO**: Benennen Sie Ereignisse mit einem Verb oder einer Verbalphrase.</span><span class="sxs-lookup"><span data-stu-id="97738-124">**✓ DO** name events with a verb or a verb phrase.</span></span>  
  
 <span data-ttu-id="97738-125">Beispiele dafür sind `Clicked`, `Painting`, `DroppedDown` usw.</span><span class="sxs-lookup"><span data-stu-id="97738-125">Examples include `Clicked`, `Painting`, `DroppedDown`, and so on.</span></span>  
  
 <span data-ttu-id="97738-126">**✓ DO**: Geben Sie Ereignissen Namen, die sich auf Vergangenheit und Zukunft beziehen. Verwenden Sie dazu Gegenwarts- und Vergangenheitsformen.</span><span class="sxs-lookup"><span data-stu-id="97738-126">**✓ DO** give events names with a concept of before and after, using the present and past tenses.</span></span>  
  
 <span data-ttu-id="97738-127">Beispielsweise wird ein Schließereignis, das ausgelöst wird, bevor ein Fenster geschlossen wird, als `Closing` bezeichnet. Ein Ereignis, das nach dem Schließen des Fensters ausgelöst wird, wird als `Closed` bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="97738-127">For example, a close event that is raised before a window is closed would be called `Closing`, and one that is raised after the window is closed would be called `Closed`.</span></span>  
  
 <span data-ttu-id="97738-128">**X DO NOT**: Verwenden Sie keine „Before“- und „After“-Präfixe und -Postfixe, um eine Aktion vor oder nach Ereignissen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="97738-128">**X DO NOT** use "Before" or "After" prefixes or postfixes to indicate pre- and post-events.</span></span> <span data-ttu-id="97738-129">Verwenden Sie wie oben beschrieben die Gegenwarts- und Vergangenheitsformen.</span><span class="sxs-lookup"><span data-stu-id="97738-129">Use present and past tenses as just described.</span></span>  
  
 <span data-ttu-id="97738-130">**✓ DO**: Benennen Sie Ereignishandler (Delegaten, die als Typen von Ereignissen verwendet werden) mit dem Suffix „EventHandler“, wie in folgendem Beispiel dargestellt:</span><span class="sxs-lookup"><span data-stu-id="97738-130">**✓ DO** name event handlers (delegates used as types of events) with the "EventHandler" suffix, as shown in the following example:</span></span>  
  
 `public delegate void ClickedEventHandler(object sender, ClickedEventArgs e);`  
  
 <span data-ttu-id="97738-131">**✓ DO**: Verwenden Sie in Ereignishandlern zwei Parameter mit der Bezeichnung `sender` und `e`.</span><span class="sxs-lookup"><span data-stu-id="97738-131">**✓ DO** use two parameters named `sender` and `e` in event handlers.</span></span>  
  
 <span data-ttu-id="97738-132">Der sender-Parameter stellt das Objekt dar, das das Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="97738-132">The sender parameter represents the object that raised the event.</span></span> <span data-ttu-id="97738-133">Der sender-Parameter ist in der Regel vom Typ `object`, auch wenn es möglich ist, einen spezifischeren Typ zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="97738-133">The sender parameter is typically of type `object`, even if it is possible to employ a more specific type.</span></span>  
  
 <span data-ttu-id="97738-134">**✓ DO**: Benennen Sie Ereignisargumentklassen mit dem Suffix „EventArgs“.</span><span class="sxs-lookup"><span data-stu-id="97738-134">**✓ DO** name event argument classes with the "EventArgs" suffix.</span></span>  
  
## <a name="names-of-fields"></a><span data-ttu-id="97738-135">Feldnamen</span><span class="sxs-lookup"><span data-stu-id="97738-135">Names of Fields</span></span>  
 <span data-ttu-id="97738-136">Die Richtlinien für die Benennung von Feldern gelten für statische öffentliche und geschützte Felder.</span><span class="sxs-lookup"><span data-stu-id="97738-136">The field-naming guidelines apply to static public and protected fields.</span></span> <span data-ttu-id="97738-137">Interne und private Felder sind nicht Gegenstand von Richtlinien, und öffentliche oder geschützte Instanzfelder sind laut den [Entwurfsrichtlinien für Member](../../../docs/standard/design-guidelines/member.md) nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="97738-137">Internal and private fields are not covered by guidelines, and public or protected instance fields are not allowed by the [member design guidelines](../../../docs/standard/design-guidelines/member.md).</span></span>  
  
 <span data-ttu-id="97738-138">**✓ DO**: Verwenden Sie die Pascal-Schreibweise in Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="97738-138">**✓ DO** use PascalCasing in field names.</span></span>  
  
 <span data-ttu-id="97738-139">**✓ DO**: Benennen Sie Felder mit einem Nomen, einer Nominalphrase oder einem Adjektiv.</span><span class="sxs-lookup"><span data-stu-id="97738-139">**✓ DO** name fields using a noun, noun phrase, or adjective.</span></span>  
  
 <span data-ttu-id="97738-140">**X DO NOT**: Verwenden Sie kein Präfix für Feldnamen.</span><span class="sxs-lookup"><span data-stu-id="97738-140">**X DO NOT** use a prefix for field names.</span></span>  
  
 <span data-ttu-id="97738-141">Verwenden Sie beispielsweise nicht „g_“ oder „s_“, um statische Felder anzugeben.</span><span class="sxs-lookup"><span data-stu-id="97738-141">For example, do not use "g_" or "s_" to indicate static fields.</span></span>  
  
 <span data-ttu-id="97738-142">*Teile ©2005, 2009 Microsoft Corporation. Alle Rechte vorbehalten.*</span><span class="sxs-lookup"><span data-stu-id="97738-142">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="97738-143">*Pearson Education, Inc. über Rechte vorbehalten [Framework-Entwurfsrichtlinien vorgestellt: Aufrufkonventionen, Ausdrücke und Muster für die Wiederverwendbare Bibliotheken für .NET, 2. Auflage](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina und Brad Abrams, 22. Oktober 2008 von Addison-Wesley Professional als Teil der Microsoft Windows Development-Reihe veröffentlicht.*</span><span class="sxs-lookup"><span data-stu-id="97738-143">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97738-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97738-144">See also</span></span>

- [<span data-ttu-id="97738-145">Frameworkentwurfsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="97738-145">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)
- [<span data-ttu-id="97738-146">Richtlinien für die Benennung</span><span class="sxs-lookup"><span data-stu-id="97738-146">Naming Guidelines</span></span>](../../../docs/standard/design-guidelines/naming-guidelines.md)
