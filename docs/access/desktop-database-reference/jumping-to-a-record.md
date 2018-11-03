---
title: Saltar a un registro
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9ce27722600ae8a634092612ddf11694faa4ecef
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944476"
---
# <a name="jumping-to-a-record"></a>Saltar a un registro


**Se aplica a**: Access 2013, Office 2013

El método [Move](move-method-ado.md) permite avanzar o retroceder un número determinado de registros en el **conjunto de registros** utilizando la sintaxis siguiente:

```vb 
 
oRs.Move NumRecords, Start
```

El método **Move** se admite en todos los objetos **Recordset**.

Si el argumento *NumRecords* es mayor que cero, la posición de registro activo avanza (hacia el final del **conjunto de registros**). Si *NumRecords* es menor que cero, la posición de registro activo retrocede (hacia el principio del **conjunto de registros**).

Si la llamada a **Move** moviese la posición del registro activo a un punto anterior al primer registro, ADO establecería el registro activo en la posición anterior al primer registro del **conjunto de registros** (**BOF** es **True**). Si se intenta retroceder cuando la propiedad **BOF** ya es **True**, se produce un error.

Si la llamada a **Move** moviese la posición del registro activo a un punto posterior al último registro, ADO establecería el registro activo en la posición posterior al último registro del **conjunto de registros** (**EOF** es **True**). Si se intenta avanzar cuando la propiedad **EOF** ya es **True**, se produce un error.

Si se llama a **Move** desde un objeto **Recordset** vacío, se genera un error.

Si se pasa un marcador en el argumento *Start* , el movimiento es respecto al registro con este marcador, suponiendo que el objeto **Recordset** admite marcadores. Un marcador se obtiene usando la propiedad [Bookmark](bookmark-property-ado.md). Si no se especifica, el desplazamiento se realiza respecto al registro activo.

Si se utiliza la propiedad **CacheSize** para localmente en caché registros del proveedor, pasando un argumento *NumRecords* que mueve la posición de registro actual fuera del actual grupo de registros almacenados en caché obliga a ADO para recuperar un nuevo grupo de registros, empezando por el registro de destino. La propiedad **CacheSize** determina el tamaño del grupo recién recuperado y el registro de destino es el primer registro recuperado.

