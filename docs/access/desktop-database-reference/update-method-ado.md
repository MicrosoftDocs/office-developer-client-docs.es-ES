---
title: Update (método, ADO)
TOCTitle: Update method (ADO)
ms:assetid: fc88cab6-c379-bb4f-530c-da08107924e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250294(v=office.15)
ms:contentKeyID: 48548893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f077634abea6fadfe5c4305fc25b28e6d57bf13e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306240"
---
# <a name="update-method-ado"></a>Update (método, ADO)

**Se aplica a:** Access 2013, Office 2013

Guarda los cambios realizados en la fila actual de un objeto [Recordset](recordset-object-ado.md) o la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxis

*objeto Recordset*. Actualizar*campos*, *valores*

*registro*. *Campos*. Actualizar

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Fields* |Es opcional. **Variant** que representa un solo nombre, o bien, matriz de tipo **Variant** que representa los nombres o las posiciones ordinales del campo o de los campos que se van a modificar.|
|*Values* |Es opcional. **Variant** que representa un solo valor, o bien, matriz de tipo **Variant** que representa los valores del campo o de los campos en el registro nuevo.|

## <a name="remarks"></a>Comentarios

### <a name="recordset"></a>Recordset

Use el método **Update** para guardar los cambios efectuados en el registro actual de un objeto **Recordset** desde la llamada al método [AddNew](addnew-method-ado.md) o desde el cambio de alguno de los valores de campo de un registro existente. El objeto **Recordset** debe ser compatible con las actualizaciones.

Para establecer los valores de campo, siga uno de estos procedimientos:

- Asigne valores a la propiedad [Value](value-property-ado.md) de un objeto [Field](field-object-ado.md) y llame al método **Update**.

- Pase un nombre de campo y un valor como argumentos con la llamada a **Update**.

- Pase una matriz de nombres de campo y una matriz de valores con la llamada a **Update**.

Cuando utiliza matrices de campos y valores, debe haber el mismo número de elementos en ambas matrices. Además, el orden de los nombres de campo debe coincidir con el orden de los valores de campo. Si no coinciden el número ni el orden de los campos y valores, se produce un error.

Si el objeto **Recordset** admite la actualización por lotes, se pueden almacenar en la memoria caché local varios cambios realizados en uno o varios registros hasta que se llama al método [UpdateBatch](updatebatch-method-ado.md). Si está modificando el registro actual o agregando un nuevo registro mientras llama al método **UpdateBatch**, ADO llamará automáticamente al método **Update** para guardar todos los cambios pendientes en el registro actual antes de transmitir al proveedor los cambios por lotes.

Si sale del registro que está agregando o editando antes de llamar al método **Update**, ADO llamará automáticamente al método **Update** para guardar los cambios. Debe llamar al método [CancelUpdate](cancelupdate-method-ado.md) si desea cancelar los cambios realizados en el registro actual o descartar un registro que acaba de agregar.

El registro actual se mantiene actual después de llamar al método **Update**.

### <a name="record"></a>Record

El método **Update** finaliza las adiciones, eliminaciones y actualizaciones realizadas en los campos de la colección [Fields](fields-collection-ado.md) de un objeto **Record**.

Por ejemplo, los campos eliminados con el método **Delete** quedan inmediatamente marcados para su eliminación pero permanecen en la colección. Es preciso llamar al método **Update** para eliminar realmente estos campos de la colección del proveedor.

