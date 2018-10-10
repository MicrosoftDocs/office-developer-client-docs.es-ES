---
title: ObjectStateEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a08713e5363cb023021e2dd5acb6b38431a6b5e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486664"
---
# <a name="objectstateenum"></a><span data-ttu-id="b1afe-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="b1afe-102">ObjectStateEnum</span></span>


<span data-ttu-id="b1afe-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1afe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b1afe-104">Especifica si un objeto está abierto o cerrado, conectando con un origen de datos, ejecutando un comando o recuperando datos.</span><span class="sxs-lookup"><span data-stu-id="b1afe-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1afe-105">Constante</span><span class="sxs-lookup"><span data-stu-id="b1afe-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b1afe-106">Valor</span><span class="sxs-lookup"><span data-stu-id="b1afe-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b1afe-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1afe-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1afe-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="b1afe-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="b1afe-109">0</span><span class="sxs-lookup"><span data-stu-id="b1afe-109">0</span></span></p></td>
<td><p><span data-ttu-id="b1afe-110">Indica que el objeto está cerrado.</span><span class="sxs-lookup"><span data-stu-id="b1afe-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1afe-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="b1afe-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="b1afe-112">1</span><span class="sxs-lookup"><span data-stu-id="b1afe-112">1</span></span></p></td>
<td><p><span data-ttu-id="b1afe-113">Indica que el objeto está abierto.</span><span class="sxs-lookup"><span data-stu-id="b1afe-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1afe-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="b1afe-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="b1afe-115">2</span><span class="sxs-lookup"><span data-stu-id="b1afe-115">2</span></span></p></td>
<td><p><span data-ttu-id="b1afe-116">Indica que el objeto se está conectando.</span><span class="sxs-lookup"><span data-stu-id="b1afe-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1afe-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="b1afe-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="b1afe-118">4</span><span class="sxs-lookup"><span data-stu-id="b1afe-118">4</span></span></p></td>
<td><p><span data-ttu-id="b1afe-119">Indica que el objeto está ejecutando un comando.</span><span class="sxs-lookup"><span data-stu-id="b1afe-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1afe-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="b1afe-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="b1afe-121">8</span><span class="sxs-lookup"><span data-stu-id="b1afe-121">8</span></span></p></td>
<td><p><span data-ttu-id="b1afe-122">Indica que se están recuperando las filas del objeto.</span><span class="sxs-lookup"><span data-stu-id="b1afe-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1afe-123">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="b1afe-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="b1afe-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b1afe-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b1afe-125">Constante</span><span class="sxs-lookup"><span data-stu-id="b1afe-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1afe-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="b1afe-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1afe-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="b1afe-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1afe-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="b1afe-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1afe-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="b1afe-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1afe-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="b1afe-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

