---
title: DataTypeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7d1cbc0964c4e980c1dd5216431c5efd0c467dc4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878265"
---
# <a name="datatypeenum"></a><span data-ttu-id="dbf16-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="dbf16-102">DataTypeEnum</span></span>

<span data-ttu-id="dbf16-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dbf16-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dbf16-p101">Especifica el tipo de datos de un objeto [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) o [Property](property-object-ado.md). El indicador correspondiente de tipo OLE DB se muestra entre paréntesis en la columna Descripción de la tabla siguiente. Para obtener más información acerca de los tipos de datos OLE DB, vea el Capítulo 13 y el Apéndice A de la *Referencia del programador de OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="dbf16-p101">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md). The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table. For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dbf16-107">Constante</span><span class="sxs-lookup"><span data-stu-id="dbf16-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="dbf16-108">Valor</span><span class="sxs-lookup"><span data-stu-id="dbf16-108">Value</span></span></p></th>
<th><p><span data-ttu-id="dbf16-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbf16-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="dbf16-110"><strong>AdArray</span></span><br /><span data-ttu-id="dbf16-111">
</strong>(No se aplica a ADOX)</span><span class="sxs-lookup"><span data-stu-id="dbf16-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="dbf16-112">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="dbf16-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="dbf16-113">Un valor de marca, siempre combinado con otra constante de tipo de datos, que indica una matriz de ese otro tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="dbf16-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-115">20</span><span class="sxs-lookup"><span data-stu-id="dbf16-115">20</span></span></p></td>
<td><p><span data-ttu-id="dbf16-116">Indica un entero de ocho bytes con signo (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="dbf16-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-118">128</span><span class="sxs-lookup"><span data-stu-id="dbf16-118">128</span></span></p></td>
<td><p><span data-ttu-id="dbf16-119">Indica un valor binario (DBTYPE_BYTES).</span><span class="sxs-lookup"><span data-stu-id="dbf16-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-121">11</span><span class="sxs-lookup"><span data-stu-id="dbf16-121">11</span></span></p></td>
<td><p><span data-ttu-id="dbf16-122">Indica un valor de tipo booleano (DBTYPE_BOOL).</span><span class="sxs-lookup"><span data-stu-id="dbf16-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-124">8</span><span class="sxs-lookup"><span data-stu-id="dbf16-124">8</span></span></p></td>
<td><p><span data-ttu-id="dbf16-125">Indica una cadena de caracteres terminada en el carácter nulo (Unicode) (DBTYPE_BSTR).</span><span class="sxs-lookup"><span data-stu-id="dbf16-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-126"><strong>Dbtype_hchapter</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-127">136</span><span class="sxs-lookup"><span data-stu-id="dbf16-127">136</span></span></p></td>
<td><p><span data-ttu-id="dbf16-128">Indica un valor de capítulo de cuatro bytes que identifica las filas de un conjunto de filas secundario (DBTYPE_HCHAPTER).</span><span class="sxs-lookup"><span data-stu-id="dbf16-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-129"><strong>Cada</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-130">129</span><span class="sxs-lookup"><span data-stu-id="dbf16-130">129</span></span></p></td>
<td><p><span data-ttu-id="dbf16-131">Indica un valor de cadena (DBTYPE_STR).</span><span class="sxs-lookup"><span data-stu-id="dbf16-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-133">6</span><span class="sxs-lookup"><span data-stu-id="dbf16-133">6</span></span></p></td>
<td><p><span data-ttu-id="dbf16-p102">Indica un valor de moneda (DBTYPE_CY). Este valor es un número de punto fijo con cuatro dígitos a la derecha del separador decimal. Se almacena en un entero de ocho bytes con signo y con un factor de escala de 10.000.</span><span class="sxs-lookup"><span data-stu-id="dbf16-p102">Indicates a currency value (DBTYPE_CY). Currency is a fixed-point number with four digits to the right of the decimal point. It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-138">7</span><span class="sxs-lookup"><span data-stu-id="dbf16-138">7</span></span></p></td>
<td><p><span data-ttu-id="dbf16-p103">Indica un valor de fecha (DBTYPE_DATE). Una fecha se almacena en un tipo double (real de doble precisión), en el que la parte entera es el número de días transcurridos desde el 30 de diciembre de 1899 y la parte fraccionaria es la fracción de un día.</span><span class="sxs-lookup"><span data-stu-id="dbf16-p103">Indicates a date value (DBTYPE_DATE). A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-141"><strong>adDBData</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-142">133</span><span class="sxs-lookup"><span data-stu-id="dbf16-142">133</span></span></p></td>
<td><p><span data-ttu-id="dbf16-143">Indica un valor de fecha (aaaammdd) (DBTYPE_DBDATE).</span><span class="sxs-lookup"><span data-stu-id="dbf16-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-145">134</span><span class="sxs-lookup"><span data-stu-id="dbf16-145">134</span></span></p></td>
<td><p><span data-ttu-id="dbf16-146">Indica un valor de hora (hhmmss) (DBTYPE_DBTIME).</span><span class="sxs-lookup"><span data-stu-id="dbf16-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-148">135</span><span class="sxs-lookup"><span data-stu-id="dbf16-148">135</span></span></p></td>
<td><p><span data-ttu-id="dbf16-149">Indica una marca de tiempo de fecha y hora (aaaammddhhmmss más una fracción en milmillonésimas) (DBTYPE_DBTIMESTAMP).</span><span class="sxs-lookup"><span data-stu-id="dbf16-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-151">14</span><span class="sxs-lookup"><span data-stu-id="dbf16-151">14</span></span></p></td>
<td><p><span data-ttu-id="dbf16-152">Indica un valor numérico exacto con una precisión y una escala fijas (DBTYPE_DECIMAL).</span><span class="sxs-lookup"><span data-stu-id="dbf16-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-153"><strong>longitud fija</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-154">5</span><span class="sxs-lookup"><span data-stu-id="dbf16-154">5</span></span></p></td>
<td><p><span data-ttu-id="dbf16-155">Indica un valor de punto flotante de doble precisión (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="dbf16-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-157">0</span><span class="sxs-lookup"><span data-stu-id="dbf16-157">0</span></span></p></td>
<td><p><span data-ttu-id="dbf16-158">No especifica ningún valor (DBTYPE_EMPTY).</span><span class="sxs-lookup"><span data-stu-id="dbf16-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-160">10</span><span class="sxs-lookup"><span data-stu-id="dbf16-160">10</span></span></p></td>
<td><p><span data-ttu-id="dbf16-161">Indica un código de error de 32 bits (DBTYPE_ERROR).</span><span class="sxs-lookup"><span data-stu-id="dbf16-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-163">64</span><span class="sxs-lookup"><span data-stu-id="dbf16-163">64</span></span></p></td>
<td><p><span data-ttu-id="dbf16-164">Indica un valor de 64 bits que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (DBTYPE_FILETIME).</span><span class="sxs-lookup"><span data-stu-id="dbf16-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-166">72</span><span class="sxs-lookup"><span data-stu-id="dbf16-166">72</span></span></p></td>
<td><p><span data-ttu-id="dbf16-167">Indica un identificador globalmente único (GUID) (DBTYPE_GUID).</span><span class="sxs-lookup"><span data-stu-id="dbf16-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-169">9</span><span class="sxs-lookup"><span data-stu-id="dbf16-169">9</span></span></p></td>
<td><p><span data-ttu-id="dbf16-170">Indica un puntero a una interfaz <strong>IDispatch</strong> sobre un objeto COM (DBTYPE_IDISPATCH).
</span><span class="sxs-lookup"><span data-stu-id="dbf16-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="dbf16-171"><strong>Nota</strong>: este tipo de datos no se admite actualmente por ADO.</span><span class="sxs-lookup"><span data-stu-id="dbf16-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="dbf16-172">Su uso puede provocar resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="dbf16-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-173"><strong>son también tipos</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-174">3</span><span class="sxs-lookup"><span data-stu-id="dbf16-174">3</span></span></p></td>
<td><p><span data-ttu-id="dbf16-175">Indica un entero de cuatro bytes con signo (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="dbf16-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-177">13</span><span class="sxs-lookup"><span data-stu-id="dbf16-177">13</span></span></p></td>
<td><p><span data-ttu-id="dbf16-178">Indica un puntero a una interfaz <strong>IUnknown</strong> sobre un objeto COM (DBTYPE_IUNKNOWN).
</span><span class="sxs-lookup"><span data-stu-id="dbf16-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="dbf16-179"><strong>Nota</strong>: este tipo de datos no se admite actualmente por ADO.</span><span class="sxs-lookup"><span data-stu-id="dbf16-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="dbf16-180">Su uso puede provocar resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="dbf16-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-182">205</span><span class="sxs-lookup"><span data-stu-id="dbf16-182">205</span></span></p></td>
<td><p><span data-ttu-id="dbf16-183">Indica un valor binario largo.</span><span class="sxs-lookup"><span data-stu-id="dbf16-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-185">201</span><span class="sxs-lookup"><span data-stu-id="dbf16-185">201</span></span></p></td>
<td><p><span data-ttu-id="dbf16-186">Indica un valor de cadena largo.</span><span class="sxs-lookup"><span data-stu-id="dbf16-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-188">203</span><span class="sxs-lookup"><span data-stu-id="dbf16-188">203</span></span></p></td>
<td><p><span data-ttu-id="dbf16-189">Indica un valor de cadena Unicode largo terminado en un carácter nulo (null).</span><span class="sxs-lookup"><span data-stu-id="dbf16-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-191">131</span><span class="sxs-lookup"><span data-stu-id="dbf16-191">131</span></span></p></td>
<td><p><span data-ttu-id="dbf16-192">Indica un valor numérico exacto con una precisión y una escala fijas (DBTYPE_NUMERIC).</span><span class="sxs-lookup"><span data-stu-id="dbf16-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-194">138</span><span class="sxs-lookup"><span data-stu-id="dbf16-194">138</span></span></p></td>
<td><p><span data-ttu-id="dbf16-195">Indica una automatización PROPVARIANT (DBTYPE_PROP_VARIANT).</span><span class="sxs-lookup"><span data-stu-id="dbf16-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-197">4</span><span class="sxs-lookup"><span data-stu-id="dbf16-197">4</span></span></p></td>
<td><p><span data-ttu-id="dbf16-198">Indica un valor de punto flotante de precisión simple (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="dbf16-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-200">2</span><span class="sxs-lookup"><span data-stu-id="dbf16-200">2</span></span></p></td>
<td><p><span data-ttu-id="dbf16-201">Indica un entero de dos bytes con signo (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="dbf16-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-202"><strong>excepto adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-203">16</span><span class="sxs-lookup"><span data-stu-id="dbf16-203">16</span></span></p></td>
<td><p><span data-ttu-id="dbf16-204">Indica un entero de un byte con signo (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="dbf16-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-206">21</span><span class="sxs-lookup"><span data-stu-id="dbf16-206">21</span></span></p></td>
<td><p><span data-ttu-id="dbf16-207">Indica un entero de ocho bytes sin signo (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="dbf16-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-209">19</span><span class="sxs-lookup"><span data-stu-id="dbf16-209">19</span></span></p></td>
<td><p><span data-ttu-id="dbf16-210">Indica un entero de cuatro bytes (DBTYPE_UI4) sin signo.</span><span class="sxs-lookup"><span data-stu-id="dbf16-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-212">18</span><span class="sxs-lookup"><span data-stu-id="dbf16-212">18</span></span></p></td>
<td><p><span data-ttu-id="dbf16-213">Indica un entero de dos bytes sin signo (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="dbf16-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-215">17</span><span class="sxs-lookup"><span data-stu-id="dbf16-215">17</span></span></p></td>
<td><p><span data-ttu-id="dbf16-216">Indica un entero de un byte sin signo (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="dbf16-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-218">132</span><span class="sxs-lookup"><span data-stu-id="dbf16-218">132</span></span></p></td>
<td><p><span data-ttu-id="dbf16-219">Indica una variable definida por el usuario (DBTYPE_UDT).</span><span class="sxs-lookup"><span data-stu-id="dbf16-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-220"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-221">204</span><span class="sxs-lookup"><span data-stu-id="dbf16-221">204</span></span></p></td>
<td><p><span data-ttu-id="dbf16-222">Indica un valor binario (sólo objeto <strong>Parameter</strong>).</span><span class="sxs-lookup"><span data-stu-id="dbf16-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-223"><strong>Parámetros</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-224">200</span><span class="sxs-lookup"><span data-stu-id="dbf16-224">200</span></span></p></td>
<td><p><span data-ttu-id="dbf16-225">Indica un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="dbf16-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-227">12</span><span class="sxs-lookup"><span data-stu-id="dbf16-227">12</span></span></p></td>
<td><p><span data-ttu-id="dbf16-228">Indica un <strong>Variant</strong> de automatización (DBTYPE_VARIANT).
</span><span class="sxs-lookup"><span data-stu-id="dbf16-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="dbf16-229"><strong>Nota</strong>: este tipo de datos no se admite actualmente por ADO.</span><span class="sxs-lookup"><span data-stu-id="dbf16-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="dbf16-230">Su uso puede provocar resultados impredecibles.</span><span class="sxs-lookup"><span data-stu-id="dbf16-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-232">139</span><span class="sxs-lookup"><span data-stu-id="dbf16-232">139</span></span></p></td>
<td><p><span data-ttu-id="dbf16-233">Indica un valor numérico (sólo objeto <strong>Parameter</strong>).</span><span class="sxs-lookup"><span data-stu-id="dbf16-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-235">202</span><span class="sxs-lookup"><span data-stu-id="dbf16-235">202</span></span></p></td>
<td><p><span data-ttu-id="dbf16-236">Indica una cadena de caracteres Unicode terminada en el carácter nulo (null).</span><span class="sxs-lookup"><span data-stu-id="dbf16-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="dbf16-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="dbf16-238">130</span><span class="sxs-lookup"><span data-stu-id="dbf16-238">130</span></span></p></td>
<td><p><span data-ttu-id="dbf16-239">Indica una cadena de caracteres Unicode terminada en el carácter nulo (DBTYPE_WSTR).</span><span class="sxs-lookup"><span data-stu-id="dbf16-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="dbf16-240">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="dbf16-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="dbf16-241">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="dbf16-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dbf16-242">Constante</span><span class="sxs-lookup"><span data-stu-id="dbf16-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="dbf16-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="dbf16-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="dbf16-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="dbf16-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="dbf16-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="dbf16-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="dbf16-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="dbf16-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="dbf16-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="dbf16-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="dbf16-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="dbf16-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="dbf16-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="dbf16-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="dbf16-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="dbf16-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="dbf16-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="dbf16-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="dbf16-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="dbf16-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="dbf16-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="dbf16-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="dbf16-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="dbf16-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="dbf16-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="dbf16-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="dbf16-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="dbf16-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="dbf16-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="dbf16-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="dbf16-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="dbf16-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="dbf16-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="dbf16-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="dbf16-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="dbf16-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="dbf16-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="dbf16-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbf16-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="dbf16-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbf16-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="dbf16-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

