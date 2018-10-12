---
title: FieldAttributeEnum (referencia de escritorio de la base de datos de Access)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 75644308b1af0dd4c6e3b40b2bd6b1c7461f928f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486175"
---
# <a name="fieldattributeenum"></a><span data-ttu-id="36970-102">FieldAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="36970-102">FieldAttributeEnum</span></span>


<span data-ttu-id="36970-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="36970-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="36970-104">Especifica uno o más atributos de un objeto [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="36970-104">Specifies one or more attributes of a [Field](field-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36970-105">Constante</span><span class="sxs-lookup"><span data-stu-id="36970-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="36970-106">Valor</span><span class="sxs-lookup"><span data-stu-id="36970-106">Value</span></span></p></th>
<th><p><span data-ttu-id="36970-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="36970-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36970-108"><strong>adFldCacheDeferred</strong></span><span class="sxs-lookup"><span data-stu-id="36970-108"><strong>adFldCacheDeferred</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="36970-109">0x1000</span></span></p></td>
<td><p><span data-ttu-id="36970-110">Indica que el proveedor almacena los valores de campo en una memoria caché y que las lecturas subsiguientes se realizan desde la caché.</span><span class="sxs-lookup"><span data-stu-id="36970-110">Indicates that the provider caches field values and that subsequent reads are done from the cache.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-111"><strong>adFldFixed</strong></span><span class="sxs-lookup"><span data-stu-id="36970-111"><strong>adFldFixed</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-112">0 x 10</span><span class="sxs-lookup"><span data-stu-id="36970-112">0x10</span></span></p></td>
<td><p><span data-ttu-id="36970-113">Indica que el campo contiene datos de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="36970-113">Indicates that the field contains fixed-length data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-114"><strong>adFldIsChapter</strong></span><span class="sxs-lookup"><span data-stu-id="36970-114"><strong>adFldIsChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-115">0 x 2000</span><span class="sxs-lookup"><span data-stu-id="36970-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="36970-p101">Indica que el campo contiene un valor de capítulo que especifica un conjunto de registros secundario (recordset) específico relacionado con este campo principal. Los campos de capítulo normalmente se utilizan con filtros o mediante la aplicación de forma a los datos.</span><span class="sxs-lookup"><span data-stu-id="36970-p101">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field. Typically chapter fields are used with data shaping or filters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-118"><strong>adFldIsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="36970-118"><strong>adFldIsCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-119">0 x 40000</span><span class="sxs-lookup"><span data-stu-id="36970-119">0x40000</span></span></p></td>
<td><p><span data-ttu-id="36970-120">Indica que el campo especifica que el recurso representado por el registro es una colección de otros recursos, tales como una carpeta, en vez de un recurso simple, tal como un archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="36970-120">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-121"><strong>adFldIsDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="36970-121"><strong>adFldIsDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-122">0 x 20000</span><span class="sxs-lookup"><span data-stu-id="36970-122">0x20000</span></span></p></td>
<td><p><span data-ttu-id="36970-123">Indica que el campo contiene la secuencia predeterminada para el recurso representado por el objeto record.</span><span class="sxs-lookup"><span data-stu-id="36970-123">Indicates that the field contains the default stream for the resource represented by the record.</span></span> <span data-ttu-id="36970-124">Por ejemplo, la secuencia predeterminada puede ser el contenido HTML de una carpeta raíz en un sitio Web, el cual se sirve automáticamente cuando se especifica la dirección URL raíz.</span><span class="sxs-lookup"><span data-stu-id="36970-124">For example, the default stream can be the HTML content of a root folder on a website, which is automatically served when the root URL is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-125"><strong>adFldIsNullable</strong></span><span class="sxs-lookup"><span data-stu-id="36970-125"><strong>adFldIsNullable</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-126">0 x 20</span><span class="sxs-lookup"><span data-stu-id="36970-126">0x20</span></span></p></td>
<td><p><span data-ttu-id="36970-127">Indica que el campo acepta valores nulos (null).</span><span class="sxs-lookup"><span data-stu-id="36970-127">Indicates that the field accepts null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-128"><strong>adFldIsRowURL</strong></span><span class="sxs-lookup"><span data-stu-id="36970-128"><strong>adFldIsRowURL</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-129">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="36970-129">0x10000</span></span></p></td>
<td><p><span data-ttu-id="36970-130">Indica que el campo contiene la dirección URL que nombra el recurso del almacén de datos representado por el registro.</span><span class="sxs-lookup"><span data-stu-id="36970-130">Indicates that the field contains the URL that names the resource from the data store represented by the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-131"><strong>adFldLong</strong></span><span class="sxs-lookup"><span data-stu-id="36970-131"><strong>adFldLong</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-132">0 x 80</span><span class="sxs-lookup"><span data-stu-id="36970-132">0x80</span></span></p></td>
<td><p><span data-ttu-id="36970-p103">Indica que el campo es un campo binario largo. También indica que se pueden utilizar los métodos <a href="appendchunk-method-ado.md">AppendChunk</a> y <a href="getchunk-method-ado.md">GetChunk</a>.</span><span class="sxs-lookup"><span data-stu-id="36970-p103">Indicates that the field is a long binary field. Also indicates that you can use the <a href="appendchunk-method-ado.md">AppendChunk</a> and <a href="getchunk-method-ado.md">GetChunk</a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-135"><strong>adFldMayBeNull</strong></span><span class="sxs-lookup"><span data-stu-id="36970-135"><strong>adFldMayBeNull</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-136">0 x 40</span><span class="sxs-lookup"><span data-stu-id="36970-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="36970-137">Indica que se pueden leer valores nulos del campo.</span><span class="sxs-lookup"><span data-stu-id="36970-137">Indicates that you can read null values from the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-138"><strong>adFldMayDefer</strong></span><span class="sxs-lookup"><span data-stu-id="36970-138"><strong>adFldMayDefer</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-139">0x2</span><span class="sxs-lookup"><span data-stu-id="36970-139">0x2</span></span></p></td>
<td><p><span data-ttu-id="36970-140">Indica que el campo está diferido, es decir, los valores del campo no se recuperan del origen de datos con el registro completo, sino sólo cuando se realiza un acceso explícito a ellos.</span><span class="sxs-lookup"><span data-stu-id="36970-140">Indicates that the field is deferred — that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-141"><strong>adFldNegativeScale</strong></span><span class="sxs-lookup"><span data-stu-id="36970-141"><strong>adFldNegativeScale</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="36970-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="36970-p104">Indica que el campo representa un valor numérico de una columna que admite valores de escala negativa. La escala se especifica mediante la propiedad <a href="numericscale-property-ado.md">NumericScale</a>.</span><span class="sxs-lookup"><span data-stu-id="36970-p104">Indicates that the field represents a numeric value from a column that supports negative scale values. The scale is specified by the <a href="numericscale-property-ado.md">NumericScale</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-145"><strong>adFldRowID</strong></span><span class="sxs-lookup"><span data-stu-id="36970-145"><strong>adFldRowID</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-146">0 x 100</span><span class="sxs-lookup"><span data-stu-id="36970-146">0x100</span></span></p></td>
<td><p><span data-ttu-id="36970-147">Indica que el campo contiene un identificador de fila persistente que no se puede escribir y que no tiene ningún valor significativo excepto el de identificar la fila (como un número de registro, un identificador único, etc.).</span><span class="sxs-lookup"><span data-stu-id="36970-147">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-148"><strong>adFldRowVersion</strong></span><span class="sxs-lookup"><span data-stu-id="36970-148"><strong>adFldRowVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-149">0 x 200</span><span class="sxs-lookup"><span data-stu-id="36970-149">0x200</span></span></p></td>
<td><p><span data-ttu-id="36970-150">Indica que el campo contiene algún tipo de marca de hora o fecha utilizada para hacer un seguimiento de las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="36970-150">Indicates that the field contains some kind of time or date stamp used to track updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-151"><strong>adFldUnknownUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="36970-151"><strong>adFldUnknownUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-152">0 x 8</span><span class="sxs-lookup"><span data-stu-id="36970-152">0x8</span></span></p></td>
<td><p><span data-ttu-id="36970-153">Indica que el proveedor no puede determinar si es posible escribir en el campo.</span><span class="sxs-lookup"><span data-stu-id="36970-153">Indicates that the provider cannot determine if you can write to the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-154"><strong>adFldUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="36970-154"><strong>adFldUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-155">-1</span><span class="sxs-lookup"><span data-stu-id="36970-155">-1</span></span><br />
<span data-ttu-id="36970-156">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="36970-156">0xFFFFFFFF</span></span></p></td>
<td><p><span data-ttu-id="36970-157">Indica que el proveedor no especifica los atributos de campo.</span><span class="sxs-lookup"><span data-stu-id="36970-157">Indicates that the provider does not specify the field attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-158"><strong>adFldUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="36970-158"><strong>adFldUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="36970-159">0 x 4</span><span class="sxs-lookup"><span data-stu-id="36970-159">0x4</span></span></p></td>
<td><p><span data-ttu-id="36970-160">Indica que es posible escribir en el campo.</span><span class="sxs-lookup"><span data-stu-id="36970-160">Indicates that you can write to the field.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="36970-161">**Equivalente ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="36970-161">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="36970-162">Paquete: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="36970-162">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36970-163">Constante</span><span class="sxs-lookup"><span data-stu-id="36970-163">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36970-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="36970-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-165">AdoEnums.FieldAttribute.FIXED</span><span class="sxs-lookup"><span data-stu-id="36970-165">AdoEnums.FieldAttribute.FIXED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-166">AdoEnums.FieldAttribute.ISNULLABLE</span><span class="sxs-lookup"><span data-stu-id="36970-166">AdoEnums.FieldAttribute.ISNULLABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-167">AdoEnums.FieldAttribute.LONG</span><span class="sxs-lookup"><span data-stu-id="36970-167">AdoEnums.FieldAttribute.LONG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-168">AdoEnums.FieldAttribute.MAYBENULL</span><span class="sxs-lookup"><span data-stu-id="36970-168">AdoEnums.FieldAttribute.MAYBENULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-169">AdoEnums.FieldAttribute.MAYDEFER</span><span class="sxs-lookup"><span data-stu-id="36970-169">AdoEnums.FieldAttribute.MAYDEFER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span><span class="sxs-lookup"><span data-stu-id="36970-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-171">AdoEnums.FieldAttribute.ROWID</span><span class="sxs-lookup"><span data-stu-id="36970-171">AdoEnums.FieldAttribute.ROWID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-172">AdoEnums.FieldAttribute.ROWVERSION</span><span class="sxs-lookup"><span data-stu-id="36970-172">AdoEnums.FieldAttribute.ROWVERSION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span><span class="sxs-lookup"><span data-stu-id="36970-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36970-174">AdoEnums.FieldAttribute.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="36970-174">AdoEnums.FieldAttribute.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36970-175">AdoEnums.FieldAttribute.UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="36970-175">AdoEnums.FieldAttribute.UPDATABLE</span></span></p></td>
</tr>
</tbody>
</table>
