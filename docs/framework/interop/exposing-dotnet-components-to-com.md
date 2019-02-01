---
title: Verfügbarmachen von .NET Framework-Komponenten in COM
ms.date: 03/30/2017
helpviewer_keywords:
- exposing .NET Framework components to COM
- interoperation with unmanaged code, exposing .NET Framework components
- COM interop, exposing COM components
ms.assetid: e42a65f7-1e61-411f-b09a-aca1bbce24c6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b5c80ba473b0080a1368c82949c765820239ef25
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715737"
---
# <a name="exposing-net-framework-components-to-com"></a><span data-ttu-id="15ee8-102">Verfügbarmachen von .NET Framework-Komponenten in COM</span><span class="sxs-lookup"><span data-stu-id="15ee8-102">Exposing .NET Framework Components to COM</span></span>
<span data-ttu-id="15ee8-103">Das Schreiben eines .NET-Typs und das Verwenden dieses Typs von nicht verwaltetem Code sind unterschiedliche Aktivitäten für Entwickler.</span><span class="sxs-lookup"><span data-stu-id="15ee8-103">Writing a .NET type and consuming that type from unmanaged code are distinct activities for developers.</span></span> <span data-ttu-id="15ee8-104">Dieser Abschnitt beschreibt einige Tipps zum Schreiben von verwaltetem Code, der mit COM-Clients interagiert:</span><span class="sxs-lookup"><span data-stu-id="15ee8-104">This section describes several tips for writing managed code that interoperates with COM clients:</span></span>  
  
-   <span data-ttu-id="15ee8-105">[Qualifizieren von .NET-Typen für die Interoperation](../../../docs/framework/interop/qualifying-net-types-for-interoperation.md).</span><span class="sxs-lookup"><span data-stu-id="15ee8-105">[Qualifying .NET types for interoperation](../../../docs/framework/interop/qualifying-net-types-for-interoperation.md).</span></span>  
  
     <span data-ttu-id="15ee8-106">Alle verwalteten Typen, Methoden, Eigenschaften, Felder und Ereignisse, die für COM verfügbar gemacht werden sollen, müssen öffentlich sein.</span><span class="sxs-lookup"><span data-stu-id="15ee8-106">All managed types, methods, properties, fields, and events that you want to expose to COM must be public.</span></span> <span data-ttu-id="15ee8-107">Typen müssen über einen öffentlichen Standardkonstruktor verfügen, da dies der einzige Konstruktor ist, der über COM aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="15ee8-107">Types must have a public default constructor, which is the only constructor that can be invoked through COM.</span></span>  
  
