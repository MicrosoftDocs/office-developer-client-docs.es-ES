---
title: Indexes.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b30748c0a1388a1175512e3b8d3fd1970795b821
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484201"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="cca2e-102">Indexes.Delete Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="cca2e-102">Indexes.Delete Method (DAO)</span></span>


<span data-ttu-id="cca2e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cca2e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cca2e-104">Elimina el objeto **Index** especificado de la colección **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="cca2e-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cca2e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cca2e-105">Syntax</span></span>

<span data-ttu-id="cca2e-106">*expresión* . Delete (***nombre***)</span><span class="sxs-lookup"><span data-stu-id="cca2e-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="cca2e-107">*expresión* Variable que representa un objeto **Indexes** .</span><span class="sxs-lookup"><span data-stu-id="cca2e-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="cca2e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cca2e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cca2e-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="cca2e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="cca2e-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="cca2e-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="cca2e-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="cca2e-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="cca2e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cca2e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cca2e-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="cca2e-113">Name</span></span></p></td>
<td><p><span data-ttu-id="cca2e-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cca2e-114">Required</span></span></p></td>
<td><p><span data-ttu-id="cca2e-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="cca2e-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="cca2e-116">Nombre del índice que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="cca2e-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cca2e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cca2e-117">Remarks</span></span>

<span data-ttu-id="cca2e-118">El método **Delete** sólo se admite cuando el objeto **Index** es nuevo y no se ha anexado a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cca2e-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

