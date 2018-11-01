---
title: Métodos de ActiveX Data Objects (ADO)
TOCTitle: ADO Methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ef05e7f322b769102ce25aab7dfc26a75b0aa22
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879336"
---
# <a name="ado-methods"></a>Métodos de ADO


**Se aplica a**: Access 2013, Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Crea un nuevo registro de un objeto <strong>Recordset</strong> actualizable.</p></td>
</tr>
<tr class="even">
<td><p><a href="append-method-ado.md">Append</a></p></td>
<td><p>Anexa un objeto a una colección. Si la colección es <strong>Fields</strong>, se puede crear un nuevo objeto <strong>Field</strong> antes de anexarlo a la colección.</p></td>
</tr>
<tr class="odd">
<td><p><a href="appendchunk-method-ado.md">AppendChunk</a></p></td>
<td><p>Anexa datos a un objeto <strong>Field</strong> de texto o de datos binarios de gran tamaño, o bien, a un objeto <strong>Parameter</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans y RollbackTrans</a></p></td>
<td><p>Administra el procesamiento de transacciones en un objeto de <strong>conexión de</strong> la siguiente manera: <strong>BeginTrans</strong> : inicia una transacción nueva.<br />
<strong>CommitTrans</strong>: guarda los cambios y termina la transacción actual. También puede iniciar una transacción nueva.<br />
<strong>RollbackTrans</strong> — cancela cualquier cambio y termina la transacción actual. También puede iniciar una transacción nueva.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Cancela la ejecución de una llamada de método asincrónico pendiente.</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Cancela una actualización por lotes que está pendiente.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Cancela los cambios realizados en la fila activa o fila nueva de un objeto <strong>Recordset</strong>, o bien, la colección <strong>Fields</strong> de un objeto <strong>Record</strong>, antes de llamar al método <strong>Update</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="clear-method-ado.md">Clear</a></p></td>
<td><p>Quita todos los objetos <strong>Error</strong> de la colección <strong>Errors</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Crea un objeto <strong>Recordset</strong> duplicado a partir de un objeto <strong>Recordset</strong> existente. Opcionalmente, especifica que el duplicado es de solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Cierra un objeto abierto y cualquier objeto dependiente.</p></td>
</tr>
<tr class="odd">
<td><p><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></p></td>
<td><p>Compara dos marcadores y devuelve una indicación de sus valores relativos.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Copia un archivo o directorio y su contenidos en otra ubicación.</p></td>
</tr>
<tr class="odd">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Copia el número especificado de caracteres o bytes (según <strong>Type</strong>) de un objeto <strong>Stream</strong> a otro objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">CreateParameter</a></p></td>
<td><p>Crea un nuevo objeto <strong>Parameter</strong> con las propiedades especificadas.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">Delete (colección Parameters de ADO)</a></p></td>
<td><p>Elimina un objeto de la colección <strong>Parameters</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">Eliminar (colección Fields de ADO)</a></p></td>
<td><p>Elimina un objeto de la colección <strong>Fields</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete (objeto Recordset de ADO)</a></p></td>
<td><p>Elimina el registro actual o un grupo de registros.</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Elimina un archivo o directorio y todos sus subdirectorios.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute (objeto Command de ADO)</a></p></td>
<td><p>Ejecuta la consulta, la instrucción SQL o el procedimiento almacenado especificados en la propiedad <strong>CommandText</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute (objeto Connection de ADO)</a></p></td>
<td><p>Ejecuta la consulta, la instrucción SQL, el procedimiento almacenado o texto específico del proveedor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Find</a></p></td>
<td><p>Busca en un objeto <strong>Recordset</strong> la fila que cumpla los criterios especificados.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Vaciar</a></p></td>
<td><p>Vuelca el contenido del objeto <strong>Stream</strong> que queda en el búfer de ADO en el objeto subyacente al que está asociado el objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Devuelve un <strong>objeto Recordset</strong> cuyas filas representan los archivos y subdirectorios del directorio representado por este <strong>registro</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">GetChunk</a></p></td>
<td><p>Devuelve todo o parte del contenido de un objeto <strong>Field</strong> de datos binarios o de texto de gran tamaño.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Recupera varios registros de un objeto <strong>Recordset</strong> en una matriz.</p></td>
</tr>
<tr class="even">
<td><p><a href="getstring-method-ado.md">GetString</a></p></td>
<td><p>Devuelve el objeto <strong>Recordset</strong> en forma de cadena.</p></td>
</tr>
<tr class="odd">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Carga el contenido de un archivo existente en un objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="move-method-ado.md">Mover</a></p></td>
<td><p>Mueve la posición del actual registro en un objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Métodos MoveFirst, MoveLast, MoveNext y MovePrevious</a></p></td>
<td><p>Se desplaza al registro primero, último, siguiente o anterior en el objeto <strong>Recordset</strong> especificado y convierte ese registro en el registro actual.</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Mueve un archivo o directorio y su contenido a otra ubicación.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Borra el objeto <strong>Recordset</strong> actual y devuelve el siguiente objeto <strong>Recordset</strong> recorriendo varios comandos.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">Open (objeto Connection de ADO)</a></p></td>
<td><p>Abre una conexión con un origen de datos.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">Open (objeto Record de ADO)</a></p></td>
<td><p>Abre un objeto <strong>Record</strong> existente o crea un nuevo archivo o directorio.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Open (objeto Recordset de ADO)</a></p></td>
<td><p>Abre un cursor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open (objeto Stream de ADO)</a></p></td>
<td><p>Abre un objeto <strong>Stream</strong> para manipular secuencias de datos binarios o de texto.</p></td>
</tr>
<tr class="even">
<td><p><a href="openschema-method-ado.md">OpenSchema</a></p></td>
<td><p>Obtiene información del esquema de base de datos del proveedor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Lee un número especificado de bytes de un objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Lee un número especificado de caracteres de un objeto <strong>Stream</strong> de texto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="refresh-method-ado.md">Refresh</a></p></td>
<td><p>Actualiza los objetos de una colección para reflejar los objetos disponibles y específicos del proveedor.</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Actualiza los datos de un objeto <strong>Recordset</strong> ejecutando de nuevo la consulta en la que se basa el objeto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Actualiza los datos del actual objeto <strong>Recordset</strong> o la colección <strong>Fields</strong> de un objeto <strong>Record</strong> de la base de datos subyacente.</p></td>
</tr>
<tr class="even">
<td><p><a href="save-method-ado.md">Save</a></p></td>
<td><p>Guarda el objeto <strong>Recordset</strong> en un archivo o un objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Guarda el contenido binario de un objeto <strong>Stream</strong> en un archivo.</p></td>
</tr>
<tr class="even">
<td><p><a href="seek-method-ado.md">Seek</a></p></td>
<td><p>Busca en el índice de un objeto <strong>Recordset</strong> para localizar rápidamente la fila que coincida con los valores especificados, y cambia la posición de fila actual a dicha fila.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Establece la posición que es el final de la secuencia.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Omite una línea completa al leer una secuencia de texto.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stat-method-ado.md">Stat</a></p></td>
<td><p>Obtiene información estadística sobre una secuencia abierta.</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Admite</a></p></td>
<td><p>Determina si el objeto <strong>Recordset</strong> especificado admite un determinado tipo de funcionalidad.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Actualizar</a></p></td>
<td><p>Guarda los cambios realizados en la fila actual de un objeto <strong>Recordset</strong> o la colección <strong>Fields</strong> de un objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Escribe en el disco todas las actualizaciones por lotes que están pendientes.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>Escribe datos binarios en un objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Escribe una cadena de texto especificada en un objeto <strong>Stream</strong>.</p></td>
</tr>
</tbody>
</table>

