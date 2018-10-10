---
title: Relations.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b228c21931131023d58efc91d0087ad76ca3b61
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484276"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="2f9f7-102">Relations.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="2f9f7-102">Relations.Delete Method (DAO)</span></span>


<span data-ttu-id="2f9f7-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f9f7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f9f7-104">Elimina el objeto **Relation** especificado de la colección **Relations**.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f9f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f9f7-105">Syntax</span></span>

<span data-ttu-id="2f9f7-106">*expresión* . Delete (***nombre***)</span><span class="sxs-lookup"><span data-stu-id="2f9f7-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="2f9f7-107">*expresión* Variable que representa un objeto **Relations** .</span><span class="sxs-lookup"><span data-stu-id="2f9f7-107">*expression* A variable that represents a **Relations** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="2f9f7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f9f7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f9f7-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="2f9f7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2f9f7-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="2f9f7-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="2f9f7-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2f9f7-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="2f9f7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f9f7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f9f7-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="2f9f7-113">Name</span></span></p></td>
<td><p><span data-ttu-id="2f9f7-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2f9f7-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2f9f7-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="2f9f7-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2f9f7-116">Nombre de la relación que se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2f9f7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f9f7-117">Remarks</span></span>

<span data-ttu-id="2f9f7-118">El método **Delete** sólo se admite cuando el objeto **Relation** es un objeto nuevo no agregado.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

