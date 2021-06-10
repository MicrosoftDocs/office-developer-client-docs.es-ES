---
title: Método Indexes.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291555"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="2ebfb-102">Método Indexes.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="2ebfb-102">Indexes.Delete method (DAO)</span></span>

<span data-ttu-id="2ebfb-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ebfb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ebfb-104">Elimina el objeto **Index** especificado de la colección **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="2ebfb-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ebfb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ebfb-105">Syntax</span></span>

<span data-ttu-id="2ebfb-106">*expresión* . Delete(***Name***)</span><span class="sxs-lookup"><span data-stu-id="2ebfb-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="2ebfb-107">*expresión* Variable que representa un **objeto Indexes.**</span><span class="sxs-lookup"><span data-stu-id="2ebfb-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ebfb-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="2ebfb-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ebfb-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ebfb-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2ebfb-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="2ebfb-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="2ebfb-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2ebfb-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="2ebfb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ebfb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ebfb-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="2ebfb-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="2ebfb-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2ebfb-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2ebfb-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="2ebfb-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2ebfb-116">Nombre del índice que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="2ebfb-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2ebfb-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2ebfb-117">Remarks</span></span>

<span data-ttu-id="2ebfb-118">El método **Delete** sólo se puede utilizar cuando el objeto **Index** es nuevo y no se ha agregado a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="2ebfb-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

