---
title: Instrucción CREATE VIEW (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 73fac5ff9dd1f5cf277b8cb241044af23609b764
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706628"
---
# <a name="create-view-statement-microsoft-access-sql"></a>Instrucción CREATE VIEW (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

Crea una nueva vista.

> [!NOTE]
> [!NOTA] El motor de base de datos de Microsoft Access no admite el uso de CREATE VIEW, ni las instrucciones DDL, con bases de datos que no sean del motor de base de datos de Microsoft Access.

## <a name="syntax"></a>Sintaxis

CREATE VIEW *vista* \[(*campo1*\[, *field2*\[,... \] \])\] AS *instrucciónSelect*

La instrucción CREATE VIEW consta de los siguientes elementos:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elemento</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>view</em></p></td>
<td><p>Nombre de la vista que se va a crear.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>Nombre del campo o campos correspondientes a los campos especificados en <em>instrucciónSelect</em>.</p></td>
</tr>
<tr class="odd">
<td><p><em>instrucciónSelect</em></p></td>
<td><p>Una instrucción SQL SELECT. Para obtener más información, vea la <a href="select-statement-microsoft-access-sql.md">instrucción SELECT</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La instrucción SELECT que define la vista no puede ser una instrucción [SELECT INTO](select-into-statement-microsoft-access-sql.md).

La instrucción SELECT que define la vista no puede contener ningún parámetro.

El nombre de la vista no puede ser igual que el nombre de una tabla existente.

Si la consulta definida por la instrucción SELECT es actualizable, la vista también es actualizable. De lo contrario, la vista es de sólo lectura.

Si dos campos de la consulta definida en la instrucción SELECT tienen el mismo nombre, la definición de la vista debe incluir una lista de campos en la que se especifiquen nombres únicos para cada uno de los campos de la consulta.

