---
title: Methodenparameter – C#-Referenz
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- methods [C#], parameters
- method parameters [C#]
- parameters [C#]
ms.assetid: 680e39ff-775b-48b0-9f47-4186a5bfc4a1
ms.openlocfilehash: 72917d356ed0fce96502faeef68494c7fdcb214f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564759"
---
# <a name="method-parameters-c-reference"></a>Methodenparameter (C#-Referenz)

Parameter, die ohne [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) oder [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) für eine Methode deklariert werden, werden nach Werten an die aufgerufene Methode übergeben. Dieser Wert kann in der Methode geändert werden, aber der geänderte Wert wird nicht gespeichert, wenn die aufrufende Prozedur wieder die Steuerung übernimmt. Wenn Sie ein Schlüsselwort für einen Methodenparameter verwenden, können Sie dieses Verhalten ändern.  
  
 In diesem Abschnitt wird das Schlüsselwort beschrieben, dass Sie verwenden können, wenn Sie Methodenparameter deklarieren.  
  
-   Mit [params](../../../csharp/language-reference/keywords/params.md) wird festgelegt, dass für diesen Parameter eine veränderliche Anzahl von Argumenten akzeptiert werden.
  
-   Mit [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md) wird festgelegt, dass dieser Parameter als Verweis übergeben wird, jedoch nur von der aufgerufenen Methode gelesen wird.
  
-   Mit [ref](../../../csharp/language-reference/keywords/ref.md) wird festgelegt, dass dieser Parameter als Verweis übergeben wird und von der aufgerufenen Methode gelesen oder geschrieben werden kann.
  
-   Mit [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) wird festgelegt, dass dieser Parameter als Verweis übergeben wird und von der aufgerufenen Methode geschrieben wird.
  
## <a name="see-also"></a>Siehe auch

- [C#-Referenz](../../../csharp/language-reference/index.md)
- [C#-Programmierhandbuch](../../../csharp/programming-guide/index.md)
- [C#-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)
