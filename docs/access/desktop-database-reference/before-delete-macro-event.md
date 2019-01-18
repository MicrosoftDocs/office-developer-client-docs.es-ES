---
title: Eliminación previa (evento de macro)
TOCTitle: Before Delete macro event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2b2a4f978a4af2ba79cab7807f0142d35d7d30c7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705004"
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
<td><p><a href="comment-macro-statement.md">Instrucción de macro de comentario</a></p></td>
</tr>
<tr class="even">
<td><p>Flujo de programas</p></td>
<td><p><a href="group-macro-statement.md">Instrucción de macro de grupo</a></p></td>
</tr>
<tr class="odd">
<td><p>Flujo de programas</p></td>
<td><p><a href="if-then-else-macro-block.md">If... A continuación... Bloque de macro Else</a></p></td>
</tr>
<tr class="even">
<td><p>Bloque de datos</p></td>
<td><p><a href="lookuprecord-data-block.md">Acción de macro BuscarRegistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Acción de macro BorrarErrorDeMacro</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="onerror-macro-action.md">Acción de macro AlOcurrirError</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="raiseerror-macro-action.md">Acción de macro Provocarerror</a></p></td>
</tr>
<tr class="even">
<td><p>Acción de datos</p></td>
<td><p><a href="setlocalvar-macro-action.md">Acción de macro EstablecerVariableLocal</a></p></td>
</tr>
<tr class="odd">
<td><p>Acción de datos</p></td>
<td><p><a href="stopmacro-macro-action.md">Acción de macro DetenerMacro</a></p></td>
</tr>
</tbody>
</table>


Para crear una macro de datos que capture el evento **Eliminación previa**, utilice los pasos siguientes.

1.  Abra la tabla en la que desee capturar el evento **Eliminación previa**.

2.  En la ficha **tabla** , en el grupo **Antes de eventos** , seleccione **Antes de eliminar**.

