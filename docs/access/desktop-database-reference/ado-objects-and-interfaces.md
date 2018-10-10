---
title: Objetos de ADO e interfaces
TOCTitle: ADO Objects and Interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ce04896e6ae59af6917497d9e37dc1ae97222eff
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483679"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="59d82-102">Objetos de ADO e interfaces</span><span class="sxs-lookup"><span data-stu-id="59d82-102">ADO Objects and Interfaces</span></span>


<span data-ttu-id="59d82-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="59d82-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="59d82-104">Las relaciones entre estos objetos se representan en el Modelo de objetos de ADO.</span><span class="sxs-lookup"><span data-stu-id="59d82-104">The relationships between these objects are represented in the ADO Object Model.</span></span>

<span data-ttu-id="59d82-p101">Cada objeto puede estar contenido en su colección correspondiente. Por ejemplo, un objeto [Error](error-object-ado.md) puede estar contenido en una colección [Errors](errors-collection-ado.md). Para obtener más información, vea [Colecciones de ADO](ado-collections.md) o el tema de una colección específica.</span><span class="sxs-lookup"><span data-stu-id="59d82-p101">Each object can be contained in its corresponding collection. For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection. For more information, see [ADO Collections](ado-collections.md) or a specific collection topic.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59d82-108"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="59d82-108"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="59d82-109">Construye un objeto <strong>Record</strong> de ADO a partir de un objeto <strong>Row</strong> de OLE DB de una aplicación C/C++.</span><span class="sxs-lookup"><span data-stu-id="59d82-109">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59d82-110"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="59d82-110"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="59d82-111">Construye un objeto <strong>Recordset</strong> de ADO a partir de un objeto <strong>Rowset</strong> de OLE DB de una aplicación C/C++.</span><span class="sxs-lookup"><span data-stu-id="59d82-111">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59d82-112"><a href="error-object-ado.md">Error</a></span><span class="sxs-lookup"><span data-stu-id="59d82-112"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="59d82-113">Contiene detalles sobre errores de acceso a datos relacionados con una operación única que implica al proveedor.</span><span class="sxs-lookup"><span data-stu-id="59d82-113">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59d82-114"><a href="field-object-ado.md">Field</a></span><span class="sxs-lookup"><span data-stu-id="59d82-114"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="59d82-115">Representa una columna de datos con un tipo de datos común.</span><span class="sxs-lookup"><span data-stu-id="59d82-115">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59d82-116"><a href="parameter-object-ado.md">Parámetro</a></span><span class="sxs-lookup"><span data-stu-id="59d82-116"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="59d82-117">Representa un parámetro o un argumento asociado a un objeto <strong>Command</strong> basado en una consulta parametrizada o un procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="59d82-117">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59d82-118"><a href="property-object-ado.md">Propiedad</a></span><span class="sxs-lookup"><span data-stu-id="59d82-118"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="59d82-119">Representa una característica dinámica de un objeto ADO definido por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="59d82-119">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59d82-120"><a href="record-object-ado.md">Record</a></span><span class="sxs-lookup"><span data-stu-id="59d82-120"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="59d82-121">Representa una fila de un <strong>Recordset</strong> o un directorio o un archivo de un sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="59d82-121">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59d82-122"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="59d82-122"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="59d82-p102">Representa el conjunto completo de registros de una tabla base o los resultados de un comando ejecutado. En cualquier momento, el objeto <strong>Recordset</strong> hace referencia sólo a un único registro dentro del conjunto como registro actual.</span><span class="sxs-lookup"><span data-stu-id="59d82-p102">Represents the entire set of records from a base table or the results of an executed command. At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59d82-125"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="59d82-125"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="59d82-126">Representa una secuencia de datos binaria.</span><span class="sxs-lookup"><span data-stu-id="59d82-126">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

