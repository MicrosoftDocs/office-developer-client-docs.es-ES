---
title: Instrucción GRANT (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4357099f8bcb9b2308b5cda3543949765b8c3420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292135"
---
# <a name="grant-statement-microsoft-access-sql"></a>Instrucción GRANT (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Concede privilegios específicos a un usuario o grupo existente.

## <a name="syntax"></a>Sintaxis

Grant {*privilegio*\[, *privilegio*,... \]} On {TABLE *tabla* | Objeto ** Object|

Contenedor ** contenedor} to {*nombredeautorización*\[, *nombredeautorización*,... \]}

La instrucción GRANT consta de los siguientes elementos:

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
<td><p><em>privilegia</em></p></td>
<td><p>Privilegio o privilegios que se van a conceder. Los privilegios se especifican mediante las siguientes palabras clave: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA y UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>NombreDeTabla</em></p></td>
<td><p>Cualquier nombre de tabla válido.</p></td>
</tr>
<tr class="odd">
<td><p><em>object</em></p></td>
<td><p>Puede incluir cualquier objeto que no sea tabla. Por ejemplo, una consulta (vista o procedimiento) almacenada.</p></td>
</tr>
<tr class="even">
<td><p><em>recipiente</em></p></td>
<td><p>Nombre de un contenedor válido.</p></td>
</tr>
<tr class="odd">
<td><p><em>nombredeautorización</em></p></td>
<td><p>Nombre de usuario o grupo.</p></td>
</tr>
</tbody>
</table>

