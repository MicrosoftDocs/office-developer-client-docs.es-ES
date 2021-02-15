---
title: Instrucción DROP USER o GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 995f935ceea5af3b740215c5a4137e02e7ebb1b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293647"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>Instrucción DROP USER o GROUP (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Elimina uno o varios *usuarios* o grupos existentes *o* quita uno o más usuarios *existentes* de un grupo *existente.*

## <a name="syntax"></a>Sintaxis

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>Eliminar uno o más usuarios o quitar uno o más usuarios de un grupo

DROP USER *user* \[ , *user*, ... \] \[ Grupo *FROM*\]

### <a name="delete-one-or-more-groups"></a>Eliminar uno o más grupos

DROP GROUP *group,* \[ *group*, ...\]

La instrucción DROP USER o GROUP consta de los siguientes elementos:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
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

Si se usa la palabra clave FROM en  la instrucción DROP USER,  cada uno de los usuarios enumerados en la instrucción se quitará del grupo especificado después de la palabra clave FROM. Sin embargo, *los propios* usuarios no se eliminarán.

La instrucción DROP GROUP eliminará el *grupo* o los grupos especificados. Los *usuarios* que son miembros de los grupos no se verán afectados, pero ya no serán miembros de los grupos *eliminados.*

