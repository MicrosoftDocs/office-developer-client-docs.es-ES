---
title: Método Recordset2.Update (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307171"
---
# <a name="recordset2update-method-dao"></a><span data-ttu-id="b50ca-102">Método Recordset2.Update (DAO)</span><span class="sxs-lookup"><span data-stu-id="b50ca-102">Recordset2.Update method (DAO)</span></span>

<span data-ttu-id="b50ca-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b50ca-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="b50ca-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b50ca-104">Syntax</span></span>

<span data-ttu-id="b50ca-105">*expression* .Update(***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="b50ca-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="b50ca-106">*expresión* Variable que representa un **objeto Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="b50ca-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b50ca-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b50ca-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b50ca-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="b50ca-108">Name</span></span></p></th>
<th><p><span data-ttu-id="b50ca-109">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="b50ca-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b50ca-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b50ca-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="b50ca-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b50ca-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b50ca-112"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="b50ca-112"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="b50ca-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="b50ca-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="b50ca-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="b50ca-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="b50ca-115">Una constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> que indica el tipo de actualización, como se especifica en la Configuración (únicamente espacios de trabajo ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="b50ca-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b50ca-116"><em>Fuerza</em></span><span class="sxs-lookup"><span data-stu-id="b50ca-116"><em>Force</em></span></span></p></td>
<td><p><span data-ttu-id="b50ca-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="b50ca-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="b50ca-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="b50ca-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="b50ca-p101">Un valor <strong>Boolean</strong> que indica si se van a forzar los cambios en la base de datos, independientemente de que los datos subyacentes hayan sido cambiados por otro usuarios desde la llamada <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> o <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong>. Si es <strong>True</strong>, se fuerzan los cambios y se sobrescriben los cambios realizados por otros usuarios. Si es <strong>False</strong> (predeterminado), los cambios realizados por otro usuario mientras la actualización está pendiente, harán que la actualización falle para los cambios en conflicto. No se generan errores, pero las propiedades <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> y <strong>BatchCollisions</strong> indicarán el número de conflictos y las filas afectadas por los conflictos respectivamente (únicamente espacios de trabajo ODBCDirect).  </span><span class="sxs-lookup"><span data-stu-id="b50ca-p101">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong> call. If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten. If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict. No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong>BatchCollisions</strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b50ca-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b50ca-123">Remarks</span></span>

<span data-ttu-id="b50ca-124">Use **Update** para guardar el registro actual y cualquier cambio que se haya realizado.</span><span class="sxs-lookup"><span data-stu-id="b50ca-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b50ca-125">Los cambios en el registro activo se pierden si:</span><span class="sxs-lookup"><span data-stu-id="b50ca-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="b50ca-126">Utiliza el método **Edit** o **AddNew** y luego se desplaza a otro registro sin utilizar primero **Update**.</span><span class="sxs-lookup"><span data-stu-id="b50ca-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="b50ca-127">Utiliza **Edit** o **AddNew** y luego **Edit** o **AddNew** de nuevo sin utilizar primero **Update**.</span><span class="sxs-lookup"><span data-stu-id="b50ca-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="b50ca-128">Establece la propiedad **[Bookmark](recordset2-bookmark-property-dao.md)** en otro registro.</span><span class="sxs-lookup"><span data-stu-id="b50ca-128">You set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="b50ca-129">Cierra **Recordset** sin usar primero **Update**.</span><span class="sxs-lookup"><span data-stu-id="b50ca-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="b50ca-130">Cancela la operación **Edit** sin utilizar **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="b50ca-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="b50ca-p102">Para editar un registro, utilice el método **Edit** para copiar el contenido del registro activo en el búfer de copia. Si no utiliza **Edit** primero, se produce un error cuando utiliza **Update** o intenta cambiar el valor de un campo.</span><span class="sxs-lookup"><span data-stu-id="b50ca-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="b50ca-133">En un área de trabajo de ODBCDirect, puede realizar actualizaciones por lotes, siempre que la biblioteca de cursores admita actualizaciones por lotes y el objeto **Recordset** se abra con una opción de bloqueo por lotes optimista.</span><span class="sxs-lookup"><span data-stu-id="b50ca-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="b50ca-134">En un área de trabajo de Microsoft Access, cuando el valor de la propiedad **LockEdits** del objeto **Recordset** es **True** (bloqueado de forma pesimista) en un entorno multiusuario, el registro sigue bloqueado desde que se usa **Edit** hasta que se ejecuta el método **Update** o se cancela la edición.</span><span class="sxs-lookup"><span data-stu-id="b50ca-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="b50ca-135">Si el valor de la propiedad **LockEdits** es **False** (bloqueado de forma optimista), el registro se bloquea y se compara con el registro preeditado justo antes de que se actualice en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b50ca-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> <span data-ttu-id="b50ca-136">Si el registro cambió desde que se usó el método **Edit**, la operación **Update** produce un error.</span><span class="sxs-lookup"><span data-stu-id="b50ca-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="b50ca-137">Las bases de datos ODBC e ISAM instalable conectadas por el motor de base de datos de Microsoft Access usan siempre un bloqueo optimista.</span><span class="sxs-lookup"><span data-stu-id="b50ca-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="b50ca-138">Para seguir con la operación **Update** en los cambios, use el método **Update** de nuevo.</span><span class="sxs-lookup"><span data-stu-id="b50ca-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="b50ca-139">Para volver a ver el registro como el otro usuario lo había cambiado, actualice el registro actual mediante Move 0.</span><span class="sxs-lookup"><span data-stu-id="b50ca-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>

> [!NOTE]
> <span data-ttu-id="b50ca-p104">Para agregar, editar o eliminar un registro, debe haber un índice único en el registro en el origen de datos subyacente. En caso contrario, se produce un error de "denegación de permiso" en la llamada a método **AddNew**, **Delete** o **Edit** en un área de trabajo de Microsoft Access o un error de "argumento no válido" en la llamada **Update** en un área de trabajo de ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="b50ca-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>


