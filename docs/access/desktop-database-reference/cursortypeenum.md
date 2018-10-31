---
title: CursorTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c394f8000f1d4ae7867d83974e0e186616145fb5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864034"
---
# <a name="cursortypeenum"></a>CursorTypeEnum

**Se aplica a**: Access 2013 | Office 2013

Especifica el tipo de cursor usado en un objeto [Recordset](recordset-object-ado.md).

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
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p>2</p></td>
<td><p>Usa un cursor dinámico. Las adiciones, los cambios y las eliminaciones realizadas por otros usuarios son visibles y se permiten todos los tipos de movimiento por el <strong>Recordset</strong>, excepto para marcadores, si el proveedor no los admite.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>0</p></td>
<td><p>Valor predeterminado. Usa un cursor de solo avance. Es idéntico a un cursor estático, excepto que solo se puede desplazar por los registros hacia adelante. Este cursor permite mejorar el rendimiento cuando solo se necesita recorrer un objeto <strong>Recordset</strong> una vez.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p>1</p></td>
<td><p>Usa un cursor de conjunto de claves. Igual que un cursor dinámico, excepto que no se pueden ver los registros agregados por otros usuarios, aunque los registros eliminados por otros usuarios son inaccesibles desde el objeto <strong>Recordset</strong>. Los cambios en los datos realizados por otros usuarios siguen siendo visibles.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p>3</p></td>
<td><p>Utiliza un cursor estático. Una copia estática de conjunto de registros que se puede utilizar para buscar datos o generar informes. Las adiciones, modificaciones o eliminaciones realizadas por otros usuarios no son visibles.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>No especifica el tipo de cursor.</p></td>
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
<td><p>AdoEnums.CursorType.DYNAMIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.FORWARDONLY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.KEYSET</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.STATIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

