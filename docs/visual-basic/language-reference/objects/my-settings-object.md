---
title: My.Settings-Objekt (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.MySettingsProperty.Settings
- My.Settings
helpviewer_keywords:
- My.Settings object
ms.assetid: 41f30dc1-202a-4273-b9b7-5728941f996c
ms.openlocfilehash: 293e7cd6449b8a35b5e42b4823a4412e0d6a3f14
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54628161"
---
# <a name="mysettings-object"></a><span data-ttu-id="97468-102">My.Settings-Objekt</span><span class="sxs-lookup"><span data-stu-id="97468-102">My.Settings Object</span></span>
<span data-ttu-id="97468-103">Stellt Eigenschaften und Methoden für den Zugriff auf die Einstellungen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="97468-103">Provides properties and methods for accessing the application's settings.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="97468-104">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97468-104">Remarks</span></span>  
 <span data-ttu-id="97468-105">Die `My.Settings` Objekt bietet Zugriff auf die Einstellungen der Anwendung und ermöglicht es Ihnen, dynamisch speichern und Abrufen von Eigenschaften und andere Informationen für Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="97468-105">The `My.Settings` object provides access to the application's settings and allows you to dynamically store and retrieve property settings and other information for your application.</span></span> <span data-ttu-id="97468-106">Weitere Informationen finden Sie unter [Verwalten von Anwendungseinstellungen (.NET)](/visualstudio/ide/managing-application-settings-dotnet).</span><span class="sxs-lookup"><span data-stu-id="97468-106">For more information, see [Managing Application Settings (.NET)](/visualstudio/ide/managing-application-settings-dotnet).</span></span>  
  
## <a name="properties"></a><span data-ttu-id="97468-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="97468-107">Properties</span></span>  
 <span data-ttu-id="97468-108">Die Eigenschaften des `My.Settings`-Objekts ermöglichen den Zugriff auf die Einstellungen Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="97468-108">The properties of the `My.Settings` object provide access to your application's settings.</span></span> <span data-ttu-id="97468-109">Verwenden Sie zum Hinzufügen oder entfernen Sie die Einstellungen, die **Einstellungs-Designer**.</span><span class="sxs-lookup"><span data-stu-id="97468-109">To add or remove settings, use the **Settings Designer**.</span></span>  
  
 <span data-ttu-id="97468-110">Jede Einstellung eine **Namen**, **Typ**, **Bereich**, und **Wert**, und diese Einstellungen bestimmen, wie die Eigenschaft auf jede Einstellung wird in der `My.Settings` Objekt:</span><span class="sxs-lookup"><span data-stu-id="97468-110">Each setting has a **Name**, **Type**, **Scope**, and **Value**, and these settings determine how the property to access each setting appears in the `My.Settings` object:</span></span>  
  
-   <span data-ttu-id="97468-111">**Namen** bestimmt den Namen der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="97468-111">**Name** determines the name of the property.</span></span>  
  
-   <span data-ttu-id="97468-112">**Typ** bestimmt den Typ der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="97468-112">**Type** determines the type of the property.</span></span>  
  
-   <span data-ttu-id="97468-113">**Bereich** gibt an, ob die Eigenschaft schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="97468-113">**Scope** indicates if the property is read-only.</span></span> <span data-ttu-id="97468-114">Wenn der Wert ist **Anwendung**, die Eigenschaft schreibgeschützt ist; wenn der Wert ist **Benutzer**, die Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="97468-114">If the value is **Application**, the property is read-only; if the value is **User**, the property is read-write.</span></span>  
  
-   <span data-ttu-id="97468-115">**Wert** ist der Standardwert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="97468-115">**Value** is the default value of the property.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="97468-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="97468-116">Methods</span></span>  
  
|<span data-ttu-id="97468-117">Methode</span><span class="sxs-lookup"><span data-stu-id="97468-117">Method</span></span>|<span data-ttu-id="97468-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97468-118">Description</span></span>|  
|---|---|  
|`Reload`|<span data-ttu-id="97468-119">Lädt die benutzereinstellungen, über die zuletzt gespeicherten Werte.</span><span class="sxs-lookup"><span data-stu-id="97468-119">Reloads the user settings from the last saved values.</span></span>|  
|`Save`|<span data-ttu-id="97468-120">Speichert die aktuellen benutzereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="97468-120">Saves the current user settings.</span></span>|  
  
 <span data-ttu-id="97468-121">Die `My.Settings` -Objekt bietet auch erweiterte Eigenschaften und Methoden, geerbt von der <xref:System.Configuration.ApplicationSettingsBase> Klasse.</span><span class="sxs-lookup"><span data-stu-id="97468-121">The `My.Settings` object also provides advanced properties and methods, inherited from the <xref:System.Configuration.ApplicationSettingsBase> class.</span></span>  
  
## <a name="tasks"></a><span data-ttu-id="97468-122">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="97468-122">Tasks</span></span>  
 <span data-ttu-id="97468-123">Die folgende Tabelle enthält Beispiele für Aufgaben im Zusammenhang mit der `My.Settings` Objekt.</span><span class="sxs-lookup"><span data-stu-id="97468-123">The following table lists examples of tasks involving the `My.Settings` object.</span></span>  
  
|<span data-ttu-id="97468-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97468-124">To</span></span>|<span data-ttu-id="97468-125">Siehe</span><span class="sxs-lookup"><span data-stu-id="97468-125">See</span></span>|  
|---|---|  
|<span data-ttu-id="97468-126">Lesen Sie eine anwendungseinstellung</span><span class="sxs-lookup"><span data-stu-id="97468-126">Read an application setting</span></span>|[<span data-ttu-id="97468-127">Vorgehensweise: Lesen von Anwendungseinstellungen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="97468-127">How to: Read Application Settings in Visual Basic</span></span>](../../../visual-basic/developing-apps/programming/app-settings/how-to-read-application-settings.md)|  
|<span data-ttu-id="97468-128">Eine benutzereinstellung ändern</span><span class="sxs-lookup"><span data-stu-id="97468-128">Change a user setting</span></span>|[<span data-ttu-id="97468-129">Vorgehensweise: Ändern von Benutzereinstellungen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="97468-129">How to: Change User Settings in Visual Basic</span></span>](../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)|  
|<span data-ttu-id="97468-130">Beibehalten von benutzereinstellungen</span><span class="sxs-lookup"><span data-stu-id="97468-130">Persist user settings</span></span>|[<span data-ttu-id="97468-131">Vorgehensweise: Beibehalten von Benutzereinstellungen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="97468-131">How to: Persist User Settings in Visual Basic</span></span>](../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)|  
|<span data-ttu-id="97468-132">Erstellen Sie ein Eigenschaftenraster für benutzereinstellungen</span><span class="sxs-lookup"><span data-stu-id="97468-132">Create a property grid for user settings</span></span>|[<span data-ttu-id="97468-133">Vorgehensweise: Erstellen von Eigenschaftenrastern für Benutzereinstellungen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="97468-133">How to: Create Property Grids for User Settings in Visual Basic</span></span>](../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)|  
  
## <a name="example"></a><span data-ttu-id="97468-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="97468-134">Example</span></span>  
 <span data-ttu-id="97468-135">In diesem Beispiel wird der Wert der `Nickname`-Einstellung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="97468-135">This example displays the value of the `Nickname` setting.</span></span>  
  
 [!code-vb[VbVbalrMyResources#14](../../../visual-basic/developing-apps/programming/app-settings/codesnippet/VisualBasic/my-settings-object_1.vb)]  
  
 <span data-ttu-id="97468-136">Damit dieses Beispiel funktioniert, muss Ihre Anwendung eine `Nickname`-Einstellung vom Typ `String` aufweisen.</span><span class="sxs-lookup"><span data-stu-id="97468-136">For this example to work, your application must have a `Nickname` setting, of type `String`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97468-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97468-137">See also</span></span>
- <xref:System.Configuration.ApplicationSettingsBase>
- [<span data-ttu-id="97468-138">Vorgehensweise: Lesen von Anwendungseinstellungen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="97468-138">How to: Read Application Settings in Visual Basic</span></span>](../../../visual-basic/developing-apps/programming/app-settings/how-to-read-application-settings.md)
- [<span data-ttu-id="97468-139">Vorgehensweise: Ändern von Benutzereinstellungen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="97468-139">How to: Change User Settings in Visual Basic</span></span>](../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)
- [<span data-ttu-id="97468-140">Vorgehensweise: Beibehalten von Benutzereinstellungen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="97468-140">How to: Persist User Settings in Visual Basic</span></span>](../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)
- [<span data-ttu-id="97468-141">Vorgehensweise: Erstellen von Eigenschaftenrastern für Benutzereinstellungen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="97468-141">How to: Create Property Grids for User Settings in Visual Basic</span></span>](../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)
- [<span data-ttu-id="97468-142">Verwalten von Anwendungseinstellungen (.NET)</span><span class="sxs-lookup"><span data-stu-id="97468-142">Managing Application Settings (.NET)</span></span>](/visualstudio/ide/managing-application-settings-dotnet)
