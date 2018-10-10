---
title: Funciones de agregado, la función CALC y la palabra clave NEW
TOCTitle: Aggregate Functions, the CALC Function, and the NEW Keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3616ab20e1d1f6a5d80c70f90a90ad13b3abc0fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484214"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a><span data-ttu-id="ae197-102">Funciones de agregado, la función CALC y la palabra clave NEW</span><span class="sxs-lookup"><span data-stu-id="ae197-102">Aggregate Functions, the CALC Function, and the NEW Keyword</span></span>


<span data-ttu-id="ae197-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae197-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ae197-p101">El servicio de forma de datos admite las siguientes funciones. El nombre asignado al capítulo que contiene la columna en la que se van a realizar las operaciones es el *alias del capítulo*.</span><span class="sxs-lookup"><span data-stu-id="ae197-p101">Data shaping supports the following functions. The name assigned to the chapter containing the column to be operated on is the *chapter-alias*.</span></span>

<span data-ttu-id="ae197-p102">Un alias de capítulo puede ser completo y constar del nombre de columna de cada capítulo que lleva al capítulo que contiene el *nombre de columna*, todo separado por puntos. Por ejemplo, si el capítulo principal, chap1, contiene un capítulo secundario, chap2, que tiene una columna de cantidad, amt, entonces el nombre completo será chap1.chap2.amt.</span><span class="sxs-lookup"><span data-stu-id="ae197-p102">A chapter-alias may be fully qualified, consisting of each chapter column name leading to the chapter containing the *column-name,* all separated by periods. For example, if the parent chapter, chap1, contains a child chapter, chap2, that has an amount column, amt, then the qualified name would be chap1.chap2.amt.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae197-108">Funciones de agregado</span><span class="sxs-lookup"><span data-stu-id="ae197-108">Aggregate Functions</span></span></p></th>
<th><p><span data-ttu-id="ae197-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae197-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae197-110">SUMA (<em>alias de capítulo</em>.<em> nombre de la columna</em>)</span><span class="sxs-lookup"><span data-stu-id="ae197-110">SUM(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="ae197-111">Calcula la suma de todos los valores de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="ae197-111">Calculates the sum of all values in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-112">AVG (<em>alias de capítulo</em>.<em> nombre de la columna</em>)</span><span class="sxs-lookup"><span data-stu-id="ae197-112">AVG(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="ae197-113">Calcula el promedio de todos los valores de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="ae197-113">Calculates the average of all values in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-114">MAX (<em>alias de capítulo</em>.<em> nombre de la columna</em>)</span><span class="sxs-lookup"><span data-stu-id="ae197-114">MAX(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="ae197-115">Calcula el valor máximo de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="ae197-115">Calculates the maximum value in the specified column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-116">MIN (<em>alias de capítulo</em>.<em> nombre de la columna</em>)</span><span class="sxs-lookup"><span data-stu-id="ae197-116">MIN(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="ae197-117">Calcula el valor mínimo de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="ae197-117">Calculates the minimum value in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-118">COUNT (<em>alias de capítulo</em>[.<em> nombre de la columna</em>])</span><span class="sxs-lookup"><span data-stu-id="ae197-118">COUNT(<em>chapter-alias</em>[.<em>column-name</em>])</span></span></p></td>
<td><p><span data-ttu-id="ae197-p103">Cuenta el número de filas en el alias especificado. Si se especifica una columna, en el recuento sólo se incluirán las filas para las que la columna no tiene un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="ae197-p103">Counts the number of rows in the specified alias. If a column is specified, only rows for which that column is non-Null are included in the count.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-121">STDEV (<em>alias de capítulo</em>.<em> nombre de la columna</em>)</span><span class="sxs-lookup"><span data-stu-id="ae197-121">STDEV(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="ae197-122">Calcula la desviación estándar de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="ae197-122">Calculates the standard deviation in the specified column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-123">CUALQUIER (<em>alias de capítulo</em>.<em> nombre de la columna</em>)</span><span class="sxs-lookup"><span data-stu-id="ae197-123">ANY(<em>chapter-alias</em>.<em>column-name</em>)</span></span></p></td>
<td><p><span data-ttu-id="ae197-p104">Un valor de la columna especificada. ANY sólo tiene un valor predecible si el valor de la columna es el mismo para todas las filas del capítulo.
</span><span class="sxs-lookup"><span data-stu-id="ae197-p104">A value of the specified column. ANY has a predictable value only when the value of the column is the same for all rows in the chapter.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="ae197-126">Si la columna no contiene el mismo valor para todas las filas del capítulo, el comando SHAPE devuelve arbitrariamente uno de los valores para que sea el valor de la función ANY.</span><span class="sxs-lookup"><span data-stu-id="ae197-126">If the column does not contain the same value for all of the rows in the chapter, the SHAPE command arbitrarily returns one of the values to be the value of the ANY function.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae197-127">Expresión calculada</span><span class="sxs-lookup"><span data-stu-id="ae197-127">Calculated expression</span></span></p></th>
<th><p><span data-ttu-id="ae197-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae197-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae197-129">CALC(<em>expresión</em>)</span><span class="sxs-lookup"><span data-stu-id="ae197-129">CALC(<em>expression</em>)</span></span></p></td>
<td><p><span data-ttu-id="ae197-p105">Calcula una expresión arbitraria, pero sólo en la fila del <strong>conjunto de registros</strong> que contiene la función CALC. Se admite toda expresión que utilice estas <a href="visual-basic-for-applications-functions.md">funciones de Visual Basic para Aplicaciones (VBA)</a>.</span><span class="sxs-lookup"><span data-stu-id="ae197-p105">Calculates an arbitrary expression, but only on the row of the <strong>Recordset</strong> containing the CALC function. Any expression using these <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications (VBA) Functions</a> is allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae197-132">Palabra clave NEW</span><span class="sxs-lookup"><span data-stu-id="ae197-132">NEW keyword</span></span></p></th>
<th><p><span data-ttu-id="ae197-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae197-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae197-134">NUEVO <em>tipo de campo</em> [(<em>ancho</em> | <em>escala</em> | <em>precisión</em> | <em>error</em> [, <em>escala</em> | <em>error</em>])]</span><span class="sxs-lookup"><span data-stu-id="ae197-134">NEW <em>field-type</em> [(<em>width</em> | <em>scale</em> | <em>precision</em> | <em>error</em> [, <em>scale</em> | <em>error</em>])]</span></span></p></td>
<td><p><span data-ttu-id="ae197-135">Agrega una columna vacía del tipo especificado al <strong>conjunto de registros</strong>.</span><span class="sxs-lookup"><span data-stu-id="ae197-135">Adds an empty column of the specified type to the <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ae197-136">El *tipo de campo* que se pasa con la palabra clave NEW puede ser cualquiera de los tipos de datos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ae197-136">The *field-type* passed with the NEW keyword can be any of the following data types.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae197-137">Tipos de datos de OLE DB</span><span class="sxs-lookup"><span data-stu-id="ae197-137">OLE DB data types</span></span></p></th>
<th><p><span data-ttu-id="ae197-138">Tipo de datos de ADO equivalentes</span><span class="sxs-lookup"><span data-stu-id="ae197-138">ADO data type equivalent(s)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae197-139">DBTYPE_BSTR</span><span class="sxs-lookup"><span data-stu-id="ae197-139">DBTYPE_BSTR</span></span></p></td>
<td><p><span data-ttu-id="ae197-140">adBSTR</span><span class="sxs-lookup"><span data-stu-id="ae197-140">adBSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-141">DBTYPE_BOOL</span><span class="sxs-lookup"><span data-stu-id="ae197-141">DBTYPE_BOOL</span></span></p></td>
<td><p><span data-ttu-id="ae197-142">adBoolean</span><span class="sxs-lookup"><span data-stu-id="ae197-142">adBoolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-143">DBTYPE_DECIMAL</span><span class="sxs-lookup"><span data-stu-id="ae197-143">DBTYPE_DECIMAL</span></span></p></td>
<td><p><span data-ttu-id="ae197-144">adDecimal</span><span class="sxs-lookup"><span data-stu-id="ae197-144">adDecimal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-145">DBTYPE_UI1</span><span class="sxs-lookup"><span data-stu-id="ae197-145">DBTYPE_UI1</span></span></p></td>
<td><p><span data-ttu-id="ae197-146">adUnsignedTinyInt</span><span class="sxs-lookup"><span data-stu-id="ae197-146">adUnsignedTinyInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-147">DBTYPE_I1</span><span class="sxs-lookup"><span data-stu-id="ae197-147">DBTYPE_I1</span></span></p></td>
<td><p><span data-ttu-id="ae197-148">excepto adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="ae197-148">adTinyInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-149">DBTYPE_UI2</span><span class="sxs-lookup"><span data-stu-id="ae197-149">DBTYPE_UI2</span></span></p></td>
<td><p><span data-ttu-id="ae197-150">adUnsignedSmallInt</span><span class="sxs-lookup"><span data-stu-id="ae197-150">adUnsignedSmallInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-151">DBTYPE_UI4</span><span class="sxs-lookup"><span data-stu-id="ae197-151">DBTYPE_UI4</span></span></p></td>
<td><p><span data-ttu-id="ae197-152">adUnsignedInt</span><span class="sxs-lookup"><span data-stu-id="ae197-152">adUnsignedInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-153">DBTYPE_I8</span><span class="sxs-lookup"><span data-stu-id="ae197-153">DBTYPE_I8</span></span></p></td>
<td><p><span data-ttu-id="ae197-154">adBigInt</span><span class="sxs-lookup"><span data-stu-id="ae197-154">adBigInt</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-155">DBTYPE_UI8</span><span class="sxs-lookup"><span data-stu-id="ae197-155">DBTYPE_UI8</span></span></p></td>
<td><p><span data-ttu-id="ae197-156">adUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="ae197-156">adUnsignedBigInt</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-157">DBTYPE_GUID</span><span class="sxs-lookup"><span data-stu-id="ae197-157">DBTYPE_GUID</span></span></p></td>
<td><p><span data-ttu-id="ae197-158">adGuid</span><span class="sxs-lookup"><span data-stu-id="ae197-158">adGuid</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-159">DBTYPE_BYTES</span><span class="sxs-lookup"><span data-stu-id="ae197-159">DBTYPE_BYTES</span></span></p></td>
<td><p><span data-ttu-id="ae197-160">adLongVarBinary adBinary, AdVarBinary,</span><span class="sxs-lookup"><span data-stu-id="ae197-160">adBinary, AdVarBinary, adLongVarBinary</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-161">DBTYPE_STR</span><span class="sxs-lookup"><span data-stu-id="ae197-161">DBTYPE_STR</span></span></p></td>
<td><p><span data-ttu-id="ae197-162">Cada, adVarChar, adLongVarChar</span><span class="sxs-lookup"><span data-stu-id="ae197-162">adChar, adVarChar, adLongVarChar</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-163">DBTYPE_WSTR</span><span class="sxs-lookup"><span data-stu-id="ae197-163">DBTYPE_WSTR</span></span></p></td>
<td><p><span data-ttu-id="ae197-164">adWChar, adVarWChar, adLongVarWChar</span><span class="sxs-lookup"><span data-stu-id="ae197-164">adWChar, adVarWChar, adLongVarWChar</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-165">DBTYPE_NUMERIC</span><span class="sxs-lookup"><span data-stu-id="ae197-165">DBTYPE_NUMERIC</span></span></p></td>
<td><p><span data-ttu-id="ae197-166">adNumeric</span><span class="sxs-lookup"><span data-stu-id="ae197-166">adNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-167">DBTYPE_DBDATE</span><span class="sxs-lookup"><span data-stu-id="ae197-167">DBTYPE_DBDATE</span></span></p></td>
<td><p><span data-ttu-id="ae197-168">adDBData</span><span class="sxs-lookup"><span data-stu-id="ae197-168">adDBDate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-169">DBTYPE_DBTIME</span><span class="sxs-lookup"><span data-stu-id="ae197-169">DBTYPE_DBTIME</span></span></p></td>
<td><p><span data-ttu-id="ae197-170">adDBTime</span><span class="sxs-lookup"><span data-stu-id="ae197-170">adDBTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-171">DBTYPE_DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="ae197-171">DBTYPE_DBTIMESTAMP</span></span></p></td>
<td><p><span data-ttu-id="ae197-172">adDBTimeStamp</span><span class="sxs-lookup"><span data-stu-id="ae197-172">adDBTimeStamp</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-173">DBTYPE_VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="ae197-173">DBTYPE_VARNUMERIC</span></span></p></td>
<td><p><span data-ttu-id="ae197-174">adVarNumeric</span><span class="sxs-lookup"><span data-stu-id="ae197-174">adVarNumeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae197-175">DBTYPE_FILETIME</span><span class="sxs-lookup"><span data-stu-id="ae197-175">DBTYPE_FILETIME</span></span></p></td>
<td><p><span data-ttu-id="ae197-176">adFileTime</span><span class="sxs-lookup"><span data-stu-id="ae197-176">adFileTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae197-177">DBTYPE_ERROR</span><span class="sxs-lookup"><span data-stu-id="ae197-177">DBTYPE_ERROR</span></span></p></td>
<td><p><span data-ttu-id="ae197-178">adError</span><span class="sxs-lookup"><span data-stu-id="ae197-178">adError</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ae197-179">Cuando el campo nuevo es de tipo decimal (en OLE DB, DBTYPE\_DECIMAL, o en ADO, adDecimal), debe especificar los valores de precisión y una escala.</span><span class="sxs-lookup"><span data-stu-id="ae197-179">When the new field is of type decimal (in OLE DB, DBTYPE\_DECIMAL, or in ADO, adDecimal), you must specify the precision and scale values.</span></span>

