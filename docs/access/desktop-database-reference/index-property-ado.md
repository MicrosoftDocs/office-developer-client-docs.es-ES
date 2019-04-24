---
title: Index (propiedad, ADO)
TOCTitle: Index property (ADO)
ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15)
ms:contentKeyID: 48544715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d436ec9102c4c75688b6c6ac973ca85e8c280d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291709"
---
# <a name="index-property-ado"></a>Index (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el nombre del índice en vigor para un objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Valores de configuración y devueltos

Establece o devuelve un valor de tipo **String** que es el nombre del índice.

## <a name="remarks"></a>Comentarios

El índice denominado por la propiedad **Index** debe haber sido declarado previamente en la tabla base subyacente al objeto **Recordset**. Es decir, el índice debe haber sido declarado mediante programación como un objeto [Index](index-object-adox.md) de ADOX o al crear la tabla base.

Si no se puede establecer el índice, se producirá un error en tiempo de ejecución. No se puede establecer la propiedad **Index**:

  - En un controlador de eventos [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) o **RecordsetChangeComplete**.

  - Si el objeto **Recordset** sigue ejecutando una operación (lo que se determina mediante la propiedad [Estado (State)](state-property-ado.md)).

  - Si se ha establecido un filtro en el objeto **Recordset** con la propiedad [Filter](filter-property-ado.md).

La propiedad **Index** siempre se puede establecer correctamente si el objeto **Recordset** está cerrado; sin embargo, el objeto **Recordset** no se abrirá correctamente o el índice no será útil si el proveedor subyacente no admite índices.

Si se puede establecer el índice, la posición actual de la fila puede cambiar. Eso provocará una actualización de la propiedad [AbsolutePosition](absoluteposition-property-ado.md), así como la generación de eventos **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md) y [MoveComplete](willmove-and-movecomplete-events-ado.md).

Si es posible establecer el índice y la propiedad [LockType](locktype-property-ado.md) es **adLockPessimistic** o **adLockOptimistic**, se realiza una operación implícita [UpdateBatch](updatebatch-method-ado.md). Eso libera al grupo actual y a los afectados. Se liberan todos los filtros existentes y la posición actual de la fila se cambia por la primera fila del reordenado objeto **Recordset**.

La propiedad **Index** se usa junto con el método [Seek](seek-method-ado.md). Si el proveedor subyacente no es compatible con la propiedad **Index** ni con el método **Seek**, considere la posibilidad de usar el método [Find](find-method-ado.md) en su lugar. DeTermine si el objeto **Recordset** admite índices con el método [Supports](supports-method-ado.md)**(adIndex)** .

La propiedad integrada **Index** no está relacionada con la propiedad dinámica [Optimize](optimize-property-dynamic-ado.md), aunque ambas tienen que ver con los índices.

