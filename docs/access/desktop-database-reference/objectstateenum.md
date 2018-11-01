---
title: ObjectStateEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 48fcf6c0135b4704155aa23765e848de5b3e6313
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879959"
---
# <a name="objectstateenum"></a><span data-ttu-id="9a7f7-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="9a7f7-102">ObjectStateEnum</span></span>

<span data-ttu-id="9a7f7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a7f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a7f7-104">Especifica si un objeto está abierto o cerrado, conectando con un origen de datos, ejecutando un comando o recuperando datos.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a7f7-105">Constante</span><span class="sxs-lookup"><span data-stu-id="9a7f7-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="9a7f7-106">Valor</span><span class="sxs-lookup"><span data-stu-id="9a7f7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9a7f7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a7f7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a7f7-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="9a7f7-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="9a7f7-109">0</span><span class="sxs-lookup"><span data-stu-id="9a7f7-109">0</span></span></p></td>
<td><p><span data-ttu-id="9a7f7-110">Indica que el objeto está cerrado.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a7f7-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="9a7f7-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="9a7f7-112">1</span><span class="sxs-lookup"><span data-stu-id="9a7f7-112">1</span></span></p></td>
<td><p><span data-ttu-id="9a7f7-113">Indica que el objeto está abierto.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a7f7-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="9a7f7-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="9a7f7-115">2</span><span class="sxs-lookup"><span data-stu-id="9a7f7-115">2</span></span></p></td>
<td><p><span data-ttu-id="9a7f7-116">Indica que el objeto se está conectando.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a7f7-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="9a7f7-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="9a7f7-118">4</span><span class="sxs-lookup"><span data-stu-id="9a7f7-118">4</span></span></p></td>
<td><p><span data-ttu-id="9a7f7-119">Indica que el objeto está ejecutando un comando.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a7f7-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="9a7f7-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="9a7f7-121">8</span><span class="sxs-lookup"><span data-stu-id="9a7f7-121">8</span></span></p></td>
<td><p><span data-ttu-id="9a7f7-122">Indica que se están recuperando las filas del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a7f7-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9a7f7-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="9a7f7-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="9a7f7-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9a7f7-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a7f7-125">Constante</span><span class="sxs-lookup"><span data-stu-id="9a7f7-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a7f7-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="9a7f7-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a7f7-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="9a7f7-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a7f7-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="9a7f7-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a7f7-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="9a7f7-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a7f7-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="9a7f7-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

