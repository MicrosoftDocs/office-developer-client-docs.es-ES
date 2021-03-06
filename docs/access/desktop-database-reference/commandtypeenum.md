---
title: CommandTypeEnum (referencia de base de datos de escritorio de Access)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9114128771d4753265208dada763ac0c9f796d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296118"
---
# <a name="commandtypeenum"></a>CommandTypeEnum

**Se aplica a:** Access 2013, Office 2013

Especifica cómo se debe interpretar un argumento de comando.

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
<td><p><strong>adCmdUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>No especifica el argumento de tipo de comando.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdText</strong></p></td>
<td><p>1</p></td>
<td><p>Evalúa <a href="commandtext-property-ado.md">CommandText</a> como definición de texto de una llamada a un comando o procedimiento almacenado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTable</strong></p></td>
<td><p>2</p></td>
<td><p>Evalúa <strong>CommandText</strong> como nombre de tabla cuyas columnas se devuelven todas mediante una consulta SQL generada internamente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdStoredProc</strong></p></td>
<td><p>4 </p></td>
<td><p>Evalúa <strong>CommandText</strong> como nombre de procedimiento almacenado.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdUnknown</strong></p></td>
<td><p>8 </p></td>
<td><p>Valor predeterminado. Indica que el tipo de comando de la propiedad <strong>CommandText</strong> no se conoce.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdFile</strong></p></td>
<td><p>256</p></td>
<td><p>Evalúa <strong>CommandText</strong> como el nombre de archivo de un objeto <a href="recordset-object-ado.md">Recordset</a> almacenado de forma persistente. Se usa únicamente con un objeto <strong>Recordset</strong><a href="open-method-ado-recordset.md">Open</a> o <a href="requery-method-ado.md">Requery</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTableDirect</strong></p></td>
<td><p>512</p></td>
<td><p>Evalúa <strong>CommandText</strong> como nombre de tabla cuyas columnas se devuelven todas. Solo se usa con <strong>Recordset.Open</strong> o <strong>Requery</strong>. Para usar el método <a href="seek-method-ado.md">Seek</a>, el objeto <strong>Recordset</strong> se debe abrir con <strong>adCmdTableDirect</strong>. Este valor no se puede combinar con el valor <strong>adAsyncExecute</strong> de <a href="executeoptionenum.md">ExecuteOptionEnum</a>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente a ADO/WFC

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
<td><p>AdoEnums.CommandType.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.TEXT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.STOREDPROC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.UNKNOWN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.FILE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLEDIRECT</p></td>
</tr>
</tbody>
</table>

