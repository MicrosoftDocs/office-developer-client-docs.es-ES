---
title: FieldEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e42dcfe63194364986e5b235c59b011231307a7c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726088"
---
# <a name="fieldenum"></a>FieldEnum

**Se aplica a**: Access 2013, Office 2013

Especifica los campos especiales a los que se hace referencia en la colección [Fields](record-object-ado.md) de un objeto [Record](fields-collection-ado.md).

## <a name="remarks"></a>Observaciones

Estas constantes proporcionan "métodos abreviados" para obtener acceso a campos especiales asociados a un **Record**. Recupere el objeto [Field](field-object-ado.md) de la colección **Fields** y, a continuación, obtenga su contenido con la propiedad **Value** del objeto [Field](value-property-ado.md).

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
<td><p><strong>adDefaultStream</strong></p></td>
<td><p>-1</p></td>
<td><p>Hace referencia al campo que contiene el objeto <a href="stream-object-ado.md">Stream</a> predeterminado asociado a un <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecordURL</strong></p></td>
<td><p>-2</p></td>
<td><p>Hace referencia al campo que contiene la cadena URL absoluta para el <strong>Record</strong> actual.</p></td>
</tr>
</tbody>
</table>

