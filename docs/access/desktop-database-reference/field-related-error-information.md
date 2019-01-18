---
title: Información de errores relacionados con campos
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a0d0362b8f0ff9570a92a3c1c364061d1f9a584
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710555"
---
# <a name="field-related-error-information"></a>Información de errores relacionados con campos


**Se aplica a**: Access 2013, Office 2013

Si un error está relacionado directamente con un campo (por ejemplo, si faltan datos o si no son del tipo correcto para el campo), puede recuperar más información sobre la causa del problema examinando la propiedad **Status** del objeto **Field**. Esta propiedad se ha mejorado para que proporcione información específica sobre el problema. Así pues, por ejemplo, si una llamada a **UpdateBatch** falla, la causa del problema se puede determinar examinando la propiedad **Status** de los **campos** en cada uno de los registros afectados. La propiedad contendrá uno de los valores de la constante **FieldStatusEnum**. La tabla siguiente incluye los valores que son especialmente interesantes cuando se produce un error.

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
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Indica que el campo no se puede recuperar ni almacenar sin pérdida de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6</p></td>
<td><p>Indica que los datos devueltos desde el proveedor desbordaron el tipo de datos del campo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Indica que se utilizó el valor predeterminado del campo al configurar datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>Indica que este campo se omitió cuando se establecieron valores de datos en el origen. El proveedor no estableció ningún valor.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Indica que el campo no se puede modificar porque es una entidad calculada o derivada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>Indica que el proveedor devolvió un valor nulo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Indica que el proveedor no puede obtener suficiente espacio de almacenamiento para completar una operación de movimiento o de copia.</p></td>
</tr>
</tbody>
</table>

