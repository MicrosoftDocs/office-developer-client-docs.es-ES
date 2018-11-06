---
title: Relations.Delete (método) (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7c7a42098bcc64a58f8a004c0f1d5a35fd4f34b7
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998927"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="d82d6-102">Relations.Delete (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="d82d6-102">Relations.Delete method (DAO)</span></span>

<span data-ttu-id="d82d6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d82d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d82d6-104">Elimina el objeto **Relation** especificado de la colección **Relations**.</span><span class="sxs-lookup"><span data-stu-id="d82d6-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d82d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d82d6-105">Syntax</span></span>

<span data-ttu-id="d82d6-106">*expresión* . Delete (***nombre***)</span><span class="sxs-lookup"><span data-stu-id="d82d6-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="d82d6-107">*expresión* Variable que representa un objeto **Relations** .</span><span class="sxs-lookup"><span data-stu-id="d82d6-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d82d6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d82d6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d82d6-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="d82d6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d82d6-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="d82d6-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d82d6-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d82d6-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d82d6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d82d6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d82d6-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="d82d6-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="d82d6-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d82d6-114">Required</span></span></p></td>
<td><p><span data-ttu-id="d82d6-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d82d6-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d82d6-116">Nombre de la relación que se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="d82d6-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d82d6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d82d6-117">Remarks</span></span>

<span data-ttu-id="d82d6-118">El método **Delete** sólo se admite cuando el objeto **Relation** es un objeto nuevo no agregado.</span><span class="sxs-lookup"><span data-stu-id="d82d6-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

