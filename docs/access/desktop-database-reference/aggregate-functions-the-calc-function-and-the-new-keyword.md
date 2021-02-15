---
title: Funciones de agregado, función CALC y palabra clave NEW
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25f52489430465235a928fff3c38469ec6ba83ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297196"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="da68c-102">Funciones de agregado, función CALC y palabra clave NEW</span><span class="sxs-lookup"><span data-stu-id="da68c-102">Aggregate functions, the CALC function, and the NEW keyword</span></span>


<span data-ttu-id="da68c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da68c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="da68c-104">El servicio de forma de datos admite las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="da68c-104">Data shaping supports the following functions.</span></span> <span data-ttu-id="da68c-105">El nombre asignado al capítulo que contiene la columna en la que se van a realizar las operaciones es el *alias del capítulo*.</span><span class="sxs-lookup"><span data-stu-id="da68c-105">The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="da68c-p102">Un alias de capítulo puede ser completo y constar del nombre de columna de cada capítulo que lleva al capítulo que contiene el *nombre de columna*, todo separado por puntos. Por ejemplo, si el capítulo principal, chap1, contiene un capítulo secundario, chap2, que tiene una columna de cantidad, amt, entonces el nombre completo será chap1.chap2.amt.</span><span class="sxs-lookup"><span data-stu-id="da68c-p102">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods. For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da68c-108">Funciones de agregado</span><span class="sxs-lookup"><span data-stu-id="da68c-108">Aggregate functions</span></span></p></th>
<th><p><span data-ttu-id="da68c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="da68c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da68c-110">SUM(<em>chapter-alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="da68c-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="da68c-111">Calcula la suma de todos los valores de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="da68c-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-112">AVG(<em>chapter-alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="da68c-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="da68c-113">Calcula el promedio de todos los valores de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="da68c-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-114">MAX(<em>chapter-alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="da68c-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="da68c-115">Calcula el valor máximo de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="da68c-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-116">MIN(<em>chapter-alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="da68c-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="da68c-117">Calcula el valor mínimo de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="da68c-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-118">COUNT(<em>chapter-alias</em>[.<em> column-name</em>])</span><span class="sxs-lookup"><span data-stu-id="da68c-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="da68c-p103">Cuenta el número de filas en el alias especificado. Si se especifica una columna, en el recuento sólo se incluirán las filas para las que la columna no tiene un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="da68c-p103">Counts the number of rows in the specified alias. If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-121">STDEV(<em>chapter-alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="da68c-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="da68c-122">Calcula la desviación estándar de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="da68c-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-123">ANY(<em>chapter-alias</em>.<em> column-name</em>)</span><span class="sxs-lookup"><span data-stu-id="da68c-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="da68c-124">Un valor de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="da68c-124">A value of the specified column.</span></span> <span data-ttu-id="da68c-125">ANY sólo tiene un valor predecible si el valor de la columna es el mismo para todas las filas del capítulo.</span><span class="sxs-lookup"><span data-stu-id="da68c-125">ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p><p><span data-ttu-id="da68c-126"><strong>NOTA:</strong>si la columna no contiene el mismo valor para todas las filas del capítulo, el comando SHAPE devuelve arbitrariamente uno de los valores para que sea el valor de la función ANY.</span><span class="sxs-lookup"><span data-stu-id="da68c-126"><strong>NOTE</strong>: If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da68c-127">Expresión calculada</span><span class="sxs-lookup"><span data-stu-id="da68c-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="da68c-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="da68c-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da68c-129">CALC(<em>expresión</em>)</span><span class="sxs-lookup"><span data-stu-id="da68c-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="da68c-p105">Calcula una expresión arbitraria, pero sólo en la fila del <strong>conjunto de registros</strong> que contiene la función CALC. Se admite toda expresión que utilice estas <a href="visual-basic-for-applications-functions.md">funciones de Visual Basic para Aplicaciones (VBA)</a>.</span><span class="sxs-lookup"><span data-stu-id="da68c-p105">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function. Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da68c-132">Palabra clave NEW</span><span class="sxs-lookup"><span data-stu-id="da68c-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="da68c-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="da68c-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da68c-134">NUEVO <em>tipo de campo</em> [( error<em>de</em>precisión  |  <em></em>  |  <em>de</em>  |  <em>escala de ancho</em> [, error <em>de</em>  |  <em>escala</em>])]</span><span class="sxs-lookup"><span data-stu-id="da68c-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="da68c-135">Agrega una columna vacía del tipo especificado al <strong>conjunto de registros</strong>.</span><span class="sxs-lookup"><span data-stu-id="da68c-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="da68c-136">El *tipo de campo* que se pasa con la palabra clave NEW puede ser cualquiera de los tipos de datos siguientes.</span><span class="sxs-lookup"><span data-stu-id="da68c-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da68c-137">Tipos de datos de OLE DB</span><span class="sxs-lookup"><span data-stu-id="da68c-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="da68c-138">Tipo de datos de ADO equivalentes</span><span class="sxs-lookup"><span data-stu-id="da68c-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da68c-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="da68c-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="da68c-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="da68c-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="da68c-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="da68c-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="da68c-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="da68c-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="da68c-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="da68c-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="da68c-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="da68c-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="da68c-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="da68c-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="da68c-148">adTinyInt</span><span class="sxs-lookup"><span data-stu-id="da68c-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="da68c-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="da68c-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="da68c-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="da68c-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="da68c-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="da68c-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="da68c-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="da68c-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="da68c-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="da68c-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="da68c-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="da68c-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="da68c-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="da68c-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="da68c-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="da68c-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="da68c-160">adBinary, AdVarBinary, adLongVarBinary</span><span class="sxs-lookup"><span data-stu-id="da68c-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="da68c-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="da68c-162">adChar, adVarChar, adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="da68c-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="da68c-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="da68c-164">adWChar, adVarWChar, adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="da68c-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="da68c-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="da68c-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="da68c-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="da68c-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="da68c-168">adDBDate</span><span class="sxs-lookup"><span data-stu-id="da68c-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="da68c-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="da68c-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="da68c-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="da68c-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="da68c-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="da68c-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="da68c-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="da68c-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="da68c-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da68c-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="da68c-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="da68c-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="da68c-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da68c-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="da68c-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="da68c-178">adError</span><span class="sxs-lookup"><span data-stu-id="da68c-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="da68c-179">Cuando el nuevo campo es de tipo decimal (en OLE DB, DBTYPE DECIMAL o en ADO, adDecimal), debe especificar los valores de precisión \_ y escala.</span><span class="sxs-lookup"><span data-stu-id="da68c-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

