---
title: Propiedades BOF y EOF (ADO)
TOCTitle: BOF, EOF Properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 14cd61f6bd2985d71321d848a6426c06c4c7a94d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484044"
---
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="de44d-102">Propiedades BOF y EOF (ADO)</span><span class="sxs-lookup"><span data-stu-id="de44d-102">BOF, EOF Properties (ADO)</span></span>


<span data-ttu-id="de44d-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="de44d-103">**Applies to**: Access 2013 | Office 2013</span></span>

  - <span data-ttu-id="de44d-104">**BOF**: indica que la posición de registro actual se sitúa delante del primer registro de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="de44d-104">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

  - <span data-ttu-id="de44d-105">**EOF**: indica que la posición de registro actual se sitúa después del último registro de un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="de44d-105">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="de44d-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de44d-106">Return Value</span></span>

<span data-ttu-id="de44d-107">Las propiedades **BOF** y **EOF** devuelven valores **booleanos**.</span><span class="sxs-lookup"><span data-stu-id="de44d-107">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="de44d-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de44d-108">Remarks</span></span>

<span data-ttu-id="de44d-109">Use las propiedades **BOF** y **EOF** para determinar si un objeto **Recordset** contiene registros o si se ha desplazado más allá de los límites de un objeto **Recordset** cuando se mueve de un registro a otro.</span><span class="sxs-lookup"><span data-stu-id="de44d-109">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="de44d-110">La propiedad **BOF** devuelve **True** (-1) si la posición de registro actual se sitúa delante del primer registro y devuelve **False** (0) si la posición de registro actual se sitúa en el primer registro o después del mismo.</span><span class="sxs-lookup"><span data-stu-id="de44d-110">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="de44d-111">La propiedad **EOF** devuelve **True** si la posición de registro actual se sitúa después del último registro y devuelve **False** si la posición de registro actual se sitúa en el último registro o delante del mismo.</span><span class="sxs-lookup"><span data-stu-id="de44d-111">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="de44d-112">Si la propiedad **BOF** o **EOF** es **True**, no hay ningún registro actual.</span><span class="sxs-lookup"><span data-stu-id="de44d-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="de44d-p101">Si se abre un objeto **Recordset** que no contiene registros, las propiedades **BOF** y **EOF** tienen el valor **True** (vea la propiedad [RecordCount](recordcount-property-ado.md) para obtener más información sobre este estado de un objeto **Recordset**). Si se abre un objeto **Recordset** que contiene al menos un registro, el primer registro es el registro actual y las propiedades **BOF** y **EOF** tienen el valor **False**.</span><span class="sxs-lookup"><span data-stu-id="de44d-p101">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**). When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="de44d-115">Si se elimina el último registro que queda en el objeto **Recordset**, puede que el valor de las propiedades **BOF** y **EOF** siga siendo **False** hasta que se intente ajustar la posición del registro actual.</span><span class="sxs-lookup"><span data-stu-id="de44d-115">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="de44d-116">En esta tabla se muestran los métodos **Move** permitidos con diferentes combinaciones de las propiedades **BOF** y **EOF**.</span><span class="sxs-lookup"><span data-stu-id="de44d-116">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="de44d-117">Métodos MoveFirst,</span><span class="sxs-lookup"><span data-stu-id="de44d-117">MoveFirst,</span></span><br />
<span data-ttu-id="de44d-118">MoveLast</span><span class="sxs-lookup"><span data-stu-id="de44d-118">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="de44d-119">MovePrevious,</span><span class="sxs-lookup"><span data-stu-id="de44d-119">MovePrevious,</span></span><br />
<span data-ttu-id="de44d-120">Mover &lt; 0</span><span class="sxs-lookup"><span data-stu-id="de44d-120">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="de44d-121">Move 0</span><span class="sxs-lookup"><span data-stu-id="de44d-121">Move 0</span></span></p></th>
<th><p><span data-ttu-id="de44d-122">MoveNext,</span><span class="sxs-lookup"><span data-stu-id="de44d-122">MoveNext,</span></span><br />
<span data-ttu-id="de44d-123">Mover &gt; 0</span><span class="sxs-lookup"><span data-stu-id="de44d-123">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de44d-124"><strong>BOF = True,</strong></span><span class="sxs-lookup"><span data-stu-id="de44d-124"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="de44d-125">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="de44d-125">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="de44d-126">Permitido</span><span class="sxs-lookup"><span data-stu-id="de44d-126">Allowed</span></span></p></td>
<td><p><span data-ttu-id="de44d-127">Error</span><span class="sxs-lookup"><span data-stu-id="de44d-127">Error</span></span></p></td>
<td><p><span data-ttu-id="de44d-128">Error</span><span class="sxs-lookup"><span data-stu-id="de44d-128">Error</span></span></p></td>
<td><p><span data-ttu-id="de44d-129">Permitido</span><span class="sxs-lookup"><span data-stu-id="de44d-129">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de44d-130"><strong>BOF = False,</strong></span><span class="sxs-lookup"><span data-stu-id="de44d-130"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="de44d-131">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="de44d-131">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="de44d-132">Permitido</span><span class="sxs-lookup"><span data-stu-id="de44d-132">Allowed</span></span></p></td>
<td><p><span data-ttu-id="de44d-133">Permitido</span><span class="sxs-lookup"><span data-stu-id="de44d-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="de44d-134">Error</span><span class="sxs-lookup"><span data-stu-id="de44d-134">Error</span></span></p></td>
<td><p><span data-ttu-id="de44d-135">Error</span><span class="sxs-lookup"><span data-stu-id="de44d-135">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de44d-136">Ambas propiedades son <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="de44d-136">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="de44d-137">Error</span><span class="sxs-lookup"><span data-stu-id="de44d-137">Error</span></span></p></td>
<td><p><span data-ttu-id="de44d-138">Error</span><span class="sxs-lookup"><span data-stu-id="de44d-138">Error</span></span></p></td>
<td><p><span data-ttu-id="de44d-139">Error</span><span class="sxs-lookup"><span data-stu-id="de44d-139">Error</span></span></p></td>
<td><p><span data-ttu-id="de44d-140">Error</span><span class="sxs-lookup"><span data-stu-id="de44d-140">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de44d-141">Ambas propiedades son <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="de44d-141">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="de44d-142">Permitido</span><span class="sxs-lookup"><span data-stu-id="de44d-142">Allowed</span></span></p></td>
<td><p><span data-ttu-id="de44d-143">Permitido</span><span class="sxs-lookup"><span data-stu-id="de44d-143">Allowed</span></span></p></td>
<td><p><span data-ttu-id="de44d-144">Permitido</span><span class="sxs-lookup"><span data-stu-id="de44d-144">Allowed</span></span></p></td>
<td><p><span data-ttu-id="de44d-145">Permitido</span><span class="sxs-lookup"><span data-stu-id="de44d-145">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="de44d-146">Si un método **Move** está permitido, esto no garantiza que busque correctamente un registro; sólo significa que las llamadas al método **Move** especificado no generarán un error.</span><span class="sxs-lookup"><span data-stu-id="de44d-146">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="de44d-147">En la tabla siguiente se muestra lo que les sucede a los valores de configuración de **BOF** y **EOF** cuando se llama a varios métodos **Move** y no se puede encontrar un registro.</span><span class="sxs-lookup"><span data-stu-id="de44d-147">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="de44d-148">BOF</span><span class="sxs-lookup"><span data-stu-id="de44d-148">BOF</span></span></p></th>
<th><p><span data-ttu-id="de44d-149">EOF</span><span class="sxs-lookup"><span data-stu-id="de44d-149">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de44d-150"><strong>Métodos MoveFirst</strong>, <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="de44d-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="de44d-151">Establecer en <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="de44d-151">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="de44d-152">Establecer en <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="de44d-152">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de44d-153"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="de44d-153"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="de44d-154">No cambia</span><span class="sxs-lookup"><span data-stu-id="de44d-154">No change</span></span></p></td>
<td><p><span data-ttu-id="de44d-155">No cambia</span><span class="sxs-lookup"><span data-stu-id="de44d-155">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de44d-156"><strong>MovePrevious</strong>, <strong>mueva</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="de44d-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="de44d-157">Se establece en <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="de44d-157">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="de44d-158">No cambia</span><span class="sxs-lookup"><span data-stu-id="de44d-158">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de44d-159"><strong>MoveNext</strong>, <strong>mueva</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="de44d-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="de44d-160">No cambia</span><span class="sxs-lookup"><span data-stu-id="de44d-160">No change</span></span></p></td>
<td><p><span data-ttu-id="de44d-161">Se establece en <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="de44d-161">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>
