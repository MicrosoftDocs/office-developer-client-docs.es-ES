---
title: Funciones escalares ODBC
TOCTitle: ODBC scalar functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 33443fda474b3785d34d457719e49f5e358bb254
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288514"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="feacb-102">Funciones escalares ODBC</span><span class="sxs-lookup"><span data-stu-id="feacb-102">ODBC scalar functions</span></span>

<span data-ttu-id="feacb-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="feacb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="feacb-104">Microsoft Access SQL admite el uso de la sintaxis definida por ODBC para funciones escalares.</span><span class="sxs-lookup"><span data-stu-id="feacb-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="feacb-105">Por ejemplo, la consulta devolvería todas las filas en las que el valor absoluto del cambio en el precio de un valor bursátil fuera `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` superior a cinco.</span><span class="sxs-lookup"><span data-stu-id="feacb-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="feacb-p101">Se admite un subconjunto de las funciones escalares definidas por ODBC. En la siguiente tabla, se enumeran las funciones admitidas.</span><span class="sxs-lookup"><span data-stu-id="feacb-p101">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="feacb-108">Para obtener una descripción de los argumentos y una explicación completa de la sintaxis de escape para incluir funciones en una instrucción SQL, vea la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="feacb-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="feacb-109">Funciones de cadena</span><span class="sxs-lookup"><span data-stu-id="feacb-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feacb-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="feacb-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="feacb-111">LENGTH</span><span class="sxs-lookup"><span data-stu-id="feacb-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="feacb-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="feacb-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feacb-113">CHAR</span><span class="sxs-lookup"><span data-stu-id="feacb-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="feacb-114">LOCATE</span><span class="sxs-lookup"><span data-stu-id="feacb-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="feacb-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="feacb-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feacb-116">CONCAT</span><span class="sxs-lookup"><span data-stu-id="feacb-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="feacb-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="feacb-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="feacb-118">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="feacb-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feacb-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="feacb-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="feacb-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="feacb-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="feacb-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="feacb-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feacb-122">LEFT</span><span class="sxs-lookup"><span data-stu-id="feacb-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="feacb-123">Funciones numéricas</span><span class="sxs-lookup"><span data-stu-id="feacb-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feacb-124">ABS</span><span class="sxs-lookup"><span data-stu-id="feacb-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="feacb-125">FLOOR</span><span class="sxs-lookup"><span data-stu-id="feacb-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="feacb-126">SIN</span><span class="sxs-lookup"><span data-stu-id="feacb-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feacb-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="feacb-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="feacb-128">LOG</span><span class="sxs-lookup"><span data-stu-id="feacb-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="feacb-129">SQRT</span><span class="sxs-lookup"><span data-stu-id="feacb-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feacb-130">CEILING</span><span class="sxs-lookup"><span data-stu-id="feacb-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="feacb-131">ENERGÍA</span><span class="sxs-lookup"><span data-stu-id="feacb-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="feacb-132">TAN</span><span class="sxs-lookup"><span data-stu-id="feacb-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feacb-133">COS</span><span class="sxs-lookup"><span data-stu-id="feacb-133">COS</span></span></p></td>
<td><p><span data-ttu-id="feacb-134">RAND</span><span class="sxs-lookup"><span data-stu-id="feacb-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="feacb-135">MOD</span><span class="sxs-lookup"><span data-stu-id="feacb-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feacb-136">EXP</span><span class="sxs-lookup"><span data-stu-id="feacb-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="feacb-137">SIGN</span><span class="sxs-lookup"><span data-stu-id="feacb-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="feacb-138">Funciones Time & Date</span><span class="sxs-lookup"><span data-stu-id="feacb-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feacb-139">CURDATE</span><span class="sxs-lookup"><span data-stu-id="feacb-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="feacb-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="feacb-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="feacb-141">MONTH</span><span class="sxs-lookup"><span data-stu-id="feacb-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feacb-142">CURTIME</span><span class="sxs-lookup"><span data-stu-id="feacb-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="feacb-143">YEAR</span><span class="sxs-lookup"><span data-stu-id="feacb-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="feacb-144">SEMANA</span><span class="sxs-lookup"><span data-stu-id="feacb-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feacb-145">NOW</span><span class="sxs-lookup"><span data-stu-id="feacb-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="feacb-146">HOUR</span><span class="sxs-lookup"><span data-stu-id="feacb-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="feacb-147">QUARTER</span><span class="sxs-lookup"><span data-stu-id="feacb-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feacb-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="feacb-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="feacb-149">MINUTE</span><span class="sxs-lookup"><span data-stu-id="feacb-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="feacb-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="feacb-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feacb-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="feacb-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="feacb-152">SECOND</span><span class="sxs-lookup"><span data-stu-id="feacb-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="feacb-153">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="feacb-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="feacb-154">Conversión de tipos de datos</span><span class="sxs-lookup"><span data-stu-id="feacb-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feacb-155">CONVERT</span><span class="sxs-lookup"><span data-stu-id="feacb-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="feacb-156">Los literales de cadena se pueden convertir a los siguientes tipos de datos: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR y SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="feacb-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

