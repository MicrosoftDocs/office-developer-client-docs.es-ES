---
title: Eliminación previa (evento de macro)
TOCTitle: Before Delete Macro Event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0ee4878a742454eb1b02f4b9a45c14ad79097c46
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876263"
---
# <a name="before-delete-macro-event"></a>Eliminación previa (evento de macro)

**Se aplica a**: Access 2013, Office 2013

El evento **Eliminación previa** se produce cuando se elimina un registro, pero antes de confirmar el cambio.

> [!NOTE]
> [!NOTA] El evento **Eliminación previa** solo está disponible en macros de datos.

## <a name="remarks"></a>Comentarios

Utilice el evento **Eliminación previa** para realizar cualquier acción que desee que ocurra antes de eliminar un registro. **Cambio previo** se suele utilizar para realizar la validación y para provocar mensajes de error personalizados.

Puede tener acceso a un valor en el registro que se va a eliminar mediante el uso de la sintaxis siguiente:

`[Old].[Field Name]`

Por ejemplo, para tener acceso al valor del campo QuantityInStock en el registro que se va a eliminar, use la siguiente sintaxis:

`[Old].[QuantityInStock]`

Cuando finaliza el evento **Eliminación previa**, se eliminan permanentemente los valores contenidos en el registro que hay que eliminar.

Puede cancelar el evento **Eliminación previa** mediante la acción **ProvocarError**. Cuando se produce un error, se descartan los cambios incluidos en el evento **Antes de eliminar** .

La siguiente tabla enumera los comandos de macro que pueden utilizarse en el evento **Eliminación previa**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de comando</p></th>
<th><p>Comando</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Flujo de programas</p></td>
<td><p><a href="comment-macro-statement.md">Comentario (instrucción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Flujo de programas</p></td>
<td><p><a href="group-macro-statement.md">Grupo (instrucción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Flujo de programas</p></td>
<td><p><a href="if-then-else-macro-block.md">Si...Entonces...Sino (bloque de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Bloque de datos</p></td>
<td><p><a href="lookuprecord-data-block.md">Acción de Macro BuscarRegistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="clearmacroerror-macro-action.md">BorrarErrorDeMacro (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="onerror-macro-action.md">AlOcurrirError (acción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="raiseerror-macro-action.md">ProvocarError (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="setlocalvar-macro-action.md">EstablecerVariableLocal (acción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="stopmacro-macro-action.md">DetenerMacro (acción de macro)</a></p></td>
</tr>
</tbody>
</table>


Para crear una macro de datos que capture el evento **Eliminación previa**, utilice los pasos siguientes.

1.  Abra la tabla en la que desee capturar el evento **Eliminación previa**.

2.  En la ficha **tabla** , en el grupo **Antes de eventos** , seleccione **Antes de eliminar**.

