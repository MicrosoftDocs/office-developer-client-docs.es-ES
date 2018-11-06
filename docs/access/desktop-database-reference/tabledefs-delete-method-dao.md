---
title: TableDefs.Delete (método) (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d511155f7a5fe1e6b83092e2065302bab99765b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999011"
---
# <a name="tabledefsdelete-method-dao"></a><span data-ttu-id="71c3d-102">TableDefs.Delete (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="71c3d-102">TableDefs.Delete method (DAO)</span></span>

<span data-ttu-id="71c3d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71c3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71c3d-104">Elimina el objeto **TableDef** especificado de la colección **TableDefs**.</span><span class="sxs-lookup"><span data-stu-id="71c3d-104">Deletes the specified **TableDef** object from the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c3d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71c3d-105">Syntax</span></span>

<span data-ttu-id="71c3d-106">*expresión* . Delete (***nombre***)</span><span class="sxs-lookup"><span data-stu-id="71c3d-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="71c3d-107">*expresión* Variable que representa un objeto **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="71c3d-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="71c3d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71c3d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71c3d-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="71c3d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="71c3d-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="71c3d-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="71c3d-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="71c3d-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="71c3d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="71c3d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71c3d-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="71c3d-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="71c3d-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="71c3d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="71c3d-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="71c3d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="71c3d-116">Nombre de TableDef que se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="71c3d-116">The name of the TableDef to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="71c3d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71c3d-117">Remarks</span></span>

<span data-ttu-id="71c3d-118">El método Delete está admitido sólo cuando el objeto **TableDef** es nuevo y no se ha anexado a la base de datos, o cuando la propiedad **Updatable** de **TableDef** está establecida en **True**.</span><span class="sxs-lookup"><span data-stu-id="71c3d-118">The Delete method is supported only when the **TableDef** object is new and hasn’t been appended to the database, or when the **Updatable** property of the **TableDef** is set to **True**.</span></span>

