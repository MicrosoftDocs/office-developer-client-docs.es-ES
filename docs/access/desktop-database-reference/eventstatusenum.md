---
title: EventStatusEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 027ecde525d603b15bb7844e99edc2534774bb37
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867618"
---
# <a name="eventstatusenum"></a><span data-ttu-id="f0bab-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="f0bab-102">EventStatusEnum</span></span>

<span data-ttu-id="f0bab-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0bab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0bab-104">Especifica el estado actual de la ejecución de un evento.</span><span class="sxs-lookup"><span data-stu-id="f0bab-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0bab-105">Constante</span><span class="sxs-lookup"><span data-stu-id="f0bab-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f0bab-106">Valor</span><span class="sxs-lookup"><span data-stu-id="f0bab-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f0bab-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0bab-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0bab-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="f0bab-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="f0bab-109">4</span><span class="sxs-lookup"><span data-stu-id="f0bab-109">4</span></span></p></td>
<td><p><span data-ttu-id="f0bab-110">Solicita la cancelación de la operación que ocasionó el evento.</span><span class="sxs-lookup"><span data-stu-id="f0bab-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0bab-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="f0bab-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="f0bab-112">3</span><span class="sxs-lookup"><span data-stu-id="f0bab-112">3</span></span></p></td>
<td><p><span data-ttu-id="f0bab-113">Indica que la operación no puede solicitar la cancelación de la operación pendiente.</span><span class="sxs-lookup"><span data-stu-id="f0bab-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0bab-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="f0bab-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="f0bab-115">2</span><span class="sxs-lookup"><span data-stu-id="f0bab-115">2</span></span></p></td>
<td><p><span data-ttu-id="f0bab-116">Indica que la operación que provocó el evento no funcionó correctamente debido a uno o varios errores.</span><span class="sxs-lookup"><span data-stu-id="f0bab-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0bab-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="f0bab-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="f0bab-118">1</span><span class="sxs-lookup"><span data-stu-id="f0bab-118">1</span></span></p></td>
<td><p><span data-ttu-id="f0bab-119">Indica que la operación que provocó el evento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f0bab-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0bab-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="f0bab-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="f0bab-121">5</span><span class="sxs-lookup"><span data-stu-id="f0bab-121">5</span></span></p></td>
<td><p><span data-ttu-id="f0bab-122">Impide posibles notificaciones posteriores antes de que el método de evento haya terminado de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="f0bab-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f0bab-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="f0bab-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="f0bab-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f0bab-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f0bab-125">Constante</span><span class="sxs-lookup"><span data-stu-id="f0bab-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0bab-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="f0bab-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0bab-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="f0bab-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0bab-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="f0bab-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0bab-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="f0bab-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0bab-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="f0bab-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

