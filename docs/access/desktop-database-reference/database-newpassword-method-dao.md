---
title: Database.NewPassword Method (DAO)
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
ms.openlocfilehash: 892dc16d0422572e83f92316ce2c1c67f9ce5cc0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860647"
---
# <a name="databasenewpassword-method-dao"></a>Database.NewPassword Method (DAO)


**Se aplica a**: Access 2013 | Office 2013

Cambia la contraseña de una base de datos existente del motor de base de datos de Microsoft Access (sólo en áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . NewPassword (***bstrOld***, ***bstrNew***)

*expresión* Una expresión que devuelve un objeto de **base de datos** .

### <a name="parameters"></a>Parámetros

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
<th><p>Necesario/Opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>bstrOld</p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Valor actual de la propiedad <strong>Password</strong> del objeto <strong>Database</strong>.</p></td>
</tr>
<tr class="even">
<td><p>bstrNew</p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>La nueva configuración de la propiedad <strong>Password</strong> del objeto de <strong>base de datos</strong> .</p>

> [!NOTE]
> [!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Las cadenas bstrOld y bstrNew pueden tener hasta 20 caracteres y pueden incluir cualquier carácter excepto el carácter ASCII 0 (null). Para borrar la contraseña, utilice una cadena de longitud cero ("") para bstrNew.

Las contraseñas distinguen entre mayúsculas y minúsculas.

Si una base de datos no tiene contraseña, el motor de base de datos de Microsoft Access creará automáticamente una pasando una cadena de longitud cero ("") para la contraseña antigua.


> [!IMPORTANT]
> [!IMPORTANTE] Si pierde la contraseña, puede que nunca vuelva a abrir la base de datos.


