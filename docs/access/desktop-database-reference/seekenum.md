---
title: SeekEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f8334cbfc8e0f6a362a36e03984739d1d52b6f6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698613"
---
# <a name="seekenum"></a><span data-ttu-id="413e0-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="413e0-102">SeekEnum</span></span>

<span data-ttu-id="413e0-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="413e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="413e0-104">Especifica el tipo de búsqueda ([Seek](seek-method-ado.md)) que se debe ejecutar.</span><span class="sxs-lookup"><span data-stu-id="413e0-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="413e0-105">Constante</span><span class="sxs-lookup"><span data-stu-id="413e0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="413e0-106">Valor</span><span class="sxs-lookup"><span data-stu-id="413e0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="413e0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="413e0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="413e0-108">adSeekFirstEQ</span><span class="sxs-lookup"><span data-stu-id="413e0-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="413e0-109">1</span><span class="sxs-lookup"><span data-stu-id="413e0-109">1</span></span></p></td>
<td><p><span data-ttu-id="413e0-110">Busca la primera clave igual a <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="413e0-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="413e0-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="413e0-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="413e0-112">2</span><span class="sxs-lookup"><span data-stu-id="413e0-112">2</span></span></p></td>
<td><p><span data-ttu-id="413e0-113">Busca la última clave igual a <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="413e0-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="413e0-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="413e0-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="413e0-115">4</span><span class="sxs-lookup"><span data-stu-id="413e0-115">4</span></span></p></td>
<td><p><span data-ttu-id="413e0-116">Busca una clave igual a <em>KeyValues</em> o justo después de donde la coincidencia se habría producido.</span><span class="sxs-lookup"><span data-stu-id="413e0-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="413e0-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="413e0-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="413e0-118">8</span><span class="sxs-lookup"><span data-stu-id="413e0-118">8</span></span></p></td>
<td><p><span data-ttu-id="413e0-119">Busca una clave justo después de donde se habría producido una coincidencia con <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="413e0-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="413e0-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="413e0-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="413e0-121">16</span><span class="sxs-lookup"><span data-stu-id="413e0-121">16</span></span></p></td>
<td><p><span data-ttu-id="413e0-122">Busca una clave igual a <em>KeyValues</em> o justo antes de donde se habría producido esa coincidencia.</span><span class="sxs-lookup"><span data-stu-id="413e0-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="413e0-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="413e0-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="413e0-124">32</span><span class="sxs-lookup"><span data-stu-id="413e0-124">32</span></span></p></td>
<td><p><span data-ttu-id="413e0-125">Busca una clave justo antes de donde se habría producido una coincidencia con <em>KeyValues</em>.</span><span class="sxs-lookup"><span data-stu-id="413e0-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="413e0-126">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="413e0-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="413e0-127">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="413e0-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="413e0-128">Constante</span><span class="sxs-lookup"><span data-stu-id="413e0-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="413e0-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="413e0-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="413e0-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="413e0-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="413e0-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="413e0-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="413e0-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="413e0-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="413e0-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="413e0-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="413e0-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="413e0-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

