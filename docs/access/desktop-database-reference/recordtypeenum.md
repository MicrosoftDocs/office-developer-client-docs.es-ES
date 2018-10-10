---
title: RecordTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: RecordTypeEnum
ms:assetid: 7edd6508-1507-4649-f1aa-03f1873ef09c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249534(v=office.15)
ms:contentKeyID: 48545890
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4eedd04b630e0cc1cf855eefe09bd071dfbbbb50
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485937"
---
# <a name="recordtypeenum"></a>RecordTypeEnum


**Se aplica a**: Access 2013 | Office 2013

Especifica el tipo de objeto [Record](record-object-ado.md).

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
<td><p><strong>adSimpleRecord</strong></p></td>
<td><p>0</p></td>
<td><p>Indica un registro <em>simple</em> (que no contiene nodos secundarios).</p></td>
</tr>
<tr class="even">
<td><p><strong>es adCollectionRecord</strong></p></td>
<td><p>1</p></td>
<td><p>Indica un registro <em>colección</em> (que contiene nodos secundarios).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecordUnknown</strong></p></td>
<td><p>-1</p></td>
<td><p>Indica que se desconoce el tipo de este objeto <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStructDoc</strong></p></td>
<td><p>2</p></td>
<td><p>Indica un tipo especial de registro <em>colección</em> que representa documentos estructurados COM.</p></td>
</tr>
</tbody>
</table>


**Equivalente ADO/WFC**

Estas constantes no tienen equivalentes ADO/WFC.

