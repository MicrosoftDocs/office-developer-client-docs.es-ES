---
title: IsolationLevelEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80e7d22a5152b24894bf746b939f705739d4220d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486673"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="a2b7e-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="a2b7e-102">IsolationLevelEnum</span></span>


<span data-ttu-id="a2b7e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2b7e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a2b7e-104">Especifica el nivel de aislamiento de transacción para un objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a2b7e-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2b7e-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a2b7e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a2b7e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a2b7e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a2b7e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2b7e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2b7e-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="a2b7e-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b7e-109">-1</span><span class="sxs-lookup"><span data-stu-id="a2b7e-109">-1</span></span></p></td>
<td><p><span data-ttu-id="a2b7e-110">Indica que el proveedor usa un nivel de aislamiento diferente del especificado, pero que no se puede determinar.</span><span class="sxs-lookup"><span data-stu-id="a2b7e-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b7e-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="a2b7e-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b7e-112">16</span><span class="sxs-lookup"><span data-stu-id="a2b7e-112">16</span></span></p></td>
<td><p><span data-ttu-id="a2b7e-113">Indica que los cambios pendientes procedentes de transacciones con mayor nivel de aislamiento no se pueden sobrescribir.</span><span class="sxs-lookup"><span data-stu-id="a2b7e-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b7e-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="a2b7e-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b7e-115">256</span><span class="sxs-lookup"><span data-stu-id="a2b7e-115">256</span></span></p></td>
<td><p><span data-ttu-id="a2b7e-116">Indica que, desde una transacción, es posible ver cambios no confirmados en otras transacciones.</span><span class="sxs-lookup"><span data-stu-id="a2b7e-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b7e-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="a2b7e-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b7e-118">256</span><span class="sxs-lookup"><span data-stu-id="a2b7e-118">256</span></span></p></td>
<td><p><span data-ttu-id="a2b7e-119">Igual que <strong>adXactBrowse</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2b7e-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b7e-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="a2b7e-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b7e-121">4096</span><span class="sxs-lookup"><span data-stu-id="a2b7e-121">4096</span></span></p></td>
<td><p><span data-ttu-id="a2b7e-122">Indica que, desde una transacción, es posible ver cambios en otras transacciones sólo después de que se hayan confirmado.</span><span class="sxs-lookup"><span data-stu-id="a2b7e-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b7e-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="a2b7e-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b7e-124">4096</span><span class="sxs-lookup"><span data-stu-id="a2b7e-124">4096</span></span></p></td>
<td><p><span data-ttu-id="a2b7e-125">Igual que <strong>adXactCursorStability</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2b7e-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b7e-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="a2b7e-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b7e-127">65536</span><span class="sxs-lookup"><span data-stu-id="a2b7e-127">65536</span></span></p></td>
<td><p><span data-ttu-id="a2b7e-128">Indica que, desde una transacción, no es posible ver cambios realizados en otras transacciones, pero que, volviendo a hacer consultas, se pueden recuperar nuevos objetos <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2b7e-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b7e-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="a2b7e-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b7e-130">1048576</span><span class="sxs-lookup"><span data-stu-id="a2b7e-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="a2b7e-131">Indica que las transacciones se llevan a cabo aisladas de otras transacciones.</span><span class="sxs-lookup"><span data-stu-id="a2b7e-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b7e-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="a2b7e-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="a2b7e-133">1048576</span><span class="sxs-lookup"><span data-stu-id="a2b7e-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="a2b7e-134">Igual que <strong>adXactIsolated</strong>.</span><span class="sxs-lookup"><span data-stu-id="a2b7e-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a2b7e-135">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="a2b7e-135">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="a2b7e-136">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a2b7e-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2b7e-137">Constante</span><span class="sxs-lookup"><span data-stu-id="a2b7e-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2b7e-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="a2b7e-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b7e-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="a2b7e-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b7e-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="a2b7e-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b7e-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="a2b7e-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b7e-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="a2b7e-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b7e-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="a2b7e-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b7e-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="a2b7e-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2b7e-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="a2b7e-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2b7e-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="a2b7e-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>
