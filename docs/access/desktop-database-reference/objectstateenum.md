---
title: ObjectStateEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: e15faf0b31965a0a8a71440f424729b13b117b05
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861459"
---
# <a name="objectstateenum"></a><span data-ttu-id="22a66-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="22a66-102">ObjectStateEnum</span></span>

<span data-ttu-id="22a66-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="22a66-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="22a66-104">Especifica si un objeto está abierto o cerrado, conectando con un origen de datos, ejecutando un comando o recuperando datos.</span><span class="sxs-lookup"><span data-stu-id="22a66-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22a66-105">Constante</span><span class="sxs-lookup"><span data-stu-id="22a66-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="22a66-106">Valor</span><span class="sxs-lookup"><span data-stu-id="22a66-106">Value</span></span></p></th>
<th><p><span data-ttu-id="22a66-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="22a66-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22a66-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="22a66-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="22a66-109">0</span><span class="sxs-lookup"><span data-stu-id="22a66-109">0</span></span></p></td>
<td><p><span data-ttu-id="22a66-110">Indica que el objeto está cerrado.</span><span class="sxs-lookup"><span data-stu-id="22a66-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a66-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="22a66-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="22a66-112">1</span><span class="sxs-lookup"><span data-stu-id="22a66-112">1</span></span></p></td>
<td><p><span data-ttu-id="22a66-113">Indica que el objeto está abierto.</span><span class="sxs-lookup"><span data-stu-id="22a66-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a66-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="22a66-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="22a66-115">2</span><span class="sxs-lookup"><span data-stu-id="22a66-115">2</span></span></p></td>
<td><p><span data-ttu-id="22a66-116">Indica que el objeto se está conectando.</span><span class="sxs-lookup"><span data-stu-id="22a66-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a66-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="22a66-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="22a66-118">4</span><span class="sxs-lookup"><span data-stu-id="22a66-118">4</span></span></p></td>
<td><p><span data-ttu-id="22a66-119">Indica que el objeto está ejecutando un comando.</span><span class="sxs-lookup"><span data-stu-id="22a66-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a66-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="22a66-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="22a66-121">8</span><span class="sxs-lookup"><span data-stu-id="22a66-121">8</span></span></p></td>
<td><p><span data-ttu-id="22a66-122">Indica que se están recuperando las filas del objeto.</span><span class="sxs-lookup"><span data-stu-id="22a66-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="22a66-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="22a66-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="22a66-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="22a66-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22a66-125">Constante</span><span class="sxs-lookup"><span data-stu-id="22a66-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22a66-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="22a66-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a66-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="22a66-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a66-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="22a66-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22a66-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="22a66-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22a66-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="22a66-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

