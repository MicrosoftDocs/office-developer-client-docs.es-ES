---
title: DataTypeEnum (referencia de base de datos de escritorio de Access)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ffba234ed1c5dc56138a665d6dd07038f55da7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294445"
---
# <a name="datatypeenum"></a><span data-ttu-id="604b8-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="604b8-102">DataTypeEnum</span></span>

<span data-ttu-id="604b8-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="604b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="604b8-p101">Especifica el tipo de datos de un objeto [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) o [Property](property-object-ado.md). El indicador correspondiente de tipo OLE DB se muestra entre paréntesis en la columna Descripción de la tabla siguiente. Para obtener más información acerca de los tipos de datos OLE DB, vea el Capítulo 13 y el Apéndice A de la *Referencia del programador de OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="604b8-p101">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md). The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="604b8-107">Constante</span><span class="sxs-lookup"><span data-stu-id="604b8-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="604b8-108">Valor</span><span class="sxs-lookup"><span data-stu-id="604b8-108">Value</span></span></p></th>
<th><p><span data-ttu-id="604b8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="604b8-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="604b8-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="604b8-110"><strong>AdArray</span></span><br /><span data-ttu-id="604b8-111">
</strong>(No se aplica a ADOX).</span><span class="sxs-lookup"><span data-stu-id="604b8-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="604b8-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="604b8-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="604b8-113">Un valor de marca, siempre combinado con otra constante de tipo de datos, que indica una matriz de ese otro tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="604b8-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-115">20</span><span class="sxs-lookup"><span data-stu-id="604b8-115">20</span></span></p></td>
<td><p><span data-ttu-id="604b8-116">Indica un entero de ocho bytes con signo (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="604b8-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-118">128</span><span class="sxs-lookup"><span data-stu-id="604b8-118">128</span></span></p></td>
<td><p><span data-ttu-id="604b8-119">Indica un valor binario (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="604b8-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-121">11</span><span class="sxs-lookup"><span data-stu-id="604b8-121">11</span></span></p></td>
<td><p><span data-ttu-id="604b8-122">Indica un valor de tipo booleano (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="604b8-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-124">8 </span><span class="sxs-lookup"><span data-stu-id="604b8-124">8</span></span></p></td>
<td><p><span data-ttu-id="604b8-125">Indica una cadena de caracteres terminada en el carácter nulo (Unicode) (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="604b8-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-127">136</span><span class="sxs-lookup"><span data-stu-id="604b8-127">136</span></span></p></td>
<td><p><span data-ttu-id="604b8-128">Indica un valor de capítulo de cuatro bytes que identifica las filas de un conjunto de filas secundario (DBTYPE_HCHAPTER).</span><span class="sxs-lookup"><span data-stu-id="604b8-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-129"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-130">129</span><span class="sxs-lookup"><span data-stu-id="604b8-130">129</span></span></p></td>
<td><p><span data-ttu-id="604b8-131">Indica un valor de cadena (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="604b8-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-133">6 </span><span class="sxs-lookup"><span data-stu-id="604b8-133">6</span></span></p></td>
<td><p><span data-ttu-id="604b8-p102">Indica un valor de moneda (DBTYPE_CY). Este valor es un número de punto fijo con cuatro dígitos a la derecha del separador decimal. Se almacena en un entero de ocho bytes con signo y con un factor de escala de 10.000.</span><span class="sxs-lookup"><span data-stu-id="604b8-p102">Indicates a currency value (DBTYPE_CY). Currency is a fixed-point number with four digits to the right of the decimal point. It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-138">7 </span><span class="sxs-lookup"><span data-stu-id="604b8-138">7</span></span></p></td>
<td><p><span data-ttu-id="604b8-p103">Indica un valor de fecha (DBTYPE_DATE). Una fecha se almacena en un tipo double (real de doble precisión), en el que la parte entera es el número de días transcurridos desde el 30 de diciembre de 1899 y la parte fraccionaria es la fracción de un día.</span><span class="sxs-lookup"><span data-stu-id="604b8-p103">Indicates a date value (DBTYPE_DATE). A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-142">133</span><span class="sxs-lookup"><span data-stu-id="604b8-142">133</span></span></p></td>
<td><p><span data-ttu-id="604b8-143">Indica un valor de fecha (aaaammdd) (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="604b8-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-145">134</span><span class="sxs-lookup"><span data-stu-id="604b8-145">134</span></span></p></td>
<td><p><span data-ttu-id="604b8-146">Indica un valor de hora (hhmmss) (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="604b8-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-148">135</span><span class="sxs-lookup"><span data-stu-id="604b8-148">135</span></span></p></td>
<td><p><span data-ttu-id="604b8-149">Indica una marca de tiempo de fecha y hora (aaaammddhhmmss más una fracción en milmillonésimas) (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="604b8-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-151">14 </span><span class="sxs-lookup"><span data-stu-id="604b8-151">14</span></span></p></td>
<td><p><span data-ttu-id="604b8-152">Indica un valor numérico exacto con una precisión y una escala fijas (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="604b8-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-154">5 </span><span class="sxs-lookup"><span data-stu-id="604b8-154">5</span></span></p></td>
<td><p><span data-ttu-id="604b8-155">Indica un valor de punto flotante de doble precisión (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="604b8-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-157">0</span><span class="sxs-lookup"><span data-stu-id="604b8-157">0</span></span></p></td>
<td><p><span data-ttu-id="604b8-158">No especifica ningún valor (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="604b8-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-160">10</span><span class="sxs-lookup"><span data-stu-id="604b8-160">10</span></span></p></td>
<td><p><span data-ttu-id="604b8-161">Indica un código de error de 32 bits (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="604b8-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-163">64</span><span class="sxs-lookup"><span data-stu-id="604b8-163">64</span></span></p></td>
<td><p><span data-ttu-id="604b8-164">Indica un valor de 64 bits que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="604b8-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-166">72</span><span class="sxs-lookup"><span data-stu-id="604b8-166">72</span></span></p></td>
<td><p><span data-ttu-id="604b8-167">Indica un identificador globalmente único (GUID) (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="604b8-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-169">9 </span><span class="sxs-lookup"><span data-stu-id="604b8-169">9</span></span></p></td>
<td><p><span data-ttu-id="604b8-170">Indica un puntero a una interfaz <strong>IDispatch</strong> sobre un objeto COM (DBTYPE_IDISPATCH).</span><span class="sxs-lookup"><span data-stu-id="604b8-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="604b8-171"><strong>NOTA:</strong>Este tipo de datos actualmente no es compatible con ADO.</span><span class="sxs-lookup"><span data-stu-id="604b8-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="604b8-172">Su uso puede provocar resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="604b8-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-173"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-174">3</span><span class="sxs-lookup"><span data-stu-id="604b8-174">3</span></span></p></td>
<td><p><span data-ttu-id="604b8-175">Indica un entero de cuatro bytes con signo (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="604b8-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-177">13</span><span class="sxs-lookup"><span data-stu-id="604b8-177">13</span></span></p></td>
<td><p><span data-ttu-id="604b8-178">Indica un puntero a una interfaz <strong>IUnknown</strong> sobre un objeto COM (DBTYPE_IUNKNOWN).</span><span class="sxs-lookup"><span data-stu-id="604b8-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="604b8-179"><strong>NOTA:</strong>Este tipo de datos actualmente no es compatible con ADO.</span><span class="sxs-lookup"><span data-stu-id="604b8-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="604b8-180">Su uso puede provocar resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="604b8-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-182">205</span><span class="sxs-lookup"><span data-stu-id="604b8-182">205</span></span></p></td>
<td><p><span data-ttu-id="604b8-183">Indica un valor binario largo.</span><span class="sxs-lookup"><span data-stu-id="604b8-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-185">201</span><span class="sxs-lookup"><span data-stu-id="604b8-185">201</span></span></p></td>
<td><p><span data-ttu-id="604b8-186">Indica un valor de cadena largo.</span><span class="sxs-lookup"><span data-stu-id="604b8-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-188">203</span><span class="sxs-lookup"><span data-stu-id="604b8-188">203</span></span></p></td>
<td><p><span data-ttu-id="604b8-189">Indica un valor de cadena Unicode largo terminado en un carácter nulo (null).</span><span class="sxs-lookup"><span data-stu-id="604b8-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-191">131</span><span class="sxs-lookup"><span data-stu-id="604b8-191">131</span></span></p></td>
<td><p><span data-ttu-id="604b8-192">Indica un valor numérico exacto con una precisión y una escala fijas (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="604b8-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-194">138</span><span class="sxs-lookup"><span data-stu-id="604b8-194">138</span></span></p></td>
<td><p><span data-ttu-id="604b8-195">Indica una automatización PROPVARIANT (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="604b8-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-197">4 </span><span class="sxs-lookup"><span data-stu-id="604b8-197">4</span></span></p></td>
<td><p><span data-ttu-id="604b8-198">Indica un valor de punto flotante de precisión simple (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="604b8-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-200">2</span><span class="sxs-lookup"><span data-stu-id="604b8-200">2</span></span></p></td>
<td><p><span data-ttu-id="604b8-201">Indica un entero de dos bytes con signo (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="604b8-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-203">16 </span><span class="sxs-lookup"><span data-stu-id="604b8-203">16</span></span></p></td>
<td><p><span data-ttu-id="604b8-204">Indica un entero de un byte con signo (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="604b8-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-206"> 21</span><span class="sxs-lookup"><span data-stu-id="604b8-206">21</span></span></p></td>
<td><p><span data-ttu-id="604b8-207">Indica un entero de ocho bytes sin signo (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="604b8-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-209">19</span><span class="sxs-lookup"><span data-stu-id="604b8-209">19</span></span></p></td>
<td><p><span data-ttu-id="604b8-210">Indica un entero de cuatro bytes (DBTYPE_UI4) sin signo.</span><span class="sxs-lookup"><span data-stu-id="604b8-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-212">18 </span><span class="sxs-lookup"><span data-stu-id="604b8-212">18</span></span></p></td>
<td><p><span data-ttu-id="604b8-213">Indica un entero de dos bytes sin signo (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="604b8-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-215">17 </span><span class="sxs-lookup"><span data-stu-id="604b8-215">17</span></span></p></td>
<td><p><span data-ttu-id="604b8-216">Indica un entero de un byte sin signo (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="604b8-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-218">132</span><span class="sxs-lookup"><span data-stu-id="604b8-218">132</span></span></p></td>
<td><p><span data-ttu-id="604b8-219">Indica una variable definida por el usuario (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="604b8-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-220"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-221">204</span><span class="sxs-lookup"><span data-stu-id="604b8-221">204</span></span></p></td>
<td><p><span data-ttu-id="604b8-222">Indica un valor binario (sólo objeto <strong>Parameter</strong>).</span><span class="sxs-lookup"><span data-stu-id="604b8-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-223"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-224">200</span><span class="sxs-lookup"><span data-stu-id="604b8-224">200</span></span></p></td>
<td><p><span data-ttu-id="604b8-225">Indica un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="604b8-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-227">12 </span><span class="sxs-lookup"><span data-stu-id="604b8-227">12</span></span></p></td>
<td><p><span data-ttu-id="604b8-228">Indica un <strong>Variant</strong> de automatización (DBTYPE_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="604b8-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="604b8-229"><strong>NOTA:</strong>Este tipo de datos actualmente no es compatible con ADO.</span><span class="sxs-lookup"><span data-stu-id="604b8-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="604b8-230">Su uso puede provocar resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="604b8-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-232">139</span><span class="sxs-lookup"><span data-stu-id="604b8-232">139</span></span></p></td>
<td><p><span data-ttu-id="604b8-233">Indica un valor numérico (sólo objeto <strong>Parameter</strong>).</span><span class="sxs-lookup"><span data-stu-id="604b8-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-235">202</span><span class="sxs-lookup"><span data-stu-id="604b8-235">202</span></span></p></td>
<td><p><span data-ttu-id="604b8-236">Indica una cadena de caracteres Unicode terminada en el carácter nulo (null).</span><span class="sxs-lookup"><span data-stu-id="604b8-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="604b8-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="604b8-238">130</span><span class="sxs-lookup"><span data-stu-id="604b8-238">130</span></span></p></td>
<td><p><span data-ttu-id="604b8-239">Indica una cadena de caracteres Unicode terminada en el carácter nulo (DBTYPE_WSTR).</span><span class="sxs-lookup"><span data-stu-id="604b8-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="604b8-240">Equivalente a ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="604b8-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="604b8-241">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="604b8-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="604b8-242">Constante</span><span class="sxs-lookup"><span data-stu-id="604b8-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="604b8-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="604b8-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="604b8-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="604b8-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="604b8-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="604b8-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="604b8-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="604b8-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="604b8-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="604b8-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="604b8-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="604b8-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="604b8-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="604b8-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="604b8-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="604b8-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="604b8-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="604b8-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="604b8-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="604b8-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="604b8-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="604b8-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="604b8-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="604b8-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="604b8-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="604b8-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="604b8-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="604b8-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="604b8-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="604b8-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="604b8-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="604b8-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="604b8-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="604b8-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="604b8-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="604b8-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="604b8-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="604b8-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="604b8-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="604b8-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="604b8-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="604b8-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="604b8-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

