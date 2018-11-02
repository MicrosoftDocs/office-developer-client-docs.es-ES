---
title: Indexes.Delete (método) (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66f08fa9733de0b63ca8bb659972abbc59183e16
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922324"
---
# <a name="indexesdelete-method-dao"></a><span data-ttu-id="62e24-102">Indexes.Delete (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="62e24-102">Indexes.Delete method (DAO)</span></span>


<span data-ttu-id="62e24-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62e24-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="62e24-104">Elimina el objeto **Index** especificado de la colección **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="62e24-104">Deletes the specified **Index** from the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="62e24-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62e24-105">Syntax</span></span>

<span data-ttu-id="62e24-106">*expresión* . Delete (***nombre***)</span><span class="sxs-lookup"><span data-stu-id="62e24-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="62e24-107">*expresión* Variable que representa un objeto **Indexes** .</span><span class="sxs-lookup"><span data-stu-id="62e24-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="62e24-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62e24-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="62e24-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="62e24-109">Name</span></span></p></th>
<th><p><span data-ttu-id="62e24-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="62e24-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="62e24-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="62e24-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="62e24-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="62e24-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62e24-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="62e24-113">Name</span></span></p></td>
<td><p><span data-ttu-id="62e24-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="62e24-114">Required</span></span></p></td>
<td><p><span data-ttu-id="62e24-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="62e24-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="62e24-116">Nombre del índice que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="62e24-116">The name of the index to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="62e24-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62e24-117">Remarks</span></span>

<span data-ttu-id="62e24-118">El método **Delete** sólo se admite cuando el objeto **Index** es nuevo y no se ha anexado a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="62e24-118">The **Delete** method is supported only when the **Index** object is new and hasn’t been appended to the database.</span></span>

