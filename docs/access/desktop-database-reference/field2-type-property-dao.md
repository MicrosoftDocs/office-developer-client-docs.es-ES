---
title: Propiedad Field2.Type (DAO)
TOCTitle: Type Property
ms:assetid: 057d6ec9-b72c-cee6-005a-6d916e3dda29
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844921(v=office.15)
ms:contentKeyID: 48543032
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 867f964dab4967bf6f545083e1f53a1419e877d1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920420"
---
# <a name="field2type-property-dao"></a><span data-ttu-id="9f638-102">Propiedad Field2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="9f638-102">Field2.Type property (DAO)</span></span>


<span data-ttu-id="9f638-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f638-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f638-p101">Establece un valor que indica el tipo operativo o de datos de un objeto. **Integer** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9f638-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f638-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f638-106">Syntax</span></span>

<span data-ttu-id="9f638-107">*expresión* . Tipo de</span><span class="sxs-lookup"><span data-stu-id="9f638-107">*expression* .Type</span></span>

<span data-ttu-id="9f638-108">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="9f638-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f638-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f638-109">Remarks</span></span>

<span data-ttu-id="9f638-p102">La configuración o el valor devuelto es una constante que indica un tipo operativo o de datos. Para un objeto **Field2**, esta propiedad es de lectura y escritura hasta que el objeto se anexa a una colección o a otro objeto, después será de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="9f638-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="9f638-112">Para un objeto **Field2**, los valores o valores enteros posibles se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="9f638-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f638-113">Constante</span><span class="sxs-lookup"><span data-stu-id="9f638-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="9f638-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f638-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f638-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-116">Entero grande</span><span class="sxs-lookup"><span data-stu-id="9f638-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f638-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-118">Binario</span><span class="sxs-lookup"><span data-stu-id="9f638-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f638-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="9f638-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f638-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-122">Byte</span><span class="sxs-lookup"><span data-stu-id="9f638-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f638-123"><strong>CarDb</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-124">Carácter</span><span class="sxs-lookup"><span data-stu-id="9f638-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f638-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-126">Moneda</span><span class="sxs-lookup"><span data-stu-id="9f638-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f638-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-128">Fecha y hora</span><span class="sxs-lookup"><span data-stu-id="9f638-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f638-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="9f638-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f638-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-132">Doble</span><span class="sxs-lookup"><span data-stu-id="9f638-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f638-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-134">Flotante</span><span class="sxs-lookup"><span data-stu-id="9f638-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f638-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-136">GUID</span><span class="sxs-lookup"><span data-stu-id="9f638-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f638-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-138">Entero</span><span class="sxs-lookup"><span data-stu-id="9f638-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f638-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-140">Long</span><span class="sxs-lookup"><span data-stu-id="9f638-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f638-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-142">Binario largo (objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="9f638-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f638-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-144">Memo</span><span class="sxs-lookup"><span data-stu-id="9f638-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f638-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-146">Numérico</span><span class="sxs-lookup"><span data-stu-id="9f638-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f638-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-148">Single</span><span class="sxs-lookup"><span data-stu-id="9f638-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f638-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-150">Texto</span><span class="sxs-lookup"><span data-stu-id="9f638-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f638-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-152">Time</span><span class="sxs-lookup"><span data-stu-id="9f638-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f638-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-154">Marca de hora</span><span class="sxs-lookup"><span data-stu-id="9f638-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f638-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9f638-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9f638-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="9f638-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9f638-157">Cuando se anexa un nuevo objeto **Field2**, **Parameter** o **Property** a la colección de un objeto **Index**, **QueryDef**, **Recordset** o **TableDef**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="9f638-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

