---
title: LockTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 57cef1ca3a31665db1db517c22756213abf49042
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860535"
---
# <a name="locktypeenum"></a><span data-ttu-id="9ac55-102">LockTypeEnum</span><span class="sxs-lookup"><span data-stu-id="9ac55-102">LockTypeEnum</span></span>

<span data-ttu-id="9ac55-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ac55-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9ac55-104">Especifica el tipo de bloqueo colocado en los registros durante su modificación.</span><span class="sxs-lookup"><span data-stu-id="9ac55-104">Specifies the type of lock placed on records during editing.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ac55-105">Constante</span><span class="sxs-lookup"><span data-stu-id="9ac55-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="9ac55-106">Valor</span><span class="sxs-lookup"><span data-stu-id="9ac55-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9ac55-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ac55-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ac55-108"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="9ac55-108"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="9ac55-109">4</span><span class="sxs-lookup"><span data-stu-id="9ac55-109">4</span></span></p></td>
<td><p><span data-ttu-id="9ac55-p101">Indica actualizaciones optimistas por lotes. Se requiere para el modo de actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="9ac55-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ac55-112"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="9ac55-112"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="9ac55-113">3</span><span class="sxs-lookup"><span data-stu-id="9ac55-113">3</span></span></p></td>
<td><p><span data-ttu-id="9ac55-p102">Indica un bloqueo optimista, registro por registro. El proveedor usa el bloqueo optimista para bloquear registros sólo al llamar al método <a href="update-method-ado.md">Update</a>.</span><span class="sxs-lookup"><span data-stu-id="9ac55-p102">Indicates optimistic locking, record by record. The provider uses optimistic locking, locking records only when you call the <a href="update-method-ado.md">Update</a> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ac55-116"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="9ac55-116"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="9ac55-117">2</span><span class="sxs-lookup"><span data-stu-id="9ac55-117">2</span></span></p></td>
<td><p><span data-ttu-id="9ac55-p103">Indica un bloqueo pesimista, registro por registro. El proveedor realiza las acciones necesarias para garantizar la modificación correcta de los registros, normalmente bloqueando los registros en el origen de datos inmediatamente después de la modificación.</span><span class="sxs-lookup"><span data-stu-id="9ac55-p103">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately after editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ac55-120"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="9ac55-120"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="9ac55-121">1</span><span class="sxs-lookup"><span data-stu-id="9ac55-121">1</span></span></p></td>
<td><p><span data-ttu-id="9ac55-p104">Indica registros de sólo lectura. No es posible alterar los datos.</span><span class="sxs-lookup"><span data-stu-id="9ac55-p104">Indicates read-only records. You cannot alter the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ac55-124"><strong>adLockUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="9ac55-124"><strong>adLockUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="9ac55-125">-1</span><span class="sxs-lookup"><span data-stu-id="9ac55-125">-1</span></span></p></td>
<td><p><span data-ttu-id="9ac55-p105">No especifica un tipo de bloqueo. En caso de duplicados, el duplicado se crea con el mismo tipo de bloqueo que el original.</span><span class="sxs-lookup"><span data-stu-id="9ac55-p105">Does not specify a type of lock. For clones, the clone is created with the same lock type as the original.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9ac55-128">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="9ac55-128">ADO/WFC equivalent</span></span>

<span data-ttu-id="9ac55-129">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9ac55-129">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ac55-130">Constante</span><span class="sxs-lookup"><span data-stu-id="9ac55-130">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ac55-131">AdoEnums.LockType.BATCHOPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="9ac55-131">AdoEnums.LockType.BATCHOPTIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ac55-132">AdoEnums.LockType.OPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="9ac55-132">AdoEnums.LockType.OPTIMISTIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ac55-133">AdoEnums.LockType.PESSIMISTIC</span><span class="sxs-lookup"><span data-stu-id="9ac55-133">AdoEnums.LockType.PESSIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ac55-134">AdoEnums.LockType.READONLY</span><span class="sxs-lookup"><span data-stu-id="9ac55-134">AdoEnums.LockType.READONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ac55-135">AdoEnums.LockType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="9ac55-135">AdoEnums.LockType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

