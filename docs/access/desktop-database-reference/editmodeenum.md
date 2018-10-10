---
title: EditModeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7322193971e4230afaacbb1f614c7ab682f3c149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485245"
---
# <a name="editmodeenum"></a><span data-ttu-id="a0e77-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="a0e77-102">EditModeEnum</span></span>


<span data-ttu-id="a0e77-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0e77-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a0e77-104">Especifica el estado de edición de un registro.</span><span class="sxs-lookup"><span data-stu-id="a0e77-104">Specifies the editing status of a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0e77-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a0e77-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a0e77-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a0e77-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a0e77-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0e77-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0e77-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="a0e77-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e77-109">0</span><span class="sxs-lookup"><span data-stu-id="a0e77-109">0</span></span></p></td>
<td><p><span data-ttu-id="a0e77-110">Indica que no se está realizando ninguna operación de edición.</span><span class="sxs-lookup"><span data-stu-id="a0e77-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e77-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="a0e77-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e77-112">1</span><span class="sxs-lookup"><span data-stu-id="a0e77-112">1</span></span></p></td>
<td><p><span data-ttu-id="a0e77-113">Indica que los datos del registro actual se han modificado, pero no se han guardado.</span><span class="sxs-lookup"><span data-stu-id="a0e77-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e77-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="a0e77-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e77-115">2</span><span class="sxs-lookup"><span data-stu-id="a0e77-115">2</span></span></p></td>
<td><p><span data-ttu-id="a0e77-116">Indica que se ha realizado una llamada al método <a href="addnew-method-ado.md">AddNew</a>, y que el registro actual en el búfer de copia es un registro nuevo que no se ha guardado en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a0e77-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e77-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="a0e77-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e77-118">4</span><span class="sxs-lookup"><span data-stu-id="a0e77-118">4</span></span></p></td>
<td><p><span data-ttu-id="a0e77-119">Indica que se ha eliminado el registro actual.</span><span class="sxs-lookup"><span data-stu-id="a0e77-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0e77-120">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="a0e77-120">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="a0e77-121">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a0e77-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0e77-122">Constante</span><span class="sxs-lookup"><span data-stu-id="a0e77-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0e77-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="a0e77-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e77-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="a0e77-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e77-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="a0e77-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e77-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="a0e77-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

