---
title: Relations.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1a7ad2345e547232b79085ec5942ce5ca7d8b5c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870026"
---
# <a name="relationsdelete-method-dao"></a><span data-ttu-id="d3670-102">Relations.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="d3670-102">Relations.Delete Method (DAO)</span></span>


<span data-ttu-id="d3670-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3670-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3670-104">Elimina el objeto **Relation** especificado de la colección **Relations**.</span><span class="sxs-lookup"><span data-stu-id="d3670-104">Deletes the specified **Relation** from the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3670-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3670-105">Syntax</span></span>

<span data-ttu-id="d3670-106">*expresión* . Delete (***nombre***)</span><span class="sxs-lookup"><span data-stu-id="d3670-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="d3670-107">*expresión* Variable que representa un objeto **Relations** .</span><span class="sxs-lookup"><span data-stu-id="d3670-107">*expression* A variable that represents a **Relations** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="d3670-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3670-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d3670-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3670-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d3670-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="d3670-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="d3670-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d3670-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="d3670-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3670-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3670-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3670-113">Name</span></span></p></td>
<td><p><span data-ttu-id="d3670-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d3670-114">Required</span></span></p></td>
<td><p><span data-ttu-id="d3670-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="d3670-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="d3670-116">Nombre de la relación que se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="d3670-116">The name of the relation to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d3670-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3670-117">Remarks</span></span>

<span data-ttu-id="d3670-118">El método **Delete** sólo se admite cuando el objeto **Relation** es un objeto nuevo no agregado.</span><span class="sxs-lookup"><span data-stu-id="d3670-118">The **Delete** method is supported only when the **Relation** object is a new, unappended object.</span></span>

