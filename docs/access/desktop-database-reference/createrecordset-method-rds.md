---
title: CreateRecordset (método, RDS)
TOCTitle: CreateRecordset Method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d975faf45cf6a16bdae9f800084ebbbbaec3127d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868535"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="e4120-102">CreateRecordset (método, RDS)</span><span class="sxs-lookup"><span data-stu-id="e4120-102">CreateRecordset Method (RDS)</span></span>


<span data-ttu-id="e4120-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4120-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="e4120-104">Crea un objeto [Recordset](recordset-object-ado.md) vacío y desconectado.</span><span class="sxs-lookup"><span data-stu-id="e4120-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4120-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4120-105">Syntax</span></span>

<span data-ttu-id="e4120-106">*objeto*. CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="e4120-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="e4120-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4120-107">Parameters</span></span>

  - <span data-ttu-id="e4120-108">*Object*</span><span class="sxs-lookup"><span data-stu-id="e4120-108">*Object*</span></span>

  - <span data-ttu-id="e4120-109">Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md) o [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="e4120-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="e4120-110">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="e4120-110">*ColumnsInfos*</span></span>

  - <span data-ttu-id="e4120-p101">Matriz de atributos **Variant** que define cada columna del objeto **Recordset** creado. Cada definición de columna contiene una matriz de cuatro atributos necesarios y un atributo opcional. A continuación, el conjunto de matrices de columnas se agrupa en una matriz, que define el **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e4120-p101">A **Variant** array of attributes that defines each column in the **Recordset** created. Each column definition contains an array of four required attributes and one optional attribute. The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="e4120-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="e4120-114">Attribute</span></span></p></th>
    <th><p><span data-ttu-id="e4120-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4120-115">Description</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="e4120-116">Name</span><span class="sxs-lookup"><span data-stu-id="e4120-116">Name</span></span></p></td>
    <td><p><span data-ttu-id="e4120-117">Nombre del encabezado de columna.</span><span class="sxs-lookup"><span data-stu-id="e4120-117">Name of the column header.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="e4120-118">Type</span><span class="sxs-lookup"><span data-stu-id="e4120-118">Type</span></span></p></td>
    <td><p><span data-ttu-id="e4120-119">Entero del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e4120-119">Integer of the data type.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="e4120-120">Size</span><span class="sxs-lookup"><span data-stu-id="e4120-120">Size</span></span></p></td>
    <td><p><span data-ttu-id="e4120-121">Entero del ancho en caracteres, independientemente del tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e4120-121">Integer of the width in characters, regardless of data type.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="e4120-122">Nullability</span><span class="sxs-lookup"><span data-stu-id="e4120-122">Nullability</span></span></p></td>
    <td><p><span data-ttu-id="e4120-123">Valor booleano.</span><span class="sxs-lookup"><span data-stu-id="e4120-123">Boolean value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="e4120-124">Scale</span><span class="sxs-lookup"><span data-stu-id="e4120-124">Scale</span></span><br />
<span data-ttu-id="e4120-125">(Opcional)</span><span class="sxs-lookup"><span data-stu-id="e4120-125">(Optional)</span></span></p></td>
    <td><p><span data-ttu-id="e4120-p102">Este atributo opcional define la escala de los campos numéricos.

Si no se especifica este valor, los valores numéricos se truncarán en una escala de tres.

No se ve afectada la precisión, pero el número de dígitos después del separador decimal se truncará en tres.</span><span class="sxs-lookup"><span data-stu-id="e4120-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="e4120-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4120-129">Remarks</span></span>

<span data-ttu-id="e4120-130">El objeto de negocio de servidor puede rellenar el objeto **Recordset** resultante con los datos de un proveedor de datos que no sea OLE DB, como un archivo de sistema operativo que contiene cotizaciones.</span><span class="sxs-lookup"><span data-stu-id="e4120-130">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="e4120-p103">En la tabla siguiente figuran los valores de [DataTypeEnum](datatypeenum.md) admitidos por el método **CreateRecordset**. El número que aparece es el número de referencia usado para definir los campos.</span><span class="sxs-lookup"><span data-stu-id="e4120-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="e4120-p104">Cada uno de los tipos de datos es de longitud fija o longitud variable.

Los tipos de longitud fija deben definirse con un tamaño de -1, porque el tamaño viene previamente determinado y se sigue requiriendo una definición de tamaño.

Los tipos de datos de longitud variable permiten un tamaño que oscila entre 1 y 32767.</span><span class="sxs-lookup"><span data-stu-id="e4120-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="e4120-p105">Para algunos de los tipos de datos de longitud variable, puede que el tipo se convierta en el tipo que aparece en la columna Sustitución. Las sustituciones no se verán hasta que se cree y se rellene el objeto **Recordset**. Después, se podrá buscar el tipo de datos real, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="e4120-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e4120-139">Longitud</span><span class="sxs-lookup"><span data-stu-id="e4120-139">Length</span></span></p></th>
<th><p><span data-ttu-id="e4120-140">Constante</span><span class="sxs-lookup"><span data-stu-id="e4120-140">Constant</span></span></p></th>
<th><p><span data-ttu-id="e4120-141">Número</span><span class="sxs-lookup"><span data-stu-id="e4120-141">Number</span></span></p></th>
<th><p><span data-ttu-id="e4120-142">Sustitución</span><span class="sxs-lookup"><span data-stu-id="e4120-142">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e4120-143">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-143">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-144"><strong>excepto adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-144"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-145">16</span><span class="sxs-lookup"><span data-stu-id="e4120-145">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-146">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-147"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-147"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-148">2</span><span class="sxs-lookup"><span data-stu-id="e4120-148">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-149">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-150"><strong>son también tipos</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-150"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-151">3</span><span class="sxs-lookup"><span data-stu-id="e4120-151">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-152">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-153"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-153"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-154">20</span><span class="sxs-lookup"><span data-stu-id="e4120-154">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-155">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-156"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-156"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-157">17</span><span class="sxs-lookup"><span data-stu-id="e4120-157">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-158">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-159"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-159"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-160">18</span><span class="sxs-lookup"><span data-stu-id="e4120-160">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-161">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-162"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-162"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-163">19</span><span class="sxs-lookup"><span data-stu-id="e4120-163">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-164">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-165"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-165"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-166">21</span><span class="sxs-lookup"><span data-stu-id="e4120-166">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-167">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-168"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-168"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-169">4</span><span class="sxs-lookup"><span data-stu-id="e4120-169">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-170">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-171"><strong>longitud fija</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-171"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-172">5</span><span class="sxs-lookup"><span data-stu-id="e4120-172">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-173">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-174"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-174"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-175">6</span><span class="sxs-lookup"><span data-stu-id="e4120-175">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-176">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-177"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-177"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-178">14</span><span class="sxs-lookup"><span data-stu-id="e4120-178">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-179">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-180"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-180"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-181">131</span><span class="sxs-lookup"><span data-stu-id="e4120-181">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-182">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-183"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-183"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-184">11</span><span class="sxs-lookup"><span data-stu-id="e4120-184">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-185">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-186"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-186"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-187">10</span><span class="sxs-lookup"><span data-stu-id="e4120-187">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-188">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-189"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-189"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-190">72</span><span class="sxs-lookup"><span data-stu-id="e4120-190">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-191">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-192"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-192"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-193">7</span><span class="sxs-lookup"><span data-stu-id="e4120-193">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-194">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-195"><strong>adDBData</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-195"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-196">133</span><span class="sxs-lookup"><span data-stu-id="e4120-196">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-197">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-198"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-198"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-199">134</span><span class="sxs-lookup"><span data-stu-id="e4120-199">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-200">Fija</span><span class="sxs-lookup"><span data-stu-id="e4120-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="e4120-201"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-201"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-202">135</span><span class="sxs-lookup"><span data-stu-id="e4120-202">135</span></span></p></td>
<td><p><span data-ttu-id="e4120-203">7</span><span class="sxs-lookup"><span data-stu-id="e4120-203">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-204">Variable</span><span class="sxs-lookup"><span data-stu-id="e4120-204">Variable</span></span></p></td>
<td><p><span data-ttu-id="e4120-205"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-205"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-206">8</span><span class="sxs-lookup"><span data-stu-id="e4120-206">8</span></span></p></td>
<td><p><span data-ttu-id="e4120-207">130</span><span class="sxs-lookup"><span data-stu-id="e4120-207">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-208">Variable</span><span class="sxs-lookup"><span data-stu-id="e4120-208">Variable</span></span></p></td>
<td><p><span data-ttu-id="e4120-209"><strong>Cada</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-209"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-210">129</span><span class="sxs-lookup"><span data-stu-id="e4120-210">129</span></span></p></td>
<td><p><span data-ttu-id="e4120-211">200</span><span class="sxs-lookup"><span data-stu-id="e4120-211">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-212">Variable</span><span class="sxs-lookup"><span data-stu-id="e4120-212">Variable</span></span></p></td>
<td><p><span data-ttu-id="e4120-213"><strong>Parámetros</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-213"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-214">200</span><span class="sxs-lookup"><span data-stu-id="e4120-214">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-215">Variable</span><span class="sxs-lookup"><span data-stu-id="e4120-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="e4120-216"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-216"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-217">201</span><span class="sxs-lookup"><span data-stu-id="e4120-217">201</span></span></p></td>
<td><p><span data-ttu-id="e4120-218">200</span><span class="sxs-lookup"><span data-stu-id="e4120-218">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-219">Variable</span><span class="sxs-lookup"><span data-stu-id="e4120-219">Variable</span></span></p></td>
<td><p><span data-ttu-id="e4120-220"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-220"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-221">130</span><span class="sxs-lookup"><span data-stu-id="e4120-221">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-222">Variable</span><span class="sxs-lookup"><span data-stu-id="e4120-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="e4120-223"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-223"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-224">202</span><span class="sxs-lookup"><span data-stu-id="e4120-224">202</span></span></p></td>
<td><p><span data-ttu-id="e4120-225">130</span><span class="sxs-lookup"><span data-stu-id="e4120-225">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-226">Variable</span><span class="sxs-lookup"><span data-stu-id="e4120-226">Variable</span></span></p></td>
<td><p><span data-ttu-id="e4120-227"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-227"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-228">203</span><span class="sxs-lookup"><span data-stu-id="e4120-228">203</span></span></p></td>
<td><p><span data-ttu-id="e4120-229">130</span><span class="sxs-lookup"><span data-stu-id="e4120-229">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-230">Variable</span><span class="sxs-lookup"><span data-stu-id="e4120-230">Variable</span></span></p></td>
<td><p><span data-ttu-id="e4120-231"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-231"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-232">128</span><span class="sxs-lookup"><span data-stu-id="e4120-232">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e4120-233">Variable</span><span class="sxs-lookup"><span data-stu-id="e4120-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="e4120-234"><strong>adVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-234"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-235">204</span><span class="sxs-lookup"><span data-stu-id="e4120-235">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e4120-236">Variable</span><span class="sxs-lookup"><span data-stu-id="e4120-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="e4120-237"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e4120-237"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e4120-238">205</span><span class="sxs-lookup"><span data-stu-id="e4120-238">205</span></span></p></td>
<td><p><span data-ttu-id="e4120-239">204</span><span class="sxs-lookup"><span data-stu-id="e4120-239">204</span></span></p></td>
</tr>
</tbody>
</table>

