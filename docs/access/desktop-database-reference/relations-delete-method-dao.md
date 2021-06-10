---
title: Método Relations.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0b7fbf20a8732e8f4db525fd32bf4e5737b4d79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306968"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="db861-102">Método Relations.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="db861-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="db861-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db861-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="db861-104">Elimina el objeto **Relation** especificado de la colección **Relations**.</span><span class="sxs-lookup"><span data-stu-id="db861-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="db861-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db861-105">Syntax</span></span>

<span data-ttu-id="db861-106">*expresión* . Delete(***Name***)</span><span class="sxs-lookup"><span data-stu-id="db861-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="db861-107">*expresión* Variable que representa un **objeto Relations.**</span><span class="sxs-lookup"><span data-stu-id="db861-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="db861-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="db861-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db861-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="db861-109">Name</span></span></p></th>
<th><p><span data-ttu-id="db861-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="db861-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="db861-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="db861-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="db861-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="db861-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db861-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="db861-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="db861-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="db861-114">Required</span></span></p></td>
<td><p><span data-ttu-id="db861-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="db861-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="db861-116">Nombre de la relación que se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="db861-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="db861-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db861-117">Remarks</span></span>

<span data-ttu-id="db861-118">El método **Delete** sólo se admite cuando el objeto **Relation** es un objeto nuevo no agregado.</span><span class="sxs-lookup"><span data-stu-id="db861-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

