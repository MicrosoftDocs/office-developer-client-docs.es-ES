---
title: ObjectTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e3b470c8c0d0c3f04b59bd382b66117bd79c188
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711836"
---
# <a name="objecttypeenum"></a><span data-ttu-id="f4246-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="f4246-102">ObjectTypeEnum</span></span>

<span data-ttu-id="f4246-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4246-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4246-104">Especifica el tipo de objeto de base de datos para que el que se establecerán permisos o propiedad.</span><span class="sxs-lookup"><span data-stu-id="f4246-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4246-105">Constante</span><span class="sxs-lookup"><span data-stu-id="f4246-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f4246-106">Valor</span><span class="sxs-lookup"><span data-stu-id="f4246-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f4246-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4246-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4246-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="f4246-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="f4246-109">2</span><span class="sxs-lookup"><span data-stu-id="f4246-109">2</span></span></p></td>
<td><p><span data-ttu-id="f4246-110">El objeto es una columna.</span><span class="sxs-lookup"><span data-stu-id="f4246-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4246-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="f4246-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="f4246-112">3</span><span class="sxs-lookup"><span data-stu-id="f4246-112">3</span></span></p></td>
<td><p><span data-ttu-id="f4246-113">El objeto es una base de datos.</span><span class="sxs-lookup"><span data-stu-id="f4246-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4246-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="f4246-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="f4246-115">4</span><span class="sxs-lookup"><span data-stu-id="f4246-115">4</span></span></p></td>
<td><p><span data-ttu-id="f4246-116">El objeto es un procedimiento.</span><span class="sxs-lookup"><span data-stu-id="f4246-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4246-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="f4246-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="f4246-118">-1</span><span class="sxs-lookup"><span data-stu-id="f4246-118">-1</span></span></p></td>
<td><p><span data-ttu-id="f4246-p101">El objeto es un tipo definido por el proveedor. Se producirá un error si el parámetro <em>ObjectType</em> es <strong>adPermObjProviderSpecific</strong> y si no se proporciona un valor de <em>ObjectTypeId</em>.</span><span class="sxs-lookup"><span data-stu-id="f4246-p101">The object is a type defined by the provider. An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4246-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="f4246-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="f4246-122">1</span><span class="sxs-lookup"><span data-stu-id="f4246-122">1</span></span></p></td>
<td><p><span data-ttu-id="f4246-123">El objeto es una tabla.</span><span class="sxs-lookup"><span data-stu-id="f4246-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4246-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="f4246-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="f4246-125">5</span><span class="sxs-lookup"><span data-stu-id="f4246-125">5</span></span></p></td>
<td><p><span data-ttu-id="f4246-126">El objeto es una vista.</span><span class="sxs-lookup"><span data-stu-id="f4246-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

