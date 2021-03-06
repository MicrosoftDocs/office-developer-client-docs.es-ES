---
title: Instrucción ALTER USER o DATABASE (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2514ca6403ce70acae9e344d610fbd7b9ba7d73b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297182"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>Instrucción ALTER USER o DATABASE (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Cambia la contraseña de un usuario existente o de una base de datos.

## <a name="syntax"></a>Sintaxis

ALTER DATABASE PASSWORD *contraseñaNueva contraseñaAntigua*

ALTER USER *usuario* PASSWORD *contraseñaNueva contraseñaAntigua*

La instrucción ALTER USER o DATABASE consta de los siguientes elementos:

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
<td><p><em>usuario</em></p></td>
<td><p>Nombre de un usuario que se agregará al archivo de información de grupo de trabajo.</p></td>
</tr>
<tr class="even">
<td><p><em>newpassword</em></p></td>
<td><p>Nueva contraseña que se asociará con el nombre del <em>usuario</em> o la <em>base de datos</em> especificados.</p></td>
</tr>
<tr class="odd">
<td><p><em>oldpassword</em></p></td>
<td><p>Contraseña existente que se asociará con el nombre del <em>usuario</em> o <em>grupo</em> especificados.</p></td>
</tr>
</tbody>
</table>

