---
title: ADD USER (instrucción de Microsoft Access SQL)
TOCTitle: ADD USER Statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba08ab3104fa08780e8affa310b52a65f67d8831
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485127"
---
# <a name="add-user-statement-microsoft-access-sql"></a>ADD USER (instrucción de Microsoft Access SQL)

**Se aplica a**: Access 2013 | Office 2013

Agrega uno o varios *usuarios* existentes a un *grupo* existente.

## <a name="syntax"></a>Sintaxis

ADD USER *usuario*\[, *usuario*,... \] Al *grupo*

La instrucción ADD USER consta de los siguientes elementos:

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
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Una vez que un *usuario* se haya agregado a un *grupo*, el *usuario* tendrá todos los permisos concedidos a dicho *grupo*.

