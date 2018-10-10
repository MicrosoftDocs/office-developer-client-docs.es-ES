---
title: StringFormatEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: StringFormatEnum
ms:assetid: ab069d67-d983-f390-5d45-876a9f9d9691
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249794(v=office.15)
ms:contentKeyID: 48546964
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7814b15c75cfd1dbd48c793ee8c30cc2c5348ec9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484442"
---
# <a name="stringformatenum"></a>StringFormatEnum


**Se aplica a**: Access 2013 | Office 2013

Especifica el formato que se aplica al recuperar un objeto [Recordset](recordset-object-ado.md) como cadena.

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
<td><p><strong>adClipString</strong></p></td>
<td><p>2</p></td>
<td><p>Delimita filas por <em>RowDelimiter</em>, columnas por <em>ColumnDelimiter</em> y valores nulos por <em>NullExpr</em>. Estos tres parámetros del método <a href="getstring-method-ado.md">GetString</a> sólo son válidos con un <em>StringFormat</em> de <strong>adClipString</strong>.</p></td>
</tr>
</tbody>
</table>


**Equivalente ADO/WFC**

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
<td><p>AdoEnums.StringFormat.CLIPSTRING</p></td>
</tr>
</tbody>
</table>

