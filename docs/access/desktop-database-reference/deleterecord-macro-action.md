---
title: EliminarRegistro (acción de macro)
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 052e7a489eaec526db1552ced89b095f65f652df
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921589"
---
# <a name="deleterecord-macro-action"></a><span data-ttu-id="a228d-102">EliminarRegistro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="a228d-102">DeleteRecord macro action</span></span>

<span data-ttu-id="a228d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a228d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a228d-104">Puede usar la acción **EliminarRegistro** para eliminar un registro.</span><span class="sxs-lookup"><span data-stu-id="a228d-104">You can use the **DeleteRecord** action to delete a record.</span></span>

## <a name="setting"></a><span data-ttu-id="a228d-105">Valores</span><span class="sxs-lookup"><span data-stu-id="a228d-105">Setting</span></span>

<span data-ttu-id="a228d-106">El bloque de datos **CrearRegistro** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a228d-106">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a228d-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="a228d-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="a228d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a228d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a228d-109"><strong>Alias del registro</strong></span><span class="sxs-lookup"><span data-stu-id="a228d-109"><strong>Record Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="a228d-p101">Una cadena que identifica el registro que hay que eliminar. Si no se especifica el argumento <em>Alias</em>, se elimina el registro actual.</span><span class="sxs-lookup"><span data-stu-id="a228d-p101">A string that identifies the record to delete. If the <em>Alias</em> argument is not specified, then the current record is deleted.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="a228d-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a228d-112">Remarks</span></span>

<span data-ttu-id="a228d-113">Puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el último registro creado en un bloque de datos **CrearRegistro**.</span><span class="sxs-lookup"><span data-stu-id="a228d-113">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="a228d-114">Por ejemplo, utilice la siguiente sintaxis para hacer referencia al registro creado más recientemente:</span><span class="sxs-lookup"><span data-stu-id="a228d-114">For example, use the following syntax to refer to the most recently created record:</span></span>

`[LastCreateRecordIdentity]`

