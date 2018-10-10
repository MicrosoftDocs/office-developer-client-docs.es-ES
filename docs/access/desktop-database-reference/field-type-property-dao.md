---
title: Field.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dab800e390e6ceaa6bf473e54d7d576f5e6023f4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486403"
---
# <a name="fieldtype-property-dao"></a><span data-ttu-id="a23f6-102">Field.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="a23f6-102">Field.Type Property (DAO)</span></span>


<span data-ttu-id="a23f6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a23f6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a23f6-p101">Establece un valor que indica el tipo operativo o de datos de un objeto. **Integer** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a23f6-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a23f6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a23f6-106">Syntax</span></span>

<span data-ttu-id="a23f6-107">*expresión* . Tipo de</span><span class="sxs-lookup"><span data-stu-id="a23f6-107">*expression* .Type</span></span>

<span data-ttu-id="a23f6-108">*expresión* Variable que representa un objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="a23f6-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a23f6-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a23f6-109">Remarks</span></span>

<span data-ttu-id="a23f6-p102">La configuración o el valor devuelto es una constante que indica un tipo operativo o de datos. Para un objeto **Field**, esta propiedad es de lectura y escritura hasta que el objeto se anexa a una colección o a otro objeto; a partir de ese momento, es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a23f6-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="a23f6-112">Para un objeto **Field**, los valores de configuración y los valores devueltos se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a23f6-112">For a **Field** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a23f6-113">Constante</span><span class="sxs-lookup"><span data-stu-id="a23f6-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="a23f6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a23f6-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a23f6-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-116">Entero grande</span><span class="sxs-lookup"><span data-stu-id="a23f6-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a23f6-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-118">Binario</span><span class="sxs-lookup"><span data-stu-id="a23f6-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a23f6-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="a23f6-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a23f6-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-122">Byte</span><span class="sxs-lookup"><span data-stu-id="a23f6-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a23f6-123"><strong>CarDb</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-124">Carácter</span><span class="sxs-lookup"><span data-stu-id="a23f6-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a23f6-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-126">Moneda</span><span class="sxs-lookup"><span data-stu-id="a23f6-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a23f6-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-128">Fecha y hora</span><span class="sxs-lookup"><span data-stu-id="a23f6-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a23f6-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="a23f6-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a23f6-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-132">Doble</span><span class="sxs-lookup"><span data-stu-id="a23f6-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a23f6-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-134">Flotante</span><span class="sxs-lookup"><span data-stu-id="a23f6-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a23f6-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-136">GUID</span><span class="sxs-lookup"><span data-stu-id="a23f6-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a23f6-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-138">Entero</span><span class="sxs-lookup"><span data-stu-id="a23f6-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a23f6-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-140">Long</span><span class="sxs-lookup"><span data-stu-id="a23f6-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a23f6-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-142">Binario largo (objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="a23f6-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a23f6-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-144">Memo</span><span class="sxs-lookup"><span data-stu-id="a23f6-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a23f6-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-146">Numérico</span><span class="sxs-lookup"><span data-stu-id="a23f6-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a23f6-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-148">Single</span><span class="sxs-lookup"><span data-stu-id="a23f6-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a23f6-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-150">Texto</span><span class="sxs-lookup"><span data-stu-id="a23f6-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a23f6-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-152">Time</span><span class="sxs-lookup"><span data-stu-id="a23f6-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a23f6-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-154">Marca de hora</span><span class="sxs-lookup"><span data-stu-id="a23f6-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a23f6-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="a23f6-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="a23f6-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="a23f6-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a23f6-157">Cuando anexa un nuevo objeto **Field**, **Parameter** o **Property** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** o **TableDef**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="a23f6-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

