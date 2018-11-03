---
title: Instrucción DROP USER o GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f9662c4f0cb691136a556faa32cb0d5a1c775268
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936836"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>Instrucción DROP USER o GROUP (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

Elimina uno o más existentes *a los usuarios* o *grupos*, o quita uno o varios existentes *a los usuarios* de un *grupo*de existente.

## <a name="syntax"></a>Sintaxis

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>Elimine uno o varios usuarios o quitar uno o varios usuarios de un grupo

DROP USER *usuario*\[, *usuario*,... \] \[De *grupo*\]

### <a name="delete-one-or-more-groups"></a>Eliminar uno o varios grupos

DROP GROUP *grupo*\[, *grupo*,...\]

La instrucción DROP USER o GROUP consta de los siguientes elementos:

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
<td><p>Nombre de un usuario que se va a eliminar del archivo de información de grupo de trabajo.</p></td>
</tr>
<tr class="even">
<td><p><em>group</em></p></td>
<td><p>Nombre de un grupo que se va a eliminar del archivo de información de grupo de trabajo.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Si se utiliza la palabra clave FROM en la instrucción DROP USER, cada uno de los *usuarios* enumerados en la instrucción se quitarán del *grupo* especificado a continuación de la palabra clave FROM. Sin embargo, los *usuarios* no se eliminarán ellos mismos.

La instrucción DROP GROUP eliminará el *grupo*especificado (s). No se verán afectados los *usuarios* que son miembros del *grupo*(s), pero ya no serán miembros del *grupo*eliminado (s).