-   <span data-ttu-id="15ee8-108">[Anwenden von Interop-Attributen](../../../docs/framework/interop/applying-interop-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="15ee8-108">[Applying interop attributes](../../../docs/framework/interop/applying-interop-attributes.md).</span></span>  
  
     <span data-ttu-id="15ee8-109">Benutzerdefinierte Attribute in verwaltetem Code können die Interoperabilität einer Komponente verbessern.</span><span class="sxs-lookup"><span data-stu-id="15ee8-109">Custom attributes within managed code can enhance the interoperability of a component.</span></span>  
  
-   <span data-ttu-id="15ee8-110">[Verpacken einer Assembly für COM](../../../docs/framework/interop/packaging-an-assembly-for-com.md).</span><span class="sxs-lookup"><span data-stu-id="15ee8-110">[Packaging an assembly for COM](../../../docs/framework/interop/packaging-an-assembly-for-com.md).</span></span>  
  
     <span data-ttu-id="15ee8-111">COM-Entwickler fordern möglicherweise, dass Sie die Schritte für Verweise und die Bereitstellung Ihrer Assemblys zusammenfassen.</span><span class="sxs-lookup"><span data-stu-id="15ee8-111">COM developers might require that you summarize the steps involved in referencing and deploying your assemblies.</span></span>  
  
 <span data-ttu-id="15ee8-112">Darüber hinaus werden in diesem Abschnitt die Aufgaben im Zusammenhang mit der Nutzung eines verwalteten Typs von einem COM-Client beschrieben.</span><span class="sxs-lookup"><span data-stu-id="15ee8-112">Additionally, this section identifies the tasks related to consuming a managed type from a COM client.</span></span>  
  
#### <a name="to-consume-a-managed-type-from-com"></a><span data-ttu-id="15ee8-113">Nutzen eines verwalteten Typs von COM</span><span class="sxs-lookup"><span data-stu-id="15ee8-113">To consume a managed type from COM</span></span>  
  
1.  <span data-ttu-id="15ee8-114">[Registrieren von Assemblys bei COM](../../../docs/framework/interop/registering-assemblies-with-com.md).</span><span class="sxs-lookup"><span data-stu-id="15ee8-114">[Register assemblies with COM](../../../docs/framework/interop/registering-assemblies-with-com.md).</span></span>  
  
     <span data-ttu-id="15ee8-115">Typen in einer Assembly (und Typbibliotheken) müssen zur Entwurfszeit registriert werden.</span><span class="sxs-lookup"><span data-stu-id="15ee8-115">Types in an assembly (and type libraries) must be registered at design time.</span></span> <span data-ttu-id="15ee8-116">Wenn ein Installer die Assembly nicht registriert, weisen Sie die COM-Entwickler zur Nutzung von Regasm.exe an.</span><span class="sxs-lookup"><span data-stu-id="15ee8-116">If an installer does not register the assembly, instruct COM developers to use Regasm.exe.</span></span>  
  
2.  <span data-ttu-id="15ee8-117">[Verweisen auf .NET-Typen in COM](../../../docs/framework/interop/how-to-reference-net-types-from-com.md).</span><span class="sxs-lookup"><span data-stu-id="15ee8-117">[Reference .NET types from COM](../../../docs/framework/interop/how-to-reference-net-types-from-com.md).</span></span>  
  
     <span data-ttu-id="15ee8-118">COM-Entwickler können auf Typen in einer Assembly verweisen, indem sie dieselben Tools und Techniken nutzen, die sie heute bereits verwenden.</span><span class="sxs-lookup"><span data-stu-id="15ee8-118">COM developers can reference types in an assembly using the same tools and techniques they use today.</span></span>  
  
3.  <span data-ttu-id="15ee8-119">[Aufrufen eines .NET-Objekts](https://msdn.microsoft.com/library/40c9626c-aea6-4bad-b8f0-c1de462efd33(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="15ee8-119">[Call a .NET object](https://msdn.microsoft.com/library/40c9626c-aea6-4bad-b8f0-c1de462efd33(v=vs.100)).</span></span>  
  
     <span data-ttu-id="15ee8-120">COM-Entwickler können Methoden so für das .NET-Objekt aufrufen, wie sie Methoden für alle nicht verwalteten Typen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="15ee8-120">COM developers can call methods on the .NET object the same way they call methods on any unmanaged type.</span></span> <span data-ttu-id="15ee8-121">Z.B. aktiviert die COM-API **CoCreateInstance** .NET-Objekte.</span><span class="sxs-lookup"><span data-stu-id="15ee8-121">For example, the COM **CoCreateInstance** API activates .NET objects.</span></span>  
  
4.  <span data-ttu-id="15ee8-122">[Bereitstellen einer Anwendung für COM-Zugriff](https://msdn.microsoft.com/library/fb63564c-c1b9-4655-a094-a235625882ce(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="15ee8-122">[Deploy an application for COM access](https://msdn.microsoft.com/library/fb63564c-c1b9-4655-a094-a235625882ce(v=vs.100)).</span></span>  
  
     <span data-ttu-id="15ee8-123">Eine Assembly mit starkem Namen kann im globalen Assemblycache installiert werden und erfordert eine Signatur des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="15ee8-123">A strong-named assembly can be installed in the global assembly cache and requires a signature from its publisher.</span></span> <span data-ttu-id="15ee8-124">Assemblys, die keinen starken Namen haben, müssen im Anwendungsverzeichnis des Clients installiert werden.</span><span class="sxs-lookup"><span data-stu-id="15ee8-124">Assemblies that are not strong named must be installed in the application directory of the client.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15ee8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15ee8-125">See also</span></span>
- [<span data-ttu-id="15ee8-126">Interoperabilität mit nicht verwaltetem Code</span><span class="sxs-lookup"><span data-stu-id="15ee8-126">Interoperating with Unmanaged Code</span></span>](../../../docs/framework/interop/index.md)
- [<span data-ttu-id="15ee8-127">COM-Interopbeispiel: COM-Client und .NET-Server</span><span class="sxs-lookup"><span data-stu-id="15ee8-127">COM Interop Sample: COM Client and .NET Server</span></span>](../../../docs/framework/interop/com-interop-sample-com-client-and-net-server.md)
