---
title: FilterGroupEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5c42b703536e931405325d3a91219a148e6580d1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873292"
---
# <a name="filtergroupenum"></a><span data-ttu-id="188e9-102">FilterGroupEnum</span><span class="sxs-lookup"><span data-stu-id="188e9-102">FilterGroupEnum</span></span>

<span data-ttu-id="188e9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="188e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="188e9-104">Especifica el grupo de registros que se van a filtrar desde un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="188e9-104">Specifies the group of records to be filtered from a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="188e9-105">Constante</span><span class="sxs-lookup"><span data-stu-id="188e9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="188e9-106">Valor</span><span class="sxs-lookup"><span data-stu-id="188e9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="188e9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="188e9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="188e9-108"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="188e9-108"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="188e9-109">2</span><span class="sxs-lookup"><span data-stu-id="188e9-109">2</span></span></p></td>
<td><p><span data-ttu-id="188e9-110">Filtra de modo que sólo se vean los registros afectados por la última llamada a <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a> o <a href="cancelbatch-method-ado.md">CancelBatch</a>.</span><span class="sxs-lookup"><span data-stu-id="188e9-110">Filters for viewing only records affected by the last <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a>, or <a href="cancelbatch-method-ado.md">CancelBatch</a> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="188e9-111"><strong>adFilterConflictingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="188e9-111"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="188e9-112">5</span><span class="sxs-lookup"><span data-stu-id="188e9-112">5</span></span></p></td>
<td><p><span data-ttu-id="188e9-113">Filtra de modo que sólo se vean los registros que no superaron la última actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="188e9-113">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="188e9-114"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="188e9-114"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="188e9-115">3</span><span class="sxs-lookup"><span data-stu-id="188e9-115">3</span></span></p></td>
<td><p><span data-ttu-id="188e9-116">Filtra de modo que sólo se vean los registros almacenados en la memoria caché actual, es decir, el resultado de la última llamada para recuperar registros de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="188e9-116">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="188e9-117"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="188e9-117"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="188e9-118">0</span><span class="sxs-lookup"><span data-stu-id="188e9-118">0</span></span></p></td>
<td><p><span data-ttu-id="188e9-119">Quita el filtro actual de modo que vuelvan a verse todos los registros.</span><span class="sxs-lookup"><span data-stu-id="188e9-119">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="188e9-120"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="188e9-120"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="188e9-121">1</span><span class="sxs-lookup"><span data-stu-id="188e9-121">1</span></span></p></td>
<td><p><span data-ttu-id="188e9-p101">Filtra de modo que sólo se vean los registros que han cambiado pero que aún no se han enviado al servidor. Aplicable sólo para el modo de actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="188e9-p101">Filters for viewing only records that have changed but have not yet been sent to the server. Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="188e9-124">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="188e9-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="188e9-125">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="188e9-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="188e9-126">Constante</span><span class="sxs-lookup"><span data-stu-id="188e9-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="188e9-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="188e9-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="188e9-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="188e9-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="188e9-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="188e9-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="188e9-130">AdoEnums.FilterGroup.NONE</span><span class="sxs-lookup"><span data-stu-id="188e9-130">AdoEnums.FilterGroup.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="188e9-131">AdoEnums.FilterGroup.PENDINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="188e9-131">AdoEnums.FilterGroup.PENDINGRECORDS</span></span></p></td>
</tr>
</tbody>
</table>

