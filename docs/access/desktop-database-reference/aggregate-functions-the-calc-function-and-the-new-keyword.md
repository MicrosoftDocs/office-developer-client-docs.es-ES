---
title: Funciones de agregado, función CALC y palabra clave NEW
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25f52489430465235a928fff3c38469ec6ba83ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297196"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a>Funciones de agregado, función CALC y palabra clave NEW


**Se aplica a:** Access 2013, Office 2013

El servicio de forma de datos admite las siguientes funciones. El nombre asignado al capítulo que contiene la columna en la que se van a realizar las operaciones es el *alias del capítulo*.

Un alias de capítulo puede ser completo y constar del nombre de columna de cada capítulo que lleva al capítulo que contiene el *nombre de columna*, todo separado por puntos. Por ejemplo, si el capítulo principal, chap1, contiene un capítulo secundario, chap2, que tiene una columna de cantidad, amt, entonces el nombre completo será chap1.chap2.amt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Funciones de agregado</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SUM(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcula la suma de todos los valores de la columna especificada.</p></td>
</tr>
<tr class="even">
<td><p>AVG(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcula el promedio de todos los valores de la columna especificada.</p></td>
</tr>
<tr class="odd">
<td><p>MAX(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcula el valor máximo de la columna especificada.</p></td>
</tr>
<tr class="even">
<td><p>MIN(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcula el valor mínimo de la columna especificada.</p></td>
</tr>
<tr class="odd">
<td><p>COUNT(<em>chapter-alias</em>[.<em> column-name</em>])</p></td>
<td><p>Cuenta el número de filas en el alias especificado. Si se especifica una columna, en el recuento sólo se incluirán las filas para las que la columna no tiene un valor nulo.</p></td>
</tr>
<tr class="even">
<td><p>STDEV(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcula la desviación estándar de la columna especificada.</p></td>
</tr>
<tr class="odd">
<td><p>ANY(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Un valor de la columna especificada. ANY sólo tiene un valor predecible si el valor de la columna es el mismo para todas las filas del capítulo.
</p><p><strong>NOTA</strong>: Si la columna no contiene el mismo valor para todas las filas del capítulo, el comando SHAPE devuelve arbitrariamente uno de los valores para ser el valor de la función ANY.</p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Expresión calculada</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CALC(<em>expresión</em>)</p></td>
<td><p>Calcula una expresión arbitraria, pero sólo en la fila del <strong>conjunto de registros</strong> que contiene la función CALC. Se admite toda expresión que utilice estas <a href="visual-basic-for-applications-functions.md">funciones de Visual Basic para Aplicaciones (VBA)</a>.</p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Palabra clave NEW</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NUEVO <em>tipo de campo</em> [( error<em>de</em>precisión  |  <em>de escala</em>  |  <em>de</em>  |  <em>ancho</em> [, error <em>de</em>  |  <em>escala</em>])]</p></td>
<td><p>Agrega una columna vacía del tipo especificado al <strong>conjunto de registros</strong>.</p></td>
</tr>
</tbody>
</table>

<br/>

El *tipo de campo* que se pasa con la palabra clave NEW puede ser cualquiera de los tipos de datos siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipos de datos de OLE DB</p></th>
<th><p>Tipo de datos de ADO equivalentes</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBTYPE_BSTR</p></td>
<td><p>adBSTR</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_BOOL</p></td>
<td><p>adBoolean</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DECIMAL</p></td>
<td><p>adDecimal</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI1</p></td>
<td><p>adUnsignedTinyInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_I1</p></td>
<td><p>adTinyInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI2</p></td>
<td><p>adUnsignedSmallInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI4</p></td>
<td><p>adUnsignedInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_I8</p></td>
<td><p>adBigInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI8</p></td>
<td><p>adUnsignedBigInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_GUID</p></td>
<td><p>adGuid</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_BYTES</p></td>
<td><p>adBinary, AdVarBinary, adLongVarBinary</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_STR</p></td>
<td><p>adChar, adVarChar, adLongVarChar</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_WSTR</p></td>
<td><p>adWChar, adVarWChar, adLongVarWChar</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_NUMERIC</p></td>
<td><p>adNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBDATE</p></td>
<td><p>adDBDate</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_DBTIME</p></td>
<td><p>adDBTime</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBTIMESTAMP</p></td>
<td><p>adDBTimeStamp</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_VARNUMERIC</p></td>
<td><p>adVarNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_FILETIME</p></td>
<td><p>adFileTime</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_ERROR</p></td>
<td><p>adError</p></td>
</tr>
</tbody>
</table>


Cuando el nuevo campo es de tipo decimal (en OLE DB, DBTYPE DECIMAL o en ADO, adDecimal), debe especificar los valores de precisión \_ y escala.

