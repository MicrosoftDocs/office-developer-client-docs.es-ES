---
title: RecordStatusEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88929ced56583316c42f2d5195054e51e98a1d5b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484730"
---
# <a name="recordstatusenum"></a><span data-ttu-id="c77a0-102">RecordStatusEnum</span><span class="sxs-lookup"><span data-stu-id="c77a0-102">RecordStatusEnum</span></span>


<span data-ttu-id="c77a0-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c77a0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c77a0-104">Especifica el estado de un registro con respecto a actualizaciones por lotes y otras operaciones masivas.</span><span class="sxs-lookup"><span data-stu-id="c77a0-104">Specifies the status of a record with regard to batch updates and other bulk operations.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c77a0-105">Constante</span><span class="sxs-lookup"><span data-stu-id="c77a0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c77a0-106">Valor</span><span class="sxs-lookup"><span data-stu-id="c77a0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c77a0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c77a0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-108"><strong>adRecCanceled</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-108"><strong>adRecCanceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-109">0 x 100</span><span class="sxs-lookup"><span data-stu-id="c77a0-109">0x100</span></span></p></td>
<td><p><span data-ttu-id="c77a0-110">Indica que no se guardó el registro porque se canceló la operación.</span><span class="sxs-lookup"><span data-stu-id="c77a0-110">Indicates that the record was not saved because the operation was canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-111"><strong>adRecCantRelease</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-111"><strong>adRecCantRelease</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-112">0 x 400</span><span class="sxs-lookup"><span data-stu-id="c77a0-112">0x400</span></span></p></td>
<td><p><span data-ttu-id="c77a0-113">Indica que no se guardó el nuevo registro porque el registro existente estaba bloqueado.</span><span class="sxs-lookup"><span data-stu-id="c77a0-113">Indicates that the new record was not saved because the existing record was locked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-114"><strong>adRecConcurrencyViolation</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-114"><strong>adRecConcurrencyViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-115">0 x 800</span><span class="sxs-lookup"><span data-stu-id="c77a0-115">0x800</span></span></p></td>
<td><p><span data-ttu-id="c77a0-116">Indica que no se guardó el registro porque se estaba aplicando concurrencia optimista.</span><span class="sxs-lookup"><span data-stu-id="c77a0-116">Indicates that the record was not saved because optimistic concurrency was in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-117"><strong>adRecDBDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-117"><strong>adRecDBDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-118">0 x 40000</span><span class="sxs-lookup"><span data-stu-id="c77a0-118">0x40000</span></span></p></td>
<td><p><span data-ttu-id="c77a0-119">Indica que el registro ya se ha eliminado del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="c77a0-119">Indicates that the record has already been deleted from the data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-120"><strong>adRecDeleted</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-120"><strong>adRecDeleted</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-121">0 x 4</span><span class="sxs-lookup"><span data-stu-id="c77a0-121">0x4</span></span></p></td>
<td><p><span data-ttu-id="c77a0-122">Indica que se eliminó el registro.</span><span class="sxs-lookup"><span data-stu-id="c77a0-122">Indicates that the record was deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-123"><strong>adRecIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-123"><strong>adRecIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="c77a0-124">0x1000</span></span></p></td>
<td><p><span data-ttu-id="c77a0-125">Indica que no se guardó el registro porque el usuario infringió restricciones de integridad.</span><span class="sxs-lookup"><span data-stu-id="c77a0-125">Indicates that the record was not saved because the user violated integrity constraints.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-126"><strong>adRecInvalid</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-126"><strong>adRecInvalid</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-127">0 x 10</span><span class="sxs-lookup"><span data-stu-id="c77a0-127">0x10</span></span></p></td>
<td><p><span data-ttu-id="c77a0-128">Indica que no se guardó el registro porque su marcador no es válido.</span><span class="sxs-lookup"><span data-stu-id="c77a0-128">Indicates that the record was not saved because its bookmark is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-129"><strong>adRecMaxChangesExceeded</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-129"><strong>adRecMaxChangesExceeded</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-130">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="c77a0-130">0x2000</span></span></p></td>
<td><p><span data-ttu-id="c77a0-131">Indica que no se guardó el registro porque había demasiados cambios pendientes.</span><span class="sxs-lookup"><span data-stu-id="c77a0-131">Indicates that the record was not saved because there were too many pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-132"><strong>adRecModified</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-132"><strong>adRecModified</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-133">0x2</span><span class="sxs-lookup"><span data-stu-id="c77a0-133">0x2</span></span></p></td>
<td><p><span data-ttu-id="c77a0-134">Indica que se modificó el registro.</span><span class="sxs-lookup"><span data-stu-id="c77a0-134">Indicates that the record was modified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-135"><strong>adRecMultipleChanges</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-135"><strong>adRecMultipleChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-136">0 x 40</span><span class="sxs-lookup"><span data-stu-id="c77a0-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="c77a0-137">Indica que el registro no se guardó debido a que habría afectado a varios registros.</span><span class="sxs-lookup"><span data-stu-id="c77a0-137">Indicates that the record was not saved because it would have affected multiple records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-138"><strong>adRecNew</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-138"><strong>adRecNew</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-139">0x1</span><span class="sxs-lookup"><span data-stu-id="c77a0-139">0x1</span></span></p></td>
<td><p><span data-ttu-id="c77a0-140">Indica que el registro es nuevo.</span><span class="sxs-lookup"><span data-stu-id="c77a0-140">Indicates that the record is new.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-141"><strong>adRecObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-141"><strong>adRecObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="c77a0-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="c77a0-143">Indica que no se guardó el registro debido a un conflicto con un objeto de almacenamiento abierto.</span><span class="sxs-lookup"><span data-stu-id="c77a0-143">Indicates that the record was not saved because of a conflict with an open storage object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-144"><strong>adRecOK</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-144"><strong>adRecOK</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-145">0</span><span class="sxs-lookup"><span data-stu-id="c77a0-145">0</span></span></p></td>
<td><p><span data-ttu-id="c77a0-146">Indica que el registro se actualizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c77a0-146">Indicates that the record was successfully updated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-147"><strong>adRecOutOfMemory</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-147"><strong>adRecOutOfMemory</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-148">0 x 8000</span><span class="sxs-lookup"><span data-stu-id="c77a0-148">0x8000</span></span></p></td>
<td><p><span data-ttu-id="c77a0-149">Indica que no se guardó el registro a causa de que el equipo se ha quedado sin memoria.</span><span class="sxs-lookup"><span data-stu-id="c77a0-149">Indicates that the record was not saved because the computer has run out of memory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-150"><strong>adRecPendingChanges</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-150"><strong>adRecPendingChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-151">0 x 80</span><span class="sxs-lookup"><span data-stu-id="c77a0-151">0x80</span></span></p></td>
<td><p><span data-ttu-id="c77a0-152">Indica que no se guardó el registro debido a que hace referencia a una inserción pendiente.</span><span class="sxs-lookup"><span data-stu-id="c77a0-152">Indicates that the record was not saved because it refers to a pending insert.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-153"><strong>adRecPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-153"><strong>adRecPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-154">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="c77a0-154">0x10000</span></span></p></td>
<td><p><span data-ttu-id="c77a0-155">Indica que no se guardó el registro porque el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="c77a0-155">Indicates that the record was not saved because the user has insufficient permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-156"><strong>adRecSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-156"><strong>adRecSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-157">0 x 20000</span><span class="sxs-lookup"><span data-stu-id="c77a0-157">0x20000</span></span></p></td>
<td><p><span data-ttu-id="c77a0-158">Indica que el registro no se guardó debido a que no satisface la estructura de la base de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="c77a0-158">Indicates that the record was not saved because it violates the structure of the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-159"><strong>adRecUnmodified</strong></span><span class="sxs-lookup"><span data-stu-id="c77a0-159"><strong>adRecUnmodified</strong></span></span></p></td>
<td><p><span data-ttu-id="c77a0-160">0 x 8</span><span class="sxs-lookup"><span data-stu-id="c77a0-160">0x8</span></span></p></td>
<td><p><span data-ttu-id="c77a0-161">Indica que no se modificó el registro.</span><span class="sxs-lookup"><span data-stu-id="c77a0-161">Indicates that the record was not modified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c77a0-162">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="c77a0-162">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="c77a0-163">AdoEnums.RecordStatus.</span><span class="sxs-lookup"><span data-stu-id="c77a0-163">AdoEnums.RecordStatus.</span></span>

