---
title: IsolationLevelEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0176772b366b39d368f8bae1e402d420f0136c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707191"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="a7d52-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="a7d52-102">IsolationLevelEnum</span></span>

<span data-ttu-id="a7d52-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7d52-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a7d52-104">Especifica el nivel de aislamiento de transacción para un objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a7d52-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7d52-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a7d52-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a7d52-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a7d52-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a7d52-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7d52-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7d52-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="a7d52-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="a7d52-109">-1</span><span class="sxs-lookup"><span data-stu-id="a7d52-109">-1</span></span></p></td>
<td><p><span data-ttu-id="a7d52-110">Indica que el proveedor usa un nivel de aislamiento diferente del especificado, pero que no se puede determinar.</span><span class="sxs-lookup"><span data-stu-id="a7d52-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7d52-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="a7d52-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="a7d52-112">16</span><span class="sxs-lookup"><span data-stu-id="a7d52-112">16</span></span></p></td>
<td><p><span data-ttu-id="a7d52-113">Indica que los cambios pendientes procedentes de transacciones con mayor nivel de aislamiento no se pueden sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="a7d52-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7d52-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="a7d52-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="a7d52-115">256</span><span class="sxs-lookup"><span data-stu-id="a7d52-115">256</span></span></p></td>
<td><p><span data-ttu-id="a7d52-116">Indica que, desde una transacción, es posible ver cambios no confirmados en otras transacciones.</span><span class="sxs-lookup"><span data-stu-id="a7d52-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7d52-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="a7d52-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="a7d52-118">256</span><span class="sxs-lookup"><span data-stu-id="a7d52-118">256</span></span></p></td>
<td><p><span data-ttu-id="a7d52-119">Igual que <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="a7d52-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7d52-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="a7d52-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="a7d52-121">4096</span><span class="sxs-lookup"><span data-stu-id="a7d52-121">4096</span></span></p></td>
<td><p><span data-ttu-id="a7d52-122">Indica que, desde una transacción, es posible ver cambios en otras transacciones sólo después de que se hayan confirmado.</span><span class="sxs-lookup"><span data-stu-id="a7d52-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7d52-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="a7d52-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="a7d52-124">4096</span><span class="sxs-lookup"><span data-stu-id="a7d52-124">4096</span></span></p></td>
<td><p><span data-ttu-id="a7d52-125">Igual que <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="a7d52-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7d52-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="a7d52-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="a7d52-127">65536</span><span class="sxs-lookup"><span data-stu-id="a7d52-127">65536</span></span></p></td>
<td><p><span data-ttu-id="a7d52-128">Indica que, desde una transacción, no es posible ver cambios realizados en otras transacciones, pero que, volviendo a hacer consultas, se pueden recuperar nuevos objetos <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a7d52-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7d52-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="a7d52-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="a7d52-130">1048576</span><span class="sxs-lookup"><span data-stu-id="a7d52-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="a7d52-131">Indica que las transacciones se llevan a cabo aisladas de otras transacciones.</span><span class="sxs-lookup"><span data-stu-id="a7d52-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7d52-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="a7d52-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="a7d52-133">1048576</span><span class="sxs-lookup"><span data-stu-id="a7d52-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="a7d52-134">Igual que <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="a7d52-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="a7d52-135">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="a7d52-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="a7d52-136">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a7d52-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7d52-137">Constante</span><span class="sxs-lookup"><span data-stu-id="a7d52-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7d52-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="a7d52-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7d52-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="a7d52-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7d52-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="a7d52-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7d52-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="a7d52-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7d52-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="a7d52-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7d52-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="a7d52-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7d52-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="a7d52-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7d52-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="a7d52-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7d52-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="a7d52-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

