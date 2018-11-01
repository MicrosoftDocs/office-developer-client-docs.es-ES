---
title: Objetos de ADO e interfaces
TOCTitle: ADO Objects and Interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: efab7ce2980393282ee1f96295206e712fcbd15f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882185"
---
# <a name="ado-objects-and-interfaces"></a>Objetos de ADO e interfaces


**Se aplica a**: Access 2013, Office 2013

Las relaciones entre estos objetos se representan en el Modelo de objetos de ADO.

Cada objeto puede estar contenido en su colección correspondiente. Por ejemplo, un objeto [Error](error-object-ado.md) puede estar contenido en una colección [Errors](errors-collection-ado.md). Para obtener más información, vea [Colecciones de ADO](ado-collections.md) o el tema de una colección específica.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></p></td>
<td><p>Construye un objeto <strong>Record</strong> de ADO a partir de un objeto <strong>Row</strong> de OLE DB de una aplicación C/C++.</p></td>
</tr>
<tr class="even">
<td><p><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></p></td>
<td><p>Construye un objeto <strong>Recordset</strong> de ADO a partir de un objeto <strong>Rowset</strong> de OLE DB de una aplicación C/C++.</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Error</a></p></td>
<td><p>Contiene detalles sobre errores de acceso a datos relacionados con una operación única que implica al proveedor.</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Field</a></p></td>
<td><p>Representa una columna de datos con un tipo de datos común.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameter-object-ado.md">Parámetro</a></p></td>
<td><p>Representa un parámetro o un argumento asociado a un objeto <strong>Command</strong> basado en una consulta parametrizada o un procedimiento almacenado.</p></td>
</tr>
<tr class="even">
<td><p><a href="property-object-ado.md">Propiedad</a></p></td>
<td><p>Representa una característica dinámica de un objeto ADO definido por el proveedor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="record-object-ado.md">Record</a></p></td>
<td><p>Representa una fila de un <strong>Recordset</strong> o un directorio o un archivo de un sistema de archivos.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordset-object-ado.md">Recordset</a></p></td>
<td><p>Representa el conjunto completo de registros de una tabla base o los resultados de un comando ejecutado. En cualquier momento, el objeto <strong>Recordset</strong> hace referencia sólo a un único registro dentro del conjunto como registro actual.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stream-object-ado.md">Stream</a></p></td>
<td><p>Representa una secuencia de datos binaria.</p></td>
</tr>
</tbody>
</table>

