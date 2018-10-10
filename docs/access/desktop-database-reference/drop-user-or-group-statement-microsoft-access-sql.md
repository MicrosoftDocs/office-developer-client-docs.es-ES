---
title: DROP USER o GROUP (instrucción de Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483848"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER o GROUP (instrucción de Microsoft Access SQL)


**Se aplica a**: Access 2013 | Office 2013

Elimina uno o varios *usuarios* o *grupos* existentes, o elimina uno o varios *usuarios* en un *grupo* existente.

## <a name="syntax"></a>Sintaxis

Para eliminar uno o varios *usuarios*, o eliminar uno o varios *usuarios* en un *grupo*:

DROP USER *usuario*\[, *usuario*,... \] \[De *grupo*\]

Para eliminar uno o varios *grupos*:

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

Si se usa la palabra clave FROM en la instrucción DROP USER, cada uno de los *usuarios* enumerados en la instrucción se eliminará del *grupo* especificado a continuación de la palabra clave FROM. Sin embargo, los *usuarios* en sí no se eliminarán.

La instrucción DROP GROUP eliminará el *grupo* o los grupos especificados. Los *usuarios* que sean miembros del *grupo* o grupos no se verán afectados, pero ya no serán miembros del *grupo* eliminado.

