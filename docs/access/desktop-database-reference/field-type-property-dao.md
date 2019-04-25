---
title: Propiedad Field.Type (DAO)
TOCTitle: Type Property
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c8f212c5e1f10f4270987c9453802575d88cebfa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292954"
---
# <a name="fieldtype-property-dao"></a><span data-ttu-id="3a4aa-102">Propiedad Field.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="3a4aa-102">Field.Type property (DAO)</span></span>


<span data-ttu-id="3a4aa-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a4aa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a4aa-104">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto.</span><span class="sxs-lookup"><span data-stu-id="3a4aa-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="3a4aa-105">Valor **Entero** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3a4aa-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a4aa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a4aa-106">Syntax</span></span>

<span data-ttu-id="3a4aa-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="3a4aa-107">expression  . Type</span></span>

<span data-ttu-id="3a4aa-108">*expression* Variable que representa un objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="3a4aa-108">*expression*  A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a4aa-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a4aa-109">Remarks</span></span>

<span data-ttu-id="3a4aa-p102">La configuración o el valor devuelto es una constante que indica un tipo operativo o de datos. Para un objeto **Field**, esta propiedad es de lectura y escritura hasta que el objeto se anexa a una colección o a otro objeto; a partir de ese momento, es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="3a4aa-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="3a4aa-112">Para un objeto **Field**, los valores de configuración y los valores devueltos se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3a4aa-112">For a **Field** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a4aa-113">Constante</span><span class="sxs-lookup"><span data-stu-id="3a4aa-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="3a4aa-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a4aa-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a4aa-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-116">Big Integer</span><span class="sxs-lookup"><span data-stu-id="3a4aa-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4aa-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-118">Binario</span><span class="sxs-lookup"><span data-stu-id="3a4aa-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4aa-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="3a4aa-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4aa-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-122">Byte</span><span class="sxs-lookup"><span data-stu-id="3a4aa-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4aa-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-124">Char</span><span class="sxs-lookup"><span data-stu-id="3a4aa-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4aa-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-126">Moneda</span><span class="sxs-lookup"><span data-stu-id="3a4aa-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4aa-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-128">Fecha y hora</span><span class="sxs-lookup"><span data-stu-id="3a4aa-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4aa-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="3a4aa-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4aa-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-132">Doble</span><span class="sxs-lookup"><span data-stu-id="3a4aa-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4aa-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-134">Float</span><span class="sxs-lookup"><span data-stu-id="3a4aa-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4aa-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-136">GUID</span><span class="sxs-lookup"><span data-stu-id="3a4aa-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4aa-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-138">Entero</span><span class="sxs-lookup"><span data-stu-id="3a4aa-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4aa-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-140">Long</span><span class="sxs-lookup"><span data-stu-id="3a4aa-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4aa-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-142">Long Binary (objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="3a4aa-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4aa-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-144">Memo</span><span class="sxs-lookup"><span data-stu-id="3a4aa-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4aa-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-146">Numérico</span><span class="sxs-lookup"><span data-stu-id="3a4aa-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4aa-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-148">Simple</span><span class="sxs-lookup"><span data-stu-id="3a4aa-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4aa-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-150">Texto</span><span class="sxs-lookup"><span data-stu-id="3a4aa-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4aa-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-152">Hora</span><span class="sxs-lookup"><span data-stu-id="3a4aa-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a4aa-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-154">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="3a4aa-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a4aa-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="3a4aa-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="3a4aa-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="3a4aa-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a4aa-157">Cuando se anexa un nuevo objeto **Field**, **Parameter** o **Property** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** o **TableDef**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="3a4aa-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

