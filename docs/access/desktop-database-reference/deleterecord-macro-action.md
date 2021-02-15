---
title: EliminarRegistro (acción de macro)
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8fb20068052972696b09ea0d2165b344e97ea922
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294018"
---
# <a name="deleterecord-macro-action"></a><span data-ttu-id="742a2-102">EliminarRegistro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="742a2-102">DeleteRecord macro action</span></span>

<span data-ttu-id="742a2-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="742a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="742a2-104">Puede usar la acción **EliminarRegistro** para eliminar un registro.</span><span class="sxs-lookup"><span data-stu-id="742a2-104">You can use the **DeleteRecord** action to delete a record.</span></span>

## <a name="setting"></a><span data-ttu-id="742a2-105">Setting</span><span class="sxs-lookup"><span data-stu-id="742a2-105">Setting</span></span>

<span data-ttu-id="742a2-106">El bloque de datos **CrearRegistro** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="742a2-106">The **CreateRecord** data block has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="742a2-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="742a2-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="742a2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="742a2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="742a2-109"><strong>Alias del registro</strong></span><span class="sxs-lookup"><span data-stu-id="742a2-109"><strong>Record Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="742a2-110">Una cadena que identifica el registro que hay que eliminar.</span><span class="sxs-lookup"><span data-stu-id="742a2-110">A string that identifies the record to delete.</span></span> <span data-ttu-id="742a2-111">Si no se especifica el argumento <em>Alias</em>, se elimina el registro actual.</span><span class="sxs-lookup"><span data-stu-id="742a2-111">If the <em>Alias</em> argument is not specified, then the current record is deleted.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="742a2-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="742a2-112">Remarks</span></span>

<span data-ttu-id="742a2-113">Puede utilizar la variable local **ÚltimaIdentidadDeRegistroCreada** para trabajar con el último registro creado en un bloque de datos **CrearRegistro**.</span><span class="sxs-lookup"><span data-stu-id="742a2-113">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="742a2-114">Por ejemplo, use la siguiente sintaxis para hacer referencia al registro creado más recientemente:</span><span class="sxs-lookup"><span data-stu-id="742a2-114">For example, use the following syntax to refer to the most recently created record:</span></span>

`[LastCreateRecordIdentity]`

