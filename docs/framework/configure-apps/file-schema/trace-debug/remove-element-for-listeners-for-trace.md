---
title: '&lt;Entfernen Sie&gt; -Element für &lt;Listener&gt; für &lt;Ablaufverfolgung&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners/remove
helpviewer_keywords:
- remove element
- <remove> element
ms.assetid: 9a5cd1b5-be1a-485f-8f0c-2890ad3ef3e0
author: mcleblanc
ms.author: markl
ms.openlocfilehash: d2e68a93840022776530bb9ed2f94a7505a8a3b6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642791"
---
# <a name="ltremovegt-element-for-ltlistenersgt-for-lttracegt"></a><span data-ttu-id="3c139-102">&lt;Entfernen Sie&gt; -Element für &lt;Listener&gt; für &lt;Ablaufverfolgung&gt;</span><span class="sxs-lookup"><span data-stu-id="3c139-102">&lt;remove&gt; Element for &lt;listeners&gt; for &lt;trace&gt;</span></span>
<span data-ttu-id="3c139-103">Entfernt einen Listener aus der **Listener** Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3c139-103">Removes a listener from the **Listeners** collection.</span></span>  
  
 <span data-ttu-id="3c139-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="3c139-104">\<configuration></span></span>  
<span data-ttu-id="3c139-105">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="3c139-105">\<system.diagnostics></span></span>  
<span data-ttu-id="3c139-106">\<trace></span><span class="sxs-lookup"><span data-stu-id="3c139-106">\<trace></span></span>  
<span data-ttu-id="3c139-107">\<listeners></span><span class="sxs-lookup"><span data-stu-id="3c139-107">\<listeners></span></span>  
<span data-ttu-id="3c139-108">\<remove></span><span class="sxs-lookup"><span data-stu-id="3c139-108">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c139-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c139-109">Syntax</span></span>  
  
```xml  
<remove name="listener name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3c139-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3c139-110">Attributes and Elements</span></span>  
 <span data-ttu-id="3c139-111">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3c139-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3c139-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c139-112">Attributes</span></span>  
  
|<span data-ttu-id="3c139-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="3c139-113">Attribute</span></span>|<span data-ttu-id="3c139-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c139-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3c139-115">**name**</span><span class="sxs-lookup"><span data-stu-id="3c139-115">**name**</span></span>|<span data-ttu-id="3c139-116">Erforderliches Attribut.</span><span class="sxs-lookup"><span data-stu-id="3c139-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="3c139-117">Der Name des Listeners, Aufheben der **Listener** Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3c139-117">The name of the listener to remove from the **Listeners** collection.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3c139-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c139-118">Child Elements</span></span>  
 <span data-ttu-id="3c139-119">Keine</span><span class="sxs-lookup"><span data-stu-id="3c139-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3c139-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c139-120">Parent Elements</span></span>  
  
|<span data-ttu-id="3c139-121">Element</span><span class="sxs-lookup"><span data-stu-id="3c139-121">Element</span></span>|<span data-ttu-id="3c139-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c139-122">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="3c139-123">Das Stammelement in jeder von den Common Language Runtime- und .NET Framework-Anwendungen verwendeten Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="3c139-123">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`listeners`|<span data-ttu-id="3c139-124">Gibt an, einen Listener, der sammelt, speichert, und leitet Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="3c139-124">Specifies a listener that collects, stores, and routes messages.</span></span> <span data-ttu-id="3c139-125">Listener leiten die Ablaufverfolgungsausgabe an ein entsprechendes Ziel.</span><span class="sxs-lookup"><span data-stu-id="3c139-125">Listeners direct the tracing output to an appropriate target.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="3c139-126">Gibt Ablaufverfolgungslistener an, die Meldungen sammeln, speichern und weiterleiten sowie die Ebene, für die ein Ablaufverfolgungsschalter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3c139-126">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`trace`|<span data-ttu-id="3c139-127">Konfiguriert den ASP.NET-Ablaufverfolgungsdienst.</span><span class="sxs-lookup"><span data-stu-id="3c139-127">Configures the ASP.NET trace service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3c139-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3c139-128">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3c139-129">Entfernen der <xref:System.Diagnostics.DefaultTraceListener> aus der `Listeners` Auflistung ändert das Sitzungsverhalten, sodass die <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType>, und <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType> Methoden.</span><span class="sxs-lookup"><span data-stu-id="3c139-129">Removing the <xref:System.Diagnostics.DefaultTraceListener> from the `Listeners` collection alters the behavior of the <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType>, and <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType> methods.</span></span> <span data-ttu-id="3c139-130">Aufrufen einer `Assert` oder `Fail` -Methode führt normalerweise in der Anzeige eines Meldungsfelds, aber das Feld nicht angezeigt wird der <xref:System.Diagnostics.DefaultTraceListener> befindet sich nicht in der `Listeners` Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3c139-130">Calling an `Assert` or `Fail` method normally results in the display of a message box, however the message box is not displayed if the <xref:System.Diagnostics.DefaultTraceListener> is not in the `Listeners` collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3c139-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3c139-131">Example</span></span>  
 <span data-ttu-id="3c139-132">Das folgende Beispiel zeigt, wie Sie den standardmäßigen Ablaufverfolgungslistener aus der Ablaufverfolgung entfernen **Listener** Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3c139-132">The following example shows how to remove the default trace listener from the trace **Listeners** collection.</span></span>  
  
```xml  
<configuration>  
   <system.diagnostics>  
      <trace autoflush="true" indentsize="0">  
         <listeners>  
            <remove name="Default" />  
         </listeners>  
      </trace>  
   </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="3c139-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c139-133">See also</span></span>
- <xref:System.Diagnostics.TraceListener>
- <xref:System.Diagnostics.DefaultTraceListener>
- <xref:System.Diagnostics.TextWriterTraceListener>
- <xref:System.Diagnostics.EventLogTraceListener>
- [<span data-ttu-id="3c139-134">Trace and Debug Settings Schema (Schema für Ablaufverfolgungs- und Debugeinstellungen)</span><span class="sxs-lookup"><span data-stu-id="3c139-134">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
