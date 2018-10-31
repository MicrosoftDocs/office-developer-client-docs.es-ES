---
title: ResyncEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 837bc16435ea574bd9d8e2e5e21ae50a4e852ee6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861081"
---
# <a name="resyncenum"></a><span data-ttu-id="ac546-102">ResyncEnum</span><span class="sxs-lookup"><span data-stu-id="ac546-102">ResyncEnum</span></span>

<span data-ttu-id="ac546-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac546-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ac546-104">Especifica si los valores subyacentes se sobrescriben al realizar una llamada a [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ac546-104">Specifies whether underlying values are overwritten by a call to [Resync](resync-method-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac546-105">Constante</span><span class="sxs-lookup"><span data-stu-id="ac546-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ac546-106">Valor</span><span class="sxs-lookup"><span data-stu-id="ac546-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ac546-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac546-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac546-108"><strong>adResyncAllValues</strong></span><span class="sxs-lookup"><span data-stu-id="ac546-108"><strong>adResyncAllValues</strong></span></span></p></td>
<td><p><span data-ttu-id="ac546-109">2</span><span class="sxs-lookup"><span data-stu-id="ac546-109">2</span></span></p></td>
<td><p><span data-ttu-id="ac546-p101">Valor predeterminado. Sobrescribe datos y se cancelan las actualizaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="ac546-p101">Default. Overwrites data, and pending updates are canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac546-112"><strong>adResyncUnderlyingValues</strong></span><span class="sxs-lookup"><span data-stu-id="ac546-112"><strong>adResyncUnderlyingValues</strong></span></span></p></td>
<td><p><span data-ttu-id="ac546-113">1</span><span class="sxs-lookup"><span data-stu-id="ac546-113">1</span></span></p></td>
<td><p><span data-ttu-id="ac546-114">No sobrescribe datos y no se cancelan las actualizaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="ac546-114">Does not overwrite data, and pending updates are not canceled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ac546-115">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ac546-115">ADO/WFC equivalent</span></span>

<span data-ttu-id="ac546-116">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ac546-116">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac546-117">Constante</span><span class="sxs-lookup"><span data-stu-id="ac546-117">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac546-118">AdoEnums.Resync.ALLVALUES</span><span class="sxs-lookup"><span data-stu-id="ac546-118">AdoEnums.Resync.ALLVALUES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac546-119">AdoEnums.Resync.UNDERLYINGVALUES</span><span class="sxs-lookup"><span data-stu-id="ac546-119">AdoEnums.Resync.UNDERLYINGVALUES</span></span></p></td>
</tr>
</tbody>
</table>

