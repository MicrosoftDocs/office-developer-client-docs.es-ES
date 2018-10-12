---
title: Delete (método, objeto Recordset de ADO)
TOCTitle: Delete Method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 118cc56bf33812819dd34089ac97c72259228f4c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485716"
---
# <a name="delete-method-ado-recordset"></a><span data-ttu-id="d569a-102">Delete (método, objeto Recordset de ADO)</span><span class="sxs-lookup"><span data-stu-id="d569a-102">Delete Method (ADO Recordset)</span></span>


<span data-ttu-id="d569a-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d569a-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="d569a-104">Elimina el registro actual o un grupo de registros.</span><span class="sxs-lookup"><span data-stu-id="d569a-104">Deletes the current record or a group of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="d569a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d569a-105">Syntax</span></span>

<span data-ttu-id="d569a-106">*conjunto de registros*. Eliminar *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="d569a-106">*recordset*.Delete *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="d569a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d569a-107">Parameters</span></span>

  - <span data-ttu-id="d569a-108">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="d569a-108">*AffectRecords*</span></span>

  - <span data-ttu-id="d569a-p101">Valor de [AffectEnum](affectenum.md) que determina cuántos registros se verán afectados por el método **Delete**. El valor predeterminado es **adAffectCurrent**.</span><span class="sxs-lookup"><span data-stu-id="d569a-p101">An [AffectEnum](affectenum.md) value that determines how many records the **Delete** method will affect. The default value is **adAffectCurrent**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d569a-111">[!NOTA] <STRONG>adAffectAll</STRONG> y <STRONG>adAffectAllChapters</STRONG> no son argumentos válidos para el método <STRONG>Delete</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d569a-111"><STRONG>adAffectAll</STRONG> and <STRONG>adAffectAllChapters</STRONG> are not valid arguments to <STRONG>Delete</STRONG>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="d569a-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d569a-112">Remarks</span></span>

<span data-ttu-id="d569a-p102">Si usa el método **Delete**, el registro actual o un grupo de registros de un objeto [Recordset](recordset-object-ado.md) quedan marcados para su eliminación. Si el objeto **Recordset** no permite la eliminación de sus registros, se produce un error. Si se encuentra en modo de actualización inmediata, la eliminación se lleva a cabo inmediatamente en la base de datos. Si un registro no puede eliminarse correctamente (debido, por ejemplo, a infracciones de la integridad de la base de datos), el registro permanecerá en modo de edición tras llamar a **Update**. Esto significa que debe cancelar la actualización con [CancelUpdate](cancelupdate-method-ado.md) antes de salir del registro actual (por ejemplo, con [Close](close-method-ado.md), [Move](move-method-ado.md) o [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="d569a-p102">Using the **Delete** method marks the current record or a group of records in a [Recordset](recordset-object-ado.md) object for deletion. If the **Recordset** object doesn't allow record deletion, an error occurs. If you are in immediate update mode, deletions occur in the database immediately. If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**. This means that you must cancel the update with [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, with [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="d569a-p103">Si se encuentra en modo de actualización por lotes, los registros se marcan para su eliminación de la caché y la eliminación se produce realmente al llamar al método [UpdateBatch](updatebatch-method-ado.md). (Utilice la propiedad [Filter](filter-property-ado.md) para ver los registros eliminados.)</span><span class="sxs-lookup"><span data-stu-id="d569a-p103">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the [UpdateBatch](updatebatch-method-ado.md) method. (Use the [Filter](filter-property-ado.md) property to view the deleted records.)</span></span>

<span data-ttu-id="d569a-p104">Si recupera valores de campo del registro eliminado, se genera un error. Tras eliminar el registro actual, el registro eliminado permanece actual hasta que se mueva a otro registro. Cuando salga del registro eliminado, ya no podrá obtener acceso al mismo.</span><span class="sxs-lookup"><span data-stu-id="d569a-p104">Retrieving field values from the deleted record generates an error. After deleting the current record, the deleted record remains current until you move to a different record. Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="d569a-p105">Si anida eliminaciones en una transacción, podrá recuperar los registros eliminados con el método [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si está en modo de actualización por lotes, podrá cancelar una eliminación pendiente o un grupo de eliminaciones pendientes con el método [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d569a-p105">If you nest deletions in a transaction, you can recover deleted records with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If you are in batch update mode, you can cancel a pending deletion or group of pending deletions with the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="d569a-p106">Si un intento de eliminar registros genera un error debido a un conflicto con los datos subyacentes (por ejemplo, un registro ya ha sido eliminado anteriormente por otro usuario), el proveedor devuelve advertencias a la colección [Errors](errors-collection-ado.md) pero no detiene la ejecución del programa. Se produce un error en tiempo de ejecución solo si hay conflictos en todos los registros solicitados.</span><span class="sxs-lookup"><span data-stu-id="d569a-p106">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="d569a-127">Si está establecida la propiedad dinámica [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) y el objeto **Recordset** es el resultado de la ejecución de una operación JOIN en varias tablas, el método **Delete** eliminará únicamente las filas de la tabla especificada en la propiedad [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d569a-127">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property is set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Delete** method will only delete rows from the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) property.</span></span>
