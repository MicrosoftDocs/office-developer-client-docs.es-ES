---
title: Eliminación de registros utilizando el método Delete
TOCTitle: Deleting records using the Delete method
ms:assetid: 22917c33-4d14-ebab-d85c-2cbe7f68c560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249003(v=office.15)
ms:contentKeyID: 48543708
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a476e9bc57224b0e46afb31bf092450c26de0a17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293969"
---
# <a name="deleting-records-using-the-delete-method"></a>Eliminación de registros utilizando el método Delete


**Se aplica a:** Access 2013, Office 2013

Con el método **Delete**, se marca el registro activo o un grupo de registros de un objeto **Recordset** para su eliminación. Si el objeto **Recordset** no admite la eliminación de registros, se produce un error. En modo de actualización inmediata, las eliminaciones se producen en la base de datos directamente. Si no se consigue eliminar un registro (debido a infracciones de la integridad de la base de datos, por ejemplo), el registro permanecerá en modo de edición después de la llamada a **Update**. Esto significa que se debe cancelar la actualización mediante [CancelUpdate](cancelupdate-method-ado.md) antes de abandonar el registro activo (por ejemplo, usando [Close](close-method-ado.md), [Move](move-method-ado.md) o [NextRecordset](nextrecordset-method-ado.md)).

En modo de actualización por lotes, los registros se marcan para eliminación de la caché y la eliminación real ocurre cuando se llama al método **UpdateBatch** (para ver los registros eliminados, establezca la propiedad **Filter** en **adFilterAffectedRecords** después de llamar a **Delete** ).

Si intenta recuperar valores de campos del registro eliminado, se producirá un error. Después de eliminar el registro activo, el registro eliminado seguirá siendo el activo hasta que se mueva a otro registro. Cuando abandone el registro eliminado, ya no se podrá volver a obtener acceso a él.

Si anida eliminaciones en una transacción, puede recuperar registros eliminados utilizando el método **RollbackTrans**. En modo de actualización por lotes, puede cancelar una eliminación pendiente o un grupo de eliminaciones pendientes mediante el método **CancelBatch**.

Si el intento de eliminar registros falla debido a un conflicto con los datos subyacentes (por ejemplo, que un registro ya haya sido eliminado por otro usuario), el proveedor devuelve advertencias a la colección **Errors**, pero no detiene la ejecución del programa. Sólo se produce un error en tiempo de ejecución si hay conflictos con todos los registros solicitados.

Si se ha establecido la propiedad dinámica **Tabla única** y el **conjunto de registros** es el resultado de ejecutar una operación JOIN en varias tablas, el método **Delete** sólo eliminará filas de la tabla mencionada en la propiedad **Tabla única**.

El método **Delete** toma un argumento opcional que permite especificar a qué registros afecta la operación **Delete**. Los únicos valores válidos para este argumento son las constantes enumeradas **AffectEnum** de ADO siguientes:

  - **adAffectCurrent** Afecta sólo al registro actual.

  - **adAffectGroup** Afecta solo a los registros que satisfacen el valor de **la propiedad Filter** actual. The **Filter** property must be set to a **FilterGroupEnum** value or an array of **Bookmarks** to use this option.

El código siguiente muestra un ejemplo de especificación de **adAffectGroup** cuando se llama al método **Delete**. En este ejemplo, se agregan algunos registros al **conjunto de registros** de ejemplo y se actualiza la base de datos. Después, se filtra el **conjunto de registros** utilizando la constante enumerada de filtro **adFilterAffectedRecords**, que sólo deja visibles los registros recién agregados en el **conjunto de registros**. Por último, llama al método **Delete** y especifica que se deben eliminar todos los registros que satisfagan la configuración activa de la propiedad **Filter** (los nuevos registros).

```vb 
 
'BeginDeleteGroup 
 'add some bogus records 
 With objRs1 
 For i = 0 To 8 
 .AddNew 
 .Fields("CompanyName") = "Shipper Number " & i + 1 
 .Fields("Phone") = "(425) 555-000" & (i + 1) 
 .Update 
 Next i 
 
 're-connect & update 
 .ActiveConnection = GetNewConnection 
 .UpdateBatch 
 
 'filter on newly added records 
 .Filter = adFilterAffectedRecords 
 Debug.Print "Deleting the " & .RecordCount & _ 
 " records you just added." 
 
 'delete the newly added bogus records 
 .Delete adAffectGroup 
 .Filter = adFilterNone 
 Debug.Print .RecordCount & " records remain." 
 
 .Close 
 End With 
'EndDeleteGroup 
```

