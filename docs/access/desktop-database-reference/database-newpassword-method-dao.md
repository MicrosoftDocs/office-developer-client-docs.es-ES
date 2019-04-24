---
title: Método Database. NewPassword (DAO)
TOCTitle: NewPassword Method
ms:assetid: 01c1c454-d651-222c-225a-2b02734a1b7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844754(v=office.15)
ms:contentKeyID: 48542941
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20f09dbfba50526409472f7eb804ba2c47e4d1d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294858"
---
# <a name="databasenewpassword-method-dao"></a>Método Database. NewPassword (DAO)

**Se aplica a:** Access 2013, Office 2013

Cambia la contraseña de una base de datos existente del motor de base de datos de Microsoft Access (sólo en áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . NewPassword (***bstrOld***, ***bstrNew***)

*expresión* Expresión que devuelve un objeto **Database** .

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>bstrOld</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Valor actual de la propiedad <strong>Password</strong> del objeto <strong>Database</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>bstrNew</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>El nuevo valor de la propiedad <strong>password</strong> del objeto <strong>Database</strong> .</p>
<p><strong>Nota</strong>: Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas débiles no combinan estos elementos. Un ejemplo de contraseña segura es: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Las cadenas bstrOld y bstrNew pueden tener hasta 20 caracteres de longitud y pueden incluir cualquier carácter excepto el carácter ASCII 0 (NULL). Para borrar la contraseña, use una cadena de longitud cero ("") para bstrNew.

Las contraseñas distinguen entre mayúsculas y minúsculas.

Si una base de datos no tiene contraseña, el motor de base de datos de Microsoft Access creará automáticamente una pasando una cadena de longitud cero ("") para la contraseña antigua.


> [!IMPORTANT]
> [!IMPORTANTE] Si pierde la contraseña, puede que nunca vuelva a abrir la base de datos.