<span data-ttu-id="c77a0-164">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c77a0-164">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c77a0-165">Constante</span><span class="sxs-lookup"><span data-stu-id="c77a0-165">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-166">AdoEnums.RecordStatus.CANCELED</span><span class="sxs-lookup"><span data-stu-id="c77a0-166">AdoEnums.RecordStatus.CANCELED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-167">AdoEnums.RecordStatus.CANTRELEASE</span><span class="sxs-lookup"><span data-stu-id="c77a0-167">AdoEnums.RecordStatus.CANTRELEASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="c77a0-168">AdoEnums.RecordStatus.CONCURRENCYVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-169">AdoEnums.RecordStatus.DBDELETED</span><span class="sxs-lookup"><span data-stu-id="c77a0-169">AdoEnums.RecordStatus.DBDELETED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-170">AdoEnums.RecordStatus.DELETED</span><span class="sxs-lookup"><span data-stu-id="c77a0-170">AdoEnums.RecordStatus.DELETED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span><span class="sxs-lookup"><span data-stu-id="c77a0-171">AdoEnums.RecordStatus.INTEGRITYVIOLATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-172">AdoEnums.RecordStatus.INVALID</span><span class="sxs-lookup"><span data-stu-id="c77a0-172">AdoEnums.RecordStatus.INVALID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span><span class="sxs-lookup"><span data-stu-id="c77a0-173">AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-174">AdoEnums.RecordStatus.MODIFIED</span><span class="sxs-lookup"><span data-stu-id="c77a0-174">AdoEnums.RecordStatus.MODIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span><span class="sxs-lookup"><span data-stu-id="c77a0-175">AdoEnums.RecordStatus.MULTIPLECHANGES</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-176">AdoEnums.RecordStatus.NEW</span><span class="sxs-lookup"><span data-stu-id="c77a0-176">AdoEnums.RecordStatus.NEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-177">AdoEnums.RecordStatus.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="c77a0-177">AdoEnums.RecordStatus.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-178">AdoEnums.RecordStatus.OK</span><span class="sxs-lookup"><span data-stu-id="c77a0-178">AdoEnums.RecordStatus.OK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-179">AdoEnums.RecordStatus.OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="c77a0-179">AdoEnums.RecordStatus.OUTOFMEMORY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-180">AdoEnums.RecordStatus.PENDINGCHANGES</span><span class="sxs-lookup"><span data-stu-id="c77a0-180">AdoEnums.RecordStatus.PENDINGCHANGES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span><span class="sxs-lookup"><span data-stu-id="c77a0-181">AdoEnums.RecordStatus.PERMISSIONDENIED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c77a0-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span><span class="sxs-lookup"><span data-stu-id="c77a0-182">AdoEnums.RecordStatus.SCHEMAVIOLATION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c77a0-183">AdoEnums.RecordStatus.UNMODIFIED</span><span class="sxs-lookup"><span data-stu-id="c77a0-183">AdoEnums.RecordStatus.UNMODIFIED</span></span></p></td>
</tr>
</tbody>
</table>

