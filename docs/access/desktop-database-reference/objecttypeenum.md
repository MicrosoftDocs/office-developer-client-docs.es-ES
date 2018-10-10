---
title: ObjectTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38992451063e71609ab822bb231362f7a0f2cb3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483857"
---
# <a name="objecttypeenum"></a><span data-ttu-id="fb953-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="fb953-102">ObjectTypeEnum</span></span>


<span data-ttu-id="fb953-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb953-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fb953-104">Especifica el tipo de objeto de base de datos para que el que se establecerán permisos o propiedad.</span><span class="sxs-lookup"><span data-stu-id="fb953-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb953-105">Constante</span><span class="sxs-lookup"><span data-stu-id="fb953-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="fb953-106">Valor</span><span class="sxs-lookup"><span data-stu-id="fb953-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fb953-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb953-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb953-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="fb953-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="fb953-109">2</span><span class="sxs-lookup"><span data-stu-id="fb953-109">2</span></span></p></td>
<td><p><span data-ttu-id="fb953-110">El objeto es una columna.</span><span class="sxs-lookup"><span data-stu-id="fb953-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb953-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="fb953-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="fb953-112">3</span><span class="sxs-lookup"><span data-stu-id="fb953-112">3</span></span></p></td>
<td><p><span data-ttu-id="fb953-113">El objeto es una base de datos.</span><span class="sxs-lookup"><span data-stu-id="fb953-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb953-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="fb953-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="fb953-115">4</span><span class="sxs-lookup"><span data-stu-id="fb953-115">4</span></span></p></td>
<td><p><span data-ttu-id="fb953-116">El objeto es un procedimiento.</span><span class="sxs-lookup"><span data-stu-id="fb953-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb953-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="fb953-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="fb953-118">-1</span><span class="sxs-lookup"><span data-stu-id="fb953-118">-1</span></span></p></td>
<td><p><span data-ttu-id="fb953-p101">El objeto es un tipo definido por el proveedor. Se producirá un error si el parámetro <em>ObjectType</em> es <strong>adPermObjProviderSpecific</strong> y si no se proporciona un valor de <em>ObjectTypeId</em>.</span><span class="sxs-lookup"><span data-stu-id="fb953-p101">The object is a type defined by the provider. An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb953-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="fb953-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="fb953-122">1</span><span class="sxs-lookup"><span data-stu-id="fb953-122">1</span></span></p></td>
<td><p><span data-ttu-id="fb953-123">El objeto es una tabla.</span><span class="sxs-lookup"><span data-stu-id="fb953-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb953-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="fb953-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="fb953-125">5</span><span class="sxs-lookup"><span data-stu-id="fb953-125">5</span></span></p></td>
<td><p><span data-ttu-id="fb953-126">El objeto es una vista.</span><span class="sxs-lookup"><span data-stu-id="fb953-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

