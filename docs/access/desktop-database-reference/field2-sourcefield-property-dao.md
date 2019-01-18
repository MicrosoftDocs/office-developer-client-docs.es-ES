---
title: Propiedad Field2.SourceField (DAO)
TOCTitle: SourceField Property
ms:assetid: f89146c1-d4a4-1129-636a-c22cf7921a4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836948(v=office.15)
ms:contentKeyID: 48548784
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1d0bedd3c1f9f2af6ccf156e1cf8c0192551f582
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717408"
---
# <a name="field2sourcefield-property-dao"></a>Propiedad Field2.SourceField (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve un valor que indica el nombre del campo que es la fuente original de los datos para un objeto **Field2**. **String** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . SourceField

*expresión* Variable que representa un objeto **Field2** .

## <a name="remarks"></a>Observaciones

Para un objeto **Field2**, utilice las propiedades **SourceField** y **SourceTable** dependiendo del objeto que contenga la colección **Fields** al que el objeto **Field2** está anexado, como se muestra en la siguiente tabla.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto anexado a</p></th>
<th><p>Uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Índice</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="even">
<td><p><strong>Relación</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
</tbody>
</table>


Estas propiedades indican que el campo original y los nombres de tabla están asociados con un objeto **Field2**. Por ejemplo, podría utilizar estas propiedades para determinar el origen inicial de los datos en un campo de consulta cuyo nombre no está relacionado con el nombre del campo de una tabla base.

