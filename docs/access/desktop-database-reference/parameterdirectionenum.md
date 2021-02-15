---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fac07165416841691ee7bc3ca5dfcdc366861023
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287975"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="82e02-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="82e02-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="82e02-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82e02-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82e02-104">Especifica si el objeto [Parameter](parameter-object-ado.md) representa un parámetro de entrada, un parámetro de salida, ambos o el valor devuelto desde un procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="82e02-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82e02-105">Constante</span><span class="sxs-lookup"><span data-stu-id="82e02-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="82e02-106">Valor</span><span class="sxs-lookup"><span data-stu-id="82e02-106">Value</span></span></p></th>
<th><p><span data-ttu-id="82e02-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="82e02-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82e02-108"><strong>adParamInput</strong></span><span class="sxs-lookup"><span data-stu-id="82e02-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="82e02-109">1 </span><span class="sxs-lookup"><span data-stu-id="82e02-109">1</span></span></p></td>
<td><p><span data-ttu-id="82e02-p101">Valor predeterminado. Indica que el parámetro representa un parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="82e02-p101">Default. Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82e02-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="82e02-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="82e02-113">3 </span><span class="sxs-lookup"><span data-stu-id="82e02-113">3</span></span></p></td>
<td><p><span data-ttu-id="82e02-114">Indica que el parámetro representa un parámetro de entrada y de salida.</span><span class="sxs-lookup"><span data-stu-id="82e02-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82e02-115"><strong>adParamOutput</strong></span><span class="sxs-lookup"><span data-stu-id="82e02-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="82e02-116">2 </span><span class="sxs-lookup"><span data-stu-id="82e02-116">2</span></span></p></td>
<td><p><span data-ttu-id="82e02-117">Indica que el parámetro representa un parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="82e02-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82e02-118"><strong>adParamReturnValue</strong></span><span class="sxs-lookup"><span data-stu-id="82e02-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="82e02-119">4 </span><span class="sxs-lookup"><span data-stu-id="82e02-119">4</span></span></p></td>
<td><p><span data-ttu-id="82e02-120">Indica que el parámetro representa un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="82e02-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82e02-121"><strong>adParamUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="82e02-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="82e02-122">0</span><span class="sxs-lookup"><span data-stu-id="82e02-122">0</span></span></p></td>
<td><p><span data-ttu-id="82e02-123">Indica que se desconoce la dirección del parámetro.</span><span class="sxs-lookup"><span data-stu-id="82e02-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="82e02-124">Equivalente a ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="82e02-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="82e02-125">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="82e02-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82e02-126">Constante</span><span class="sxs-lookup"><span data-stu-id="82e02-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82e02-127">AdoEnums.ParameterDirection.INPUT</span><span class="sxs-lookup"><span data-stu-id="82e02-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82e02-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="82e02-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82e02-129">AdoEnums.ParameterDirection.OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82e02-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82e02-130">AdoEnums.ParameterDirection.RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="82e02-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82e02-131">AdoEnums.ParameterDirection.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="82e02-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

