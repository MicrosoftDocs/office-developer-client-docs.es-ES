---
title: RDS devuelve el error "Objeto Stream no leído"
TOCTitle: RDS returns "Stream Not Read" error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 56bd90daef7b7571d8f0c6adca239ef24955f65a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944630"
---
# <a name="rds-returns-stream-not-read-error"></a><span data-ttu-id="04ec1-102">RDS devuelve \"Stream no leído\" error</span><span class="sxs-lookup"><span data-stu-id="04ec1-102">RDS returns \"Stream Not Read\" error</span></span>


<span data-ttu-id="04ec1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04ec1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04ec1-p101">"El objeto Stream no se pudo leer porque está vacío o la posición actual se encuentra al final de la secuencia. Para secuencias no vacías, establezca la posición actual con la propiedad Position. Para determinar si un objeto Stream está vacío, compruebe la propiedad Size".</span><span class="sxs-lookup"><span data-stu-id="04ec1-p101">"The Stream object could not be read because it is empty, or the current position is at the end of the Stream. For non-empty Streams, set the current position with the Position property. To determine if a Stream is empty, check the Size property."</span></span>

<span data-ttu-id="04ec1-p102">Si obtiene el error anterior, puede ser el resultado de intentar utilizar una consulta jerárquica parametrizada sobre http. RDS no permite enviar de forma remota jerarquías parametrizadas.</span><span class="sxs-lookup"><span data-stu-id="04ec1-p102">If you get the error above, it may be a result of trying to use a parameterized hierarchical query over http. RDS does not permit you to remote parameterized hierarchies.</span></span>

