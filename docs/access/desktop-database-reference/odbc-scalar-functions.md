---
title: Funciones escalares ODBC
TOCTitle: ODBC Scalar Functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f4a519f1853c0779777d59e6e6c314cbaaf60621
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937459"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="f9308-102">Funciones escalares ODBC</span><span class="sxs-lookup"><span data-stu-id="f9308-102">ODBC Scalar Functions</span></span>


<span data-ttu-id="f9308-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9308-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9308-104">Microsoft Access SQL admite el uso de la sintaxis definida ODBC para funciones escalares.</span><span class="sxs-lookup"><span data-stu-id="f9308-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> <span data-ttu-id="f9308-105">Por ejemplo, la consulta:</span><span class="sxs-lookup"><span data-stu-id="f9308-105">For example, the query:</span></span>

<span data-ttu-id="f9308-106">SELECT CIERREDIARIO, CAMBIODIARIO FROM COTIZACIÓNDIARIA WHERE {fn ABS(CAMBIODIARIO)} \> 5</span><span class="sxs-lookup"><span data-stu-id="f9308-106">SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} \> 5</span></span>

<span data-ttu-id="f9308-107">devolvería todas las filas en las que el valor absoluto del cambio en el precio de un valor bursátil es mayor de cinco.</span><span class="sxs-lookup"><span data-stu-id="f9308-107">Would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="f9308-p102">Se admite un subconjunto de las funciones escalares definidas por ODBC. En la siguiente tabla, se enumeran las funciones admitidas.</span><span class="sxs-lookup"><span data-stu-id="f9308-p102">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="f9308-110">Para obtener una descripción de los argumentos y una explicación completa de la sintaxis de escape para incluir funciones en una instrucción SQL, vea la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="f9308-110">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="f9308-111">Funciones de cadena</span><span class="sxs-lookup"><span data-stu-id="f9308-111">String Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9308-112">ASCII</span><span class="sxs-lookup"><span data-stu-id="f9308-112">ASCII</span></span></p></td>
<td><p><span data-ttu-id="f9308-113">LENGTH</span><span class="sxs-lookup"><span data-stu-id="f9308-113">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="f9308-114">RTRIM</span><span class="sxs-lookup"><span data-stu-id="f9308-114">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9308-115">CHAR</span><span class="sxs-lookup"><span data-stu-id="f9308-115">CHAR</span></span></p></td>
<td><p><span data-ttu-id="f9308-116">LOCATE</span><span class="sxs-lookup"><span data-stu-id="f9308-116">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="f9308-117">SPACE</span><span class="sxs-lookup"><span data-stu-id="f9308-117">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9308-118">CONCAT</span><span class="sxs-lookup"><span data-stu-id="f9308-118">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="f9308-119">LTRIM</span><span class="sxs-lookup"><span data-stu-id="f9308-119">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="f9308-120">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="f9308-120">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9308-121">LCASE</span><span class="sxs-lookup"><span data-stu-id="f9308-121">LCASE</span></span></p></td>
<td><p><span data-ttu-id="f9308-122">RIGHT</span><span class="sxs-lookup"><span data-stu-id="f9308-122">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="f9308-123">UCASE</span><span class="sxs-lookup"><span data-stu-id="f9308-123">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9308-124">LEFT</span><span class="sxs-lookup"><span data-stu-id="f9308-124">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="f9308-125">Funciones numéricas</span><span class="sxs-lookup"><span data-stu-id="f9308-125">Numeric Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9308-126">ABS</span><span class="sxs-lookup"><span data-stu-id="f9308-126">ABS</span></span></p></td>
<td><p><span data-ttu-id="f9308-127">FLOOR</span><span class="sxs-lookup"><span data-stu-id="f9308-127">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="f9308-128">SIN</span><span class="sxs-lookup"><span data-stu-id="f9308-128">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9308-129">ATAN</span><span class="sxs-lookup"><span data-stu-id="f9308-129">ATAN</span></span></p></td>
<td><p><span data-ttu-id="f9308-130">LOG</span><span class="sxs-lookup"><span data-stu-id="f9308-130">LOG</span></span></p></td>
<td><p><span data-ttu-id="f9308-131">SQRT</span><span class="sxs-lookup"><span data-stu-id="f9308-131">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9308-132">CEILING</span><span class="sxs-lookup"><span data-stu-id="f9308-132">CEILING</span></span></p></td>
<td><p><span data-ttu-id="f9308-133">POWER</span><span class="sxs-lookup"><span data-stu-id="f9308-133">POWER</span></span></p></td>
<td><p><span data-ttu-id="f9308-134">TAN</span><span class="sxs-lookup"><span data-stu-id="f9308-134">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9308-135">COS</span><span class="sxs-lookup"><span data-stu-id="f9308-135">COS</span></span></p></td>
<td><p><span data-ttu-id="f9308-136">RAND</span><span class="sxs-lookup"><span data-stu-id="f9308-136">RAND</span></span></p></td>
<td><p><span data-ttu-id="f9308-137">MOD</span><span class="sxs-lookup"><span data-stu-id="f9308-137">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9308-138">EXP</span><span class="sxs-lookup"><span data-stu-id="f9308-138">EXP</span></span></p></td>
<td><p><span data-ttu-id="f9308-139">SIGN</span><span class="sxs-lookup"><span data-stu-id="f9308-139">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="f9308-140">Funciones de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="f9308-140">Time & Date Functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9308-141">CURDATE</span><span class="sxs-lookup"><span data-stu-id="f9308-141">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="f9308-142">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="f9308-142">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="f9308-143">MONTH</span><span class="sxs-lookup"><span data-stu-id="f9308-143">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9308-144">CURTIME</span><span class="sxs-lookup"><span data-stu-id="f9308-144">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="f9308-145">YEAR</span><span class="sxs-lookup"><span data-stu-id="f9308-145">YEAR</span></span></p></td>
<td><p><span data-ttu-id="f9308-146">WEEK</span><span class="sxs-lookup"><span data-stu-id="f9308-146">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9308-147">NOW</span><span class="sxs-lookup"><span data-stu-id="f9308-147">NOW</span></span></p></td>
<td><p><span data-ttu-id="f9308-148">HOUR</span><span class="sxs-lookup"><span data-stu-id="f9308-148">HOUR</span></span></p></td>
<td><p><span data-ttu-id="f9308-149">QUARTER</span><span class="sxs-lookup"><span data-stu-id="f9308-149">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9308-150">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="f9308-150">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="f9308-151">MINUTE</span><span class="sxs-lookup"><span data-stu-id="f9308-151">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="f9308-152">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="f9308-152">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9308-153">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="f9308-153">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="f9308-154">SECOND</span><span class="sxs-lookup"><span data-stu-id="f9308-154">SECOND</span></span></p></td>
<td><p><span data-ttu-id="f9308-155">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="f9308-155">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="f9308-156">Conversión de tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f9308-156">Data Type Conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9308-157">CONVERT</span><span class="sxs-lookup"><span data-stu-id="f9308-157">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="f9308-158">Los literales de cadena se pueden convertir a los siguientes tipos de datos: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR y SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="f9308-158">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

