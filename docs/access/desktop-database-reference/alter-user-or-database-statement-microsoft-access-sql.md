---
title: Instrucción ALTER USER o DATABASE (Microsoft Access SQL)
TOCTitle: ALTER USER or DATABASE Statement (Microsoft Access SQL)
ms:assetid: 86ccd296-5171-97e7-683f-cdaab4bde9ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197012(v=office.15)
ms:contentKeyID: 48546093
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d6e471adb7ef2c5826d24f569174b40247d0fd8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484536"
---
# <a name="alter-user-or-database-statement-microsoft-access-sql"></a>Instrucción ALTER USER o DATABASE (Microsoft Access SQL)


**Se aplica a**: Access 2013 | Office 2013

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
<td><p><em>contraseñaNueva</em></p></td>
<td><p>Nueva contraseña que se asociará con el nombre del <em>usuario</em> o la <em>base de datos</em> especificados.</p></td>
</tr>
<tr class="odd">
<td><p><em>contraseñaAntigua</em></p></td>
<td><p>Contraseña existente que se asociará con el nombre del <em>usuario</em> o <em>grupo</em> especificados.</p></td>
</tr>
</tbody>
</table>

