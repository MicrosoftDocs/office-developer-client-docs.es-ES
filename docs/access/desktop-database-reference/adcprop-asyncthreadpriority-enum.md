---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ae89c81b903930eb114cf050688598bc2802a25e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485837"
---
# <a name="adcpropasyncthreadpriorityenum"></a><span data-ttu-id="c8e95-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span><span class="sxs-lookup"><span data-stu-id="c8e95-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span></span>

<span data-ttu-id="c8e95-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8e95-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c8e95-104">Para un objeto [Recordset](recordset-object-ado.md) de RDS, especifica la prioridad de ejecución del subproceso asincrónico que recupera datos.</span><span class="sxs-lookup"><span data-stu-id="c8e95-104">For an RDS [Recordset](recordset-object-ado.md) object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span>

<span data-ttu-id="c8e95-105">Use estas constantes con la propiedad dinámica "**Background Thread Priority**" del objeto **Recordset** que aparece en el Índice de propiedades dinámicas de ADO y se explica en la documentación del [Servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md).</span><span class="sxs-lookup"><span data-stu-id="c8e95-105">Use these constants with the **Recordset** "**Background Thread Priority**" dynamic property, which is referenced in the ADO Dynamic Property Index and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8e95-106">Constante</span><span class="sxs-lookup"><span data-stu-id="c8e95-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="c8e95-107">Valor</span><span class="sxs-lookup"><span data-stu-id="c8e95-107">Value</span></span></p></th>
<th><p><span data-ttu-id="c8e95-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8e95-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8e95-109"><strong>adPriorityAboveNormal</strong></span><span class="sxs-lookup"><span data-stu-id="c8e95-109"><strong>adPriorityAboveNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="c8e95-110">4</span><span class="sxs-lookup"><span data-stu-id="c8e95-110">4</span></span></p></td>
<td><p><span data-ttu-id="c8e95-111">Establece las prioridades comprendidas entre la normal y la más alta.</span><span class="sxs-lookup"><span data-stu-id="c8e95-111">Sets priority between normal and highest.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8e95-112"><strong>adPriorityBelowNormal</strong></span><span class="sxs-lookup"><span data-stu-id="c8e95-112"><strong>adPriorityBelowNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="c8e95-113">2</span><span class="sxs-lookup"><span data-stu-id="c8e95-113">2</span></span></p></td>
<td><p><span data-ttu-id="c8e95-114">Establece las prioridades comprendidas entre la normal y la más baja.</span><span class="sxs-lookup"><span data-stu-id="c8e95-114">Sets priority between lowest and normal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8e95-115"><strong>adPriorityHighest</strong></span><span class="sxs-lookup"><span data-stu-id="c8e95-115"><strong>adPriorityHighest</strong></span></span></p></td>
<td><p><span data-ttu-id="c8e95-116">5</span><span class="sxs-lookup"><span data-stu-id="c8e95-116">5</span></span></p></td>
<td><p><span data-ttu-id="c8e95-117">Establece la prioridad en el nivel más alto posible.</span><span class="sxs-lookup"><span data-stu-id="c8e95-117">Sets priority to the highest possible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8e95-118"><strong>AdPriorityLowest</strong></span><span class="sxs-lookup"><span data-stu-id="c8e95-118"><strong>AdPriorityLowest</strong></span></span></p></td>
<td><p><span data-ttu-id="c8e95-119">1</span><span class="sxs-lookup"><span data-stu-id="c8e95-119">1</span></span></p></td>
<td><p><span data-ttu-id="c8e95-120">Establece la prioridad en el nivel más bajo posible.</span><span class="sxs-lookup"><span data-stu-id="c8e95-120">Sets priority to the lowest possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8e95-121"><strong>adPriorityNormal</strong></span><span class="sxs-lookup"><span data-stu-id="c8e95-121"><strong>adPriorityNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="c8e95-122">3</span><span class="sxs-lookup"><span data-stu-id="c8e95-122">3</span></span></p></td>
<td><p><span data-ttu-id="c8e95-123">Establece la prioridad como normal.</span><span class="sxs-lookup"><span data-stu-id="c8e95-123">Sets priority to normal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8e95-124">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="c8e95-124">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="c8e95-125">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c8e95-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8e95-126">Constante</span><span class="sxs-lookup"><span data-stu-id="c8e95-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8e95-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span><span class="sxs-lookup"><span data-stu-id="c8e95-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8e95-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span><span class="sxs-lookup"><span data-stu-id="c8e95-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8e95-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span><span class="sxs-lookup"><span data-stu-id="c8e95-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8e95-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span><span class="sxs-lookup"><span data-stu-id="c8e95-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8e95-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span><span class="sxs-lookup"><span data-stu-id="c8e95-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span></span></p></td>
</tr>
</tbody>
</table>

