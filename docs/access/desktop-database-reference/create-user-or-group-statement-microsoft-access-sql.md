---
title: Instrucción CREATE USER o GROUP (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 391c31240acf33a458895b00335d1600b975e834
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862649"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a>Instrucción CREATE USER o GROUP (Microsoft Access SQL)

**Se aplica a**: Access 2013 | Office 2013

Crea uno o varios usuarios o grupos nuevos.

## <a name="syntax"></a>Sintaxis

**Crear un usuario**:

CREATE USER *usuario* *contraseña pid* \[, *usuario* *contraseña pid*,...\]

**Creación de un grupo**:

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
<td><p><em>group</em></p></td>
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

