---
title: IsolationLevelEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7e32cd3c8ae78199f90fcac8cccdf377bf332d38
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863944"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="ec864-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="ec864-102">IsolationLevelEnum</span></span>

<span data-ttu-id="ec864-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec864-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ec864-104">Especifica el nivel de aislamiento de transacción para un objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ec864-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec864-105">Constante</span><span class="sxs-lookup"><span data-stu-id="ec864-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ec864-106">Valor</span><span class="sxs-lookup"><span data-stu-id="ec864-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ec864-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec864-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec864-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="ec864-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="ec864-109">-1</span><span class="sxs-lookup"><span data-stu-id="ec864-109">-1</span></span></p></td>
<td><p><span data-ttu-id="ec864-110">Indica que el proveedor usa un nivel de aislamiento diferente del especificado, pero que no se puede determinar.</span><span class="sxs-lookup"><span data-stu-id="ec864-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec864-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="ec864-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="ec864-112">16</span><span class="sxs-lookup"><span data-stu-id="ec864-112">16</span></span></p></td>
<td><p><span data-ttu-id="ec864-113">Indica que los cambios pendientes procedentes de transacciones con mayor nivel de aislamiento no se pueden sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="ec864-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec864-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="ec864-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="ec864-115">256</span><span class="sxs-lookup"><span data-stu-id="ec864-115">256</span></span></p></td>
<td><p><span data-ttu-id="ec864-116">Indica que, desde una transacción, es posible ver cambios no confirmados en otras transacciones.</span><span class="sxs-lookup"><span data-stu-id="ec864-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec864-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="ec864-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="ec864-118">256</span><span class="sxs-lookup"><span data-stu-id="ec864-118">256</span></span></p></td>
<td><p><span data-ttu-id="ec864-119">Igual que <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec864-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec864-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="ec864-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="ec864-121">4096</span><span class="sxs-lookup"><span data-stu-id="ec864-121">4096</span></span></p></td>
<td><p><span data-ttu-id="ec864-122">Indica que, desde una transacción, es posible ver cambios en otras transacciones sólo después de que se hayan confirmado.</span><span class="sxs-lookup"><span data-stu-id="ec864-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec864-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="ec864-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="ec864-124">4096</span><span class="sxs-lookup"><span data-stu-id="ec864-124">4096</span></span></p></td>
<td><p><span data-ttu-id="ec864-125">Igual que <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec864-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec864-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="ec864-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="ec864-127">65536</span><span class="sxs-lookup"><span data-stu-id="ec864-127">65536</span></span></p></td>
<td><p><span data-ttu-id="ec864-128">Indica que, desde una transacción, no es posible ver cambios realizados en otras transacciones, pero que, volviendo a hacer consultas, se pueden recuperar nuevos objetos <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec864-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec864-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="ec864-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="ec864-130">1048576</span><span class="sxs-lookup"><span data-stu-id="ec864-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="ec864-131">Indica que las transacciones se llevan a cabo aisladas de otras transacciones.</span><span class="sxs-lookup"><span data-stu-id="ec864-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec864-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="ec864-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="ec864-133">1048576</span><span class="sxs-lookup"><span data-stu-id="ec864-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="ec864-134">Igual que <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec864-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ec864-135">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ec864-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="ec864-136">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ec864-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec864-137">Constante</span><span class="sxs-lookup"><span data-stu-id="ec864-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec864-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="ec864-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec864-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="ec864-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec864-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="ec864-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec864-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="ec864-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec864-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="ec864-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec864-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="ec864-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec864-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="ec864-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec864-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="ec864-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec864-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="ec864-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

