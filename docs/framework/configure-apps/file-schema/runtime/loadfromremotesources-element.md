---
title: <loadFromRemoteSources>-Element
ms.date: 05/24/2018
helpviewer_keywords:
- loadFromRemoteSources element
- <loadFromRemoteSources> element
ms.assetid: 006d1280-2ac3-4db6-a984-a3d4e275046a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7568129f30267b212737ec8aa688cf882e19bbff
ms.sourcegitcommit: b8ace47d839f943f785b89e2fff8092b0bf8f565
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2019
ms.locfileid: "55675308"
---
# <a name="loadfromremotesources-element"></a><span data-ttu-id="7d1ff-102">\<LoadFromRemoteSources >-Element</span><span class="sxs-lookup"><span data-stu-id="7d1ff-102">\<loadFromRemoteSources> element</span></span>
<span data-ttu-id="7d1ff-103">Gibt an, ob Assemblys aus Remotequellen geladen volle Vertrauenswürdigkeit in .NET Framework 4 und höher gewährt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-103">Specifies whether assemblies loaded from remote sources should be granted full trust in .NET Framework 4 and later.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="7d1ff-104">Wenn Sie aufgrund einer Fehlermeldung in der Fehlerliste von Visual Studio-Projekt oder einen Buildfehler zu diesem Artikel weitergeleitet wurden, finden Sie unter [Vorgehensweise: Verwenden Sie eine Assembly aus dem Web in Visual Studio](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee890038(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="7d1ff-104">If you were directed to this article because of an error message in the Visual Studio project error list or a build error, see [How to: Use an Assembly from the Web in Visual Studio](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ee890038(v=vs.100)).</span></span>  
  
 <span data-ttu-id="7d1ff-105">\<configuration></span><span class="sxs-lookup"><span data-stu-id="7d1ff-105">\<configuration></span></span>  
<span data-ttu-id="7d1ff-106">\<runtime></span><span class="sxs-lookup"><span data-stu-id="7d1ff-106">\<runtime></span></span>  
<span data-ttu-id="7d1ff-107">\<loadFromRemoteSources></span><span class="sxs-lookup"><span data-stu-id="7d1ff-107">\<loadFromRemoteSources></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d1ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d1ff-108">Syntax</span></span>  
  
