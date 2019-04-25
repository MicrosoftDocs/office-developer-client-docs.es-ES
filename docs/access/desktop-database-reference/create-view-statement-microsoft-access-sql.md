---
title: CREATE VIEW (instrucción de Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 73fac5ff9dd1f5cf277b8cb241044af23609b764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295369"
---
# <a name="create-view-statement-microsoft-access-sql"></a>CREATE VIEW (instrucción de Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Crea una vista.

> [!NOTE]
> El motor de base de datos de Microsoft Access no admite el uso de CREATE VIEW, ni de cualquiera de las instrucciones DDL, con bases de datos distintas del motor de base de datos de Microsoft Access.

## <a name="syntax"></a>Sintaxis

CREATE VIEW *view* \[(*campo1*\[, *campo2*\[, …\]\])\] AS *selectstatement*

La instrucción CREATE VIEW tiene estas partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Part</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>view</em></p></td>
<td><p>El nombre de la vista que se creará.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>El nombre de los campos correspondientes especificados en <em>selectstatement</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>selectstatement</em></p></td>
<td><p>Una instrucción SELECT de SQL. Para obtener más información, vea <a href="select-statement-microsoft-access-sql.md">SELECT (instrucción)</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La instrucción SELECT que define la vista no puede ser una instrucción [SELECT INTO](select-into-statement-microsoft-access-sql.md).

La instrucción SELECT que define la vista no puede contener ningún parámetro.

El nombre de la vista no puede coincidir con el nombre de una tabla existente.

Si la consulta definida en la instrucción SELECT se puede actualizar, la vista también se puede actualizar. De lo contrario, la vista será de solo lectura.

Si alguno de los dos campos de la consulta definida por la instrucción SELECT tienen el mismo nombre, en la definición de vista es necesario incluir una lista de campos que especifiquen nombres únicos para cada uno de los campos de la consulta.

