---
title: Propiedad Field2.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e7bf23dcde9b522e5a9ed74c4dc969c5312f5a3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931235"
---
# <a name="field2validationtext-property-dao"></a>Propiedad Field2.ValidationText (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve un valor que especifica el texto del mensaje que su aplicación muestra si el valor de un objeto **Field2** no satisface la regla de validación que especifica el valor de la propiedad **ValidationRule** (sólo para áreas de trabajo de Microsoft Access). **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . ValidationText

*expresión* Variable que representa un objeto **Field2** .

## <a name="remarks"></a>Observaciones

La configuración o el valor devuelto es **String** que especifica el texto que aparece si un usuario intenta especificar un valor no válido para un campo. Para un objeto que todavía no está anexado a una colección, esta propiedad es de lectura y escritura.

Para un objeto **Field2**, la utilización de la propiedad **ValidationText** depende del objeto que contiene la colección **[Fields](fields-collection-dao.md)** a la que está anexado el objeto **Field2**, como se muestra en la siguiente tabla.

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
<td><p><strong>Index</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="even">
<td><p><strong>Objeto QueryDef</strong></p></td>
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
<td><p>Lectura y escritura</p></td>
</tr>
</tbody>
</table>

