---
title: Interfaces y objetos de ADO
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 539feb1918877189548d0e7cff6ceb28e50abddc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718864"
---
# <a name="ado-objects-and-interfaces"></a><span data-ttu-id="ba5cb-102">Interfaces y objetos de ADO</span><span class="sxs-lookup"><span data-stu-id="ba5cb-102">ADO objects and interfaces</span></span>

<span data-ttu-id="ba5cb-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba5cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba5cb-104">Las relaciones entre estos objetos se representan en el modelo de objetos de ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="ba5cb-104">The relationships between these objects are represented in the ActiveX Data Objects (ADO) Object Model.</span></span>

<span data-ttu-id="ba5cb-105">Cada objeto puede estar contenido en su colección correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-105">Each object can be contained in its corresponding collection.</span></span> <span data-ttu-id="ba5cb-106">Por ejemplo, un objeto [Error](error-object-ado.md) puede estar contenido en una colección [Errors](errors-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ba5cb-106">For example, an [Error](error-object-ado.md) object can be contained in an [Errors](errors-collection-ado.md) collection.</span></span> <span data-ttu-id="ba5cb-107">Para obtener más información, vea [colecciones de ADO](ado-collections.md) o el tema de una colección específica.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-107">For more information, see [ADO collections](ado-collections.md) or a specific collection topic.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="ba5cb-108">Objeto</span><span class="sxs-lookup"><span data-stu-id="ba5cb-108">Object</span></span></th>
<th><span data-ttu-id="ba5cb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba5cb-109">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba5cb-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span><span class="sxs-lookup"><span data-stu-id="ba5cb-110"><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="ba5cb-111">Construye un objeto <strong>Record</strong> de ADO a partir de un objeto <strong>Row</strong> de OLE DB de una aplicación C/C++.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-111">Constructs an ADO <strong>Record</strong> object from an OLE DB <strong>Row</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba5cb-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span><span class="sxs-lookup"><span data-stu-id="ba5cb-112"><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></span></span></p></td>
<td><p><span data-ttu-id="ba5cb-113">Construye un objeto <strong>Recordset</strong> de ADO a partir de un objeto <strong>Rowset</strong> de OLE DB de una aplicación C/C++.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-113">Constructs an ADO <strong>Recordset</strong> object from an OLE DB <strong>Rowset</strong> object in a C/C++ application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba5cb-114"><a href="error-object-ado.md">Command</a></span><span class="sxs-lookup"><span data-stu-id="ba5cb-114"><a href="error-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="ba5cb-115">Define un comando específico que se intenta ejecutar con respecto a un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-115">Defines a specific command that you intend to execute against a data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba5cb-116"><a href="field-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="ba5cb-116"><a href="field-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="ba5cb-117">Representa una conexión abierta con un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-117">Represents an open connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba5cb-118"><a href="error-object-ado.md">Error</a></span><span class="sxs-lookup"><span data-stu-id="ba5cb-118"><a href="error-object-ado.md">Error</a></span></span></p></td>
<td><p><span data-ttu-id="ba5cb-119">Contiene detalles sobre errores de acceso a datos relacionados con una operación única que implica al proveedor.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-119">Contains details about data access errors that pertain to a single operation involving the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba5cb-120"><a href="field-object-ado.md">Field</a></span><span class="sxs-lookup"><span data-stu-id="ba5cb-120"><a href="field-object-ado.md">Field</a></span></span></p></td>
<td><p><span data-ttu-id="ba5cb-121">Representa una columna de datos con un tipo de datos común.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-121">Represents a column of data with a common data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba5cb-122"><a href="parameter-object-ado.md">Parámetro</a></span><span class="sxs-lookup"><span data-stu-id="ba5cb-122"><a href="parameter-object-ado.md">Parameter</a></span></span></p></td>
<td><p><span data-ttu-id="ba5cb-123">Representa un parámetro o un argumento asociado a un objeto <strong>Command</strong> basado en una consulta parametrizada o un procedimiento almacenado.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-123">Represents a parameter or argument associated with a <strong>Command</strong> object based on a parameterized query or stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba5cb-124"><a href="property-object-ado.md">Propiedad</a></span><span class="sxs-lookup"><span data-stu-id="ba5cb-124"><a href="property-object-ado.md">Property</a></span></span></p></td>
<td><p><span data-ttu-id="ba5cb-125">Representa una característica dinámica de un objeto ADO definido por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-125">Represents a dynamic characteristic of an ADO object that is defined by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba5cb-126"><a href="record-object-ado.md">Registro</a></span><span class="sxs-lookup"><span data-stu-id="ba5cb-126"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="ba5cb-127">Representa una fila de un <strong>Recordset</strong> o un directorio o un archivo de un sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-127">Represents a row of a <strong>Recordset</strong>, or a directory or file in a file system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba5cb-128"><a href="recordset-object-ado.md">Recordset</a></span><span class="sxs-lookup"><span data-stu-id="ba5cb-128"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="ba5cb-p102">Representa el conjunto completo de registros de una tabla base o los resultados de un comando ejecutado. En cualquier momento, el objeto <strong>Recordset</strong> hace referencia sólo a un único registro dentro del conjunto como registro actual.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-p102">Represents the entire set of records from a base table or the results of an executed command. At any time, the <strong>Recordset</strong> object refers to only a single record within the set as the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba5cb-131"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="ba5cb-131"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="ba5cb-132">Representa una secuencia de datos binaria.</span><span class="sxs-lookup"><span data-stu-id="ba5cb-132">Represents a binary stream of data.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

