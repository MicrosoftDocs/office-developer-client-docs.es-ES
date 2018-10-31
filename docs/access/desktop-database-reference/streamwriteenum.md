---
title: StreamWriteEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 76286fcd09e5b92f19d8dbf0e8d0419ad4c600df
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861893"
---
# <a name="streamwriteenum"></a>StreamWriteEnum

**Se aplica a**: Access 2013 | Office 2013

Especifica si se agrega un separador de línea a la cadena escrita en un objeto [Stream](stream-object-ado.md).

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
<td><p><strong>adWriteChar</strong></p></td>
<td><p>0</p></td>
<td><p>Valor predeterminado. Se escribe la cadena de texto (especificada por el parámetro <em>Data</em>) en el objeto <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adWriteLine</strong></p></td>
<td><p>1</p></td>
<td><p>Escribe una cadena de texto y un carácter separador de línea en un objeto <strong>Stream</strong>. Si la propiedad <a href="lineseparator-property-ado.md">LineSeparator</a> no está definida, se devuelve un error en tiempo de ejecución.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Estas constantes no tienen equivalentes ADO/WFC.

