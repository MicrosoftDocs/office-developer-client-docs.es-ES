---
title: ADD USER (instrucción de Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ba60a646fd234748bcc39b9a5604a33675caee5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280428"
---
# <a name="add-user-statement-microsoft-access-sql"></a>ADD USER (instrucción de Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Agrega uno o varios *usuarios* existentes a un *grupo* existente.

## <a name="syntax"></a>Sintaxis

Agregar usuario **\[usuario, *usuario*,... \] Para *agrupar*

La instrucción ADD USER consta de los siguientes elementos:

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
<td><p><em>grupo</em></p></td>
<td><p>Nombre de un grupo que se agregará al archivo de información de grupo de trabajo.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Una vez que se ha agregado un *usuario* a un *Grupo*, el *usuario* tiene todos los permisos que se han concedido al *Grupo*.

