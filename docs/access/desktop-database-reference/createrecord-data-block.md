---
title: Bloque de datos CreateRecord
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63e189143e77f9fcc42fa8d48c3ebfb2feda6633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295355"
---
# <a name="createrecord-data-block"></a>Bloque de datos CreateRecord


**Se aplica a:** Access 2013, Office 2013

Puede utilizar el bloque de datos **CrearRegistro** para crear un nuevo registro en la tabla especificada.

> [!NOTE]
> El bloque de datos **CrearRegistro** solo está disponible en macros de datos.

## <a name="setting"></a>Configuración

El bloque de datos **CrearRegistro** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Necesario</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Crear un registro en </strong></p></td>
<td><p>Sí</p></td>
<td><p>Nombre de la tabla en la que se creará el nuevo registro.</p></td>
</tr>
<tr class="even">
<td><p><strong>Alias</strong></p></td>
<td><p>No</p></td>
<td><p>Una cadena que identifica el registro. Puede utilizar el alias del registro para identificar</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

El registro creado por **CrearRegistro** se convierte automáticamente en el registro actual.

Después **de la instrucción CreateRecord,** puede insertar un bloque de comandos que se ejecutará antes de que se confirma el nuevo registro. Las acciones siguientes están disponibles en un bloque de datos **CrearRegistro**.

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
<td><p><a href="if-then-else-macro-block.md">Si... A continuación... Instrucción de macro Else</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">EstablecerCampo (acción de macro)</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">EstablecerVariableLocal (acción de macro)</a></p></td>
</tr>
</tbody>
</table>


Después de que la acción **CrearRegistro** cree un registro, utilice la acción **EstablecerCampo** para especificar un valor de un campo en el nuevo registro.

Puede utilizar una instrucción **Si... Entonces... Sino** para realizar operaciones según una condición.

Para cancelar la creación de un registro, utilice la acción **CancelarCambioDeRegistro**. Esto evita que se confirmen los cambios y permite salir del bloque de datos **CrearRegistro**.

Una vez que se confirma el nuevo registro, puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el registro. Por ejemplo, use la siguiente sintaxis para hacer referencia al campo AssignedTo del registro creado más recientemente.

`[LastCreateRecordIdentity].[AssignedTo]`

El bloque de datos **CrearRegistro** solo se puede utilizar en los eventos de macro de datos **[Después de insertar](after-insert-macro-event.md)**, **[Después de actualizar](after-update-macro-event.md)** y **[Después de actualizar](after-update-macro-event.md)**.

