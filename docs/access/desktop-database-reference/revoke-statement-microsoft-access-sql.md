---
title: Instrucción REVOKE (Microsoft Access SQL)
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
localization_priority: Normal
ms.openlocfilehash: 20122fee617597987940766a076d5f968a87c2d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306534"
---
# <a name="revoke-statement-microsoft-access-sql"></a>Instrucción REVOKE (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Revoca privilegios específicos a un usuario o grupo existente.

## <a name="syntax"></a>Sintaxis

REVOKE {*privilegio*\[, *privilegio*,... \]} On {TABLE *tabla* | Objeto ** Object|

Container *Container*} from {*nombredeautorización*\[, *nombredeautorización*,... \]}

La instrucción REVOKE consta de los siguientes elementos:

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
<td><p>Privilegio o privilegios que se van a revocar. Los privilegios se especifican mediante las siguientes palabras clave: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA y UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
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

