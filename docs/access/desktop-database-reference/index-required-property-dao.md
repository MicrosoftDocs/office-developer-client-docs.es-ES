---
title: Propiedad index. reQuired (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2660a4cb422d91cf46b98a8d3870d2ab2db73fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291702"
---
# <a name="indexrequired-property-dao"></a>Propiedad index. reQuired (DAO)

**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que indica si un objeto **[Field](field-object-dao.md)** requiere un valor no Null.

## <a name="syntax"></a>Sintaxis

*expresión* . Necesarios

*expresión* Variable que representa un objeto **index** .

## <a name="remarks"></a>Comentarios

> [!NOTE]
> [!NOTA] Cuando pueda establecer esta propiedad tanto para un objeto **Index** como para un objeto **Field**, establézcala para el objeto **Field**. La validez del valor de la propiedad para un objeto **Field** se comprueba antes que para un objeto **Index**.

La disponibilidad de la propiedad **Required** depende del objeto que contiene la colección [Fields](fields-collection-dao.md), como se muestra en la siguiente tabla.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Si la colección Fields pertenece a un</p></th>
<th><p>Entonces Required</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>
						Objeto <strong>Index</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="even">
<td><p>
						Objeto <strong>QueryDef</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="odd">
<td><p>
						Objeto <strong>Recordset</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="even">
<td><p>
						Objeto <strong>Relation</strong></p></td>
<td><p>No está admitido</p></td>
</tr>
<tr class="odd">
<td><p>
						Objeto <strong>TableDef</strong></p></td>
<td><p>Lectura y escritura</p></td>
</tr>
</tbody>
</table>

