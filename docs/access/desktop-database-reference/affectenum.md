---
title: AffectEnum (referencia de bases de datos de escritorio de Access)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297203"
---
# <a name="affectenum"></a><span data-ttu-id="62bc2-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="62bc2-102">AffectEnum</span></span>

<span data-ttu-id="62bc2-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62bc2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="62bc2-104">Especifica a qué registros afecta una operación.</span><span class="sxs-lookup"><span data-stu-id="62bc2-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="62bc2-105">Constante</span><span class="sxs-lookup"><span data-stu-id="62bc2-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="62bc2-106">Valor</span><span class="sxs-lookup"><span data-stu-id="62bc2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="62bc2-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="62bc2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62bc2-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="62bc2-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="62bc2-109">3</span><span class="sxs-lookup"><span data-stu-id="62bc2-109">3</span></span></p></td>
<td><p><span data-ttu-id="62bc2-110">Si no existe ninguna propiedad <a href="filter-property-ado.md">Filter</a> aplicada al objeto <strong>Recordset</strong>, afecta a todos los registros.</span><span class="sxs-lookup"><span data-stu-id="62bc2-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="62bc2-111">Si la propiedad <strong>Filter</strong> se establece en un criterio de cadena (como &quot;author = ' Smith '&quot;), la operación afecta a registros visibles en el capítulo actual.</span><span class="sxs-lookup"><span data-stu-id="62bc2-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="62bc2-112">Si la propiedad <strong>Filter</strong> se establece en un miembro de <a href="filtergroupenum.md">FilterGroupEnum</a> o en una matriz de marcadores, la operación afectará a todas las filas del <strong>objeto Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="62bc2-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="62bc2-113"><strong>Nota</strong>: adAffectAll está oculto en el examinador de objetos de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="62bc2-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62bc2-114"><strong>adAffectAllChapters</strong></span><span class="sxs-lookup"><span data-stu-id="62bc2-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="62bc2-115">4</span><span class="sxs-lookup"><span data-stu-id="62bc2-115">4</span></span></p></td>
<td><p><span data-ttu-id="62bc2-116">Afecta a todos los registros de todos los capítulos secundarios del <strong>Recordset</strong>, incluidos aquellos no visibles a través de ningún <strong>Filtro</strong> aplicado actualmente.</span><span class="sxs-lookup"><span data-stu-id="62bc2-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62bc2-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="62bc2-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="62bc2-118">1</span><span class="sxs-lookup"><span data-stu-id="62bc2-118">1</span></span></p></td>
<td><p><span data-ttu-id="62bc2-119">Afecta sólo al registro actual.</span><span class="sxs-lookup"><span data-stu-id="62bc2-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62bc2-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="62bc2-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="62bc2-121">segundo</span><span class="sxs-lookup"><span data-stu-id="62bc2-121">2</span></span></p></td>
<td><p><span data-ttu-id="62bc2-p102">Afecta únicamente a los registros que cumplen el valor actual de la propiedad <a href="filter-property-ado.md">Filter</a>. Para usar esta opción, debe establecer la propiedad <strong>Filter</strong> en un valor <strong>FilterGroupEnum</strong> o en una matriz de <strong>marcadores</strong>.</span><span class="sxs-lookup"><span data-stu-id="62bc2-p102">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting. You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="62bc2-124">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="62bc2-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="62bc2-125">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="62bc2-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="62bc2-126">Constante</span><span class="sxs-lookup"><span data-stu-id="62bc2-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62bc2-127">AdoEnums. reVerse. ALL</span><span class="sxs-lookup"><span data-stu-id="62bc2-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62bc2-128">AdoEnums. inFluyeble. ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="62bc2-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62bc2-129">AdoEnums. inFluyeble. CURRENT</span><span class="sxs-lookup"><span data-stu-id="62bc2-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62bc2-130">AdoEnums. inFluye en el grupo</span><span class="sxs-lookup"><span data-stu-id="62bc2-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

