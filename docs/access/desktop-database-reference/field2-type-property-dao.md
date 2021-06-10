---
title: Propiedad Field2.Type (DAO)
TOCTitle: Type Property
ms:assetid: 057d6ec9-b72c-cee6-005a-6d916e3dda29
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844921(v=office.15)
ms:contentKeyID: 48543032
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4da32f18a2b3e9dddbb0ae04e3257de34ba09761
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292667"
---
# <a name="field2type-property-dao"></a><span data-ttu-id="5aef7-102">Propiedad Field2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="5aef7-102">Field2.Type property (DAO)</span></span>


<span data-ttu-id="5aef7-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5aef7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5aef7-p101">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. **Integer** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5aef7-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aef7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aef7-106">Syntax</span></span>

<span data-ttu-id="5aef7-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="5aef7-107">*expression* .Type</span></span>

<span data-ttu-id="5aef7-108">*expression* Variable que representa un objeto **Field2**.</span><span class="sxs-lookup"><span data-stu-id="5aef7-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aef7-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5aef7-109">Remarks</span></span>

<span data-ttu-id="5aef7-p102">La configuración o el valor devuelto es una constante que indica un tipo operativo o de datos. Para un objeto **Field2**, esta propiedad es de lectura y escritura hasta que el objeto se anexa a una colección o a otro objeto, después será de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aef7-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="5aef7-112">Para un objeto **Field2**, los valores o valores enteros posibles se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5aef7-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5aef7-113">Constante</span><span class="sxs-lookup"><span data-stu-id="5aef7-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="5aef7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aef7-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5aef7-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-116">Big Integer</span><span class="sxs-lookup"><span data-stu-id="5aef7-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aef7-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-118">Binario</span><span class="sxs-lookup"><span data-stu-id="5aef7-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aef7-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="5aef7-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aef7-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-122">Byte</span><span class="sxs-lookup"><span data-stu-id="5aef7-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aef7-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-124">Char</span><span class="sxs-lookup"><span data-stu-id="5aef7-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aef7-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-126">Moneda</span><span class="sxs-lookup"><span data-stu-id="5aef7-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aef7-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-128">Fecha y hora</span><span class="sxs-lookup"><span data-stu-id="5aef7-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aef7-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="5aef7-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aef7-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-132">Doble</span><span class="sxs-lookup"><span data-stu-id="5aef7-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aef7-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-134">Float</span><span class="sxs-lookup"><span data-stu-id="5aef7-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aef7-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-136">GUID</span><span class="sxs-lookup"><span data-stu-id="5aef7-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aef7-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-138">Entero</span><span class="sxs-lookup"><span data-stu-id="5aef7-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aef7-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-140">Long</span><span class="sxs-lookup"><span data-stu-id="5aef7-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aef7-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-142">Long Binary (objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="5aef7-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aef7-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-144">Memo</span><span class="sxs-lookup"><span data-stu-id="5aef7-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aef7-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-146">Numérico</span><span class="sxs-lookup"><span data-stu-id="5aef7-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aef7-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-148">Simple</span><span class="sxs-lookup"><span data-stu-id="5aef7-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aef7-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-150">Texto</span><span class="sxs-lookup"><span data-stu-id="5aef7-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aef7-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-152">Hora</span><span class="sxs-lookup"><span data-stu-id="5aef7-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5aef7-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-154">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="5aef7-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5aef7-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="5aef7-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5aef7-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="5aef7-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5aef7-157">Cuando se anexa un nuevo objeto **Field2**, **Parameter** o **Property** a la colección de un objeto **Index**, **QueryDef**, **Recordset** o **TableDef**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="5aef7-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

