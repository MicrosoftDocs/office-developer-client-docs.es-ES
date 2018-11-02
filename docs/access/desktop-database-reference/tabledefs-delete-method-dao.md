---
title: TableDefs.Delete (método) (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 122f30e5f6310bc180dd43582a6e1e05cc970d4b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926496"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="7255e-102">TableDefs.Delete (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="7255e-102">TableDefs.Delete method (DAO)</span></span>


<span data-ttu-id="7255e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7255e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7255e-104">Elimina el objeto **TableDef** especificado de la colección **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="7255e-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7255e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7255e-105">Syntax</span></span>

<span data-ttu-id="7255e-106">*expresión* . Delete (***nombre***)</span><span class="sxs-lookup"><span data-stu-id="7255e-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="7255e-107">*expresión* Variable que representa un objeto **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="7255e-107">*expression* A variable that represents a **TableDefs** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="7255e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7255e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7255e-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="7255e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7255e-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="7255e-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="7255e-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7255e-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="7255e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7255e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7255e-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="7255e-113">Name</span></span></p></td>
<td><p><span data-ttu-id="7255e-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7255e-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7255e-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7255e-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7255e-116">Nombre de TableDef que se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="7255e-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7255e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7255e-117">Remarks</span></span>

<span data-ttu-id="7255e-118">El método Delete está admitido sólo cuando el objeto **TableDef** es nuevo y no se ha anexado a la base de datos, o cuando la propiedad **Updatable** de **TableDef** está establecida en **True**.</span><span class="sxs-lookup"><span data-stu-id="7255e-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

