---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e456cfcc344c818504cb2ae1c2af9a4294b004ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876417"
---
# <a name="searchdirectionenum"></a><span data-ttu-id="42f39-102">SearchDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="42f39-102">SearchDirectionEnum</span></span>


<span data-ttu-id="42f39-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="42f39-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42f39-104">Especifica la dirección de una búsqueda de registro dentro de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="42f39-104">Specifies the direction of a record search within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42f39-105">Constante</span><span class="sxs-lookup"><span data-stu-id="42f39-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="42f39-106">Valor</span><span class="sxs-lookup"><span data-stu-id="42f39-106">Value</span></span></p></th>
<th><p><span data-ttu-id="42f39-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="42f39-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42f39-108"><strong>adSearchBackward</strong></span><span class="sxs-lookup"><span data-stu-id="42f39-108"><strong>adSearchBackward</strong></span></span></p></td>
<td><p><span data-ttu-id="42f39-109">-1</span><span class="sxs-lookup"><span data-stu-id="42f39-109">-1</span></span></p></td>
<td><p><span data-ttu-id="42f39-p101">Busca hacia atrás y se detiene al principio del objeto <strong>Recordset</strong>. Si no se encuentra el registro, el puntero de registro se coloca en <a href="bof-eof-properties-ado.md">BOF</a> (inicio del archivo).</span><span class="sxs-lookup"><span data-stu-id="42f39-p101">Searches backward, stopping at the beginning of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">BOF</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42f39-112"><strong>adSearchForward</strong></span><span class="sxs-lookup"><span data-stu-id="42f39-112"><strong>adSearchForward</strong></span></span></p></td>
<td><p><span data-ttu-id="42f39-113">1</span><span class="sxs-lookup"><span data-stu-id="42f39-113">1</span></span></p></td>
<td><p><span data-ttu-id="42f39-p102">Busca hacia adelante y se detiene al final del objeto <strong>Recordset</strong>. Si no se encuentra el registro, el puntero de registro se coloca en <a href="bof-eof-properties-ado.md"> EOF</a> (fin del archivo).</span><span class="sxs-lookup"><span data-stu-id="42f39-p102">Searches forward, stopping at the end of the <strong>Recordset</strong>. If a match is not found, the record pointer is positioned at <a href="bof-eof-properties-ado.md">EOF</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="42f39-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="42f39-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="42f39-117">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="42f39-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42f39-118">Constante</span><span class="sxs-lookup"><span data-stu-id="42f39-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42f39-119">AdoEnums.SearchDirection.BACKWARD</span><span class="sxs-lookup"><span data-stu-id="42f39-119">AdoEnums.SearchDirection.BACKWARD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42f39-120">AdoEnums.SearchDirection.FORWARD</span><span class="sxs-lookup"><span data-stu-id="42f39-120">AdoEnums.SearchDirection.FORWARD</span></span></p></td>
</tr>
</tbody>
</table>

