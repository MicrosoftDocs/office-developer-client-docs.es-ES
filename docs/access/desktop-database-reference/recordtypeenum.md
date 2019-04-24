---
title: RecordTypeEnum (referencia de base de datos de escritorio de Access)
TOCTitle: RecordTypeEnum
ms:assetid: 7edd6508-1507-4649-f1aa-03f1873ef09c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249534(v=office.15)
ms:contentKeyID: 48545890
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c95e4b78a3e2259c3dc5961e87b98ca65ea55692
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309286"
---
# <a name="recordtypeenum"></a>RecordTypeEnum

**Se aplica a:** Access 2013, Office 2013

Especifica el tipo de objeto [Record](record-object-ado.md).

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
<td><p><strong>adSimpleRecord</strong></p></td>
<td><p>comprendi</p></td>
<td><p>Indica un registro <em>simple</em> (que no contiene nodos secundarios).</p></td>
</tr>
<tr class="even">
<td><p><strong>adCollectionRecord</strong></p></td>
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
<td><p>segundo</p></td>
<td><p>Indica un tipo especial de registro <em>colección</em> que representa documentos estructurados COM.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Estas constantes no tienen equivalentes ADO/WFC.

