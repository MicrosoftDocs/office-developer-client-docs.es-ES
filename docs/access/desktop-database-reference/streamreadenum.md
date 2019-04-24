---
title: Van (referencia de base de datos de escritorio de Access)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4d9c96a7bb34fe0ab3512a316a92e1f7a01ef4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314724"
---
# <a name="streamreadenum"></a>StreamReadEnum

**Se aplica a:** Access 2013, Office 2013

Especifica si se debe leer toda la secuencia o sólo la línea siguiente de un objeto [Stream](stream-object-ado.md).

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


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Estas constantes no tienen equivalentes ADO/WFC.

