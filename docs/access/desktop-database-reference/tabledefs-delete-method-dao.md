---
title: Método TableDefs. Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313996"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="52042-102">Método TableDefs. Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="52042-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="52042-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52042-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52042-104">Elimina el objeto **TableDef** especificado de la colección **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="52042-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="52042-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52042-105">Syntax</span></span>

<span data-ttu-id="52042-106">*expresión* . Delete (***nombre***)</span><span class="sxs-lookup"><span data-stu-id="52042-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="52042-107">*expresión* Variable que representa un objeto **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="52042-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="52042-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="52042-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52042-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="52042-109">Name</span></span></p></th>
<th><p><span data-ttu-id="52042-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="52042-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="52042-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="52042-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="52042-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="52042-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52042-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="52042-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="52042-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="52042-114">Required</span></span></p></td>
<td><p><span data-ttu-id="52042-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="52042-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="52042-116">Nombre de TableDef que se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="52042-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="52042-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52042-117">Remarks</span></span>

<span data-ttu-id="52042-118">El método Delete está admitido sólo cuando el objeto **TableDef** es nuevo y no se ha anexado a la base de datos o si la propiedad **Updatable** de **TableDef** está establecida en **True**.</span><span class="sxs-lookup"><span data-stu-id="52042-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

