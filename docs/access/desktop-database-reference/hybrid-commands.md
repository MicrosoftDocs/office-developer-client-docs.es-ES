---
title: Comandos híbridos (referencia de escritorio de la base de datos de Access)
TOCTitle: Hybrid Commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa95956fb50a5cd15fa4415e65d4a701f2e48feb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485071"
---
# <a name="hybrid-commands"></a>Comandos híbridos


**Se aplica a**: Access 2013 | Office 2013

Los comandos híbridos son comandos parcialmente parametrizados. Por ejemplo:

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

El comportamiento de caché para un comando híbrido es el mismo que el de los comandos parametrizados normales.

