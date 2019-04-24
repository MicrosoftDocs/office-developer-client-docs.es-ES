---
title: FieldAttributeEnum ((referencia de base de datos de escritorio de Access)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 079c79af3d15a6a5864a7db7f8334393258cfd42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292604"
---
# <a name="fieldattributeenum"></a>FieldAttributeEnum

**Se aplica a:** Access 2013, Office 2013

Especifica uno o más atributos de un objeto [Field](field-object-ado.md).

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFldCacheDeferred</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Indica que el proveedor almacena los valores de campo en una memoria caché y que las lecturas subsiguientes se realizan desde la caché.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldFixed</strong></p></td>
<td><p>0x10</p></td>
<td><p>Indica que el campo contiene datos de longitud fija.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsChapter</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Indica que el campo contiene un valor de capítulo que especifica un conjunto de registros secundario (recordset) específico relacionado con este campo principal. Los campos de capítulo normalmente se utilizan con filtros o mediante la aplicación de forma a los datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsCollection</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Indica que el campo especifica que el recurso representado por el registro es una colección de otros recursos, tales como una carpeta, en vez de un recurso simple, tal como un archivo de texto.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsDefaultStream</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Indica que el campo contiene la secuencia predeterminada para el recurso representado por el registro. Por ejemplo, la secuencia predeterminada puede ser el contenido HTML de una carpeta raíz en un sitio web, que se atiende automáticamente cuando se especifica la dirección URL raíz.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsNullable</strong></p></td>
<td><p>0x20</p></td>
<td><p>Indica que el campo acepta valores nulos (null).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsRowURL</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Indica que el campo contiene la dirección URL que nombra el recurso del almacén de datos representado por el registro.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bit adfldlong</strong></p></td>
<td><p>0x80</p></td>
<td><p>Indica que el campo es un campo binario largo. También indica que se pueden utilizar los métodos <a href="appendchunk-method-ado.md">AppendChunk</a> y <a href="getchunk-method-ado.md">GetChunk</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldMayBeNull</strong></p></td>
<td><p>0x40</p></td>
<td><p>Indica que se pueden leer valores nulos del campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldMayDefer</strong></p></td>
<td><p>0x2</p></td>
<td><p>Indica que el campo está diferido, es decir, los valores del campo no se recuperan del origen de datos con el registro completo, sino sólo cuando se realiza un acceso explícito a ellos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldNegativeScale</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Indica que el campo representa un valor numérico de una columna que admite valores de escala negativa. La escala se especifica mediante la propiedad <a href="numericscale-property-ado.md">NumericScale</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldRowID</strong></p></td>
<td><p>0x100</p></td>
<td><p>Indica que el campo contiene un identificador de fila persistente que no se puede escribir y que no tiene ningún valor significativo excepto el de identificar la fila (como un número de registro, un identificador único, etc.).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldRowVersion</strong></p></td>
<td><p>0x200</p></td>
<td><p>Indica que el campo contiene algún tipo de marca de hora o fecha utilizada para hacer un seguimiento de las actualizaciones.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUnknownUpdatable</strong></p></td>
<td><p>0x8</p></td>
<td><p>Indica que el proveedor no puede determinar si es posible escribir en el campo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnspecified</strong></p></td>
<td><p>-1<br />
0xFFFFFFFF</p></td>
<td><p>Indica que el proveedor no especifica los atributos de campo.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUpdatable</strong></p></td>
<td><p>0x4</p></td>
<td><p>Indica que es posible escribir en el campo.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Paquete: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. FieldAttribute. CACHEDEFERRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. FieldAttribute. FIXED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. FieldAttribute. ISNULLABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. FieldAttribute. LONG</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. FieldAttribute. MAYBENULL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. FieldAttribute. MAYDEFER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. FieldAttribute. NEGATIVESCALE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. FieldAttribute. ROWID</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. FieldAttribute. ROWVERSION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. FieldAttribute. UNKNOWNUPDATABLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. FieldAttribute. no especificado</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. FieldAttribute. UPDATABLE</p></td>
</tr>
</tbody>
</table>

