---
title: ObjectTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c5fb9dbf86823ab4d84327d97eceb037eb77dec0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863727"
---
# <a name="objecttypeenum"></a><span data-ttu-id="ffa45-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="ffa45-102">ObjectTypeEnum</span></span>

<span data-ttu-id="ffa45-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffa45-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ffa45-104">Especifica el tipo de objeto de base de datos para que el que se establecerán permisos o propiedad.</span><span class="sxs-lookup"><span data-stu-id="ffa45-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ffa45-105">Constante</span><span class="sxs-lookup"><span data-stu-id="ffa45-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ffa45-106">Valor</span><span class="sxs-lookup"><span data-stu-id="ffa45-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ffa45-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffa45-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ffa45-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="ffa45-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="ffa45-109">2</span><span class="sxs-lookup"><span data-stu-id="ffa45-109">2</span></span></p></td>
<td><p><span data-ttu-id="ffa45-110">El objeto es una columna.</span><span class="sxs-lookup"><span data-stu-id="ffa45-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffa45-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="ffa45-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="ffa45-112">3</span><span class="sxs-lookup"><span data-stu-id="ffa45-112">3</span></span></p></td>
<td><p><span data-ttu-id="ffa45-113">El objeto es una base de datos.</span><span class="sxs-lookup"><span data-stu-id="ffa45-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffa45-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="ffa45-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="ffa45-115">4</span><span class="sxs-lookup"><span data-stu-id="ffa45-115">4</span></span></p></td>
<td><p><span data-ttu-id="ffa45-116">El objeto es un procedimiento.</span><span class="sxs-lookup"><span data-stu-id="ffa45-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffa45-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="ffa45-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="ffa45-118">-1</span><span class="sxs-lookup"><span data-stu-id="ffa45-118">-1</span></span></p></td>
<td><p><span data-ttu-id="ffa45-p101">El objeto es un tipo definido por el proveedor. Se producirá un error si el parámetro <em>ObjectType</em> es <strong>adPermObjProviderSpecific</strong> y si no se proporciona un valor de <em>ObjectTypeId</em>.</span><span class="sxs-lookup"><span data-stu-id="ffa45-p101">The object is a type defined by the provider. An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffa45-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="ffa45-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="ffa45-122">1</span><span class="sxs-lookup"><span data-stu-id="ffa45-122">1</span></span></p></td>
<td><p><span data-ttu-id="ffa45-123">El objeto es una tabla.</span><span class="sxs-lookup"><span data-stu-id="ffa45-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffa45-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="ffa45-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="ffa45-125">5</span><span class="sxs-lookup"><span data-stu-id="ffa45-125">5</span></span></p></td>
<td><p><span data-ttu-id="ffa45-126">El objeto es una vista.</span><span class="sxs-lookup"><span data-stu-id="ffa45-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

