---
title: AffectEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9e1bd4d86e6e269c9363daca0ffa7b8df6303326
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863672"
---
# <a name="affectenum"></a><span data-ttu-id="e618f-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="e618f-102">AffectEnum</span></span>

<span data-ttu-id="e618f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e618f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e618f-104">Especifica a qué registros afecta una operación.</span><span class="sxs-lookup"><span data-stu-id="e618f-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e618f-105">Constante</span><span class="sxs-lookup"><span data-stu-id="e618f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e618f-106">Valor</span><span class="sxs-lookup"><span data-stu-id="e618f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e618f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e618f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e618f-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="e618f-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="e618f-109">3</span><span class="sxs-lookup"><span data-stu-id="e618f-109">3</span></span></p></td>
<td><p><span data-ttu-id="e618f-110">Si no existe ninguna propiedad <a href="filter-property-ado.md">Filter</a> aplicada al objeto <strong>Recordset</strong>, afecta a todos los registros.
</span><span class="sxs-lookup"><span data-stu-id="e618f-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="e618f-111">Si la propiedad <strong>Filter</strong> se establece en criterios de cadena (como &quot;autor = 'Cervantes'&quot;), la operación afecta a registros visibles del capítulo actual.</span><span class="sxs-lookup"><span data-stu-id="e618f-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="e618f-112">Si la propiedad <strong>Filter</strong> se establece en un miembro de <a href="filtergroupenum.md">FilterGroupEnum</a> o una matriz de marcadores, la operación afectará a todas las filas del <strong>conjunto de registros</strong>.</span><span class="sxs-lookup"><span data-stu-id="e618f-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p>
<p><span data-ttu-id="e618f-113"><strong>Nota</strong>: adAffectAll está oculto en el Explorador de objetos de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e618f-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e618f-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="e618f-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="e618f-115">4</span><span class="sxs-lookup"><span data-stu-id="e618f-115">4</span></span></p></td>
<td><p><span data-ttu-id="e618f-116">Afecta a todos los registros de todos los capítulos secundarios del <strong>Recordset</strong>, incluidos aquellos no visibles a través de ningún <strong>Filtro</strong> aplicado actualmente.</span><span class="sxs-lookup"><span data-stu-id="e618f-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e618f-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="e618f-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="e618f-118">1</span><span class="sxs-lookup"><span data-stu-id="e618f-118">1</span></span></p></td>
<td><p><span data-ttu-id="e618f-119">Afecta sólo al registro actual.</span><span class="sxs-lookup"><span data-stu-id="e618f-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e618f-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="e618f-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="e618f-121">2</span><span class="sxs-lookup"><span data-stu-id="e618f-121">2</span></span></p></td>
<td><p><span data-ttu-id="e618f-p102">Afecta únicamente a los registros que cumplen el valor actual de la propiedad <a href="filter-property-ado.md">Filter</a>. Para usar esta opción, debe establecer la propiedad <strong>Filter</strong> en un valor <strong>FilterGroupEnum</strong> o en una matriz de <strong>marcadores</strong>.</span><span class="sxs-lookup"><span data-stu-id="e618f-p102">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting. You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e618f-124">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="e618f-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="e618f-125">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="e618f-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e618f-126">Constante</span><span class="sxs-lookup"><span data-stu-id="e618f-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e618f-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="e618f-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e618f-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="e618f-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e618f-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="e618f-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e618f-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="e618f-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

