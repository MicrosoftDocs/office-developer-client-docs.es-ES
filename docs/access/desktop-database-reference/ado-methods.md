---
title: Métodos de ActiveX Data Objects (ADO)
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3169b7eaab6ad290bfc385881f5de69edc80111f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283285"
---
# <a name="ado-methods"></a><span data-ttu-id="a1927-102">Métodos de ADO</span><span class="sxs-lookup"><span data-stu-id="a1927-102">ADO methods</span></span>

<span data-ttu-id="a1927-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1927-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="a1927-104">Método</span><span class="sxs-lookup"><span data-stu-id="a1927-104">Method</span></span></th>
<th><span data-ttu-id="a1927-105">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1927-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-106"><a href="addnew-method-ado.md">Funcionan</a></span><span class="sxs-lookup"><span data-stu-id="a1927-106"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-107">Crea un registro nuevo para un objeto <strong> Recordset</strong> actualizable.</span><span class="sxs-lookup"><span data-stu-id="a1927-107">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-108"><a href="append-method-ado.md">Append</a></span><span class="sxs-lookup"><span data-stu-id="a1927-108"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-p101">Anexa un objeto a una colección. Si la colección es <strong>Fields</strong>, se puede crear un nuevo objeto <strong>Field</strong> antes de anexarlo a la colección.</span><span class="sxs-lookup"><span data-stu-id="a1927-p101">Appends an object to a collection. If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="a1927-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-112">Anexa datos a un objeto <strong>Field</strong> de datos binarios o texto grande, o a un objeto <strong>Parameter</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-112">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans y RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="a1927-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-114">Administra el procesamiento de transacciones dentro de un objeto <strong>Connection</strong> del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="a1927-114">Manages transaction processing within a <strong>Connection</strong> object as follows:</span></span><br/><br/><span data-ttu-id="a1927-115"><strong>BeginTrans</strong>: inicia una transacción nueva.</span><span class="sxs-lookup"><span data-stu-id="a1927-115"><strong>BeginTrans</strong> — Begins a new transaction.</span></span><br/><br/><span data-ttu-id="a1927-p102">
<strong>CommitTrans</strong>: guarda los cambios y termina la transacción actual. También puede iniciar una transacción nueva.</span><span class="sxs-lookup"><span data-stu-id="a1927-p102">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span><br/><br/><span data-ttu-id="a1927-118">
<strong>RollbackTrans</strong> : cancela los cambios y finaliza la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="a1927-118">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="a1927-119">También puede iniciar una transacción nueva.</span><span class="sxs-lookup"><span data-stu-id="a1927-119">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-120"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="a1927-120"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-121">Cancela la ejecución de una llamada de método asincrónico pendiente.</span><span class="sxs-lookup"><span data-stu-id="a1927-121">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="a1927-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-123">Cancela una actualización por lotes que está pendiente.</span><span class="sxs-lookup"><span data-stu-id="a1927-123">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="a1927-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-125">Cancela cualquier cambio realizado en la fila activa o nueva de un objeto <strong>Recordset</strong>, o la colección <strong>Fields</strong> de un objeto <strong>Recordset</strong>, antes de llamar al método <strong>Update</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-125">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-126"><a href="clear-method-ado.md">Clear</a></span><span class="sxs-lookup"><span data-stu-id="a1927-126"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-127">Quita todos los objetos <strong>Error</strong> de la colección <strong>Errors</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-127">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-128"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="a1927-128"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-129">Crea un objeto <strong>Recordset</strong> duplicado a partir de un objeto <strong>Recordset</strong> existente.</span><span class="sxs-lookup"><span data-stu-id="a1927-129">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object.</span></span> <span data-ttu-id="a1927-130">Opcionalmente, especifica que el duplicado es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a1927-130">Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-131"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="a1927-131"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-132">Cierra un objeto abierto y cualquier objeto dependiente.</span><span class="sxs-lookup"><span data-stu-id="a1927-132">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="a1927-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-134">Compara dos marcadores y devuelve una indicación de sus valores relativos.</span><span class="sxs-lookup"><span data-stu-id="a1927-134">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="a1927-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-136">Copia un archivo o directorio y su contenidos en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="a1927-136">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-137"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="a1927-137"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-138">Copia el número especificado de caracteres o bytes (según <strong>Type</strong>) del objeto <strong>Stream</strong> en otro objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-138">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-139"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="a1927-139"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-140">Crea un objeto <strong>Parameter</strong> nuevo con las propiedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="a1927-140">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-141"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span><span class="sxs-lookup"><span data-stu-id="a1927-141"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-142">Elimina un objeto de la colección <strong>Parameters</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-142">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-143"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span><span class="sxs-lookup"><span data-stu-id="a1927-143"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-144">Elimina un objeto de la colección <strong>Fields</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-144">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-145"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span><span class="sxs-lookup"><span data-stu-id="a1927-145"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-146">Elimina el registro actual o un grupo de registros.</span><span class="sxs-lookup"><span data-stu-id="a1927-146">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="a1927-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-148">Elimina un archivo o directorio y todos sus subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="a1927-148">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO Command)</a></span><span class="sxs-lookup"><span data-stu-id="a1927-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-150">Ejecuta la consulta, la instrucción SQL o el procedimiento almacenado especificado en la propiedad <strong>CommandText</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-150">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO Connection)</a></span><span class="sxs-lookup"><span data-stu-id="a1927-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-152">Ejecuta la consulta especificada, la instrucción SQL, el procedimiento almacenado o el texto específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a1927-152">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-153"><a href="find-method-ado.md">Find</a></span><span class="sxs-lookup"><span data-stu-id="a1927-153"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-154">Busca en un objeto <strong>Recordset</strong> la fila que cumple los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="a1927-154">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-155"><a href="flush-method-ado.md">Limpia</a></span><span class="sxs-lookup"><span data-stu-id="a1927-155"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-156">Vacía el contenido del objeto <strong>Stream</strong> que queda en el búfer de ADO y lo introduce en el objeto subyacente con el que el <strong>Stream</strong> está asociado.</span><span class="sxs-lookup"><span data-stu-id="a1927-156">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-157"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="a1927-157"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-158">Devuelve un objeto <strong>Recordset</strong> cuyas filas representan los archivos y los subdirectorios del directorio representado por este <strong>registro</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-158">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-159"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="a1927-159"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-160">Devuelve todo o parte del contenido de un objeto <strong>Field</strong> de datos binarios o de texto grande.</span><span class="sxs-lookup"><span data-stu-id="a1927-160">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-161"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="a1927-161"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-162">Recupera varios registros de un objeto <strong>Recordset</strong> y los inserta en una matriz.</span><span class="sxs-lookup"><span data-stu-id="a1927-162">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-163"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="a1927-163"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-164">Devuelve el objeto <strong>Recordset</strong> como una cadena.</span><span class="sxs-lookup"><span data-stu-id="a1927-164">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="a1927-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-166">Carga el contenido de un archivo existente en un <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-166">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-167"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="a1927-167"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-168">Mueve la posición del registro actual de un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-168">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="a1927-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-170">Se desplaza al registro primero, último, siguiente o anterior de un objeto <strong>Recordset</strong> especificado y convierte ese registro en el registro actual.</span><span class="sxs-lookup"><span data-stu-id="a1927-170">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-171"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="a1927-171"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-172">Mueve un archivo, o un directorio y su contenido, a otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="a1927-172">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="a1927-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-174">Borra el objeto <strong>Recordset</strong> actual y devuelve el objeto <strong>Recordset</strong> siguiente avanzando mediante una serie de comandos.</span><span class="sxs-lookup"><span data-stu-id="a1927-174">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-175"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span><span class="sxs-lookup"><span data-stu-id="a1927-175"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-176">Abre una conexión con un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="a1927-176">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-177"><a href="open-method-ado-record.md">Open (ADO Record)</a></span><span class="sxs-lookup"><span data-stu-id="a1927-177"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-178">Abre un objeto <strong>Record</strong> existente o crea un archivo o un directorio.</span><span class="sxs-lookup"><span data-stu-id="a1927-178">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-179"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span><span class="sxs-lookup"><span data-stu-id="a1927-179"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-180">Abre un cursor.</span><span class="sxs-lookup"><span data-stu-id="a1927-180">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-181"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span><span class="sxs-lookup"><span data-stu-id="a1927-181"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-182">Abre un objeto <strong>Stream</strong> para manipular secuencias de datos binarios o de texto.</span><span class="sxs-lookup"><span data-stu-id="a1927-182">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-183"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="a1927-183"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-184">Obtiene información del esquema de base de datos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a1927-184">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-185"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="a1927-185"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-186">Lee un número especificado de bytes de un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-186">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-187"><a href="readtext-method-ado.md">Dtex</a></span><span class="sxs-lookup"><span data-stu-id="a1927-187"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-188">Lee un número especificado de caracteres de un objeto <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="a1927-188">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-189"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="a1927-189"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-190">Actualiza los objetos de una colección para reflejar los objetos disponibles y específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a1927-190">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-191"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="a1927-191"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-192">Actualiza los datos de un objeto <strong>Recordset</strong> volviendo a ejecutar la consulta en la que se basa el objeto.</span><span class="sxs-lookup"><span data-stu-id="a1927-192">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-193"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="a1927-193"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-194">Actualiza los datos del objeto <strong>Recordset</strong> actual, o de la colección <strong>Fields</strong> de un objeto <strong>Record</strong>, de la base de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="a1927-194">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-195"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="a1927-195"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-196">Guarda el objeto <strong>Recordset</strong> en un archivo o un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-196">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-197"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="a1927-197"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-198">Guarda el contenido binario de un <strong>Stream</strong> en un archivo.</span><span class="sxs-lookup"><span data-stu-id="a1927-198">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-199"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="a1927-199"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-200">Busca en el índice de un objeto <strong>Recordset</strong> para encontrar rápidamente la fila que coincide con los valores especificados y cambia la posición de la fila actual a esa fila.</span><span class="sxs-lookup"><span data-stu-id="a1927-200">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-201"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="a1927-201"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-202">Establece la posición que es el final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a1927-202">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-203"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="a1927-203"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-204">Omite una línea completa al leer una secuencia de texto.</span><span class="sxs-lookup"><span data-stu-id="a1927-204">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-205"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="a1927-205"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-206">Obtiene información estadística sobre una secuencia abierta.</span><span class="sxs-lookup"><span data-stu-id="a1927-206">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-207"><a href="supports-method-ado.md">Admita</a></span><span class="sxs-lookup"><span data-stu-id="a1927-207"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-208">Determina si un objeto <strong>Recordset</strong> especificado admite un tipo determinado de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="a1927-208">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-209"><a href="update-method-ado.md">Actualización</a></span><span class="sxs-lookup"><span data-stu-id="a1927-209"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-210">Guarda cualquier cambio efectuado a la fila actual de un objeto <strong>Recordset</strong> o la colección <strong>Fields</strong> de un objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-210">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="a1927-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-212">Escribe en disco todas las actualizaciones por lote pendientes.</span><span class="sxs-lookup"><span data-stu-id="a1927-212">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1927-213"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="a1927-213"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-214">Escribe datos binarios en un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-214">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1927-215"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="a1927-215"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="a1927-216">Escribe una cadena de texto especificada en un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1927-216">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
