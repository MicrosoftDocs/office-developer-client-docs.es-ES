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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718038"
---
# <a name="odbc-scalar-functions"></a><span data-ttu-id="1db0a-102">Funciones escalares ODBC</span><span class="sxs-lookup"><span data-stu-id="1db0a-102">ODBC scalar functions</span></span>

<span data-ttu-id="1db0a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1db0a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1db0a-104">Microsoft Access SQL admite el uso de la sintaxis definida ODBC para funciones escalares.</span><span class="sxs-lookup"><span data-stu-id="1db0a-104">Microsoft Access SQL supports the use of the ODBC defined syntax for scalar functions.</span></span> 

<span data-ttu-id="1db0a-105">Por ejemplo, la consulta `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` devolvería todas las filas donde el valor absoluto del cambio en el precio de un valor bursátil es mayor de cinco.</span><span class="sxs-lookup"><span data-stu-id="1db0a-105">For example, the query `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` would return all rows where the absolute value of the change in the price of a stock was greater than five.</span></span>

<span data-ttu-id="1db0a-p101">Se admite un subconjunto de las funciones escalares definidas por ODBC. En la siguiente tabla, se enumeran las funciones admitidas.</span><span class="sxs-lookup"><span data-stu-id="1db0a-p101">A subset of the ODBC defined scalar functions is supported. The following table lists the functions that are supported.</span></span>

<span data-ttu-id="1db0a-108">Para obtener una descripción de los argumentos y una explicación completa de la sintaxis de escape para incluir funciones en una instrucción SQL, vea la documentación de ODBC.</span><span class="sxs-lookup"><span data-stu-id="1db0a-108">For a description of the arguments and a complete explanation of the escape syntax for including functions in a SQL statement, see the ODBC documentation.</span></span>