```xml  
<loadFromRemoteSources    
   enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7d1ff-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7d1ff-109">Attributes and elements</span></span>
 <span data-ttu-id="7d1ff-110">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7d1ff-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="7d1ff-111">Attributes</span></span>  
  
|<span data-ttu-id="7d1ff-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="7d1ff-112">Attribute</span></span>|<span data-ttu-id="7d1ff-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d1ff-113">Description</span></span>|  
|---------------|-----------------|  
|`enabled`|<span data-ttu-id="7d1ff-114">Erforderliches Attribut.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="7d1ff-115">Gibt an, ob eine Assembly, die von einer Remotequelle geladen wird, volle Vertrauenswürdigkeit gewährt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-115">Specifies whether an assembly that is loaded from a remote source should be granted full trust.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="7d1ff-116">Enabled-Attribut</span><span class="sxs-lookup"><span data-stu-id="7d1ff-116">enabled attribute</span></span>  
  
|<span data-ttu-id="7d1ff-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7d1ff-117">Value</span></span>|<span data-ttu-id="7d1ff-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d1ff-118">Description</span></span>|  
|-----------|-----------------|  
|`false`|<span data-ttu-id="7d1ff-119">Gewähren Sie volle Vertrauenswürdigkeit nicht auf Anwendungen aus Remotequellen.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-119">Do not grant full trust to applications from remote sources.</span></span> <span data-ttu-id="7d1ff-120">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-120">This is the default.</span></span>|  
|`true`|<span data-ttu-id="7d1ff-121">Gewähren Sie volle Vertrauenswürdigkeit auf Anwendungen aus Remotequellen.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-121">Grant full trust to applications from remote sources.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7d1ff-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d1ff-122">Child elements</span></span>  
 <span data-ttu-id="7d1ff-123">Keine</span><span class="sxs-lookup"><span data-stu-id="7d1ff-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7d1ff-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d1ff-124">Parent elements</span></span>  
  
|<span data-ttu-id="7d1ff-125">Element</span><span class="sxs-lookup"><span data-stu-id="7d1ff-125">Element</span></span>|<span data-ttu-id="7d1ff-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d1ff-126">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="7d1ff-127">Das Stammelement in jeder von den Common Language Runtime- und .NET Framework-Anwendungen verwendeten Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-127">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="7d1ff-128">Enthält Informationen über Laufzeitinitialisierungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-128">Contains information about runtime initialization options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7d1ff-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7d1ff-129">Remarks</span></span>

<span data-ttu-id="7d1ff-130">Wenn Sie eine Assembly von einem Remotestandort befindet, Laden in das .NET Framework 3.5 und früheren Versionen wird Code in der Assembly bei teilweiser Vertrauenswürdigkeit mit einem Berechtigungssatz, der die Zone hängt von dem es geladen wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-130">In the .NET Framework 3.5 and earlier versions, if you load an assembly from a remote location, code in the assembly runs in partial trust with a grant set that depends on the zone from which it is loaded.</span></span> <span data-ttu-id="7d1ff-131">Z. B. Wenn Sie eine Assembly von einer Website laden, handelt es sich dabei in der Internetzone geladen den Internet-Berechtigungssatz.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-131">For example, if you load an assembly from a website, it is loaded into the Internet zone and granted the Internet permission set.</span></span> <span data-ttu-id="7d1ff-132">Das heißt, führt er in einem Internet-Sandkasten.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-132">In other words, it executes in an Internet sandbox.</span></span>

<span data-ttu-id="7d1ff-133">Ab .NET Framework 4, Richtlinie für die Codezugriffssicherheit (CAS) ist deaktiviert, und Assemblys mit voller Vertrauenswürdigkeit geladen werden.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-133">Starting with the .NET Framework 4, code access security (CAS) policy is disabled and assemblies are loaded in full trust.</span></span> <span data-ttu-id="7d1ff-134">Normalerweise würde diese Assemblys geladen und volle Vertrauenswürdigkeit gewähren der <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType> Methode, die zuvor Sandbox waren.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-134">Ordinarily, this would grant full trust to assemblies loaded with the <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType> method that previously had been sandboxed.</span></span> <span data-ttu-id="7d1ff-135">Um dies zu verhindern, ist die Möglichkeit zum Ausführen von Code in Assemblys, die von einer Remotequelle geladen, standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-135">To prevent this, the ability to run code in assemblies loaded from a remote source is disabled by default.</span></span> <span data-ttu-id="7d1ff-136">Standardmäßig, wenn Sie versuchen, eine Remoteassembly, laden ein <xref:System.IO.FileLoadException> mit eine Ausnahmemeldung wie, dass Sie Folgendes ausgelöst wird:</span><span class="sxs-lookup"><span data-stu-id="7d1ff-136">By default, if you attempt to load a remote assembly, a <xref:System.IO.FileLoadException> with an exception message like the following is thrown:</span></span>

```text
System.IO.FileNotFoundException: Could not load file or assembly 'file:assem.dll' or one of its dependencies. Operation is not supported. 
(Exception from HRESULT: 0x80131515)
File name: 'file:assem.dll' ---> 
System.NotSupportedException: An attempt was made to load an assembly from a network location which would have caused the assembly 
to be sandboxed in previous versions of the .NET Framework. This release of the .NET Framework does not enable CAS policy by default, 
so this load may be dangerous. If this load is not intended to sandbox the assembly, please enable the loadFromRemoteSources switch. 
```

<span data-ttu-id="7d1ff-137">Zum Laden der Assembly und deren Code ausführen, müssen Sie entweder:</span><span class="sxs-lookup"><span data-stu-id="7d1ff-137">To load the assembly and execute its code, you must either:</span></span>

- <span data-ttu-id="7d1ff-138">Erstellen Sie explizit einen Sandkasten für die Assembly (finden Sie unter [Vorgehensweise: Ausführen von teilweise vertrauenswürdigem Code in einer Sandbox](../../../../../docs/framework/misc/how-to-run-partially-trusted-code-in-a-sandbox.md)).</span><span class="sxs-lookup"><span data-stu-id="7d1ff-138">Explicitly create a sandbox for the assembly (see [How to: Run Partially Trusted Code in a Sandbox](../../../../../docs/framework/misc/how-to-run-partially-trusted-code-in-a-sandbox.md)).</span></span>

- <span data-ttu-id="7d1ff-139">Führen Sie Code von der Assembly mit voller Vertrauenswürdigkeit.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-139">Run the assembly's code in full trust.</span></span> <span data-ttu-id="7d1ff-140">Konfigurieren Sie dazu die `<loadFromRemoteSources>` Element.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-140">You do this by configuring the `<loadFromRemoteSources>` element.</span></span> <span data-ttu-id="7d1ff-141">Sie können angeben, dass die Assemblys, die bei teilweiser Vertrauenswürdigkeit in früheren Versionen von .NET Framework ausgeführt werden jetzt als voll vertrauenswürdig in der .NET Framework 4 und höher ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-141">It lets you specify that the assemblies that run in partial trust in earlier versions of the .NET Framework now run in full trust in the .NET Framework 4 and later versions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d1ff-142">Wenn die Assembly nicht mit voller Vertrauenswürdigkeit ausgeführt werden soll, legen Sie dieses Element nicht.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-142">If the assembly should not run in full trust, do not set this configuration element.</span></span> <span data-ttu-id="7d1ff-143">Erstellen Sie stattdessen eine Sandbox <xref:System.AppDomain> in dem die Assembly zu laden.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-143">Instead, create a sandboxed <xref:System.AppDomain> in which to load the assembly.</span></span>

<span data-ttu-id="7d1ff-144">Die `enabled` -Attribut für die `<loadFromRemoteSources>` Element gilt nur, wenn die Codezugriffssicherheit (CAS) deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-144">The `enabled` attribute for the `<loadFromRemoteSources>` element is effective only when code access security (CAS) is disabled.</span></span> <span data-ttu-id="7d1ff-145">Standardmäßig ist die CAS-Richtlinie in der .NET Framework 4 und höheren Versionen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-145">By default, CAS policy is disabled in the .NET Framework 4 and later versions.</span></span> <span data-ttu-id="7d1ff-146">Setzen Sie `enabled` zu `true`, remote-Assemblys die volle Vertrauenswürdigkeit gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-146">If you set `enabled` to `true`, remote assemblies are granted full trust.</span></span>

<span data-ttu-id="7d1ff-147">Wenn `enabled` ist nicht festgelegt, um `true`, <xref:System.IO.FileLoadException> wird in einer der folgenden Bedingungen ausgelöst:</span><span class="sxs-lookup"><span data-stu-id="7d1ff-147">If `enabled` is not set to `true`, a <xref:System.IO.FileLoadException> is thrown under the either of the following conditions:</span></span>

- <span data-ttu-id="7d1ff-148">Der Sandkasten-Verhalten der aktuellen Domäne unterscheidet sich vom Verhalten in .NET Framework 3.5.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-148">The sandboxing behavior of the current domain is different from its behavior in the .NET Framework 3.5.</span></span> <span data-ttu-id="7d1ff-149">Dies erfordert die CAS-Richtlinie deaktiviert werden soll, und der aktuellen Domäne nicht zu Sandbox.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-149">This requires CAS policy to be disabled, and the current domain not to be sandboxed.</span></span>

- <span data-ttu-id="7d1ff-150">Die geladene Assembly stammt nicht von der `MyComputer` Zone.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-150">The assembly being loaded is not from the `MyComputer` zone.</span></span>

<span data-ttu-id="7d1ff-151">Festlegen der `<loadFromRemoteSources>` Element `true` wird verhindert, dass diese Ausnahme ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-151">Setting the `<loadFromRemoteSources>` element to `true` prevents this exception from being thrown.</span></span> <span data-ttu-id="7d1ff-152">Damit können Sie angeben, dass nicht Sie sich die common Language Runtime für das Sandboxing die geladenen Assemblys für die Sicherheit verlassen und ermöglicht werden kann. Führen Sie in volle Vertrauenswürdigkeit.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-152">It enables you to specify that you are not relying on the common language runtime to sandbox the loaded assemblies for security, and that they can be allowed to execute in full trust.</span></span>

## <a name="notes"></a><span data-ttu-id="7d1ff-153">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7d1ff-153">Notes</span></span>

- <span data-ttu-id="7d1ff-154">In der .NET Framework 4.5 und höheren Versionen wird standardmäßig Assemblys auf der lokalen Netzwerkfreigaben mit voller Vertrauenswürdigkeit ausgeführt; Sie müssen keine aktivieren die `<loadFromRemoteSources>` Element.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-154">In the .NET Framework 4.5 and later versions, assemblies on local network shares run in full trust by default; you do not have to enable the `<loadFromRemoteSources>` element.</span></span>

- <span data-ttu-id="7d1ff-155">Wenn eine Anwendung über das Web kopiert wurde, wird er von Windows als replikationsbereit markiert eine Webanwendung, auch wenn er auf dem lokalen Computer befindet.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-155">If an application has been copied from the web, it is flagged by Windows as being a web application, even if it resides on the local computer.</span></span> <span data-ttu-id="7d1ff-156">Sie können diese Bezeichnung durch Ändern der Dateieigenschaften ändern, oder Sie können die `<loadFromRemoteSources>` Element gewähren Sie die Assembly volle Vertrauenswürdigkeit.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-156">You can change that designation by changing its file properties, or you can use the `<loadFromRemoteSources>` element to grant the assembly full trust.</span></span> <span data-ttu-id="7d1ff-157">Als Alternative können Sie die <xref:System.Reflection.Assembly.UnsafeLoadFrom%2A> Methode, um eine lokale Assembly zu laden, die das Betriebssystem gekennzeichnet wurden, als aus dem Web geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-157">As an alternative, you can use the <xref:System.Reflection.Assembly.UnsafeLoadFrom%2A> method to load a local assembly that the operating system has flagged as having been loaded from the web.</span></span>

- <span data-ttu-id="7d1ff-158">Sie erhalten möglicherweise eine <xref:System.IO.FileLoadException> in einer Anwendung, die in einer Windows Virtual PC-Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-158">You may get a <xref:System.IO.FileLoadException> in an application that is running in a Windows Virtual PC application.</span></span> <span data-ttu-id="7d1ff-159">Dies kann passieren, wenn Sie versuchen, eine Datei aus dem verknüpften Ordner auf dem Hostcomputer zu laden.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-159">This can happen when you try to load a file from linked folders on the hosting computer.</span></span> <span data-ttu-id="7d1ff-160">Er kann auch auftreten, wenn Sie versuchen, eine Datei aus einem Ordner, die über verknüpfte laden [Remote Desktop Services](https://go.microsoft.com/fwlink/?LinkId=182775) (Terminaldienste).</span><span class="sxs-lookup"><span data-stu-id="7d1ff-160">It can also occur when you try to load a file from a folder linked over [Remote Desktop Services](https://go.microsoft.com/fwlink/?LinkId=182775) (Terminal Services).</span></span> <span data-ttu-id="7d1ff-161">Um die Ausnahme zu vermeiden, legen Sie `enabled` zu `true`.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-161">To avoid the exception, set `enabled` to `true`.</span></span>

## <a name="configuration-file"></a><span data-ttu-id="7d1ff-162">Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="7d1ff-162">Configuration file</span></span>

<span data-ttu-id="7d1ff-163">Dieses Element wird in der Regel in der Konfigurationsdatei der Anwendung verwendet, aber in anderen Konfigurationsdateien, die je nach Kontext verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-163">This element is typically used in the application configuration file, but can be used in other configuration files depending upon the context.</span></span> <span data-ttu-id="7d1ff-164">Weitere Informationen finden Sie im Artikel [Weitere implizite verwendet der CAS-Richtlinie: LoadFromRemoteSources](https://go.microsoft.com/fwlink/p/?LinkId=266839) im .NET Security Blog.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-164">For more information, see the article [More Implicit Uses of CAS Policy: loadFromRemoteSources](https://go.microsoft.com/fwlink/p/?LinkId=266839) in the .NET Security blog.</span></span>  

## <a name="example"></a><span data-ttu-id="7d1ff-165">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7d1ff-165">Example</span></span>

<span data-ttu-id="7d1ff-166">Das folgende Beispiel zeigt, wie Sie Assemblys aus Remotequellen geladen volles Vertrauen gewähren.</span><span class="sxs-lookup"><span data-stu-id="7d1ff-166">The following example shows how to grant full trust to assemblies loaded from remote sources.</span></span>

```xml
<configuration>  
   <runtime>  
      <loadFromRemoteSources enabled="true"/>  
   </runtime>  
</configuration>  
```

## <a name="see-also"></a><span data-ttu-id="7d1ff-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d1ff-167">See also</span></span>

- [<span data-ttu-id="7d1ff-168">Mehr impliziten verwendet der CAS-Richtlinie: LoadFromRemoteSources</span><span class="sxs-lookup"><span data-stu-id="7d1ff-168">More Implicit Uses of CAS Policy: loadFromRemoteSources</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=266839)
- [<span data-ttu-id="7d1ff-169">Vorgehensweise: Ausführen von teilweise vertrauenswürdigem Code in einem Sandkasten</span><span class="sxs-lookup"><span data-stu-id="7d1ff-169">How to: Run Partially Trusted Code in a Sandbox</span></span>](../../../../../docs/framework/misc/how-to-run-partially-trusted-code-in-a-sandbox.md)
- [<span data-ttu-id="7d1ff-170">Schema für Laufzeiteinstellungen</span><span class="sxs-lookup"><span data-stu-id="7d1ff-170">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="7d1ff-171">Konfigurationsdateischema</span><span class="sxs-lookup"><span data-stu-id="7d1ff-171">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- <xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=nameWithType>
