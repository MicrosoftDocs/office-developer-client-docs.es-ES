---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0a9954319448a219d9683cfd8133929fb3d184d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483791"
---
# <a name="searchdirectionenum"></a><span data-ttu-id="18fa9-102">SearchDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="18fa9-102">SearchDirectionEnum</span></span>


<span data-ttu-id="18fa9-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="18fa9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="18fa9-104">Especifica la dirección de una búsqueda de registro dentro de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="18fa9-104">Specifies the direction of a record search within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18fa9-105">Constante</span><span class="sxs-lookup"><span data-stu-id="18fa9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="18fa9-106">Valor</span><span class="sxs-lookup"><span data-stu-id="18fa9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="18fa9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="18fa9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18fa9-108"><strong>adSearchBackward</strong></span><span class="sxs-lookup"><span data-stu-id="18fa9-108"><strong>adSearchBackward</strong></span></span></p></td>
<td><p><span data-ttu-id="18fa9-109">-1</span><span class="sxs-lookup"><span data-stu-id="18fa9-109">-1</span></span></p></td>
<td><p><span data-ttu-id="18fa9-p101">Busca hacia atrás y se detiene al principio del objeto <strong>Recordset</strong>. Si no se encuentra el registro, el puntero de registro se coloca en <a href="bof-eof-properties-ado.md">BOF</a> (inicio del archivo).</span><span class="sxs-lookup"><span data-stu-id="18fa9-p101">Searches backward, stopping at the beginning of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">BOF</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18fa9-112"><strong>adSearchForward</strong></span><span class="sxs-lookup"><span data-stu-id="18fa9-112"><strong>adSearchForward</strong></span></span></p></td>
<td><p><span data-ttu-id="18fa9-113">1</span><span class="sxs-lookup"><span data-stu-id="18fa9-113">1</span></span></p></td>
<td><p><span data-ttu-id="18fa9-p102">Busca hacia adelante y se detiene al final del objeto <strong>Recordset</strong>. Si no se encuentra el registro, el puntero de registro se coloca en <a href="bof-eof-properties-ado.md"> EOF</a> (fin del archivo).</span><span class="sxs-lookup"><span data-stu-id="18fa9-p102">Searches forward, stopping at the end of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">EOF</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18fa9-116">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="18fa9-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="18fa9-117">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="18fa9-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18fa9-118">Constante</span><span class="sxs-lookup"><span data-stu-id="18fa9-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18fa9-119">AdoEnums.SearchDirection.BACKWARD</span><span class="sxs-lookup"><span data-stu-id="18fa9-119">AdoEnums.SearchDirection.BACKWARD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18fa9-120">AdoEnums.SearchDirection.FORWARD</span><span class="sxs-lookup"><span data-stu-id="18fa9-120">AdoEnums.SearchDirection.FORWARD</span></span></p></td>
</tr>
</tbody>
</table>

