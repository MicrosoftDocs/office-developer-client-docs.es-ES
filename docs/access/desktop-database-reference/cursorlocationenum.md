---
title: CursorLocationEnum (referencia de base de datos de escritorio de Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295215"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="280b6-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="280b6-102">CursorLocationEnum</span></span>

<span data-ttu-id="280b6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="280b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="280b6-104">Especifica la ubicación del servicio de cursores.</span><span class="sxs-lookup"><span data-stu-id="280b6-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="280b6-105">Constante</span><span class="sxs-lookup"><span data-stu-id="280b6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="280b6-106">Valor</span><span class="sxs-lookup"><span data-stu-id="280b6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="280b6-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="280b6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="280b6-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="280b6-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="280b6-109">3 </span><span class="sxs-lookup"><span data-stu-id="280b6-109">3</span></span></p></td>
<td><p><span data-ttu-id="280b6-110">Usa cursores de cliente proporcionados por una biblioteca de cursores local.</span><span class="sxs-lookup"><span data-stu-id="280b6-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="280b6-111">Los servicios de cursores locales suelen ofrecer muchas características que los cursores suministrados por controlador no facilitan, así que el uso de esta opción puede proporcionar una ventaja con respecto a las características que habilitará.</span><span class="sxs-lookup"><span data-stu-id="280b6-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="280b6-112">Para mantener la compatibilidad con versiones anteriores, también se admite el sinónimo <strong>adUseClientBatch</strong>.</span><span class="sxs-lookup"><span data-stu-id="280b6-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="280b6-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="280b6-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="280b6-114">1 </span><span class="sxs-lookup"><span data-stu-id="280b6-114">1</span></span></p></td>
<td><p><span data-ttu-id="280b6-p102">No utiliza servicios de cursor (esta constante está obsoleta y aparece sólo para mantener la compatibilidad con versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="280b6-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="280b6-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="280b6-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="280b6-118">2 </span><span class="sxs-lookup"><span data-stu-id="280b6-118">2</span></span></p></td>
<td><p><span data-ttu-id="280b6-119">Éste es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="280b6-119">Default.</span></span> <span data-ttu-id="280b6-120">Usa cursores suministrados por controlador o por proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="280b6-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="280b6-121">Estos cursores a veces son muy flexibles y permiten una sensibilidad adicional a los cambios realizados por otros en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="280b6-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="280b6-122">Sin embargo, algunas características del Servicio de <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">cursores</a> de Microsoft para OLE DB (como objetos <a href="recordset-object-ado.md">Recordset</a> desasociados) no se pueden simular con cursores de servidor y estas características no estarán disponibles con esta configuración.</span><span class="sxs-lookup"><span data-stu-id="280b6-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="280b6-123">Equivalente de ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="280b6-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="280b6-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="280b6-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="280b6-125">Constante</span><span class="sxs-lookup"><span data-stu-id="280b6-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="280b6-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="280b6-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="280b6-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="280b6-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="280b6-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="280b6-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

