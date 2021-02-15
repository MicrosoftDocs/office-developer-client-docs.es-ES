---
title: RDS devuelve el error “Flujo no leído”
TOCTitle: RDS returns "Stream Not Read" error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0f54d8fdc7e37d0ee01f1ffd29c84a6a8ae799
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300857"
---
# <a name="rds-returns-stream-not-read-error"></a>RDS devuelve \" un error stream no leído \"


**Se aplica a:** Access 2013, Office 2013

"El objeto Stream no se pudo leer porque está vacío o la posición actual se encuentra al final de la secuencia. Para secuencias no vacías, establezca la posición actual con la propiedad Position. Para determinar si un objeto Stream está vacío, compruebe la propiedad Size".

Si obtiene el error anterior, puede ser el resultado de intentar utilizar una consulta jerárquica parametrizada sobre http. RDS no permite enviar de forma remota jerarquías parametrizadas.

