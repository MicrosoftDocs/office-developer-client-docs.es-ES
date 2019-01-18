---
title: Delete (método, Recordset de ADO)
TOCTitle: Delete method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e8142d4fc4fc0036f80693f0bff779d9f3f2a62e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702491"
---
# <a name="delete-method-ado-recordset"></a>Delete (método, Recordset de ADO)

**Se aplica a**: Access 2013, Office 2013

Elimina el registro actual o un grupo de registros.

## <a name="syntax"></a>Sintaxis

*conjunto de registros*. Eliminar *AffectRecords*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*AffectRecords* |Valor de [AffectEnum](affectenum.md) que determina cuántos registros se verán afectados por el método **Delete**. El valor predeterminado es **adAffectCurrent**.|

> [!NOTE]
> [!NOTA] **adAffectAll** y **adAffectAllChapters** no son argumentos válidos para el método **Delete**.

## <a name="remarks"></a>Comentarios

Si usa el método **Delete**, el registro actual o un grupo de registros de un objeto [Recordset](recordset-object-ado.md) quedan marcados para su eliminación. Si el objeto **Recordset** no permite la eliminación de sus registros, se produce un error. Si se encuentra en modo de actualización inmediata, la eliminación se lleva a cabo inmediatamente en la base de datos. Si un registro no puede eliminarse correctamente (debido, por ejemplo, a infracciones de la integridad de la base de datos), el registro permanecerá en modo de edición tras llamar a **Update**. Esto significa que debe cancelar la actualización con [CancelUpdate](cancelupdate-method-ado.md) antes de salir del registro actual (por ejemplo, con [Close](close-method-ado.md), [Move](move-method-ado.md) o [NextRecordset](nextrecordset-method-ado.md)).

Si se encuentra en modo de actualización por lotes, los registros se marcan para su eliminación de la caché y la eliminación se produce realmente al llamar al método [UpdateBatch](updatebatch-method-ado.md). (Utilice la propiedad [Filter](filter-property-ado.md) para ver los registros eliminados.)

Si recupera valores de campo del registro eliminado, se genera un error. Tras eliminar el registro actual, el registro eliminado permanece actual hasta que se mueva a otro registro. Cuando salga del registro eliminado, ya no podrá obtener acceso al mismo.

Si anida eliminaciones en una transacción, podrá recuperar los registros eliminados con el método [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si está en modo de actualización por lotes, podrá cancelar una eliminación pendiente o un grupo de eliminaciones pendientes con el método [CancelBatch](cancelbatch-method-ado.md).

Si un intento de eliminar registros genera un error debido a un conflicto con los datos subyacentes (por ejemplo, un registro ya ha sido eliminado anteriormente por otro usuario), el proveedor devuelve advertencias a la colección [Errors](errors-collection-ado.md) pero no detiene la ejecución del programa. Se produce un error en tiempo de ejecución solo si hay conflictos en todos los registros solicitados.

Si está establecida la propiedad dinámica [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) y el objeto **Recordset** es el resultado de la ejecución de una operación JOIN en varias tablas, el método **Delete** eliminará únicamente las filas de la tabla especificada en la propiedad [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).

