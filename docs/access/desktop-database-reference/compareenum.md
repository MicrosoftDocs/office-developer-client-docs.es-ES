---
title: CompareEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 8c35b04dc1b5aa0a97236ff7ece260018cbe29c3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860311"
---
# <a name="compareenum"></a><span data-ttu-id="85d1e-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="85d1e-102">CompareEnum</span></span>

<span data-ttu-id="85d1e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="85d1e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="85d1e-104">Especifica la posición relativa de dos registros representados por sus marcadores.</span><span class="sxs-lookup"><span data-stu-id="85d1e-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85d1e-105">Constante</span><span class="sxs-lookup"><span data-stu-id="85d1e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="85d1e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="85d1e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="85d1e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="85d1e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85d1e-108"><strong>adCompareEqual</strong></span><span class="sxs-lookup"><span data-stu-id="85d1e-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="85d1e-109">1</span><span class="sxs-lookup"><span data-stu-id="85d1e-109">1</span></span></p></td>
<td><p><span data-ttu-id="85d1e-110">Indica que los marcadores son iguales.</span><span class="sxs-lookup"><span data-stu-id="85d1e-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d1e-111"><strong>adCompareGreaterThan</strong></span><span class="sxs-lookup"><span data-stu-id="85d1e-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="85d1e-112">2</span><span class="sxs-lookup"><span data-stu-id="85d1e-112">2</span></span></p></td>
<td><p><span data-ttu-id="85d1e-113">Indica que el primer marcador está después del segundo.</span><span class="sxs-lookup"><span data-stu-id="85d1e-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d1e-114"><strong>adCompareLessThan</strong></span><span class="sxs-lookup"><span data-stu-id="85d1e-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="85d1e-115">0</span><span class="sxs-lookup"><span data-stu-id="85d1e-115">0</span></span></p></td>
<td><p><span data-ttu-id="85d1e-116">Indica que el primer marcador está antes que el segundo.</span><span class="sxs-lookup"><span data-stu-id="85d1e-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d1e-117"><strong>adCompareNotComparable</strong></span><span class="sxs-lookup"><span data-stu-id="85d1e-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="85d1e-118">4</span><span class="sxs-lookup"><span data-stu-id="85d1e-118">4</span></span></p></td>
<td><p><span data-ttu-id="85d1e-119">Indica que los marcadores no se pueden comparar.</span><span class="sxs-lookup"><span data-stu-id="85d1e-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d1e-120"><strong>adCompareNotEqual</strong></span><span class="sxs-lookup"><span data-stu-id="85d1e-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="85d1e-121">3</span><span class="sxs-lookup"><span data-stu-id="85d1e-121">3</span></span></p></td>
<td><p><span data-ttu-id="85d1e-122">Indica que los marcadores no son iguales y no están ordenados.</span><span class="sxs-lookup"><span data-stu-id="85d1e-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="85d1e-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="85d1e-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="85d1e-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="85d1e-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85d1e-125">Constante</span><span class="sxs-lookup"><span data-stu-id="85d1e-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85d1e-126">AdoEnums.Compare.EQUAL</span><span class="sxs-lookup"><span data-stu-id="85d1e-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d1e-127">AdoEnums.Compare.GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="85d1e-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d1e-128">AdoEnums.Compare.LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="85d1e-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85d1e-129">AdoEnums.Compare.NOTCOMPARABLE</span><span class="sxs-lookup"><span data-stu-id="85d1e-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85d1e-130">AdoEnums.Compare.NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="85d1e-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

