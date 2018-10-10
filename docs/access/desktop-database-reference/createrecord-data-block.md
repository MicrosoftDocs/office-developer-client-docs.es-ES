---
title: CrearRegistro (bloque de datos)
TOCTitle: CreateRecord Data Block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62c6902cc57c210d617b71da3ca42a2a52bdd4f6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484789"
---
# <a name="createrecord-data-block"></a><span data-ttu-id="576ee-102">CrearRegistro (bloque de datos)</span><span class="sxs-lookup"><span data-stu-id="576ee-102">CreateRecord Data Block</span></span>


<span data-ttu-id="576ee-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="576ee-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="576ee-104">Puede utilizar el bloque de datos **CrearRegistro** para crear un nuevo registro en la tabla especificada.</span><span class="sxs-lookup"><span data-stu-id="576ee-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span>

> [!NOTE]
> <span data-ttu-id="576ee-105">[!NOTA] El bloque de datos **CrearRegistro** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="576ee-105">The **CreateRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="576ee-106">Valores</span><span class="sxs-lookup"><span data-stu-id="576ee-106">Setting</span></span>

<span data-ttu-id="576ee-107">El bloque de datos **CrearRegistro** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="576ee-107">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="576ee-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="576ee-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="576ee-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="576ee-109">Required</span></span></p></th>
<th><p><span data-ttu-id="576ee-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="576ee-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="576ee-111"><strong>Crear un registro en </strong></span><span class="sxs-lookup"><span data-stu-id="576ee-111"><strong>Create a Record In</strong></span></span></p></td>
<td><p><span data-ttu-id="576ee-112">Sí</span><span class="sxs-lookup"><span data-stu-id="576ee-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="576ee-113">Nombre de la tabla en la que se creará el nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="576ee-113">The name of the table to create the new record in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="576ee-114"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="576ee-114"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="576ee-115">No</span><span class="sxs-lookup"><span data-stu-id="576ee-115">No</span></span></p></td>
<td><p><span data-ttu-id="576ee-116">Una cadena que identifica el registro.</span><span class="sxs-lookup"><span data-stu-id="576ee-116">An string that identifies the record.</span></span> <span data-ttu-id="576ee-117">Puede utilizar el alias del registro para identificar</span><span class="sxs-lookup"><span data-stu-id="576ee-117">You can use the record's alias to identify</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="576ee-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="576ee-118">Remarks</span></span>

<span data-ttu-id="576ee-119">El registro creado por **CrearRegistro** se convierte automáticamente en el registro actual.</span><span class="sxs-lookup"><span data-stu-id="576ee-119">The record created by **CreateRecord** automatically becomes the current record.</span></span>

<span data-ttu-id="576ee-120">Después de la instrucción de **CrearRegistro** , puede insertar un bloque de comandos que se ejecutará antes de confirmar el nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="576ee-120">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="576ee-121">Las acciones siguientes están disponibles en un bloque de datos **CrearRegistro**.</span><span class="sxs-lookup"><span data-stu-id="576ee-121">The following actions are available in a **CreateRecord** data block.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="576ee-122"><a href="cancelrecordchange-macro-action.md">CancelarCambioDeRegistro (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="576ee-122"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="576ee-123"><a href="comment-macro-statement.md">Comentario (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="576ee-123"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="576ee-124"><a href="group-macro-statement.md">Grupo (instrucción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="576ee-124"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="576ee-125"><a href="if-then-else-macro-block.md">If... A continuación... Instrucción de Macro Else</a></span><span class="sxs-lookup"><span data-stu-id="576ee-125"><a href="if-then-else-macro-block.md">If...Then...Else Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="576ee-126"><a href="setfield-macro-action.md">EstablecerCampo (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="576ee-126"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="576ee-127"><a href="setlocalvar-macro-action.md">EstablecerVariableLocal (acción de macro)</a></span><span class="sxs-lookup"><span data-stu-id="576ee-127"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="576ee-128">Después de que la acción **CrearRegistro** cree un registro, utilice la acción **EstablecerCampo** para especificar un valor de un campo en el nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="576ee-128">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span>

<span data-ttu-id="576ee-129">Puede utilizar una instrucción **Si... Entonces... Sino** para realizar operaciones según una condición.</span><span class="sxs-lookup"><span data-stu-id="576ee-129">You can use an **If...Then...Else** statment to perform operations based on a condition.</span></span>

<span data-ttu-id="576ee-p103">Para cancelar la creación de un registro, utilice la acción **CancelarCambioDeRegistro**. Esto evita que se confirmen los cambios y permite salir del bloque de datos **CrearRegistro**.</span><span class="sxs-lookup"><span data-stu-id="576ee-p103">To cancel the creation of a record, use the **CancelRecordChange** action. This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span>

<span data-ttu-id="576ee-132">Una vez que se confirma el nuevo registro, puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el registro.</span><span class="sxs-lookup"><span data-stu-id="576ee-132">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="576ee-133">Por ejemplo, use la siguiente sintaxis para hacer referencia al campo AssignedTo del registro creado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="576ee-133">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span>

`[LastCreateRecordIdentity].[AssignedTo]`

<span data-ttu-id="576ee-134">El bloque de datos **CrearRegistro** solo se puede utilizar en los eventos de macro de datos **[Después de insertar](after-insert-macro-event.md)**, **[Después de actualizar](after-update-macro-event.md)** y **[Después de actualizar](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="576ee-134">The **CreateRecord** data block can only be used in the **[After Insert](after-insert-macro-event.md)**, **[After Update](after-update-macro-event.md)**, and **[After Update](after-update-macro-event.md)** data macro events.</span></span>

