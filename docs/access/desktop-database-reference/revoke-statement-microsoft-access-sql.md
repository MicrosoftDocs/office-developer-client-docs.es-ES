---
title: REVOCAR declaración (Microsoft Access SQL)
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4bcdd7aa77823a53ba2a2c0cde4badbac571611a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860549"
---
# <a name="revoke-statement-microsoft-access-sql"></a>REVOCAR declaración (Microsoft Access SQL)

**Se aplica a**: Access 2013 | Office 2013

Revoca privilegios específicos a un usuario o grupo existente.

## <a name="syntax"></a>Sintaxis

REVOKE {*privilegio*\[, *privilegio*,... \]} ON {tabla *tabla* | OBJETO *objeto*|

CONTAINTER *contenedor*} FROM {*nombredeautorización*\[, *nombredeautorización*,... \]}

La instrucción REVOKE consta de los siguientes elementos:

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
<td><p><em>privilegio</em></p></td>
<td><p>Privilegio o privilegios que se va a revocar. Los privilegios se especifican mediante las siguientes palabras clave: seleccionar, eliminar, insertar, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, esquema y UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>tabla</em></p></td>
<td><p>Cualquier nombre de tabla válido.</p></td>
</tr>
<tr class="odd">
<td><p><em>object</em></p></td>
<td><p>Puede incluir cualquier objeto que no sea tabla. Por ejemplo, una consulta (vista o procedimiento) almacenada.</p></td>
</tr>
<tr class="even">
<td><p><em>contenedor</em></p></td>
<td><p>Nombre de un contenedor válido.</p></td>
</tr>
<tr class="odd">
<td><p><em>nombreDeAutorización</em></p></td>
<td><p>Nombre de usuario o grupo.</p></td>
</tr>
</tbody>
</table>