## <a name="string-functions"></a><span data-ttu-id="1db0a-109">Funciones de cadena</span><span class="sxs-lookup"><span data-stu-id="1db0a-109">String functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1db0a-110">ASCII</span><span class="sxs-lookup"><span data-stu-id="1db0a-110">ASCII</span></span></p></td>
<td><p><span data-ttu-id="1db0a-111">LENGTH</span><span class="sxs-lookup"><span data-stu-id="1db0a-111">LENGTH</span></span></p></td>
<td><p><span data-ttu-id="1db0a-112">RTRIM</span><span class="sxs-lookup"><span data-stu-id="1db0a-112">RTRIM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1db0a-113">CHAR</span><span class="sxs-lookup"><span data-stu-id="1db0a-113">CHAR</span></span></p></td>
<td><p><span data-ttu-id="1db0a-114">LOCATE</span><span class="sxs-lookup"><span data-stu-id="1db0a-114">LOCATE</span></span></p></td>
<td><p><span data-ttu-id="1db0a-115">SPACE</span><span class="sxs-lookup"><span data-stu-id="1db0a-115">SPACE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1db0a-116">CONCAT</span><span class="sxs-lookup"><span data-stu-id="1db0a-116">CONCAT</span></span></p></td>
<td><p><span data-ttu-id="1db0a-117">LTRIM</span><span class="sxs-lookup"><span data-stu-id="1db0a-117">LTRIM</span></span></p></td>
<td><p><span data-ttu-id="1db0a-118">SUBSTRING</span><span class="sxs-lookup"><span data-stu-id="1db0a-118">SUBSTRING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1db0a-119">LCASE</span><span class="sxs-lookup"><span data-stu-id="1db0a-119">LCASE</span></span></p></td>
<td><p><span data-ttu-id="1db0a-120">RIGHT</span><span class="sxs-lookup"><span data-stu-id="1db0a-120">RIGHT</span></span></p></td>
<td><p><span data-ttu-id="1db0a-121">UCASE</span><span class="sxs-lookup"><span data-stu-id="1db0a-121">UCASE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1db0a-122">LEFT</span><span class="sxs-lookup"><span data-stu-id="1db0a-122">LEFT</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a><span data-ttu-id="1db0a-123">Funciones numéricas</span><span class="sxs-lookup"><span data-stu-id="1db0a-123">Numeric functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1db0a-124">ABS</span><span class="sxs-lookup"><span data-stu-id="1db0a-124">ABS</span></span></p></td>
<td><p><span data-ttu-id="1db0a-125">FLOOR</span><span class="sxs-lookup"><span data-stu-id="1db0a-125">FLOOR</span></span></p></td>
<td><p><span data-ttu-id="1db0a-126">SIN</span><span class="sxs-lookup"><span data-stu-id="1db0a-126">SIN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1db0a-127">ATAN</span><span class="sxs-lookup"><span data-stu-id="1db0a-127">ATAN</span></span></p></td>
<td><p><span data-ttu-id="1db0a-128">LOG</span><span class="sxs-lookup"><span data-stu-id="1db0a-128">LOG</span></span></p></td>
<td><p><span data-ttu-id="1db0a-129">SQRT</span><span class="sxs-lookup"><span data-stu-id="1db0a-129">SQRT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1db0a-130">CEILING</span><span class="sxs-lookup"><span data-stu-id="1db0a-130">CEILING</span></span></p></td>
<td><p><span data-ttu-id="1db0a-131">POWER</span><span class="sxs-lookup"><span data-stu-id="1db0a-131">POWER</span></span></p></td>
<td><p><span data-ttu-id="1db0a-132">TAN</span><span class="sxs-lookup"><span data-stu-id="1db0a-132">TAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1db0a-133">COS</span><span class="sxs-lookup"><span data-stu-id="1db0a-133">COS</span></span></p></td>
<td><p><span data-ttu-id="1db0a-134">RAND</span><span class="sxs-lookup"><span data-stu-id="1db0a-134">RAND</span></span></p></td>
<td><p><span data-ttu-id="1db0a-135">MOD</span><span class="sxs-lookup"><span data-stu-id="1db0a-135">MOD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1db0a-136">EXP</span><span class="sxs-lookup"><span data-stu-id="1db0a-136">EXP</span></span></p></td>
<td><p><span data-ttu-id="1db0a-137">SIGN</span><span class="sxs-lookup"><span data-stu-id="1db0a-137">SIGN</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a><span data-ttu-id="1db0a-138">Funciones de fecha & de tiempo</span><span class="sxs-lookup"><span data-stu-id="1db0a-138">Time & Date functions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1db0a-139">CURDATE</span><span class="sxs-lookup"><span data-stu-id="1db0a-139">CURDATE</span></span></p></td>
<td><p><span data-ttu-id="1db0a-140">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1db0a-140">DAYOFYEAR</span></span></p></td>
<td><p><span data-ttu-id="1db0a-141">MONTH</span><span class="sxs-lookup"><span data-stu-id="1db0a-141">MONTH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1db0a-142">CURTIME</span><span class="sxs-lookup"><span data-stu-id="1db0a-142">CURTIME</span></span></p></td>
<td><p><span data-ttu-id="1db0a-143">YEAR</span><span class="sxs-lookup"><span data-stu-id="1db0a-143">YEAR</span></span></p></td>
<td><p><span data-ttu-id="1db0a-144">WEEK</span><span class="sxs-lookup"><span data-stu-id="1db0a-144">WEEK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1db0a-145">NOW</span><span class="sxs-lookup"><span data-stu-id="1db0a-145">NOW</span></span></p></td>
<td><p><span data-ttu-id="1db0a-146">HOUR</span><span class="sxs-lookup"><span data-stu-id="1db0a-146">HOUR</span></span></p></td>
<td><p><span data-ttu-id="1db0a-147">QUARTER</span><span class="sxs-lookup"><span data-stu-id="1db0a-147">QUARTER</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1db0a-148">DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="1db0a-148">DAYOFMONTH</span></span></p></td>
<td><p><span data-ttu-id="1db0a-149">MINUTE</span><span class="sxs-lookup"><span data-stu-id="1db0a-149">MINUTE</span></span></p></td>
<td><p><span data-ttu-id="1db0a-150">MONTHNAME</span><span class="sxs-lookup"><span data-stu-id="1db0a-150">MONTHNAME</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1db0a-151">DAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="1db0a-151">DAYOFWEEK</span></span></p></td>
<td><p><span data-ttu-id="1db0a-152">SECOND</span><span class="sxs-lookup"><span data-stu-id="1db0a-152">SECOND</span></span></p></td>
<td><p><span data-ttu-id="1db0a-153">DAYNAME</span><span class="sxs-lookup"><span data-stu-id="1db0a-153">DAYNAME</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a><span data-ttu-id="1db0a-154">Conversión de tipos de datos</span><span class="sxs-lookup"><span data-stu-id="1db0a-154">Data type conversion</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1db0a-155">CONVERT</span><span class="sxs-lookup"><span data-stu-id="1db0a-155">CONVERT</span></span></p></td>
<td><p><span data-ttu-id="1db0a-156">Los literales de cadena se pueden convertir a los siguientes tipos de datos: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR y SQL_DATETIME.</span><span class="sxs-lookup"><span data-stu-id="1db0a-156">String literals can be converted to the following data types: SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR and SQL_DATETIME.</span></span></p></td>
</tr>
</tbody>
</table>

