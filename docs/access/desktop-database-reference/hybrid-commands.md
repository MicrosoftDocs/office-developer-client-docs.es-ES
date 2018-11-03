---
title: Comandos híbridos (referencia de escritorio de la base de datos de Access)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 046d005eb4a9e1c8097908e0104b8d1e5c76e2af
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946919"
---
# <a name="hybrid-commands"></a><span data-ttu-id="2c800-102">Comandos híbridos</span><span class="sxs-lookup"><span data-stu-id="2c800-102">Hybrid commands</span></span>


<span data-ttu-id="2c800-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c800-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c800-p101">Los comandos híbridos son comandos parcialmente parametrizados. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2c800-p101">Hybrid commands are partially parameterized commands. For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="2c800-106">El comportamiento de caché para un comando híbrido es el mismo que el de los comandos parametrizados normales.</span><span class="sxs-lookup"><span data-stu-id="2c800-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

