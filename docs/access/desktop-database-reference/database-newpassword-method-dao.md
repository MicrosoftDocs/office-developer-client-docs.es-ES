---
title: Database.NewPassword (método) (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708672"
---
# <a name="databasenewpassword-method-dao"></a>Database.NewPassword (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

Cambia la contraseña de una base de datos existente del motor de base de datos de Microsoft Access (sólo en áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . NewPassword (***bstrOld***, ***bstrNew***)

*expresión* Una expresión que devuelve un objeto de **base de datos** .

## <a name="parameters"></a>Parámetros

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
<td><p>Necesario</p></td>
<td><p><strong>Cadena</strong></p></td>
<td><p>Valor actual de la propiedad <strong>Password</strong> del objeto <strong>Database</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>bstrNew</em></p></td>
<td><p>Necesario</p></td>
<td><p><strong>Cadena</strong></p></td>
<td><p>La nueva configuración de la propiedad <strong>Password</strong> del objeto de <strong>base de datos</strong> .</p>
<p><strong>Nota</strong>: utilice contraseñas seguras que combinen mayúsculas y minúsculas letras, números y símbolos. Las contraseñas no seguras no mezclan estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Las cadenas bstrOld y bstrNew pueden tener hasta 20 caracteres y pueden incluir cualquier carácter excepto el carácter ASCII 0 (null). Para borrar la contraseña, utilice una cadena de longitud cero ("") para bstrNew.

Las contraseñas distinguen entre mayúsculas y minúsculas.

Si una base de datos no tiene contraseña, el motor de base de datos de Microsoft Access creará automáticamente una pasando una cadena de longitud cero ("") para la contraseña antigua.


> [!IMPORTANT]
> [!IMPORTANTE] Si pierde la contraseña, puede que nunca vuelva a abrir la base de datos.


