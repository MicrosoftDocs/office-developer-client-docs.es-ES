---
title: EventStatusEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f49f584603c25997e1b01b94f23aaf9f5429a9e4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483312"
---
# <a name="eventstatusenum"></a><span data-ttu-id="a95c7-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="a95c7-102">EventStatusEnum</span></span>


<span data-ttu-id="a95c7-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a95c7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a95c7-104">Especifica el estado actual de la ejecución de un evento.</span><span class="sxs-lookup"><span data-stu-id="a95c7-104">Specifies the current status of the execution of an event.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a95c7-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a95c7-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a95c7-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a95c7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a95c7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a95c7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a95c7-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="a95c7-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="a95c7-109">4</span><span class="sxs-lookup"><span data-stu-id="a95c7-109">4</span></span></p></td>
<td><p><span data-ttu-id="a95c7-110">Solicita la cancelación de la operación que ocasionó el evento.</span><span class="sxs-lookup"><span data-stu-id="a95c7-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a95c7-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="a95c7-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="a95c7-112">3</span><span class="sxs-lookup"><span data-stu-id="a95c7-112">3</span></span></p></td>
<td><p><span data-ttu-id="a95c7-113">Indica que la operación no puede solicitar la cancelación de la operación pendiente.</span><span class="sxs-lookup"><span data-stu-id="a95c7-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a95c7-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="a95c7-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="a95c7-115">2</span><span class="sxs-lookup"><span data-stu-id="a95c7-115">2</span></span></p></td>
<td><p><span data-ttu-id="a95c7-116">Indica que la operación que provocó el evento no funcionó correctamente debido a uno o varios errores.</span><span class="sxs-lookup"><span data-stu-id="a95c7-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a95c7-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="a95c7-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="a95c7-118">1</span><span class="sxs-lookup"><span data-stu-id="a95c7-118">1</span></span></p></td>
<td><p><span data-ttu-id="a95c7-119">Indica que la operación que provocó el evento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a95c7-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a95c7-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="a95c7-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="a95c7-121">5</span><span class="sxs-lookup"><span data-stu-id="a95c7-121">5</span></span></p></td>
<td><p><span data-ttu-id="a95c7-122">Impide posibles notificaciones posteriores antes de que el método de evento haya terminado de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="a95c7-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a95c7-123">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="a95c7-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="a95c7-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a95c7-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a95c7-125">Constante</span><span class="sxs-lookup"><span data-stu-id="a95c7-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a95c7-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="a95c7-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a95c7-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="a95c7-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a95c7-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="a95c7-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a95c7-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="a95c7-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a95c7-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="a95c7-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

