---
title: 'Vorgehensweise: Freigeben einer Assembly für andere Anwendungen (C#)'
ms.date: 07/20/2015
ms.assetid: c30e972b-1693-4e05-b115-c31831fdf9f2
ms.openlocfilehash: d440000ef509199bf69f06c2f3b5d0819e48f724
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54713576"
---
# <a name="how-to-share-an-assembly-with-other-applications-c"></a><span data-ttu-id="a3ca5-102">Vorgehensweise: Freigeben einer Assembly für andere Anwendungen (C#)</span><span class="sxs-lookup"><span data-stu-id="a3ca5-102">How to: Share an Assembly with Other Applications (C#)</span></span>
<span data-ttu-id="a3ca5-103">Assemblys können sowohl privat als auch freigegeben sein: Standardmäßig bestehen die meisten einfachen Programme aus einer privaten Assembly, da sie nicht für den Gebrauch durch andere Anwendungen vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-103">Assemblies can be private or shared: by default, most simple programs consist of a private assembly because they are not intended to be used by other applications.</span></span>  
  
 <span data-ttu-id="a3ca5-104">Um eine Assembly für andere Anwendungen freizugeben, muss diese in den [globalen Assemblycache](../../../../framework/app-domains/gac.md) (Global Assembly Cache, GAC) platziert werden.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-104">In order to share an assembly with other applications, it must be placed in the [Global Assembly Cache](../../../../framework/app-domains/gac.md) (GAC).</span></span>  
  
### <a name="sharing-an-assembly"></a><span data-ttu-id="a3ca5-105">Freigeben einer Assembly</span><span class="sxs-lookup"><span data-stu-id="a3ca5-105">Sharing an assembly</span></span>  
  
1.  <span data-ttu-id="a3ca5-106">Erstellen Ihrer Assembly.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-106">Create your assembly.</span></span> <span data-ttu-id="a3ca5-107">Weitere Informationen finden Sie unter [Erstellen von Assemblys](../../../../framework/app-domains/create-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="a3ca5-107">For more information, see [Creating Assemblies](../../../../framework/app-domains/create-assemblies.md).</span></span>  
  
2.  <span data-ttu-id="a3ca5-108">Weisen Sie Ihrer Assembly einen starken Namen zu.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-108">Assign a strong name to your assembly.</span></span> <span data-ttu-id="a3ca5-109">Weitere Informationen finden Sie unter [Vorgehensweise: Signieren einer Assembly mit einem starken Namen](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span><span class="sxs-lookup"><span data-stu-id="a3ca5-109">For more information, see [How to: Sign an Assembly with a Strong Name](../../../../framework/app-domains/how-to-sign-an-assembly-with-a-strong-name.md).</span></span>  
  
3.  <span data-ttu-id="a3ca5-110">Weisen Sie Ihrer Assembly Versionsinformationen zu.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-110">Assign version information to your assembly.</span></span> <span data-ttu-id="a3ca5-111">Weitere Informationen dazu finden Sie unter [Assemblyversionen](../../../../../docs/framework/app-domains/assembly-versioning.md).</span><span class="sxs-lookup"><span data-stu-id="a3ca5-111">For more information, see [Assembly Versioning](../../../../../docs/framework/app-domains/assembly-versioning.md).</span></span>  
  
4.  <span data-ttu-id="a3ca5-112">Fügen Sie Ihre Assembly in den globalen Assemblycache ein.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-112">Add your assembly to the Global Assembly Cache.</span></span> <span data-ttu-id="a3ca5-113">Weitere Informationen finden Sie unter [Vorgehensweise: Installieren einer Assembly im globalen Assemblycache](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md).</span><span class="sxs-lookup"><span data-stu-id="a3ca5-113">For more information, see [How to: Install an Assembly into the Global Assembly Cache](../../../../framework/app-domains/how-to-install-an-assembly-into-the-gac.md).</span></span>  
  
5.  <span data-ttu-id="a3ca5-114">Greifen Sie auf die Typen anderer Anwendungen zu, die in der Assembly enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-114">Access the types contained in the assembly from the other applications.</span></span> <span data-ttu-id="a3ca5-115">Weitere Informationen finden Sie unter [Vorgehensweise: Verweisen auf eine Assembly mit starkem Namen](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md).</span><span class="sxs-lookup"><span data-stu-id="a3ca5-115">For more information, see [How to: Reference a Strong-Named Assembly](../../../../framework/app-domains/how-to-reference-a-strong-named-assembly.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3ca5-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3ca5-116">See also</span></span>

- [<span data-ttu-id="a3ca5-117">C#-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="a3ca5-117">C# Programming Guide</span></span>](../../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="a3ca5-118">Programmieren mit Assemblys</span><span class="sxs-lookup"><span data-stu-id="a3ca5-118">Programming with Assemblies</span></span>](../../../../framework/app-domains/programming-with-assemblies.md)
