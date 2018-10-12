---
title: CursorTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c254c41bb066887e659c86a29ec4a91ca0de9cdd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486193"
---
# <a name="cursortypeenum"></a><span data-ttu-id="dc682-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="dc682-102">CursorTypeEnum</span></span>


<span data-ttu-id="dc682-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc682-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dc682-104">Especifica el tipo de cursor usado en un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="dc682-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc682-105">Constante</span><span class="sxs-lookup"><span data-stu-id="dc682-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="dc682-106">Valor</span><span class="sxs-lookup"><span data-stu-id="dc682-106">Value</span></span></p></th>
<th><p><span data-ttu-id="dc682-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc682-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc682-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="dc682-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="dc682-109">2</span><span class="sxs-lookup"><span data-stu-id="dc682-109">2</span></span></p></td>
<td><p><span data-ttu-id="dc682-p101">Usa un cursor dinámico. Las adiciones, los cambios y las eliminaciones realizadas por otros usuarios son visibles y se permiten todos los tipos de movimiento por el <strong>Recordset</strong>, excepto para marcadores, si el proveedor no los admite.</span><span class="sxs-lookup"><span data-stu-id="dc682-p101">Uses a dynamic cursor. Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc682-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="dc682-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="dc682-113">0</span><span class="sxs-lookup"><span data-stu-id="dc682-113">0</span></span></p></td>
<td><p><span data-ttu-id="dc682-p102">Valor predeterminado. Usa un cursor de solo avance. Es idéntico a un cursor estático, excepto que solo se puede desplazar por los registros hacia adelante. Este cursor permite mejorar el rendimiento cuando solo se necesita recorrer un objeto <strong>Recordset</strong> una vez.</span><span class="sxs-lookup"><span data-stu-id="dc682-p102">Default. Uses a forward-only cursor. Identical to a static cursor, except that you can only scroll forward through records. This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc682-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="dc682-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="dc682-119">1</span><span class="sxs-lookup"><span data-stu-id="dc682-119">1</span></span></p></td>
<td><p><span data-ttu-id="dc682-p103">Usa un cursor de conjunto de claves. Igual que un cursor dinámico, excepto que no se pueden ver los registros agregados por otros usuarios, aunque los registros eliminados por otros usuarios son inaccesibles desde el objeto <strong>Recordset</strong>. Los cambios en los datos realizados por otros usuarios siguen siendo visibles.</span><span class="sxs-lookup"><span data-stu-id="dc682-p103">Uses a keyset cursor. Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>. Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc682-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="dc682-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="dc682-124">3</span><span class="sxs-lookup"><span data-stu-id="dc682-124">3</span></span></p></td>
<td><p><span data-ttu-id="dc682-p104">Utiliza un cursor estático. Una copia estática de conjunto de registros que se puede utilizar para buscar datos o generar informes. Las adiciones, modificaciones o eliminaciones realizadas por otros usuarios no son visibles.</span><span class="sxs-lookup"><span data-stu-id="dc682-p104">Uses a static cursor. A static copy of a set of records that you can use to find data or generate reports. Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc682-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="dc682-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="dc682-129">-1</span><span class="sxs-lookup"><span data-stu-id="dc682-129">-1</span></span></p></td>
<td><p><span data-ttu-id="dc682-130">No especifica el tipo de cursor.</span><span class="sxs-lookup"><span data-stu-id="dc682-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dc682-131">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="dc682-131">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="dc682-132">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="dc682-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc682-133">Constante</span><span class="sxs-lookup"><span data-stu-id="dc682-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc682-134">AdoEnums.CursorType.DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="dc682-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc682-135">AdoEnums.CursorType.FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="dc682-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc682-136">AdoEnums.CursorType.KEYSET</span><span class="sxs-lookup"><span data-stu-id="dc682-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc682-137">AdoEnums.CursorType.STATIC</span><span class="sxs-lookup"><span data-stu-id="dc682-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc682-138">AdoEnums.CursorType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="dc682-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>
