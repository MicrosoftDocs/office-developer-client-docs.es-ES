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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716400"
---
# <a name="grant-statement-microsoft-access-sql"></a>Instrucción GRANT (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

Concede privilegios específicos a un usuario o grupo existente.

## <a name="syntax"></a>Sintaxis

GRANT {*privilegio*\[, *privilegio*,... \]} ON {tabla *tabla* | OBJETO *objeto*|

*Contenedor* de contenedor} TO {*nombredeautorización*\[, *nombredeautorización*,... \]}

La instrucción GRANT consta de los siguientes elementos:

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
<td><p>El privilegio o privilegios que se conceden. Los privilegios se especifican mediante las siguientes palabras clave: seleccionar, eliminar, insertar, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, esquema y UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>nombretabla</em></p></td>
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

