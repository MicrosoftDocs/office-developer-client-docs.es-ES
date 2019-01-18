---
title: EditModeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 246d9e29f084efb975783fd15c15993eba5a6e74
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726291"
---
# <a name="editmodeenum"></a><span data-ttu-id="3cc61-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="3cc61-102">EditModeEnum</span></span>

<span data-ttu-id="3cc61-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cc61-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3cc61-104">Especifica el estado de edición de un registro.</span><span class="sxs-lookup"><span data-stu-id="3cc61-104">Specifies the editing status of a record.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cc61-105">Constante</span><span class="sxs-lookup"><span data-stu-id="3cc61-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3cc61-106">Valor</span><span class="sxs-lookup"><span data-stu-id="3cc61-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3cc61-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cc61-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cc61-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="3cc61-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc61-109">0</span><span class="sxs-lookup"><span data-stu-id="3cc61-109">0</span></span></p></td>
<td><p><span data-ttu-id="3cc61-110">Indica que no se está realizando ninguna operación de edición.</span><span class="sxs-lookup"><span data-stu-id="3cc61-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc61-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="3cc61-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc61-112">1</span><span class="sxs-lookup"><span data-stu-id="3cc61-112">1</span></span></p></td>
<td><p><span data-ttu-id="3cc61-113">Indica que los datos del registro actual se han modificado, pero no se han guardado.</span><span class="sxs-lookup"><span data-stu-id="3cc61-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc61-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="3cc61-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc61-115">2</span><span class="sxs-lookup"><span data-stu-id="3cc61-115">2</span></span></p></td>
<td><p><span data-ttu-id="3cc61-116">Indica que se ha realizado una llamada al método <a href="addnew-method-ado.md">AddNew</a>, y que el registro actual en el búfer de copia es un registro nuevo que no se ha guardado en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3cc61-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc61-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="3cc61-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="3cc61-118">4</span><span class="sxs-lookup"><span data-stu-id="3cc61-118">4</span></span></p></td>
<td><p><span data-ttu-id="3cc61-119">Indica que se ha eliminado el registro actual.</span><span class="sxs-lookup"><span data-stu-id="3cc61-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="3cc61-120">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="3cc61-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="3cc61-121">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="3cc61-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cc61-122">Constante</span><span class="sxs-lookup"><span data-stu-id="3cc61-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cc61-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="3cc61-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc61-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="3cc61-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cc61-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="3cc61-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cc61-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="3cc61-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

