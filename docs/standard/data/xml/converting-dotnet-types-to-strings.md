---
title: Konvertieren von .NET Framework-Typen in Zeichenfolgen
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: dc2e2b65-f623-4dc3-938b-d2a054d6832c
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 98ebc9248b0585295adf12e04dece0fef654c2e8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54583128"
---
# <a name="converting-net-framework-types-to-strings"></a>Konvertieren von .NET Framework-Typen in Zeichenfolgen
Wenn Sie einen .NET Framework-Typ in eine Zeichenfolge konvertieren möchten, verwenden Sie die **ToString**-Methode. Die **ToString**-Methode gibt eine Zeichenfolgendarstellung des eingelesenen Typs zurück. In der folgenden Tabelle sind die .NET Framework-Typen aufgelistet, die eine Zeichenfolge in einem Format zurückgeben, das den Spezifikationen für das XML-Schema (XSD) entspricht.  
  
|.NET Framework-Typ|Zurückgegebener Zeichenfolgentyp|  
|-------------------------|--------------------------|  
|Boolesch|"true", "false"|  
|Single.PositiveInfinity|"INF"|  
|Single.NegativeInfinity|"-INF"|  
|Double.PositiveInfinity|"INF"|  
|Double.NegativeInfinity|"-INF"|  
|DateTime|Das Format ist "jjjj-mm-ddTHH:mm:sszzzzzz" und die Teilmengen davon.|  
|Timespan|Das Format lautet PnYnMnTnHnMnS. Die bedeutet für `P2Y10M15DT10H30M20S` eine Dauer von 2 Jahren, 10 Monaten, 15 Tagen, 10 Stunden, 30 Minuten und 20 Sekunden.|  
  
## <a name="see-also"></a>Siehe auch

- [Konvertierung von XML-Datentypen](../../../../docs/standard/data/xml/conversion-of-xml-data-types.md)
- [Konvertieren von Zeichenfolgen in .NET Framework-Datentypen](../../../../docs/standard/data/xml/converting-strings-to-dotnet-data-types.md)
