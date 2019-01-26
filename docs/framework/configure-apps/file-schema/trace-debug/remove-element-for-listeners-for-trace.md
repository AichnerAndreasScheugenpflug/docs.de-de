---
title: '&lt;Entfernen Sie&gt; -Element für &lt;Listener&gt; für &lt;Ablaufverfolgung&gt;'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/trace/listeners/remove
helpviewer_keywords:
- remove element
- <remove> element
ms.assetid: 9a5cd1b5-be1a-485f-8f0c-2890ad3ef3e0
ms.openlocfilehash: c1587c28e05609970c732192752578d089ec9f35
ms.sourcegitcommit: b351b0781a035616c90c68ccae6dd60aae66a953
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2019
ms.locfileid: "55083833"
---
# <a name="ltremovegt-element-for-ltlistenersgt-for-lttracegt"></a><span data-ttu-id="a0013-102">&lt;Entfernen Sie&gt; -Element für &lt;Listener&gt; für &lt;Ablaufverfolgung&gt;</span><span class="sxs-lookup"><span data-stu-id="a0013-102">&lt;remove&gt; Element for &lt;listeners&gt; for &lt;trace&gt;</span></span>
<span data-ttu-id="a0013-103">Entfernt einen Listener aus der **Listener** Auflistung.</span><span class="sxs-lookup"><span data-stu-id="a0013-103">Removes a listener from the **Listeners** collection.</span></span>  
  
 <span data-ttu-id="a0013-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="a0013-104">\<configuration></span></span>  
<span data-ttu-id="a0013-105">\<system.diagnostics></span><span class="sxs-lookup"><span data-stu-id="a0013-105">\<system.diagnostics></span></span>  
<span data-ttu-id="a0013-106">\<trace></span><span class="sxs-lookup"><span data-stu-id="a0013-106">\<trace></span></span>  
<span data-ttu-id="a0013-107">\<listeners></span><span class="sxs-lookup"><span data-stu-id="a0013-107">\<listeners></span></span>  
<span data-ttu-id="a0013-108">\<remove></span><span class="sxs-lookup"><span data-stu-id="a0013-108">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0013-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0013-109">Syntax</span></span>  
  
```xml  
<remove name="listener name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a0013-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a0013-110">Attributes and Elements</span></span>  
 <span data-ttu-id="a0013-111">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a0013-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a0013-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0013-112">Attributes</span></span>  
  
|<span data-ttu-id="a0013-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="a0013-113">Attribute</span></span>|<span data-ttu-id="a0013-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0013-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a0013-115">**name**</span><span class="sxs-lookup"><span data-stu-id="a0013-115">**name**</span></span>|<span data-ttu-id="a0013-116">Erforderliches Attribut.</span><span class="sxs-lookup"><span data-stu-id="a0013-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="a0013-117">Der Name des Listeners, Aufheben der **Listener** Auflistung.</span><span class="sxs-lookup"><span data-stu-id="a0013-117">The name of the listener to remove from the **Listeners** collection.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a0013-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0013-118">Child Elements</span></span>  
 <span data-ttu-id="a0013-119">Keine</span><span class="sxs-lookup"><span data-stu-id="a0013-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a0013-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0013-120">Parent Elements</span></span>  
  
|<span data-ttu-id="a0013-121">Element</span><span class="sxs-lookup"><span data-stu-id="a0013-121">Element</span></span>|<span data-ttu-id="a0013-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0013-122">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="a0013-123">Das Stammelement in jeder von den Common Language Runtime- und .NET Framework-Anwendungen verwendeten Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="a0013-123">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`listeners`|<span data-ttu-id="a0013-124">Gibt an, einen Listener, der sammelt, speichert, und leitet Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="a0013-124">Specifies a listener that collects, stores, and routes messages.</span></span> <span data-ttu-id="a0013-125">Listener leiten die Ablaufverfolgungsausgabe an ein entsprechendes Ziel.</span><span class="sxs-lookup"><span data-stu-id="a0013-125">Listeners direct the tracing output to an appropriate target.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="a0013-126">Gibt Ablaufverfolgungslistener an, die Meldungen sammeln, speichern und weiterleiten sowie die Ebene, für die ein Ablaufverfolgungsschalter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a0013-126">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`trace`|<span data-ttu-id="a0013-127">Konfiguriert den ASP.NET-Ablaufverfolgungsdienst.</span><span class="sxs-lookup"><span data-stu-id="a0013-127">Configures the ASP.NET trace service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a0013-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a0013-128">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a0013-129">Entfernen der <xref:System.Diagnostics.DefaultTraceListener> aus der `Listeners` Auflistung ändert das Sitzungsverhalten, sodass die <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType>, und <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType> Methoden.</span><span class="sxs-lookup"><span data-stu-id="a0013-129">Removing the <xref:System.Diagnostics.DefaultTraceListener> from the `Listeners` collection alters the behavior of the <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=nameWithType>, <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=nameWithType>, and <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=nameWithType> methods.</span></span> <span data-ttu-id="a0013-130">Aufrufen einer `Assert` oder `Fail` -Methode führt normalerweise in der Anzeige eines Meldungsfelds, aber das Feld nicht angezeigt wird der <xref:System.Diagnostics.DefaultTraceListener> befindet sich nicht in der `Listeners` Auflistung.</span><span class="sxs-lookup"><span data-stu-id="a0013-130">Calling an `Assert` or `Fail` method normally results in the display of a message box, however the message box is not displayed if the <xref:System.Diagnostics.DefaultTraceListener> is not in the `Listeners` collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a0013-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a0013-131">Example</span></span>  
 <span data-ttu-id="a0013-132">Das folgende Beispiel zeigt, wie Sie den standardmäßigen Ablaufverfolgungslistener aus der Ablaufverfolgung entfernen **Listener** Auflistung.</span><span class="sxs-lookup"><span data-stu-id="a0013-132">The following example shows how to remove the default trace listener from the trace **Listeners** collection.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="a0013-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0013-133">See also</span></span>
- <xref:System.Diagnostics.TraceListener>
- <xref:System.Diagnostics.DefaultTraceListener>
- <xref:System.Diagnostics.TextWriterTraceListener>
- <xref:System.Diagnostics.EventLogTraceListener>
- [<span data-ttu-id="a0013-134">Trace and Debug Settings Schema (Schema für Ablaufverfolgungs- und Debugeinstellungen)</span><span class="sxs-lookup"><span data-stu-id="a0013-134">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
