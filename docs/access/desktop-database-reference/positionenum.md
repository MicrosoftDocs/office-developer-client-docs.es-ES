---
title: PositionEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c2ef44c804a413b85bcf393e1487ff4423c40f0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483838"
---
# <a name="positionenum"></a><span data-ttu-id="d6be4-102">PositionEnum</span><span class="sxs-lookup"><span data-stu-id="d6be4-102">PositionEnum</span></span>


<span data-ttu-id="d6be4-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6be4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d6be4-104">Especifica la posición actual del puntero de registro dentro de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d6be4-104">Specifies the current position of the record pointer within a [Recordset](recordset-object-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6be4-105">Constante</span><span class="sxs-lookup"><span data-stu-id="d6be4-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="d6be4-106">Valor</span><span class="sxs-lookup"><span data-stu-id="d6be4-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d6be4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6be4-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6be4-108"><strong>adPosBOF</strong></span><span class="sxs-lookup"><span data-stu-id="d6be4-108"><strong>adPosBOF</strong></span></span></p></td>
<td><p><span data-ttu-id="d6be4-109">-2</span><span class="sxs-lookup"><span data-stu-id="d6be4-109">-2</span></span></p></td>
<td><p><span data-ttu-id="d6be4-110">Indica que el puntero del registro actual está en BOF (es decir, la propiedad <a href="bof-eof-properties-ado.md">BOF</a> es <strong>True</strong>).</span><span class="sxs-lookup"><span data-stu-id="d6be4-110">Indicates that the current record pointer is at BOF (that is, the <a href="bof-eof-properties-ado.md">BOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6be4-111"><strong>adPosEOF</strong></span><span class="sxs-lookup"><span data-stu-id="d6be4-111"><strong>adPosEOF</strong></span></span></p></td>
<td><p><span data-ttu-id="d6be4-112">-3</span><span class="sxs-lookup"><span data-stu-id="d6be4-112">-3</span></span></p></td>
<td><p><span data-ttu-id="d6be4-113">Indica que el puntero del registro actual está en EOF (es decir, la propiedad <a href="bof-eof-properties-ado.md">EOF</a> es <strong>True</strong>).</span><span class="sxs-lookup"><span data-stu-id="d6be4-113">Indicates that the current record pointer is at EOF (that is, the <a href="bof-eof-properties-ado.md">EOF</a> property is <strong>True</strong>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6be4-114"><strong>adPosUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="d6be4-114"><strong>adPosUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="d6be4-115">-1</span><span class="sxs-lookup"><span data-stu-id="d6be4-115">-1</span></span></p></td>
<td><p><span data-ttu-id="d6be4-116">Indica que el objeto <strong>Recordset</strong> está vacío, que se desconoce la posición actual o que el proveedor no admite la propiedad <a href="absolutepage-property-ado.md">AbsolutePage</a> o <a href="absoluteposition-property-ado.md">AbsolutePosition</a>.</span><span class="sxs-lookup"><span data-stu-id="d6be4-116">Indicates that the <strong>Recordset</strong> is empty, the current position is unknown, or the provider does not support the <a href="absolutepage-property-ado.md">AbsolutePage</a> or <a href="absoluteposition-property-ado.md">AbsolutePosition</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d6be4-117">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="d6be4-117">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="d6be4-118">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="d6be4-118">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6be4-119">Constante</span><span class="sxs-lookup"><span data-stu-id="d6be4-119">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6be4-120">AdoEnums.Position.BOF</span><span class="sxs-lookup"><span data-stu-id="d6be4-120">AdoEnums.Position.BOF</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6be4-121">AdoEnums.Position.EOF</span><span class="sxs-lookup"><span data-stu-id="d6be4-121">AdoEnums.Position.EOF</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6be4-122">AdoEnums.Position.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="d6be4-122">AdoEnums.Position.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

