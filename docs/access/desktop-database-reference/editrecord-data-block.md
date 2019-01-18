---
title: Bloque de datos EditarRegistro
TOCTitle: EditRecord data block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32ddfbbf21e62d5967fa1f2f31bab0222664eb39
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715756"
---
# <a name="editrecord-data-block"></a>Bloque de datos EditarRegistro

**Se aplica a**: Access 2013, Office 2013

Puede utilizar el bloque de datos **EditarRegistro** para cambiar los valores contenidos en un registro existente.

> [!NOTE]
> [!NOTA] El bloque de datos **EditarRegistro** solo está disponible en macros de datos.


## <a name="setting"></a>Valores

El bloque de datos **EditarRegistro** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Una cadena que identifica el registro que hay que editar. Si no se especifica el argumento <em>Alias</em>, se edita el registro actual.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentarios

Después de la instrucción **EditarRegistro**, puede insertar un bloque de comandos que se ejecutará antes de confirmar los cambios del registro. Las acciones siguientes están disponibles en un bloque de datos **EditarRegistro**.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">CancelarCambioDeRegistro (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Comentario (instrucción de macro)</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Grupo (instrucción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">If... A continuación... Instrucción de macro Else</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">EstablecerCampo (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">EstablecerVariableLocal (acción de macro)</a></p></td>
</tr>
</tbody>
</table>

Utilice la acción de **EstablecerCampo** para especificar los nuevos valores de un campo en el registro editado.

Puede utilizar una instrucción **Si... Entonces... Sino** para realizar operaciones según una condición.

Para cancelar la edición de un registro, utilice la acción **CancelarCambioDeRegistro**. Esto evita que se confirmen los cambios y permite salir del bloque de datos **EditarRegistro**.

Puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el último registro creado en un bloque de datos **CrearRegistro**. Por ejemplo, utilice la siguiente sintaxis para hacer referencia al campo AssignedTo del registro creado más recientemente:

`[LastCreateRecordIdentity].[AssignedTo]`

El bloque de datos CrearRegistro solo se puede utilizar en los eventos de macro de datos **[Después de insertar](after-insert-macro-event.md)**, **[Después de actualizar](after-update-macro-event.md)** y **[Después de actualizar](after-update-macro-event.md)**.

