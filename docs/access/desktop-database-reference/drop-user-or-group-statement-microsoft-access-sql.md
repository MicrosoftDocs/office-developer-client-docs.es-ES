---
title: Instrucción DROP USER o GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 43c9d5ba4cd07e4ca388863fd79fb9b198a841af
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874107"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>Instrucción DROP USER o GROUP (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

Elimina uno o más existentes *a los usuarios* o *grupos*, o quita uno o varios existentes *a los usuarios* de un *grupo*de existente.

## <a name="syntax"></a>Sintaxis

**Eliminar uno o varios _usuarios_ o quitar uno o varios _usuarios_ de un _grupo_**:

DROP USER *usuario*\[, *usuario*,... \] \[De *grupo*\]

**Eliminar uno o varios _grupos_**:

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

