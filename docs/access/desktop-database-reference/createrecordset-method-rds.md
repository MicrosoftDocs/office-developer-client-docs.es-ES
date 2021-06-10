---
title: Método CreateRecordset (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3dda0840617c32e9dceea3bd1baa362c5652a373
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295341"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="69142-102">Método CreateRecordset (RDS)</span><span class="sxs-lookup"><span data-stu-id="69142-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="69142-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69142-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69142-104">Crea un objeto [Recordset](recordset-object-ado.md) vacío y desconectado.</span><span class="sxs-lookup"><span data-stu-id="69142-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="69142-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69142-105">Syntax</span></span>

<span data-ttu-id="69142-106">*objeto*. CreateRecordset(*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="69142-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="69142-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69142-107">Parameters</span></span>

|<span data-ttu-id="69142-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="69142-108">Parameter</span></span>|<span data-ttu-id="69142-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="69142-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="69142-110">*Objeto*</span><span class="sxs-lookup"><span data-stu-id="69142-110">*Object*</span></span> |<span data-ttu-id="69142-111">Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) o [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="69142-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="69142-112">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="69142-112">*ColumnsInfos*</span></span> |<span data-ttu-id="69142-113">Matriz de atributos **Variant** que define cada columna del objeto **Recordset** creado.</span><span class="sxs-lookup"><span data-stu-id="69142-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="69142-114">Cada definición de columna contiene una matriz de cuatro atributos necesarios y un atributo opcional.</span><span class="sxs-lookup"><span data-stu-id="69142-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="69142-115">A continuación, el conjunto de matrices de columnas se agrupa en una matriz, que define el **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="69142-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="69142-116">Para obtener una lista de atributos, consulte la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="69142-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="69142-117">Atributos de matriz Variant</span><span class="sxs-lookup"><span data-stu-id="69142-117">Variant array attributes</span></span>

|<span data-ttu-id="69142-118">Atributo</span><span class="sxs-lookup"><span data-stu-id="69142-118">Attribute</span></span>|<span data-ttu-id="69142-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="69142-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="69142-120">Name</span><span class="sxs-lookup"><span data-stu-id="69142-120">Name</span></span> |<span data-ttu-id="69142-121">Nombre del encabezado de columna.</span><span class="sxs-lookup"><span data-stu-id="69142-121">Name of the column header.</span></span>|
|<span data-ttu-id="69142-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="69142-122">Type</span></span> |<span data-ttu-id="69142-123">Entero del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="69142-123">Integer of the data type.</span></span>|
|<span data-ttu-id="69142-124">Size</span><span class="sxs-lookup"><span data-stu-id="69142-124">Size</span></span> |<span data-ttu-id="69142-125">Entero del ancho en caracteres, independientemente del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="69142-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="69142-126">Nullability</span><span class="sxs-lookup"><span data-stu-id="69142-126">Nullability</span></span> |<span data-ttu-id="69142-127">Valor booleano.</span><span class="sxs-lookup"><span data-stu-id="69142-127">Boolean value.</span></span>|
|<span data-ttu-id="69142-128">Escala (opcional)</span><span class="sxs-lookup"><span data-stu-id="69142-128">Scale (optional)</span></span> |<span data-ttu-id="69142-p102">Este atributo opcional define la escala de los campos numéricos.

Si no se especifica este valor, los valores numéricos se truncarán en una escala de tres.

No se ve afectada la precisión, pero el número de dígitos después del separador decimal se truncará en tres.</span><span class="sxs-lookup"><span data-stu-id="69142-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="69142-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69142-132">Remarks</span></span>

<span data-ttu-id="69142-133">El objeto de negocio de servidor puede rellenar el objeto **Recordset** resultante con los datos de un proveedor de datos que no sea OLE DB, como un archivo de sistema operativo que contiene cotizaciones.</span><span class="sxs-lookup"><span data-stu-id="69142-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="69142-p103">En la tabla siguiente figuran los valores de [DataTypeEnum](datatypeenum.md) admitidos por el método **CreateRecordset**. El número que aparece es el número de referencia usado para definir los campos.</span><span class="sxs-lookup"><span data-stu-id="69142-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="69142-p104">Cada uno de los tipos de datos es de longitud fija o longitud variable.

Los tipos de longitud fija deben definirse con un tamaño de -1, porque el tamaño viene previamente determinado y se sigue requiriendo una definición de tamaño.

Los tipos de datos de longitud variable permiten un tamaño que oscila entre 1 y 32767.</span><span class="sxs-lookup"><span data-stu-id="69142-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="69142-p105">Para algunos de los tipos de datos de longitud variable, puede que el tipo se convierta en el tipo que aparece en la columna Sustitución. Las sustituciones no se verán hasta que se cree y se rellene el objeto **Recordset**. Después, se podrá buscar el tipo de datos real, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="69142-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69142-142">Longitud</span><span class="sxs-lookup"><span data-stu-id="69142-142">Length</span></span></p></th>
<th><p><span data-ttu-id="69142-143">Constante</span><span class="sxs-lookup"><span data-stu-id="69142-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="69142-144">Número</span><span class="sxs-lookup"><span data-stu-id="69142-144">Number</span></span></p></th>
<th><p><span data-ttu-id="69142-145">Sustitución</span><span class="sxs-lookup"><span data-stu-id="69142-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69142-146">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-147"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="69142-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-148">16 </span><span class="sxs-lookup"><span data-stu-id="69142-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-149">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-150"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="69142-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-151">2</span><span class="sxs-lookup"><span data-stu-id="69142-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-152">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-153"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="69142-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-154">3</span><span class="sxs-lookup"><span data-stu-id="69142-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-155">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-156"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="69142-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-157">20</span><span class="sxs-lookup"><span data-stu-id="69142-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-158">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-159"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="69142-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-160">17 </span><span class="sxs-lookup"><span data-stu-id="69142-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-162"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="69142-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-163">18 </span><span class="sxs-lookup"><span data-stu-id="69142-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-164">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-165"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="69142-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-166">19</span><span class="sxs-lookup"><span data-stu-id="69142-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-167">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-168"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="69142-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-169"> 21</span><span class="sxs-lookup"><span data-stu-id="69142-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-170">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-171"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="69142-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-172">4 </span><span class="sxs-lookup"><span data-stu-id="69142-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-173">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-174"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="69142-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-175">5 </span><span class="sxs-lookup"><span data-stu-id="69142-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-176">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-177"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="69142-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-178">6 </span><span class="sxs-lookup"><span data-stu-id="69142-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-179">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="69142-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-181">14 </span><span class="sxs-lookup"><span data-stu-id="69142-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-182">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="69142-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-184">131</span><span class="sxs-lookup"><span data-stu-id="69142-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-185">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-186"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="69142-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-187">11</span><span class="sxs-lookup"><span data-stu-id="69142-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-188">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-189"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="69142-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-190">10</span><span class="sxs-lookup"><span data-stu-id="69142-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-191">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-192"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="69142-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-193">72</span><span class="sxs-lookup"><span data-stu-id="69142-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-194">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-195"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="69142-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-196">7 </span><span class="sxs-lookup"><span data-stu-id="69142-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-197">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-198"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="69142-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-199">133</span><span class="sxs-lookup"><span data-stu-id="69142-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-200">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-201"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="69142-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-202">134</span><span class="sxs-lookup"><span data-stu-id="69142-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-203">Decimal</span><span class="sxs-lookup"><span data-stu-id="69142-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="69142-204"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="69142-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-205">135</span><span class="sxs-lookup"><span data-stu-id="69142-205">135</span></span></p></td>
<td><p><span data-ttu-id="69142-206">7 </span><span class="sxs-lookup"><span data-stu-id="69142-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-207">Variable</span><span class="sxs-lookup"><span data-stu-id="69142-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="69142-208"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="69142-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-209">8 </span><span class="sxs-lookup"><span data-stu-id="69142-209">8</span></span></p></td>
<td><p><span data-ttu-id="69142-210">130</span><span class="sxs-lookup"><span data-stu-id="69142-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-211">Variable</span><span class="sxs-lookup"><span data-stu-id="69142-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="69142-212"><strong>adChar</strong></span><span class="sxs-lookup"><span data-stu-id="69142-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-213">129</span><span class="sxs-lookup"><span data-stu-id="69142-213">129</span></span></p></td>
<td><p><span data-ttu-id="69142-214">200</span><span class="sxs-lookup"><span data-stu-id="69142-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-215">Variable</span><span class="sxs-lookup"><span data-stu-id="69142-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="69142-216"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="69142-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-217">200</span><span class="sxs-lookup"><span data-stu-id="69142-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-218">Variable</span><span class="sxs-lookup"><span data-stu-id="69142-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="69142-219"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="69142-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-220">201</span><span class="sxs-lookup"><span data-stu-id="69142-220">201</span></span></p></td>
<td><p><span data-ttu-id="69142-221">200</span><span class="sxs-lookup"><span data-stu-id="69142-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-222">Variable</span><span class="sxs-lookup"><span data-stu-id="69142-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="69142-223"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="69142-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-224">130</span><span class="sxs-lookup"><span data-stu-id="69142-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-225">Variable</span><span class="sxs-lookup"><span data-stu-id="69142-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="69142-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="69142-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-227">202</span><span class="sxs-lookup"><span data-stu-id="69142-227">202</span></span></p></td>
<td><p><span data-ttu-id="69142-228">130</span><span class="sxs-lookup"><span data-stu-id="69142-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-229">Variable</span><span class="sxs-lookup"><span data-stu-id="69142-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="69142-230"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="69142-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-231">203</span><span class="sxs-lookup"><span data-stu-id="69142-231">203</span></span></p></td>
<td><p><span data-ttu-id="69142-232">130</span><span class="sxs-lookup"><span data-stu-id="69142-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-233">Variable</span><span class="sxs-lookup"><span data-stu-id="69142-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="69142-234"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="69142-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-235">128</span><span class="sxs-lookup"><span data-stu-id="69142-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69142-236">Variable</span><span class="sxs-lookup"><span data-stu-id="69142-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="69142-237"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="69142-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-238">204</span><span class="sxs-lookup"><span data-stu-id="69142-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69142-239">Variable</span><span class="sxs-lookup"><span data-stu-id="69142-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="69142-240"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="69142-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="69142-241">205</span><span class="sxs-lookup"><span data-stu-id="69142-241">205</span></span></p></td>
<td><p><span data-ttu-id="69142-242">204</span><span class="sxs-lookup"><span data-stu-id="69142-242">204</span></span></p></td>
</tr>
</tbody>
</table>

