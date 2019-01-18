---
title: Recordset2.Update (método) (DAO)
TOCTitle: Update Method
ms:assetid: 1b47606a-e79c-23f1-b120-46d1429bc167
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845700(v=office.15)
ms:contentKeyID: 48543537
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052882
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4259da0eb48e7ff13e246b326cc6e96d7a916ea7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714916"
---
# <a name="recordset2update-method-dao"></a>Recordset2.Update (método) (DAO)

**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . Actualización (***UpdateType***, ***Force***)

*expresión* Variable que representa un objeto **Recordset2** .

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
<td><p><em>UpdateType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Una constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> que indica el tipo de actualización, como se especifica en la Configuración (únicamente espacios de trabajo ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><em>Force</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p>Un valor <strong>Boolean</strong> que indica si se van a forzar los cambios en la base de datos, independientemente de que los datos subyacentes hayan sido cambiados por otro usuarios desde la llamada <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> o <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong>. Si es <strong>True</strong>, se fuerzan los cambios y se sobrescriben los cambios realizados por otros usuarios. Si es <strong>False</strong> (predeterminado), los cambios realizados por otro usuario mientras la actualización está pendiente, harán que la actualización falle para los cambios en conflicto. No se generan errores, pero las propiedades <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> y <strong>BatchCollisions</strong> indicarán el número de conflictos y las filas afectadas por los conflictos respectivamente (únicamente espacios de trabajo ODBCDirect).  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Utilice **Update** para guardar el registro activo y cualquier cambio realizado en él.

> [!IMPORTANT]
> [!IMPORTANTE] Los cambios en el registro activo se pierden si:
> - Utiliza el método **Edit** o **AddNew** y luego se desplaza a otro registro sin utilizar primero **Update**.
> - Utiliza **Edit** o **AddNew** y luego **Edit** o **AddNew** de nuevo sin utilizar primero **Update**.
> - Establece la propiedad **[Bookmark](recordset2-bookmark-property-dao.md)** en otro registro.
> - Cierra **Recordset** sin usar primero **Update**.
> - Cancela la operación **Edit** sin utilizar **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.

Para editar un registro, utilice el método **Edit** para copiar el contenido del registro activo en el búfer de copia. Si no utiliza **Edit** primero, se produce un error cuando utiliza **Update** o intenta cambiar el valor de un campo.

En un área de trabajo de ODBCDirect, puede realizar actualizaciones por lotes, siempre que la biblioteca de cursores admita actualizaciones por lotes y el objeto **Recordset** se abra con una opción de bloqueo por lotes optimista.

En un área de trabajo de Microsoft Access, cuando el valor de la propiedad **LockEdits** del objeto **Recordset** es **True** (bloqueado de forma pesimista) en un entorno multiusuario, el registro sigue bloqueado desde que se usa **Edit** hasta que se ejecuta el método **Update** o se cancela la edición. Si el valor de la propiedad **LockEdits** es **False** (bloqueado de forma optimista), el registro se bloquea y se compara con el registro preeditado justo antes de que se actualice en la base de datos. Si el registro cambió desde que se usó el método **Edit**, la operación **Update** produce un error. Las bases de datos ODBC e ISAM instalable conectadas por el motor de base de datos de Microsoft Access usan siempre un bloqueo optimista. Para seguir con la operación **Update** en los cambios, use el método **Update** de nuevo. Para volver al registro cuando otro usuario lo cambia, actualice el registro activo mediante Move 0.

> [!NOTE]
> [!NOTA] Para agregar, editar o eliminar un registro, debe haber un índice único en el registro en el origen de datos subyacente. En caso contrario, se produce un error de "denegación de permiso" en la llamada a método **AddNew**, **Delete** o **Edit** en un área de trabajo de Microsoft Access o un error de "argumento no válido" en la llamada **Update** en un área de trabajo de ODBCDirect.


