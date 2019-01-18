---
title: Comandos híbridos (referencia de escritorio de la base de datos de Access)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fe3e6d0afbba82cacd5a55c630f1ca41f3e318a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709155"
---
# <a name="hybrid-commands"></a><span data-ttu-id="b46c6-102">Comandos híbridos</span><span class="sxs-lookup"><span data-stu-id="b46c6-102">Hybrid commands</span></span>


<span data-ttu-id="b46c6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b46c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b46c6-p101">Los comandos híbridos son comandos parcialmente parametrizados. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b46c6-p101">Hybrid commands are partially parameterized commands. For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="b46c6-106">El comportamiento de caché para un comando híbrido es el mismo que el de los comandos parametrizados normales.</span><span class="sxs-lookup"><span data-stu-id="b46c6-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

