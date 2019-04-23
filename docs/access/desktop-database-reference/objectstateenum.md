---
title: ObjectStateEnum (referencia de base de datos de escritorio de Access)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288528"
---
# <a name="objectstateenum"></a><span data-ttu-id="64a30-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="64a30-102">ObjectStateEnum</span></span>

<span data-ttu-id="64a30-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64a30-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64a30-104">Especifica si un objeto está abierto o cerrado, conectando con un origen de datos, ejecutando un comando o recuperando datos.</span><span class="sxs-lookup"><span data-stu-id="64a30-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64a30-105">Constante</span><span class="sxs-lookup"><span data-stu-id="64a30-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="64a30-106">Valor</span><span class="sxs-lookup"><span data-stu-id="64a30-106">Value</span></span></p></th>
<th><p><span data-ttu-id="64a30-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="64a30-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64a30-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="64a30-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="64a30-109">comprendi</span><span class="sxs-lookup"><span data-stu-id="64a30-109">0</span></span></p></td>
<td><p><span data-ttu-id="64a30-110">Indica que el objeto está cerrado.</span><span class="sxs-lookup"><span data-stu-id="64a30-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64a30-111"><strong>adStateOpen</strong></span><span class="sxs-lookup"><span data-stu-id="64a30-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="64a30-112">1</span><span class="sxs-lookup"><span data-stu-id="64a30-112">1</span></span></p></td>
<td><p><span data-ttu-id="64a30-113">Indica que el objeto está abierto.</span><span class="sxs-lookup"><span data-stu-id="64a30-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64a30-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="64a30-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="64a30-115">segundo</span><span class="sxs-lookup"><span data-stu-id="64a30-115">2</span></span></p></td>
<td><p><span data-ttu-id="64a30-116">Indica que el objeto se está conectando.</span><span class="sxs-lookup"><span data-stu-id="64a30-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64a30-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="64a30-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="64a30-118">4</span><span class="sxs-lookup"><span data-stu-id="64a30-118">4</span></span></p></td>
<td><p><span data-ttu-id="64a30-119">Indica que el objeto está ejecutando un comando.</span><span class="sxs-lookup"><span data-stu-id="64a30-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64a30-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="64a30-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="64a30-121">8,5</span><span class="sxs-lookup"><span data-stu-id="64a30-121">8</span></span></p></td>
<td><p><span data-ttu-id="64a30-122">Indica que se están recuperando las filas del objeto.</span><span class="sxs-lookup"><span data-stu-id="64a30-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="64a30-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="64a30-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="64a30-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="64a30-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64a30-125">Constante</span><span class="sxs-lookup"><span data-stu-id="64a30-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64a30-126">AdoEnums. state. CLOSED</span><span class="sxs-lookup"><span data-stu-id="64a30-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64a30-127">AdoEnums. state. OPEN</span><span class="sxs-lookup"><span data-stu-id="64a30-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64a30-128">AdoEnums. state. CONNECTing</span><span class="sxs-lookup"><span data-stu-id="64a30-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64a30-129">AdoEnums. state. EXECUTing</span><span class="sxs-lookup"><span data-stu-id="64a30-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64a30-130">AdoEnums. state. FETCH</span><span class="sxs-lookup"><span data-stu-id="64a30-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

