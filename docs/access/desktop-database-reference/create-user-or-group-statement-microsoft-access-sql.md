---
title: Instrucción CREATE USER o GROUP (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b294af16498778eae94b38a7a31b93fd029585e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710926"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>Instrucción CREATE USER o GROUP (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

Crea uno o varios usuarios o grupos nuevos.

## <a name="syntax"></a>Sintaxis

### <a name="create-a-user"></a>Crear un usuario

CREATE USER *usuario* *contraseña pid* \[, *usuario* *contraseña pid*,...\]

### <a name="create-a-group"></a>Crear un grupo

CREATE GROUP *grupo* *pid*\[, *grupo* *pid*,...\]

La instrucción CREATE USER o GROUP consta de los siguientes elementos:

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
<td><p><em>user</em></p></td>
<td><p>Nombre de un usuario que se agregará al archivo de información de grupo de trabajo.</p></td>
</tr>
<tr class="even">
<td><p><em>grupo</em></p></td>
<td><p>Nombre de un grupo que se agregará al archivo de información de grupo de trabajo.</p></td>
</tr>
<tr class="odd">
<td><p><em>contraseña</em></p></td>
<td><p>Contraseña que se asociará con el nombre de <em>usuario</em> especificado.</p></td>
</tr>
<tr class="even">
<td><p><em>pid</em></p></td>
<td><p>Id. personal.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Un *usuario* y un *grupo* no pueden tener el mismo nombre.

Se requiere para cada *usuario* o *grupo* que se crea una *contraseña* .

