---
title: SeekEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5025706d64927482b632a17a5f71839cd4186619
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861417"
---
# <a name="seekenum"></a><span data-ttu-id="0d833-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="0d833-102">SeekEnum</span></span>

<span data-ttu-id="0d833-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d833-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0d833-104">Especifica el tipo de búsqueda ([Seek](seek-method-ado.md)) que se debe ejecutar.</span><span class="sxs-lookup"><span data-stu-id="0d833-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d833-105">Constante</span><span class="sxs-lookup"><span data-stu-id="0d833-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0d833-106">Valor</span><span class="sxs-lookup"><span data-stu-id="0d833-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0d833-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d833-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d833-108">adSeekFirstEQ</span><span class="sxs-lookup"><span data-stu-id="0d833-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="0d833-109">1</span><span class="sxs-lookup"><span data-stu-id="0d833-109">1</span></span></p></td>
<td><p><span data-ttu-id="0d833-110">Busca la primera clave igual a <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="0d833-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d833-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="0d833-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="0d833-112">2</span><span class="sxs-lookup"><span data-stu-id="0d833-112">2</span></span></p></td>
<td><p><span data-ttu-id="0d833-113">Busca la última clave igual a <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="0d833-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d833-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="0d833-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="0d833-115">4</span><span class="sxs-lookup"><span data-stu-id="0d833-115">4</span></span></p></td>
<td><p><span data-ttu-id="0d833-116">Busca una clave igual a <em>KeyValues</em> o justo después de donde la coincidencia se habría producido.</span><span class="sxs-lookup"><span data-stu-id="0d833-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d833-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="0d833-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="0d833-118">8</span><span class="sxs-lookup"><span data-stu-id="0d833-118">8</span></span></p></td>
<td><p><span data-ttu-id="0d833-119">Busca una clave justo después de donde se habría producido una coincidencia con <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="0d833-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d833-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="0d833-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="0d833-121">16</span><span class="sxs-lookup"><span data-stu-id="0d833-121">16</span></span></p></td>
<td><p><span data-ttu-id="0d833-122">Busca una clave igual a <em>KeyValues</em> o justo antes de donde se habría producido esa coincidencia.</span><span class="sxs-lookup"><span data-stu-id="0d833-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d833-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="0d833-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="0d833-124">32</span><span class="sxs-lookup"><span data-stu-id="0d833-124">32</span></span></p></td>
<td><p><span data-ttu-id="0d833-125">Busca una clave justo antes de donde se habría producido una coincidencia con <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="0d833-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0d833-126">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="0d833-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="0d833-127">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0d833-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d833-128">Constante</span><span class="sxs-lookup"><span data-stu-id="0d833-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d833-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="0d833-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d833-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="0d833-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d833-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="0d833-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d833-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="0d833-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d833-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="0d833-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d833-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="0d833-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

