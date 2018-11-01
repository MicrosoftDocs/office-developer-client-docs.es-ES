---
title: ExecuteOptionEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 8fa81d535a10aa0f359ba6e03b0f47048713671f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867856"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum

**Se aplica a**: Access 2013, Office 2013

Especifica la forma en que un proveedor debe ejecutar un comando.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adAsyncExecute</strong></p></td>
<td><p>0 x 10</p></td>
<td><p>Indica que el comando se debe ejecutar asincrónicamente.
 Este valor no se puede combinar con el valor <strong>adCmdTableDirect</strong> de <a href="commandtypeenum.md">CommandTypeEnum</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAsyncFetch</strong></p></td>
<td><p>0 x 20</p></td>
<td><p>Indica que las filas restantes después de la cantidad inicial especificada en la propiedad <a href="cachesize-property-ado.md">CacheSize</a> se deben recuperar asincrónicamente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAsyncFetchNonBlocking</strong></p></td>
<td><p>0 x 40</p></td>
<td><p>Indica que el subproceso principal no se bloquea en una operación de recuperación de datos. Si la fila solicitada no se ha recuperado, la fila actual se moverá automáticamente al final del archivo.
</p><p>Si abre un <a href="recordset-object-ado.md">Recordset</a> de un <a href="stream-object-ado.md">Stream</a> que contiene un objeto <strong>Recordset</strong> almacenado persistentemente, <strong>adAsyncFetchNonBlocking</strong> no tendrá un efecto (la operación será sincrónica y bloqueante). <strong>adAsynchFetchNonBlocking</strong> no tiene efecto cuando la opción <a href="commandtypeenum.md">adCmdTableDirect</a> se usa para abrir el objeto <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteNoRecords</strong></p></td>
<td><p>0 x 80</p></td>
<td><p>Indica que el texto de comando es un comando o un procedimiento almacenado que no devuelve filas (por ejemplo, un comando que sólo inserta datos). Si se recuperan todas las filas, se descartan y no se devuelve. <strong>adExecuteNoRecords</strong> sólo se puede pasar como un parámetro opcional al método <strong>Execute</strong> de <strong>Connection</strong> o <strong>comando</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adExecuteStream</strong></p></td>
<td><p>0 x 400</p></td>
<td><p>Indica que los resultados de la ejecución de un comando se deben devolver como una secuencia.
 <strong>adExecuteStream</strong> sólo se puede pasar como un parámetro opcional al método <strong>Execute</strong> de <strong>comando</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteRecord</strong></p></td>
<td><p><br />
</p></td>
<td><p>Indica que el objeto <strong>CommandText</strong> es un comando o un procedimiento almacenado que devuelve una sola fila y que se debería devolver como un objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>realiza la consulta</strong></p></td>
<td><p>-1</p></td>
<td><p>Indica que no se especifica el comando.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Paquete: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.ASYNCEXECUTE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCH</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.NORECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

