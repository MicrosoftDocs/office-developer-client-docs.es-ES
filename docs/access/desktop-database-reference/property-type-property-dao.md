---
title: Propiedad Property.Type (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c157e088c594c7a5b6a8ae7af3df4617d79e9be3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919846"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="a0e72-102">Propiedad Property.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="a0e72-102">Property.Type property (DAO)</span></span>


<span data-ttu-id="a0e72-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0e72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a0e72-p101">Establece un valor que indica el tipo operativo o de datos de un objeto. **Integer** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a0e72-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e72-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0e72-106">Syntax</span></span>

<span data-ttu-id="a0e72-107">*expresión* . Tipo de</span><span class="sxs-lookup"><span data-stu-id="a0e72-107">*expression* .Type</span></span>

<span data-ttu-id="a0e72-108">*expresión* Variable que representa un objeto **Property** .</span><span class="sxs-lookup"><span data-stu-id="a0e72-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0e72-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0e72-109">Remarks</span></span>

<span data-ttu-id="a0e72-p102">La configuración o el valor devuelto es una constante que indica un tipo operativo o de datos. Para un objeto **[Property](property-object-dao.md)**, esta propiedad es de lectura y escritura hasta que el objeto se anexa a una colección o a otro objeto, después será de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a0e72-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="a0e72-112">Para un objeto **Property**, los valores o valores enteros posibles se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a0e72-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0e72-113">Constante</span><span class="sxs-lookup"><span data-stu-id="a0e72-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="a0e72-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0e72-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0e72-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-116">Entero grande</span><span class="sxs-lookup"><span data-stu-id="a0e72-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e72-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-118">Binario</span><span class="sxs-lookup"><span data-stu-id="a0e72-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e72-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="a0e72-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e72-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-122">Byte</span><span class="sxs-lookup"><span data-stu-id="a0e72-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e72-123"><strong>CarDb</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-124">Carácter</span><span class="sxs-lookup"><span data-stu-id="a0e72-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e72-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-126">Moneda</span><span class="sxs-lookup"><span data-stu-id="a0e72-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e72-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-128">Fecha y hora</span><span class="sxs-lookup"><span data-stu-id="a0e72-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e72-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="a0e72-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e72-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-132">Doble</span><span class="sxs-lookup"><span data-stu-id="a0e72-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e72-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-134">Flotante</span><span class="sxs-lookup"><span data-stu-id="a0e72-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e72-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-136">GUID</span><span class="sxs-lookup"><span data-stu-id="a0e72-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e72-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-138">Entero</span><span class="sxs-lookup"><span data-stu-id="a0e72-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e72-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-140">Long</span><span class="sxs-lookup"><span data-stu-id="a0e72-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e72-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-142">Binario largo (objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="a0e72-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e72-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-144">Memo</span><span class="sxs-lookup"><span data-stu-id="a0e72-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e72-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-146">Numérico</span><span class="sxs-lookup"><span data-stu-id="a0e72-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e72-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-148">Single</span><span class="sxs-lookup"><span data-stu-id="a0e72-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e72-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-150">Texto</span><span class="sxs-lookup"><span data-stu-id="a0e72-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e72-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-152">Time</span><span class="sxs-lookup"><span data-stu-id="a0e72-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0e72-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-154">Marca de hora</span><span class="sxs-lookup"><span data-stu-id="a0e72-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0e72-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a0e72-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a0e72-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="a0e72-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0e72-157">Cuando anexa un nuevo objeto **Field**, **Parameter** o **Property** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** o **TableDef**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="a0e72-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

