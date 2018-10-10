---
title: CompareEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9cef64707cb2797c6ad4f1090749779f147c87f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484600"
---
# <a name="compareenum"></a><span data-ttu-id="59294-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="59294-102">CompareEnum</span></span>


<span data-ttu-id="59294-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="59294-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="59294-104">Especifica la posición relativa de dos registros representados por sus marcadores.</span><span class="sxs-lookup"><span data-stu-id="59294-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59294-105">Constante</span><span class="sxs-lookup"><span data-stu-id="59294-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="59294-106">Valor</span><span class="sxs-lookup"><span data-stu-id="59294-106">Value</span></span></p></th>
<th><p><span data-ttu-id="59294-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="59294-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59294-108"><strong>adCompareEqual</strong></span><span class="sxs-lookup"><span data-stu-id="59294-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="59294-109">1</span><span class="sxs-lookup"><span data-stu-id="59294-109">1</span></span></p></td>
<td><p><span data-ttu-id="59294-110">Indica que los marcadores son iguales.</span><span class="sxs-lookup"><span data-stu-id="59294-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59294-111"><strong>adCompareGreaterThan</strong></span><span class="sxs-lookup"><span data-stu-id="59294-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="59294-112">2</span><span class="sxs-lookup"><span data-stu-id="59294-112">2</span></span></p></td>
<td><p><span data-ttu-id="59294-113">Indica que el primer marcador está después del segundo.</span><span class="sxs-lookup"><span data-stu-id="59294-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59294-114"><strong>adCompareLessThan</strong></span><span class="sxs-lookup"><span data-stu-id="59294-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="59294-115">0</span><span class="sxs-lookup"><span data-stu-id="59294-115">0</span></span></p></td>
<td><p><span data-ttu-id="59294-116">Indica que el primer marcador está antes que el segundo.</span><span class="sxs-lookup"><span data-stu-id="59294-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59294-117"><strong>adCompareNotComparable</strong></span><span class="sxs-lookup"><span data-stu-id="59294-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="59294-118">4</span><span class="sxs-lookup"><span data-stu-id="59294-118">4</span></span></p></td>
<td><p><span data-ttu-id="59294-119">Indica que los marcadores no se pueden comparar.</span><span class="sxs-lookup"><span data-stu-id="59294-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59294-120"><strong>adCompareNotEqual</strong></span><span class="sxs-lookup"><span data-stu-id="59294-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="59294-121">3</span><span class="sxs-lookup"><span data-stu-id="59294-121">3</span></span></p></td>
<td><p><span data-ttu-id="59294-122">Indica que los marcadores no son iguales y no están ordenados.</span><span class="sxs-lookup"><span data-stu-id="59294-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="59294-123">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="59294-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="59294-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="59294-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59294-125">Constante</span><span class="sxs-lookup"><span data-stu-id="59294-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59294-126">AdoEnums.Compare.EQUAL</span><span class="sxs-lookup"><span data-stu-id="59294-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59294-127">AdoEnums.Compare.GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="59294-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59294-128">AdoEnums.Compare.LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="59294-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59294-129">AdoEnums.Compare.NOTCOMPARABLE</span><span class="sxs-lookup"><span data-stu-id="59294-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59294-130">AdoEnums.Compare.NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="59294-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

