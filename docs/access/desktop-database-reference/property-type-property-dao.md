---
title: Propiedad Property.Type (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4280b89102e06b2ecc09a783840e671b0af9ff73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302905"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="2779f-102">Propiedad Property.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="2779f-102">Property.Type property (DAO)</span></span>


<span data-ttu-id="2779f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2779f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2779f-p101">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. **Integer** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2779f-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2779f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2779f-106">Syntax</span></span>

<span data-ttu-id="2779f-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="2779f-107">*expression* .Type</span></span>

<span data-ttu-id="2779f-108">*expresión* Variable que representa un **objeto Property.**</span><span class="sxs-lookup"><span data-stu-id="2779f-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2779f-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2779f-109">Remarks</span></span>

<span data-ttu-id="2779f-p102">La configuración o el valor devuelto es una constante que indica un tipo operativo o de datos. Para un objeto **[Property](property-object-dao.md)**, esta propiedad es de lectura y escritura hasta que el objeto se anexa a una colección o a otro objeto, después será de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2779f-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="2779f-112">Para un objeto **Property**, los valores o valores enteros posibles se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2779f-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2779f-113">Constante</span><span class="sxs-lookup"><span data-stu-id="2779f-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="2779f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2779f-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2779f-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-116">Big Integer</span><span class="sxs-lookup"><span data-stu-id="2779f-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2779f-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-118">Binario</span><span class="sxs-lookup"><span data-stu-id="2779f-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2779f-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="2779f-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2779f-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-122">Byte</span><span class="sxs-lookup"><span data-stu-id="2779f-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2779f-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-124">Char</span><span class="sxs-lookup"><span data-stu-id="2779f-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2779f-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-126">Moneda</span><span class="sxs-lookup"><span data-stu-id="2779f-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2779f-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-128">Fecha y hora</span><span class="sxs-lookup"><span data-stu-id="2779f-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2779f-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="2779f-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2779f-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-132">Doble</span><span class="sxs-lookup"><span data-stu-id="2779f-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2779f-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-134">Float</span><span class="sxs-lookup"><span data-stu-id="2779f-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2779f-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-136">GUID</span><span class="sxs-lookup"><span data-stu-id="2779f-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2779f-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-138">Entero</span><span class="sxs-lookup"><span data-stu-id="2779f-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2779f-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-140">Long</span><span class="sxs-lookup"><span data-stu-id="2779f-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2779f-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-142">Long Binary (objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="2779f-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2779f-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-144">Memo</span><span class="sxs-lookup"><span data-stu-id="2779f-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2779f-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-146">Numérico</span><span class="sxs-lookup"><span data-stu-id="2779f-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2779f-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-148">Simple</span><span class="sxs-lookup"><span data-stu-id="2779f-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2779f-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-150">Texto</span><span class="sxs-lookup"><span data-stu-id="2779f-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2779f-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-152">Hora</span><span class="sxs-lookup"><span data-stu-id="2779f-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2779f-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-154">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="2779f-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2779f-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2779f-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2779f-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="2779f-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2779f-157">Cuando se anexa un nuevo objeto **Field**, **Parameter** o **Property** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** o **TableDef**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="2779f-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

