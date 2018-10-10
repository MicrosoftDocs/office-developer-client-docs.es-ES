---
title: RDS devuelve el error "Objeto Stream no leído"
TOCTitle: RDS Returns "Stream Not Read" Error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9b3372db2ff86ea2af401720ba091100d4cfce1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486623"
---
# <a name="rds-returns-stream-not-read-error"></a>RDS devuelve \"objeto Stream no leído\" Error


**Se aplica a**: Access 2013 | Office 2013

"El objeto Stream no se pudo leer porque está vacío o la posición actual se encuentra al final de la secuencia. Para secuencias no vacías, establezca la posición actual con la propiedad Position. Para determinar si un objeto Stream está vacío, compruebe la propiedad Size".

Si obtiene el error anterior, puede ser el resultado de intentar utilizar una consulta jerárquica parametrizada sobre http. RDS no permite enviar de forma remota jerarquías parametrizadas.

