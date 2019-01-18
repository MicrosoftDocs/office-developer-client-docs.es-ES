---
title: Propiedad Parameter.Type (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 208d0a5097b8473fef60b94f972f2c8579150fc7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699698"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="c5de4-102">Propiedad Parameter.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="c5de4-102">Parameter.Type property (DAO)</span></span>


<span data-ttu-id="c5de4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5de4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5de4-p101">Establece un valor que indica el tipo operativo o de datos de un objeto. **Integer** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c5de4-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5de4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5de4-106">Syntax</span></span>

<span data-ttu-id="c5de4-107">*expresión* . Tipo de</span><span class="sxs-lookup"><span data-stu-id="c5de4-107">*expression* .Type</span></span>

<span data-ttu-id="c5de4-108">*expresión* Variable que representa un objeto **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="c5de4-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5de4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5de4-109">Remarks</span></span>

<span data-ttu-id="c5de4-p102">La configuración o el valor devuelto es una constante que indica un tipo operativo o de datos. Para un objeto **[Parameter](parameter-object-dao.md)** en un área de trabajo de Microsoft Access la propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c5de4-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="c5de4-112">Para un objeto **Parameter**, los valores o valores enteros posibles se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c5de4-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5de4-113">Constante</span><span class="sxs-lookup"><span data-stu-id="c5de4-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="c5de4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5de4-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5de4-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-116">Entero grande</span><span class="sxs-lookup"><span data-stu-id="c5de4-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5de4-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-118">Binario</span><span class="sxs-lookup"><span data-stu-id="c5de4-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5de4-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="c5de4-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5de4-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-122">Byte</span><span class="sxs-lookup"><span data-stu-id="c5de4-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5de4-123"><strong>CarDb</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-124">Carácter</span><span class="sxs-lookup"><span data-stu-id="c5de4-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5de4-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-126">Moneda</span><span class="sxs-lookup"><span data-stu-id="c5de4-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5de4-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-128">Fecha y hora</span><span class="sxs-lookup"><span data-stu-id="c5de4-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5de4-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="c5de4-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5de4-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-132">Doble</span><span class="sxs-lookup"><span data-stu-id="c5de4-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5de4-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-134">Flotante</span><span class="sxs-lookup"><span data-stu-id="c5de4-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5de4-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-136">GUID</span><span class="sxs-lookup"><span data-stu-id="c5de4-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5de4-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-138">Entero</span><span class="sxs-lookup"><span data-stu-id="c5de4-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5de4-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-140">Long</span><span class="sxs-lookup"><span data-stu-id="c5de4-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5de4-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-142">Binario largo (objeto OLE)</span><span class="sxs-lookup"><span data-stu-id="c5de4-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5de4-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-144">Memo</span><span class="sxs-lookup"><span data-stu-id="c5de4-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5de4-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-146">Numérico</span><span class="sxs-lookup"><span data-stu-id="c5de4-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5de4-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-148">Single</span><span class="sxs-lookup"><span data-stu-id="c5de4-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5de4-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-150">Texto</span><span class="sxs-lookup"><span data-stu-id="c5de4-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5de4-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-152">Hora</span><span class="sxs-lookup"><span data-stu-id="c5de4-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5de4-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-154">Marca de hora</span><span class="sxs-lookup"><span data-stu-id="c5de4-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5de4-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="c5de4-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="c5de4-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="c5de4-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5de4-157">Cuando anexa un nuevo objeto **Field**, **Parameter** o **Property** a la colección de un objeto **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** o **TableDef**, se produce un error si la base de datos subyacente no admite el tipo de datos especificado para el nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="c5de4-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

