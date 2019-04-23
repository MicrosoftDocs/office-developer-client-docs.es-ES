---
title: Propiedad Parameter. Type (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 208d0a5097b8473fef60b94f972f2c8579150fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288024"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="2d2c3-102">Propiedad Parameter. Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="2d2c3-102">Parameter.Type property (DAO)</span></span>


<span data-ttu-id="2d2c3-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d2c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d2c3-104">Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto.</span><span class="sxs-lookup"><span data-stu-id="2d2c3-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="2d2c3-105">**Integer** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2d2c3-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d2c3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d2c3-106">Syntax</span></span>

<span data-ttu-id="2d2c3-107">*expresión* . Type</span><span class="sxs-lookup"><span data-stu-id="2d2c3-107">*expression* .Type</span></span>

<span data-ttu-id="2d2c3-108">*expresión* Variable que representa un objeto **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="2d2c3-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d2c3-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d2c3-109">Remarks</span></span>

<span data-ttu-id="2d2c3-p102">La configuración o el valor devuelto es una constante que indica un tipo operativo o de datos. Para un objeto **[Parameter](parameter-object-dao.md)** en un área de trabajo de Microsoft Access la propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2d2c3-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="2d2c3-112">Para un objeto **Parameter**, los valores o valores enteros posibles se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2d2c3-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d2c3-113">Constante</span><span class="sxs-lookup"><span data-stu-id="2d2c3-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="2d2c3-114">Description</span><span class="sxs-lookup"><span data-stu-id="2d2c3-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d2c3-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-116">Big Integer</span><span class="sxs-lookup"><span data-stu-id="2d2c3-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d2c3-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-118">Binary</span><span class="sxs-lookup"><span data-stu-id="2d2c3-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d2c3-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="2d2c3-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d2c3-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-122">Byte</span><span class="sxs-lookup"><span data-stu-id="2d2c3-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d2c3-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-124">Char</span><span class="sxs-lookup"><span data-stu-id="2d2c3-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d2c3-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-126">Moneda</span><span class="sxs-lookup"><span data-stu-id="2d2c3-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d2c3-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-128">Fecha y hora</span><span class="sxs-lookup"><span data-stu-id="2d2c3-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d2c3-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="2d2c3-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d2c3-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-132">Doble</span><span class="sxs-lookup"><span data-stu-id="2d2c3-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d2c3-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-134">Float</span><span class="sxs-lookup"><span data-stu-id="2d2c3-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d2c3-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-136">GUID</span><span class="sxs-lookup"><span data-stu-id="2d2c3-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d2c3-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-138">Entero</span><span class="sxs-lookup"><span data-stu-id="2d2c3-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d2c3-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-140">Long</span><span class="sxs-lookup"><span data-stu-id="2d2c3-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d2c3-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-142">Long Binary (objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="2d2c3-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d2c3-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-144">Memo</span><span class="sxs-lookup"><span data-stu-id="2d2c3-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d2c3-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-146">Numeric</span><span class="sxs-lookup"><span data-stu-id="2d2c3-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d2c3-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-148">Single</span><span class="sxs-lookup"><span data-stu-id="2d2c3-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d2c3-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-150">Texto</span><span class="sxs-lookup"><span data-stu-id="2d2c3-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d2c3-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-152">Hora</span><span class="sxs-lookup"><span data-stu-id="2d2c3-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d2c3-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-154">Time Stamp</span><span class="sxs-lookup"><span data-stu-id="2d2c3-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d2c3-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="2d2c3-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="2d2c3-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="2d2c3-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d2c3-157">Cuando se anexa un nuevo objeto **Field**, **Parameter** o **Property** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** o **TableDef**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="2d2c3-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

