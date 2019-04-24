---
title: Salto a un registro
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08d8a3d7b3d6012867a91aa306f45872bfebb2e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290789"
---
# <a name="jumping-to-a-record"></a>Salto a un registro


**Se aplica a:** Access 2013, Office 2013

El método [Move](move-method-ado.md) permite avanzar o retroceder un número determinado de registros en el **conjunto de registros** utilizando la sintaxis siguiente:

```vb 
 
oRs.Move NumRecords, Start
```

El método **Move** se admite en todos los objetos **Recordset**.

Si el argumento *NumRecords* es mayor que cero, la posición de registro activo avanza (hacia el final del **conjunto de registros**). Si *NumRecords* es menor que cero, la posición de registro activo retrocede (hacia el principio del **conjunto de registros**).

Si la llamada a **Move** moviese la posición del registro activo a un punto anterior al primer registro, ADO establecería el registro activo en la posición anterior al primer registro del **conjunto de registros** (**BOF** es **True**). Si se intenta retroceder cuando la propiedad **BOF** ya es **True**, se produce un error.

Si la llamada a **Move** moviese la posición del registro activo a un punto posterior al último registro, ADO establecería el registro activo en la posición posterior al último registro del **conjunto de registros** (**EOF** es **True**). Si se intenta avanzar cuando la propiedad **EOF** ya es **True**, se produce un error.

Si se llama al método **Move** desde un objeto **Recordset** vacío, se produce un error.

Si se pasa un marcador en el argumento *Start*, el desplazamiento se realiza respecto al registro con este marcador, suponiendo que el objeto **Recordset** admite marcadores. Un marcador se obtiene usando la propiedad [Bookmark](bookmark-property-ado.md). Si no se especifica, el desplazamiento se realiza respecto al registro activo.

Si se utiliza la propiedad **CacheSize** para almacenar localmente en caché registros del proveedor, el paso de un argumento *NumRecords* que mueve la posición del registro activo fuera del grupo actual de registros almacenados en caché provoca que ADO recupere un nuevo grupo de registros, a partir del registro de destino. La propiedad **CacheSize** determina el tamaño del grupo recién recuperado y el registro de destino es el primer registro recuperado.

