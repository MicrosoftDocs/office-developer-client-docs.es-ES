---
title: StreamReadEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1255f691f2cd0bde1e3ed83ebffc1f0d31fb3119
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485376"
---
# <a name="streamreadenum"></a>StreamReadEnum


**Se aplica a**: Access 2013 | Office 2013

Especifica si se debe leer toda la secuencia o sólo la línea siguiente de un objeto [Stream](stream-object-ado.md).

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
<td><p><strong>adReadAll</strong></p></td>
<td><p>-1</p></td>
<td><p>Valor predeterminado. Se leen todos los bytes de la secuencia, desde la posición actual hasta el marcador <a href="eos-property-ado.md">EOS</a>. Éste es el único valor válido de <strong>StreamReadEnum</strong> para secuencias binarias (que es <a href="type-property-ado-stream.md">Type</a> es <strong>adTypeBinary</strong>).</p></td>
</tr>
<tr class="even">
<td><p><strong>adReadLine</strong></p></td>
<td><p>-2</p></td>
<td><p>Se lee la línea siguiente de la secuencia (determinada por la propiedad <a href="lineseparator-property-ado.md">LineSeparator</a>).</p></td>
</tr>
</tbody>
</table>


**Equivalente ADO/WFC**

Estas constantes no tienen equivalentes ADO/WFC.

