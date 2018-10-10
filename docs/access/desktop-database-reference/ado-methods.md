---
title: Métodos de ActiveX Data Objects (ADO)
TOCTitle: ADO Methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b7a685352063c3c1dd4c9bbd62e9c1fc4cdfe11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483575"
---
# <a name="ado-methods"></a><span data-ttu-id="823b3-102">Métodos de ADO</span><span class="sxs-lookup"><span data-stu-id="823b3-102">ADO Methods</span></span>


<span data-ttu-id="823b3-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="823b3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="823b3-104"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="823b3-104"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-105">Crea un nuevo registro de un objeto <strong>Recordset</strong> actualizable.</span><span class="sxs-lookup"><span data-stu-id="823b3-105">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-106"><a href="append-method-ado.md">Append</a></span><span class="sxs-lookup"><span data-stu-id="823b3-106"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-p101">Anexa un objeto a una colección. Si la colección es <strong>Fields</strong>, se puede crear un nuevo objeto <strong>Field</strong> antes de anexarlo a la colección.</span><span class="sxs-lookup"><span data-stu-id="823b3-p101">Appends an object to a collection. If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-109"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="823b3-109"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-110">Anexa datos a un objeto <strong>Field</strong> de texto o de datos binarios de gran tamaño, o bien, a un objeto <strong>Parameter</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-110">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-111"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans y RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="823b3-111"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-112">Administra el procesamiento de transacciones en un objeto de <strong>conexión de</strong> la siguiente manera: <strong>BeginTrans</strong> : inicia una transacción nueva.</span><span class="sxs-lookup"><span data-stu-id="823b3-112">Manages transaction processing within a <strong>Connection</strong> object as follows: <strong>BeginTrans</strong> — Begins a new transaction.</span></span><br /><span data-ttu-id="823b3-p102">
<strong>CommitTrans</strong>: guarda los cambios y termina la transacción actual. También puede iniciar una transacción nueva.</span><span class="sxs-lookup"><span data-stu-id="823b3-p102">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span><br /><span data-ttu-id="823b3-115">
<strong>RollbackTrans</strong> — cancela cualquier cambio y termina la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="823b3-115">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="823b3-116">También puede iniciar una transacción nueva.</span><span class="sxs-lookup"><span data-stu-id="823b3-116">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-117"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="823b3-117"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-118">Cancela la ejecución de una llamada de método asincrónico pendiente.</span><span class="sxs-lookup"><span data-stu-id="823b3-118">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-119"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="823b3-119"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-120">Cancela una actualización por lotes que está pendiente.</span><span class="sxs-lookup"><span data-stu-id="823b3-120">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-121"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="823b3-121"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-122">Cancela los cambios realizados en la fila activa o fila nueva de un objeto <strong>Recordset</strong>, o bien, la colección <strong>Fields</strong> de un objeto <strong>Record</strong>, antes de llamar al método <strong>Update</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-122">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-123"><a href="clear-method-ado.md">Clear</a></span><span class="sxs-lookup"><span data-stu-id="823b3-123"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-124">Quita todos los objetos <strong>Error</strong> de la colección <strong>Errors</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-124">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-125"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="823b3-125"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-p104">Crea un objeto <strong>Recordset</strong> duplicado a partir de un objeto <strong>Recordset</strong> existente. Opcionalmente, especifica que el duplicado es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="823b3-p104">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object. Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-128"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="823b3-128"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-129">Cierra un objeto abierto y cualquier objeto dependiente.</span><span class="sxs-lookup"><span data-stu-id="823b3-129">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-130"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="823b3-130"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-131">Compara dos marcadores y devuelve una indicación de sus valores relativos.</span><span class="sxs-lookup"><span data-stu-id="823b3-131">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-132"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="823b3-132"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-133">Copia un archivo o directorio y su contenidos en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="823b3-133">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-134"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="823b3-134"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-135">Copia el número especificado de caracteres o bytes (según <strong>Type</strong>) de un objeto <strong>Stream</strong> a otro objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-135">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-136"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="823b3-136"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-137">Crea un nuevo objeto <strong>Parameter</strong> con las propiedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="823b3-137">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-138"><a href="delete-method-ado-parameters-collection.md">Delete (colección Parameters de ADO)</a></span><span class="sxs-lookup"><span data-stu-id="823b3-138"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-139">Elimina un objeto de la colección <strong>Parameters</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-139">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-140"><a href="delete-method-ado-fields-collection.md">Eliminar (colección Fields de ADO)</a></span><span class="sxs-lookup"><span data-stu-id="823b3-140"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-141">Elimina un objeto de la colección <strong>Fields</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-141">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-142"><a href="delete-method-ado-recordset.md">Delete (objeto Recordset de ADO)</a></span><span class="sxs-lookup"><span data-stu-id="823b3-142"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-143">Elimina el registro actual o un grupo de registros.</span><span class="sxs-lookup"><span data-stu-id="823b3-143">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-144"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="823b3-144"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-145">Elimina un archivo o directorio y todos sus subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="823b3-145">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-146"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute (objeto Command de ADO)</a></span><span class="sxs-lookup"><span data-stu-id="823b3-146"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-147">Ejecuta la consulta, la instrucción SQL o el procedimiento almacenado especificados en la propiedad <strong>CommandText</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-147">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-148"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute (objeto Connection de ADO)</a></span><span class="sxs-lookup"><span data-stu-id="823b3-148"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-149">Ejecuta la consulta, la instrucción SQL, el procedimiento almacenado o texto específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="823b3-149">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-150"><a href="find-method-ado.md">Find</a></span><span class="sxs-lookup"><span data-stu-id="823b3-150"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-151">Busca en un objeto <strong>Recordset</strong> la fila que cumpla los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="823b3-151">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-152"><a href="flush-method-ado.md">Vaciar</a></span><span class="sxs-lookup"><span data-stu-id="823b3-152"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-153">Vuelca el contenido del objeto <strong>Stream</strong> que queda en el búfer de ADO en el objeto subyacente al que está asociado el objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-153">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-154"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="823b3-154"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-155">Devuelve un <strong>objeto Recordset</strong> cuyas filas representan los archivos y subdirectorios del directorio representado por este <strong>registro</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-155">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-156"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="823b3-156"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-157">Devuelve todo o parte del contenido de un objeto <strong>Field</strong> de datos binarios o de texto de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="823b3-157">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-158"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="823b3-158"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-159">Recupera varios registros de un objeto <strong>Recordset</strong> en una matriz.</span><span class="sxs-lookup"><span data-stu-id="823b3-159">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-160"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="823b3-160"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-161">Devuelve el objeto <strong>Recordset</strong> en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="823b3-161">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="823b3-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-163">Carga el contenido de un archivo existente en un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-163">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-164"><a href="move-method-ado.md">Mover</a></span><span class="sxs-lookup"><span data-stu-id="823b3-164"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-165">Mueve la posición del actual registro en un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-165">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-166"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst, MoveLast, MoveNext y MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="823b3-166"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-167">Se desplaza al registro primero, último, siguiente o anterior en el objeto <strong>Recordset</strong> especificado y convierte ese registro en el registro actual.</span><span class="sxs-lookup"><span data-stu-id="823b3-167">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-168"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="823b3-168"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-169">Mueve un archivo o directorio y su contenido a otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="823b3-169">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-170"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="823b3-170"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-171">Borra el objeto <strong>Recordset</strong> actual y devuelve el siguiente objeto <strong>Recordset</strong> recorriendo varios comandos.</span><span class="sxs-lookup"><span data-stu-id="823b3-171">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-172"><a href="open-method-ado-connection.md">Open (objeto Connection de ADO)</a></span><span class="sxs-lookup"><span data-stu-id="823b3-172"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-173">Abre una conexión con un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="823b3-173">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-174"><a href="open-method-ado-record.md">Open (objeto Record de ADO)</a></span><span class="sxs-lookup"><span data-stu-id="823b3-174"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-175">Abre un objeto <strong>Record</strong> existente o crea un nuevo archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="823b3-175">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-176"><a href="open-method-ado-recordset.md">Open (objeto Recordset de ADO)</a></span><span class="sxs-lookup"><span data-stu-id="823b3-176"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-177">Abre un cursor.</span><span class="sxs-lookup"><span data-stu-id="823b3-177">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-178"><a href="open-method-ado-stream.md">Open (objeto Stream de ADO)</a></span><span class="sxs-lookup"><span data-stu-id="823b3-178"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-179">Abre un objeto <strong>Stream</strong> para manipular secuencias de datos binarios o de texto.</span><span class="sxs-lookup"><span data-stu-id="823b3-179">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-180"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="823b3-180"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-181">Obtiene información del esquema de base de datos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="823b3-181">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-182"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="823b3-182"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-183">Lee un número especificado de bytes de un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-183">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-184"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="823b3-184"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-185">Lee un número especificado de caracteres de un objeto <strong>Stream</strong> de texto.</span><span class="sxs-lookup"><span data-stu-id="823b3-185">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-186"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="823b3-186"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-187">Actualiza los objetos de una colección para reflejar los objetos disponibles y específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="823b3-187">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-188"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="823b3-188"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-189">Actualiza los datos de un objeto <strong>Recordset</strong> ejecutando de nuevo la consulta en la que se basa el objeto.</span><span class="sxs-lookup"><span data-stu-id="823b3-189">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-190"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="823b3-190"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-191">Actualiza los datos del actual objeto <strong>Recordset</strong> o la colección <strong>Fields</strong> de un objeto <strong>Record</strong> de la base de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="823b3-191">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-192"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="823b3-192"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-193">Guarda el objeto <strong>Recordset</strong> en un archivo o un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-193">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-194"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="823b3-194"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-195">Guarda el contenido binario de un objeto <strong>Stream</strong> en un archivo.</span><span class="sxs-lookup"><span data-stu-id="823b3-195">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-196"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="823b3-196"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-197">Busca en el índice de un objeto <strong>Recordset</strong> para localizar rápidamente la fila que coincida con los valores especificados, y cambia la posición de fila actual a dicha fila.</span><span class="sxs-lookup"><span data-stu-id="823b3-197">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-198"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="823b3-198"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-199">Establece la posición que es el final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="823b3-199">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-200"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="823b3-200"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-201">Omite una línea completa al leer una secuencia de texto.</span><span class="sxs-lookup"><span data-stu-id="823b3-201">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-202"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="823b3-202"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-203">Obtiene información estadística sobre una secuencia abierta.</span><span class="sxs-lookup"><span data-stu-id="823b3-203">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-204"><a href="supports-method-ado.md">Admite</a></span><span class="sxs-lookup"><span data-stu-id="823b3-204"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-205">Determina si el objeto <strong>Recordset</strong> especificado admite un determinado tipo de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="823b3-205">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-206"><a href="update-method-ado.md">Actualizar</a></span><span class="sxs-lookup"><span data-stu-id="823b3-206"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-207">Guarda los cambios realizados en la fila actual de un objeto <strong>Recordset</strong> o la colección <strong>Fields</strong> de un objeto <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-207">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-208"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="823b3-208"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-209">Escribe en el disco todas las actualizaciones por lotes que están pendientes.</span><span class="sxs-lookup"><span data-stu-id="823b3-209">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="823b3-210"><a href="write-method-ado.md">Escritura</a></span><span class="sxs-lookup"><span data-stu-id="823b3-210"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-211">Escribe datos binarios en un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-211">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="823b3-212"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="823b3-212"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="823b3-213">Escribe una cadena de texto especificada en un objeto <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="823b3-213">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

