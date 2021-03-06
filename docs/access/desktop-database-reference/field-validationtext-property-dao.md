---
title: Propiedad Field.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47bd400469bc17ac2b57bb249198f7609d7d0801
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292933"
---
# <a name="fieldvalidationtext-property-dao"></a>Propiedad Field.ValidationText (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que especifica el texto del mensaje que la aplicación muestra si el valor de un objeto **Field** no cumple la regla de validación especificada por el valor de la propiedad **ValidationRule** (únicamente áreas de trabajo de Microsoft Access). **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . ValidationText

*expression* Variable que representa un objeto **Field**.

## <a name="remarks"></a>Comentarios

La configuración o el valor devuelto es un objeto **String** que especifica el texto que se muestra si un usuario intenta escribir un valor no válido en un campo. Para un objeto no anexado todavía a una colección, esta propiedad es de lectura y escritura.

Para un objeto **Field**, el uso de la propiedad **ValidationText** dependerá del objeto que contenga la colección **[Fields](fields-collection-dao.md)** a la que se anexa el objeto **Field**, como se muestra en la tabla siguiente.

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
<td><p><strong>Relation</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Lectura/escritura</p></td>
</tr>
</tbody>
</table>

