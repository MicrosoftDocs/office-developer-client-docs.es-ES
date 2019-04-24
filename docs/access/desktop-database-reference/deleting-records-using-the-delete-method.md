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
# <a name="deleting-records-using-the-delete-method"></a><span data-ttu-id="c3702-102">Eliminación de registros utilizando el método Delete</span><span class="sxs-lookup"><span data-stu-id="c3702-102">Deleting records using the Delete method</span></span>


<span data-ttu-id="c3702-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c3702-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c3702-p101">Con el método **Delete**, se marca el registro activo o un grupo de registros de un objeto **Recordset** para su eliminación. Si el objeto **Recordset** no admite la eliminación de registros, se produce un error. En modo de actualización inmediata, las eliminaciones se producen en la base de datos directamente. Si no se consigue eliminar un registro (debido a infracciones de la integridad de la base de datos, por ejemplo), el registro permanecerá en modo de edición después de la llamada a **Update**. Esto significa que se debe cancelar la actualización mediante [CancelUpdate](cancelupdate-method-ado.md) antes de abandonar el registro activo (por ejemplo, usando [Close](close-method-ado.md), [Move](move-method-ado.md) o [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="c3702-p101">Using the **Delete** method marks the current record or a group of records in a **Recordset** object for deletion. If the **Recordset** object does not allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**. This means that you must cancel the update using [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, using [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="c3702-p102">En modo de actualización por lotes, los registros se marcan para eliminación de la caché y la eliminación real ocurre cuando se llama al método **UpdateBatch** (para ver los registros eliminados, establezca la propiedad **Filter** en **adFilterAffectedRecords** después de llamar a **Delete** ).</span><span class="sxs-lookup"><span data-stu-id="c3702-p102">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the **UpdateBatch** method. (To view the deleted records, set the **Filter** property to **adFilterAffectedRecords** after **Delete** is called.)</span></span>

<span data-ttu-id="c3702-p103">Si intenta recuperar valores de campos del registro eliminado, se producirá un error. Después de eliminar el registro activo, el registro eliminado seguirá siendo el activo hasta que se mueva a otro registro. Cuando abandone el registro eliminado, ya no se podrá volver a obtener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="c3702-p103">Attempting to retrieve field values from the deleted record generates an error. After deleting the current record, the deleted record remains current until you move to a different record. Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="c3702-p104">Si anida eliminaciones en una transacción, puede recuperar registros eliminados utilizando el método **RollbackTrans**. En modo de actualización por lotes, puede cancelar una eliminación pendiente o un grupo de eliminaciones pendientes mediante el método **CancelBatch**.</span><span class="sxs-lookup"><span data-stu-id="c3702-p104">If you nest deletions in a transaction, you can recover deleted records by using the **RollbackTrans** method. If you are in batch update mode, you can cancel a pending deletion or group of pending deletions by using the **CancelBatch** method.</span></span>

<span data-ttu-id="c3702-p105">Si el intento de eliminar registros falla debido a un conflicto con los datos subyacentes (por ejemplo, que un registro ya haya sido eliminado por otro usuario), el proveedor devuelve advertencias a la colección **Errors**, pero no detiene la ejecución del programa. Sólo se produce un error en tiempo de ejecución si hay conflictos con todos los registros solicitados.</span><span class="sxs-lookup"><span data-stu-id="c3702-p105">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the **Errors** collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="c3702-118">Si se ha establecido la propiedad dinámica **Tabla única** y el **conjunto de registros** es el resultado de ejecutar una operación JOIN en varias tablas, el método **Delete** sólo eliminará filas de la tabla mencionada en la propiedad **Tabla única**.</span><span class="sxs-lookup"><span data-stu-id="c3702-118">If the **Unique Table** dynamic property is set and the **Recordset** is the result of executing a JOIN operation on multiple tables, the **Delete** method will delete rows only from the table named in the **Unique Table** property.</span></span>

<span data-ttu-id="c3702-p106">El método **Delete** toma un argumento opcional que permite especificar a qué registros afecta la operación **Delete**. Los únicos valores válidos para este argumento son las constantes enumeradas **AffectEnum** de ADO siguientes:</span><span class="sxs-lookup"><span data-stu-id="c3702-p106">The **Delete** method takes an optional argument that allows you to specify which records are affected by the **Delete** operation. The only valid values for this argument are either of the following ADO **AffectEnum** enumerated constants:</span></span>

  - <span data-ttu-id="c3702-121">**adAffectCurrent** Afecta sólo al registro actual.</span><span class="sxs-lookup"><span data-stu-id="c3702-121">**adAffectCurrent**Affects only the current record.</span></span>

  - <span data-ttu-id="c3702-122">**adAffectGroup** Afecta sólo a los registros que cumplen la configuración actual de la propiedad **Filter** .</span><span class="sxs-lookup"><span data-stu-id="c3702-122">**adAffectGroup**Affects only records that satisfy the current **Filter** property setting.</span></span> <span data-ttu-id="c3702-123">The **Filter** property must be set to a **FilterGroupEnum** value or an array of **Bookmarks** to use this option.</span><span class="sxs-lookup"><span data-stu-id="c3702-123">The **Filter** property must be set to a **FilterGroupEnum** value or an array of **Bookmarks** to use this option.</span></span>

<span data-ttu-id="c3702-p108">El código siguiente muestra un ejemplo de especificación de **adAffectGroup** cuando se llama al método **Delete**. En este ejemplo, se agregan algunos registros al **conjunto de registros** de ejemplo y se actualiza la base de datos. Después, se filtra el **conjunto de registros** utilizando la constante enumerada de filtro **adFilterAffectedRecords**, que sólo deja visibles los registros recién agregados en el **conjunto de registros**. Por último, llama al método **Delete** y especifica que se deben eliminar todos los registros que satisfagan la configuración activa de la propiedad **Filter** (los nuevos registros).</span><span class="sxs-lookup"><span data-stu-id="c3702-p108">The following code shows an example of specifying **adAffectGroup** when calling the **Delete** method. This example adds some records to the sample **Recordset** and updates the database. Then it filters the **Recordset** using the **adFilterAffectedRecords** filter enumerated constant, which leaves only the newly added records visible in the **Recordset**. Finally, it calls the **Delete** method and specifies that all of the records that satisfy the current **Filter** property setting (the new records) should be deleted.</span></span>

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

