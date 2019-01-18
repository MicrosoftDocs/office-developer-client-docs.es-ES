---
title: EventStatusEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712585"
---
# <a name="eventstatusenum"></a><span data-ttu-id="bed3c-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="bed3c-102">EventStatusEnum</span></span>

<span data-ttu-id="bed3c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bed3c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bed3c-104">Especifica el estado actual de la ejecución de un evento.</span><span class="sxs-lookup"><span data-stu-id="bed3c-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bed3c-105">Constante</span><span class="sxs-lookup"><span data-stu-id="bed3c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="bed3c-106">Valor</span><span class="sxs-lookup"><span data-stu-id="bed3c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="bed3c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="bed3c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bed3c-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="bed3c-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="bed3c-109">4</span><span class="sxs-lookup"><span data-stu-id="bed3c-109">4</span></span></p></td>
<td><p><span data-ttu-id="bed3c-110">Solicita la cancelación de la operación que ocasionó el evento.</span><span class="sxs-lookup"><span data-stu-id="bed3c-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bed3c-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="bed3c-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="bed3c-112">3</span><span class="sxs-lookup"><span data-stu-id="bed3c-112">3</span></span></p></td>
<td><p><span data-ttu-id="bed3c-113">Indica que la operación no puede solicitar la cancelación de la operación pendiente.</span><span class="sxs-lookup"><span data-stu-id="bed3c-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bed3c-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="bed3c-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="bed3c-115">2</span><span class="sxs-lookup"><span data-stu-id="bed3c-115">2</span></span></p></td>
<td><p><span data-ttu-id="bed3c-116">Indica que la operación que provocó el evento no funcionó correctamente debido a uno o varios errores.</span><span class="sxs-lookup"><span data-stu-id="bed3c-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bed3c-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="bed3c-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="bed3c-118">1</span><span class="sxs-lookup"><span data-stu-id="bed3c-118">1</span></span></p></td>
<td><p><span data-ttu-id="bed3c-119">Indica que la operación que provocó el evento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bed3c-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bed3c-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="bed3c-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="bed3c-121">5</span><span class="sxs-lookup"><span data-stu-id="bed3c-121">5</span></span></p></td>
<td><p><span data-ttu-id="bed3c-122">Impide posibles notificaciones posteriores antes de que el método de evento haya terminado de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="bed3c-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="bed3c-123">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="bed3c-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="bed3c-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="bed3c-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bed3c-125">Constante</span><span class="sxs-lookup"><span data-stu-id="bed3c-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bed3c-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="bed3c-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bed3c-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="bed3c-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bed3c-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="bed3c-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bed3c-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="bed3c-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bed3c-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="bed3c-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

