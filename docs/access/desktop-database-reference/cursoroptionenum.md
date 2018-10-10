---
title: CursorOptionEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6d6f66e3bdee06611faafef5d32a2a486fc2028
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484252"
---
# <a name="cursoroptionenum"></a><span data-ttu-id="fc08e-102">CursorOptionEnum</span><span class="sxs-lookup"><span data-stu-id="fc08e-102">CursorOptionEnum</span></span>


<span data-ttu-id="fc08e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc08e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fc08e-104">Especifica qué funcionalidad debería comprobar el método [Supports](supports-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fc08e-104">Specifies what functionality the [Supports](supports-method-ado.md) method should test for.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc08e-105">Constante</span><span class="sxs-lookup"><span data-stu-id="fc08e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="fc08e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="fc08e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fc08e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc08e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-108"><strong>adAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-108"><strong>adAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-109">0x1000400</span><span class="sxs-lookup"><span data-stu-id="fc08e-109">0x1000400</span></span></p></td>
<td><p><span data-ttu-id="fc08e-110">Admite el método <a href="addnew-method-ado.md">AddNew</a> para agregar nuevos registros.</span><span class="sxs-lookup"><span data-stu-id="fc08e-110">Supports the <a href="addnew-method-ado.md">AddNew</a> method to add new records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-111"><strong>adApproxPosition</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-111"><strong>adApproxPosition</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-112">0x4000</span><span class="sxs-lookup"><span data-stu-id="fc08e-112">0x4000</span></span></p></td>
<td><p><span data-ttu-id="fc08e-113">Admite las propiedades <a href="absoluteposition-property-ado.md">AbsolutePosition</a> y <a href="absolutepage-property-ado.md">AbsolutePage</a>.</span><span class="sxs-lookup"><span data-stu-id="fc08e-113">Supports the <a href="absoluteposition-property-ado.md">AbsolutePosition</a> and <a href="absolutepage-property-ado.md">AbsolutePage</a> properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-114"><strong>adBookmark</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-114"><strong>adBookmark</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-115">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="fc08e-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="fc08e-116">Admite la propiedad <a href="bookmark-property-ado.md">Bookmark</a> para obtener acceso a registros específicos.</span><span class="sxs-lookup"><span data-stu-id="fc08e-116">Supports the <a href="bookmark-property-ado.md">Bookmark</a> property to gain access to specific records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-117"><strong>adDelete</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-117"><strong>adDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-118">0x1000800</span><span class="sxs-lookup"><span data-stu-id="fc08e-118">0x1000800</span></span></p></td>
<td><p><span data-ttu-id="fc08e-119">Admite el método <a href="delete-method-ado-recordset.md">Delete</a> para eliminar registros.</span><span class="sxs-lookup"><span data-stu-id="fc08e-119">Supports the <a href="delete-method-ado-recordset.md">Delete</a> method to delete records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-120"><strong>adFind</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-120"><strong>adFind</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-121">0 x 80000</span><span class="sxs-lookup"><span data-stu-id="fc08e-121">0x80000</span></span></p></td>
<td><p><span data-ttu-id="fc08e-122">Admite el método <a href="find-method-ado.md">Find</a> para localizar una fila en un objeto <a href="recordset-object-ado.md">Recordset</a>.</span><span class="sxs-lookup"><span data-stu-id="fc08e-122">Supports the <a href="find-method-ado.md">Find</a> method to locate a row in a <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-123"><strong>adHoldRecords</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-123"><strong>adHoldRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-124">0 x 100</span><span class="sxs-lookup"><span data-stu-id="fc08e-124">0x100</span></span></p></td>
<td><p><span data-ttu-id="fc08e-125">Recupera más registros o cambia la posición siguiente sin confirmar todos los cambios pendientes.</span><span class="sxs-lookup"><span data-stu-id="fc08e-125">Retrieves more records or changes the next position without committing all pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-126"><strong>adIndex</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-126"><strong>adIndex</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-127">0 x 100000</span><span class="sxs-lookup"><span data-stu-id="fc08e-127">0x100000</span></span></p></td>
<td><p><span data-ttu-id="fc08e-128">Admite la propiedad <a href="index-property-ado.md">Index</a> para denominar un índice.</span><span class="sxs-lookup"><span data-stu-id="fc08e-128">Supports the <a href="index-property-ado.md">Index</a> property to name an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-129"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-129"><strong>adMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-130">0 x 200</span><span class="sxs-lookup"><span data-stu-id="fc08e-130">0x200</span></span></p></td>
<td><p><span data-ttu-id="fc08e-131">Admite los métodos <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> y <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a>, así como los métodos <a href="move-method-ado.md">Move</a> o <a href="getrows-method-ado.md">GetRows</a> para mover la posición de registro actual hacia atrás sin necesidad de marcadores.</span><span class="sxs-lookup"><span data-stu-id="fc08e-131">Supports the <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> and <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> methods, and <a href="move-method-ado.md">Move</a> or <a href="getrows-method-ado.md">GetRows</a> methods to move the current record position backward without requiring bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-132"><strong>adNotify</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-132"><strong>adNotify</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-133">0 x 40000</span><span class="sxs-lookup"><span data-stu-id="fc08e-133">0x40000</span></span></p></td>
<td><p><span data-ttu-id="fc08e-134">Indica que el proveedor de datos subyacente admite notificaciones (lo cual determina si se admite eventos del objeto <strong>Recordset</strong>).</span><span class="sxs-lookup"><span data-stu-id="fc08e-134">Indicates that the underlying data provider supports notifications (which determines whether <strong>Recordset</strong> events are supported).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-135"><strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-135"><strong>adResync</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-136">0 x 20000</span><span class="sxs-lookup"><span data-stu-id="fc08e-136">0x20000</span></span></p></td>
<td><p><span data-ttu-id="fc08e-137">Admite el método <a href="resync-method-ado.md">Resync</a> para actualizar el cursor con los datos visibles de la base de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="fc08e-137">Supports the <a href="resync-method-ado.md">Resync</a> method to update the cursor with the data that is visible in the underlying database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-138"><strong>adSeek</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-138"><strong>adSeek</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-139">0x200000</span><span class="sxs-lookup"><span data-stu-id="fc08e-139">0x200000</span></span></p></td>
<td><p><span data-ttu-id="fc08e-140">Admite el método <a href="seek-method-ado.md">Seek</a> para localizar una fila en un objeto <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc08e-140">Supports the <a href="seek-method-ado.md">Seek</a> method to locate a row in a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-141"><strong>adUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-141"><strong>adUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-142">0x1008000</span><span class="sxs-lookup"><span data-stu-id="fc08e-142">0x1008000</span></span></p></td>
<td><p><span data-ttu-id="fc08e-143">Admite el método <a href="update-method-ado.md">Update</a> para modificar datos existentes.</span><span class="sxs-lookup"><span data-stu-id="fc08e-143">Supports the <a href="update-method-ado.md">Update</a> method to modify existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-144"><strong>adUpdateBatch</strong></span><span class="sxs-lookup"><span data-stu-id="fc08e-144"><strong>adUpdateBatch</strong></span></span></p></td>
<td><p><span data-ttu-id="fc08e-145">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="fc08e-145">0x10000</span></span></p></td>
<td><p><span data-ttu-id="fc08e-146">Admite actualización por lotes (métodos <a href="updatebatch-method-ado.md"> UpdateBatch</a> y <a href="cancelbatch-method-ado.md">CancelBatch</a>) para transmitir grupos de cambios al proveedor.</span><span class="sxs-lookup"><span data-stu-id="fc08e-146">Supports batch updating (<a href="updatebatch-method-ado.md">UpdateBatch</a> and <a href="cancelbatch-method-ado.md">CancelBatch</a> methods) to transmit groups of changes to the provider.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fc08e-147">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="fc08e-147">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="fc08e-148">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="fc08e-148">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc08e-149">Constante</span><span class="sxs-lookup"><span data-stu-id="fc08e-149">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-150">AdoEnums.CursorOption.ADDNEW</span><span class="sxs-lookup"><span data-stu-id="fc08e-150">AdoEnums.CursorOption.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-151">AdoEnums.CursorOption.APPROXPOSITION</span><span class="sxs-lookup"><span data-stu-id="fc08e-151">AdoEnums.CursorOption.APPROXPOSITION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-152">AdoEnums.CursorOption.BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="fc08e-152">AdoEnums.CursorOption.BOOKMARK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-153">AdoEnums.CursorOption.DELETE</span><span class="sxs-lookup"><span data-stu-id="fc08e-153">AdoEnums.CursorOption.DELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-154">AdoEnums.CursorOption.FIND</span><span class="sxs-lookup"><span data-stu-id="fc08e-154">AdoEnums.CursorOption.FIND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-155">AdoEnums.CursorOption.HOLDRECORDS</span><span class="sxs-lookup"><span data-stu-id="fc08e-155">AdoEnums.CursorOption.HOLDRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-156">AdoEnums.CursorOption.INDEX</span><span class="sxs-lookup"><span data-stu-id="fc08e-156">AdoEnums.CursorOption.INDEX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-157">AdoEnums.CursorOption.MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="fc08e-157">AdoEnums.CursorOption.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-158">AdoEnums.CursorOption.NOTIFY</span><span class="sxs-lookup"><span data-stu-id="fc08e-158">AdoEnums.CursorOption.NOTIFY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-159">AdoEnums.CursorOption.RESYNC</span><span class="sxs-lookup"><span data-stu-id="fc08e-159">AdoEnums.CursorOption.RESYNC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-160">AdoEnums.CursorOption.SEEK</span><span class="sxs-lookup"><span data-stu-id="fc08e-160">AdoEnums.CursorOption.SEEK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc08e-161">AdoEnums.CursorOption.UPDATE</span><span class="sxs-lookup"><span data-stu-id="fc08e-161">AdoEnums.CursorOption.UPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc08e-162">AdoEnums.CursorOption.UPDATEBATCH</span><span class="sxs-lookup"><span data-stu-id="fc08e-162">AdoEnums.CursorOption.UPDATEBATCH</span></span></p></td>
</tr>
</tbody>
</table>

