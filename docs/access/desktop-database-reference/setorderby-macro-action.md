---
title: ConfigurarOrdenarPor (acción de macro)
TOCTitle: SetOrderBy Macro Action
ms:assetid: 78f65ce9-b56f-f476-3bd6-f3307bc22a08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196152(v=office.15)
ms:contentKeyID: 48545765
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98639
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ac911110d313243879d6dff993061d58c208cd34
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876221"
---
# <a name="setorderby-macro-action"></a>ConfigurarOrdenarPor (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede utilizar la acción **ConfigurarOrdenarPor** para especificar cómo desea ordenar los registros en un formulario, informe, tabla o resultado de consulta.

## <a name="setting"></a>Valores

La acción **ConfigurarOrdenarPor** utiliza los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Ordenar por</strong></p></td>
<td><p>Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del control</strong></p></td>
<td><p>Si se proporciona y el objeto activo es un formulario o informe, es el nombre del control que corresponde al subformulario o subinforme que se va a ordenar. Si está vacío y el objeto activo es un formulario o informe, el formulario o el informe primario se ordena.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Al ejecutar esta acción de macro, la ordenación se aplica a la tabla, formulario, informe u hoja de datos (resultado de consulta) que está activo y tiene el enfoque.

El argumento OrdenarPor es el nombre del campo o los campos por los que desea ordenar los registros. Cuando utilice más de un nombre de campo, separe los nombres con una coma (,). La propiedad **OrdenarPor** del objeto activo se utiliza para guardar el valor de orden y aplicarlo en un momento posterior. Los valores de OrdenarPor se guardan con los objetos en los que se crean. Se cargan automáticamente cuando se abre el objeto, pero no se aplican automáticamente.

Si se establece el argumento OrdenarPor especificando uno o más nombres de campo y ejecutando la macro a continuación, los registros se ordenan en orden ascendente de forma predeterminada.

Para ordenar los registros en orden descendente, escriba DESC al final de la expresión de argumento Ordenar Por. Por ejemplo, para ordenar los registros de clientes en orden descendente por nombre de contacto, establezca el argumento Ordenar Por en "NombreDeContacto DESC". Para ordenar los nombres de forma descendente por Apellido y de forma ascendente por Nombre, establezca el argumento Ordenar Por en "Apellido DESC, Nombre ASC".

