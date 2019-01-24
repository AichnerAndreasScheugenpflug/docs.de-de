---
title: '&lt;codeBase&gt; Element'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#codeBase
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/assemblyBinding/dependentAssembly/codeBase
helpviewer_keywords:
- <codeBase> element
- container tags, <codeBase> element
- codeBase element
ms.assetid: d48a3983-2297-43ff-a14d-1f29d3995822
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 295b2c5dd3eb17ca9ba19e52d9f8e51cf108162d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54683150"
---
# <a name="ltcodebasegt-element"></a><span data-ttu-id="b109c-102">&lt;codeBase&gt; Element</span><span class="sxs-lookup"><span data-stu-id="b109c-102">&lt;codeBase&gt; Element</span></span>
<span data-ttu-id="b109c-103">Gibt an, in dem die common Language Runtime eine Assembly finden kann.</span><span class="sxs-lookup"><span data-stu-id="b109c-103">Specifies where the common language runtime can find an assembly.</span></span>  
  
 <span data-ttu-id="b109c-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="b109c-104">\<configuration></span></span>  
<span data-ttu-id="b109c-105">\<runtime></span><span class="sxs-lookup"><span data-stu-id="b109c-105">\<runtime></span></span>  
<span data-ttu-id="b109c-106">\<assemblyBinding></span><span class="sxs-lookup"><span data-stu-id="b109c-106">\<assemblyBinding></span></span>  
<span data-ttu-id="b109c-107">\<dependentAssembly></span><span class="sxs-lookup"><span data-stu-id="b109c-107">\<dependentAssembly></span></span>  
<span data-ttu-id="b109c-108">\<codeBase></span><span class="sxs-lookup"><span data-stu-id="b109c-108">\<codeBase></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b109c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b109c-109">Syntax</span></span>  
  
