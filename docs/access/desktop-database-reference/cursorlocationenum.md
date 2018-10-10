---
title: CursorLocationEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90226413579a8fac7586cbd5ef08510a36a42959
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484695"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="6e4d0-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="6e4d0-102">CursorLocationEnum</span></span>


<span data-ttu-id="6e4d0-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e4d0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6e4d0-104">Especifica la ubicación del servicio de cursores.</span><span class="sxs-lookup"><span data-stu-id="6e4d0-104">Specifies the location of the cursor service.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e4d0-105">Constante</span><span class="sxs-lookup"><span data-stu-id="6e4d0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6e4d0-106">Valor</span><span class="sxs-lookup"><span data-stu-id="6e4d0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6e4d0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e4d0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e4d0-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="6e4d0-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="6e4d0-109">3</span><span class="sxs-lookup"><span data-stu-id="6e4d0-109">3</span></span></p></td>
<td><p><span data-ttu-id="6e4d0-110">Utiliza cursores de cliente suministrados por una biblioteca de cursores local.</span><span class="sxs-lookup"><span data-stu-id="6e4d0-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="6e4d0-111">Servicios de cursores locales a menudo le permitirá muchas características que los cursores suministrados por controlador no podrán, por lo que el uso de esta configuración puede proporcionar una ventaja con respecto a las características que se habilitará.</span><span class="sxs-lookup"><span data-stu-id="6e4d0-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="6e4d0-112">Para compatibilidad con versiones anteriores, también se admite el sinónimo <strong>adUseClientBatch</strong> .</span><span class="sxs-lookup"><span data-stu-id="6e4d0-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e4d0-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="6e4d0-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="6e4d0-114">1</span><span class="sxs-lookup"><span data-stu-id="6e4d0-114">1</span></span></p></td>
<td><p><span data-ttu-id="6e4d0-p102">No utiliza servicios de cursor (esta constante está obsoleta y aparece sólo para mantener la compatibilidad con versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="6e4d0-p102">Does not use cursor services. (This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e4d0-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="6e4d0-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="6e4d0-118">2</span><span class="sxs-lookup"><span data-stu-id="6e4d0-118">2</span></span></p></td>
<td><p><span data-ttu-id="6e4d0-p103">Valor predeterminado. Usa cursores suministrados por controlador o por proveedor de datos. Estos cursores a veces son muy flexibles y permiten una sensibilidad adicional a los cambios realizados por otros en el origen de datos. No obstante, algunas características del <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Servicio de cursores de Microsoft para OLE DB</a> (como los objetos <a href="recordset-object-ado.md">Recordset</a> desasociados) no se pueden simular con cursores de servidor y dichas características no estarán disponibles con esta opción.</span><span class="sxs-lookup"><span data-stu-id="6e4d0-p103">Default. Uses data-provider or driver-supplied cursors. These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source. However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e4d0-123">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="6e4d0-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="6e4d0-124">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6e4d0-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e4d0-125">Constante</span><span class="sxs-lookup"><span data-stu-id="6e4d0-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e4d0-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="6e4d0-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e4d0-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="6e4d0-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e4d0-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="6e4d0-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

