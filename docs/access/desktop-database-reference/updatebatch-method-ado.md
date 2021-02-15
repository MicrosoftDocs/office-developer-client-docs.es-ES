---
title: Método UpdateBatch (ADO)
TOCTitle: UpdateBatch method (ADO)
ms:assetid: 69e72a65-b637-36fd-d09f-7f81050f71ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249416(v=office.15)
ms:contentKeyID: 48545420
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9d269a9012588a7b82505ac2e28466151715cbb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313579"
---
# <a name="updatebatch-method-ado"></a>UpdateBatch (método, ADO)

**Se aplica a:** Access 2013, Office 2013

Escribe en el disco todas las actualizaciones por lotes que están pendientes.

## <a name="syntax"></a>Sintaxis

*recordset*. UpdateBatch *AffectRecords*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*AffectRecords* |Es opcional. Valor de [AffectEnum](affectenum.md) que indica el número de registros afectados por el método **UpdateBatch**.|

## <a name="remarks"></a>Comentarios

Use el método **UpdateBatch** cuando modifique un objeto **Recordset** en modo de actualización por lotes para transmitir todos los cambios realizados en el objeto **Recordset** a la base de datos subyacente.

Si el objeto **Recordset** admite la actualización por lotes, se pueden almacenar en la memoria caché local varios cambios realizados en uno o varios registros hasta que se llama al método **UpdateBatch**. Si está modificando el registro actual o agregando un nuevo registro mientras llama al método **UpdateBatch**, ADO llamará automáticamente al método [Update](update-method-ado.md) para guardar todos los cambios pendientes en el registro actual antes de transmitir al proveedor los cambios por lotes. La actualización por lotes debe utilizarse únicamente con un cursor estático o un cursor dirigido por un conjunto de claves.

> [!NOTE]
> Si se especifica **adAffectGroup** como valor para este parámetro, se producirá un error cuando no haya registros visibles en el actual objeto **Recordset** (como un filtro sin registros coincidentes).

Si un intento de transmitir los cambios de algunos o todos los registros genera un error debido a un conflicto con los datos subyacentes (por ejemplo, otro usuario ya ha eliminado un registro), el proveedor devuelve advertencias a la colección [Errors](errors-collection-ado.md) y se genera un error en tiempo de ejecución. Utilice la propiedad [Filter](filter-property-ado.md) (**adFilterAffectedRecords**) y la propiedad [Status](status-property-ado-recordset.md) para localizar los registros con conflictos.

Para cancelar todas las actualizaciones por lotes que estén pendientes, utilice el método [CancelBatch](cancelbatch-method-ado.md).

Si están establecidas las propiedades dinámicas [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) y [Update Resync](update-resync-property-dynamic-ado.md), y el objeto **Recordset** es el resultado de la ejecución de una operación JOIN en varias tablas, la ejecución del método **UpdateBatch** va implícitamente seguida del método [Resync](resync-method-ado.md), según el valor de la propiedad **Update Resync**.

El orden en que se ejecutan las actualizaciones individuales de un lote en el origen de datos no es necesariamente el mismo orden en que se realizan en el objeto **Recordset** local. El orden de actualización depende del proveedor. Téngalo en cuenta cuando codifique actualizaciones relacionadas entre sí, como las restricciones de clave externa en una inserción o una actualización.