```xml  
   <codeBase    
version="Assembly version"  
href="URL of assembly"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b109c-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b109c-110">Attributes and Elements</span></span>  
 <span data-ttu-id="b109c-111">In den folgenden Abschnitten werden Attribute sowie untergeordnete und übergeordnete Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b109c-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b109c-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="b109c-112">Attributes</span></span>  
  
|<span data-ttu-id="b109c-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="b109c-113">Attribute</span></span>|<span data-ttu-id="b109c-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b109c-114">Description</span></span>|  
|---------------|-----------------|  
|`href`|<span data-ttu-id="b109c-115">Erforderliches Attribut.</span><span class="sxs-lookup"><span data-stu-id="b109c-115">Required attribute.</span></span><br /><br /> <span data-ttu-id="b109c-116">Gibt die URL, in dem die Runtime die angegebene Version der Assembly finden kann.</span><span class="sxs-lookup"><span data-stu-id="b109c-116">Specifies the URL where the runtime can find the specified version of the assembly.</span></span>|  
|`version`|<span data-ttu-id="b109c-117">Erforderliches Attribut.</span><span class="sxs-lookup"><span data-stu-id="b109c-117">Required attribute.</span></span><br /><br /> <span data-ttu-id="b109c-118">Gibt die Version der Assembly, die, der auf die Codebasis angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b109c-118">Specifies the version of the assembly the codebase applies to.</span></span> <span data-ttu-id="b109c-119">Hat das Format einer Assemblyversionsnummer *"Hauptversion.Nebenversion.Build.Revision"*.</span><span class="sxs-lookup"><span data-stu-id="b109c-119">The format of an assembly version number is *major.minor.build.revision*.</span></span>|  
  
## <a name="version-attribute"></a><span data-ttu-id="b109c-120">Version-Attribut</span><span class="sxs-lookup"><span data-stu-id="b109c-120">version Attribute</span></span>  
  
|<span data-ttu-id="b109c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b109c-121">Value</span></span>|<span data-ttu-id="b109c-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b109c-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="b109c-123">Gültige Werte für jeden Teil der Versionsnummer sind 0 bis 65535.</span><span class="sxs-lookup"><span data-stu-id="b109c-123">Valid values for each part of the version number are 0 to 65535.</span></span>|<span data-ttu-id="b109c-124">Nicht zutreffend.</span><span class="sxs-lookup"><span data-stu-id="b109c-124">Not applicable.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b109c-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b109c-125">Child Elements</span></span>  
 <span data-ttu-id="b109c-126">Keine</span><span class="sxs-lookup"><span data-stu-id="b109c-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b109c-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b109c-127">Parent Elements</span></span>  
  
|<span data-ttu-id="b109c-128">Element</span><span class="sxs-lookup"><span data-stu-id="b109c-128">Element</span></span>|<span data-ttu-id="b109c-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b109c-129">Description</span></span>|  
|-------------|-----------------|  
|`buildproviders`|<span data-ttu-id="b109c-130">Definiert eine Auflistung von Buildanbietern, die zum Kompilieren benutzerdefinierter Ressourcendateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b109c-130">Defines a collection of build providers used to compile custom resource files.</span></span> <span data-ttu-id="b109c-131">Sie können eine beliebige Anzahl von Buildanbietern verwenden.</span><span class="sxs-lookup"><span data-stu-id="b109c-131">You can have any number of build providers.</span></span>|  
|`compilation`|<span data-ttu-id="b109c-132">Konfiguriert alle kompilierungseinstellungen, mit denen ASP.NET an.</span><span class="sxs-lookup"><span data-stu-id="b109c-132">Configures all the compilation settings that ASP.NET uses.</span></span>|  
|`configuration`|<span data-ttu-id="b109c-133">Das Stammelement in jeder von den Common Language Runtime- und .NET Framework-Anwendungen verwendeten Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="b109c-133">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`System.web`|<span data-ttu-id="b109c-134">Gibt das Stammelement für den ASP.NET-Konfigurationsabschnitt an.</span><span class="sxs-lookup"><span data-stu-id="b109c-134">Specifies the root element for the ASP.NET configuration section.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b109c-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b109c-135">Remarks</span></span>  
 <span data-ttu-id="b109c-136">Für die Laufzeit die  **\<codeBase >** in einer Konfigurationsdatei des Computers oder der Herausgeberrichtliniendatei festlegen, die Datei muss auch umleiten, die Version der Assembly.</span><span class="sxs-lookup"><span data-stu-id="b109c-136">For the runtime to use the **\<codeBase>** setting in a machine configuration file or publisher policy file, the file must also redirect the assembly version.</span></span> <span data-ttu-id="b109c-137">Anwendungskonfigurationsdateien haben eine Codebase-Einstellung, ohne die Version der Assembly umleiten.</span><span class="sxs-lookup"><span data-stu-id="b109c-137">Application configuration files can have a codebase setting without redirecting the assembly version.</span></span> <span data-ttu-id="b109c-138">Nachdem die zu verwendende Assemblyversion ermittelt wurde, gilt die Runtime die Codebase-Einstellung aus der Datei, die die Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b109c-138">After determining which assembly version to use, the runtime applies the codebase setting from the file that determines the version.</span></span> <span data-ttu-id="b109c-139">Wenn keine Codebase angegeben, durchsucht die Runtime für die Assembly, auf die übliche Weise.</span><span class="sxs-lookup"><span data-stu-id="b109c-139">If no codebase is indicated, the runtime probes for the assembly in the usual way.</span></span>  
  
 <span data-ttu-id="b109c-140">Wenn die Assembly einen starken Namen aufweist, kann die Codebase-Einstellung an eine beliebige Stelle im lokalen Intranet oder Internet sein.</span><span class="sxs-lookup"><span data-stu-id="b109c-140">If the assembly has a strong name, the codebase setting can be anywhere on the local intranet or the Internet.</span></span> <span data-ttu-id="b109c-141">Wenn die Assembly über eine private Assembly handelt, muss die Codebase-Einstellung auf einen Pfad relativ zum Verzeichnis der Anwendung sein.</span><span class="sxs-lookup"><span data-stu-id="b109c-141">If the assembly is a private assembly, the codebase setting must be a path relative to the application's directory.</span></span>  
  
 <span data-ttu-id="b109c-142">Für Assemblys ohne starken Namen, Version ignoriert, und das Ladeprogramm verwendet das erste Vorkommen von \<codebase > in \<DependentAssembly >.</span><span class="sxs-lookup"><span data-stu-id="b109c-142">For assemblies without a strong name, version is ignored and the loader uses the first appearance of \<codebase> inside \<dependentAssembly>.</span></span> <span data-ttu-id="b109c-143">Wenn ein Eintrag vorhanden, in der Konfigurationsdatei der Anwendung, die Bindung an eine andere Assembly umleitet ist, hat die Umleitung Vorrang, selbst wenn die Version der Assembly nicht mit der bindungsanforderung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="b109c-143">If there is an entry in the application configuration file that redirects binding to another assembly, the redirection will take precedence even if the assembly version doesnt match the binding request.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b109c-144">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b109c-144">Example</span></span>  
 <span data-ttu-id="b109c-145">Das folgende Beispiel zeigt, wie Sie angeben, in dem die Runtime eine Assembly finden kann.</span><span class="sxs-lookup"><span data-stu-id="b109c-145">The following example shows how to specify where the runtime can find an assembly.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
         <dependentAssembly>  
            <assemblyIdentity name="myAssembly"  
                              publicKeyToken="32ab4ba45e0a69a1"  
                              culture="neutral" />  
            <codeBase version="2.0.0.0"  
                      href="http://www.litwareinc.com/myAssembly.dll"/>  
         </dependentAssembly>  
      </assemblyBinding>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b109c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b109c-146">See also</span></span>
- [<span data-ttu-id="b109c-147">Schema für Laufzeiteinstellungen</span><span class="sxs-lookup"><span data-stu-id="b109c-147">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [<span data-ttu-id="b109c-148">Konfigurationsdateischema</span><span class="sxs-lookup"><span data-stu-id="b109c-148">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="b109c-149">Festlegen des Speicherortes einer Assembly</span><span class="sxs-lookup"><span data-stu-id="b109c-149">Specifying an Assembly's Location</span></span>](../../../../../docs/framework/configure-apps/specify-assembly-location.md)
- [<span data-ttu-id="b109c-150">So sucht Common Language Runtime nach Assemblys</span><span class="sxs-lookup"><span data-stu-id="b109c-150">How the Runtime Locates Assemblies</span></span>](../../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
