---
title: AssemblyAttributesGoHereM
ms.date: 03/30/2017
api_name:
- AssemblyAttributesGoHereM
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AssemblyAttributesGoHereM
helpviewer_keywords:
- AssemblyAttributesGoHereM type
- Alink API, AssemblyAttributesGoHereM type
ms.assetid: caaa8ba9-b4bb-4dd6-934d-57e436b2f3e5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bbd5428039144fd38796ed6865c24a605f236ccd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54733804"
---
# <a name="assemblyattributesgoherem"></a><span data-ttu-id="5d23c-102">AssemblyAttributesGoHereM</span><span class="sxs-lookup"><span data-stu-id="5d23c-102">AssemblyAttributesGoHereM</span></span>
<span data-ttu-id="5d23c-103">Wird von ALink als Platzhalter verwendet, um Informationen über benutzerdefinierte Attribute zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5d23c-103">Used by ALink as a placeholder to store information about custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5d23c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d23c-104">Syntax</span></span>  
  
```  
AssemblyAttributesGoHereM  
```  
  
## <a name="remarks"></a><span data-ttu-id="5d23c-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d23c-105">Remarks</span></span>  
 <span data-ttu-id="5d23c-106">Verweise auf diesen Typ können in NETMODULE-Dateien eingebettet sein, deren Quellen benutzerdefinierte Assemblyattribute enthalten.</span><span class="sxs-lookup"><span data-stu-id="5d23c-106">References to this type might be embedded inside netmodules whose sources contain assembly custom attributes.</span></span> <span data-ttu-id="5d23c-107">Beim Erstellen eines Assemblymanifests aus mindestens einer NETMODULE-Datei, die Verweise auf diese Typen enthält, verwendet ALink die zu diesen Verweisen gehörenden Informationen, um echte benutzerdefinierte Attribute auszugeben.</span><span class="sxs-lookup"><span data-stu-id="5d23c-107">When building an assembly manifest from one or more netmodules that contain references to these types, ALink uses information attached to these references to emit real custom attributes.</span></span> <span data-ttu-id="5d23c-108">Daher wird dieser Typ nie instanziiert, und Verweise auf diesen Typ werden nur als Teil des Buildprozesses verwendet und erfüllen in der endgültigen Assembly keinen Zweck.</span><span class="sxs-lookup"><span data-stu-id="5d23c-108">As such, this type is never instantiated, and references to it are used only as part of the build process and serve no purpose in the final assembly.</span></span>  
  
 <span data-ttu-id="5d23c-109">Verweise auf diesen Typ geben benutzerdefinierte Attribute an, die nicht sicherheitsrelevant sind, aber mehrfach verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5d23c-109">References to this type indicate custom attributes that are not security related but are multiple-use.</span></span>  
  
 <span data-ttu-id="5d23c-110">Diese Typen sind in .NET Framework mit "intern" markiert und befinden sich in <xref:System.Runtime.CompilerServices>.</span><span class="sxs-lookup"><span data-stu-id="5d23c-110">These types are marked "internal" within the .NET Framework, and are located in <xref:System.Runtime.CompilerServices>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5d23c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d23c-111">Requirements</span></span>  
 <span data-ttu-id="5d23c-112">mscorlib.dll</span><span class="sxs-lookup"><span data-stu-id="5d23c-112">mscorlib.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d23c-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d23c-113">See also</span></span>
- [<span data-ttu-id="5d23c-114">AssemblyAttributesGoHere</span><span class="sxs-lookup"><span data-stu-id="5d23c-114">AssemblyAttributesGoHere</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgohere.md)
- [<span data-ttu-id="5d23c-115">AssemblyAttributesGoHereS</span><span class="sxs-lookup"><span data-stu-id="5d23c-115">AssemblyAttributesGoHereS</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgoheres.md)
- [<span data-ttu-id="5d23c-116">AssemblyAttributesGoHereSM</span><span class="sxs-lookup"><span data-stu-id="5d23c-116">AssemblyAttributesGoHereSM</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgoheresm.md)
