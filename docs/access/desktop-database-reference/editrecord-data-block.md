---
title: EditarRegistro (bloque de datos)
TOCTitle: EditRecord Data Block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9c4d5a5a1565aeda41e5a52127e9f82b5304e686
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876887"
---
# <a name="editrecord-data-block"></a><span data-ttu-id="b409e-102">EditarRegistro (bloque de datos)</span><span class="sxs-lookup"><span data-stu-id="b409e-102">EditRecord Data Block</span></span>

<span data-ttu-id="b409e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b409e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b409e-104">Puede utilizar el bloque de datos **EditarRegistro** para cambiar los valores contenidos en un registro existente.</span><span class="sxs-lookup"><span data-stu-id="b409e-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span>

> [!NOTE]
> <span data-ttu-id="b409e-105">[!NOTA] El bloque de datos **EditarRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="b409e-105">The **EditRecord** data block is available only in Data Macros.</span></span>


## <a name="setting"></a><span data-ttu-id="b409e-106">Valores</span><span class="sxs-lookup"><span data-stu-id="b409e-106">Setting</span></span>

<span data-ttu-id="b409e-107">El bloque de datos **EditarRegistro** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="b409e-107">The **EditRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b409e-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="b409e-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="b409e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b409e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b409e-110"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="b409e-110"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="b409e-p101">Una cadena que identifica el registro que hay que editar. Si no se especifica el argumento <em>Alias</em>, se edita el registro actual.</span><span class="sxs-lookup"><span data-stu-id="b409e-p101">A string that identifies the record to edit. If the <em>Alias</em> argument is not specified, then the current record is edited.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="b409e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b409e-113">Remarks</span></span>

<span data-ttu-id="b409e-p102">Después de la instrucción **EditarRegistro**, puede insertar un bloque de comandos que se ejecutará antes de confirmar los cambios del registro. Las acciones siguientes están disponibles en un bloque de datos **EditarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="b409e-p102">After **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are comitted. The following actions are available in a **EditRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b409e-116"><a href="cancelrecordchange-macro-action.md">CancelarCambioDeRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b409e-116"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b409e-117"><a href="comment-macro-statement.md">Comentario (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b409e-117"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b409e-118"><a href="group-macro-statement.md">Grupo (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b409e-118"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b409e-119"><a href="if-then-else-macro-block.md">If... A continuación... Instrucción de Macro Else</a></span><span class="sxs-lookup"><span data-stu-id="b409e-119"><a href="if-then-else-macro-block.md">If...Then...Else Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b409e-120"><a href="setfield-macro-action.md">EstablecerCampo (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b409e-120"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b409e-121"><a href="setlocalvar-macro-action.md">EstablecerVariableLocal (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="b409e-121"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b409e-122">Utilice la acción de **EstablecerCampo** para especificar los nuevos valores de un campo en el registro editado.</span><span class="sxs-lookup"><span data-stu-id="b409e-122">Use the **SetField** action to specify the new values of a field in the edited record.</span></span>

<span data-ttu-id="b409e-123">Puede utilizar una instrucción **Si... Entonces... Sino** para realizar operaciones según una condición.</span><span class="sxs-lookup"><span data-stu-id="b409e-123">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="b409e-p103">Para cancelar la edición de un registro, utilice la acción **CancelarCambioDeRegistro**. Esto evita que se confirmen los cambios y permite salir del bloque de datos **EditarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="b409e-p103">To cancel the editing of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **EditRecord** data block.</span></span>

<span data-ttu-id="b409e-126">Puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el último registro creado en un bloque de datos **CrearRegistro**.</span><span class="sxs-lookup"><span data-stu-id="b409e-126">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="b409e-127">Por ejemplo, utilice la siguiente sintaxis para hacer referencia al campo AssignedTo del registro creado más recientemente:</span><span class="sxs-lookup"><span data-stu-id="b409e-127">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="b409e-128">El bloque de datos CrearRegistro solo se puede utilizar en los eventos de macro de datos **[Después de insertar](after-insert-macro-event.md)**, **[Después de actualizar](after-update-macro-event.md)** y **[Después de actualizar](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="b409e-128">The CreateRecord data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

