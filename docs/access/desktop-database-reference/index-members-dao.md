---
title: Miembros de índice (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 895f29a5dd3e7ed267b96d6a46dc2c8710b4998e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291799"
---
# <a name="index-members-dao"></a><span data-ttu-id="82f1a-102">Miembros de índice (DAO)</span><span class="sxs-lookup"><span data-stu-id="82f1a-102">Index members (DAO)</span></span>


<span data-ttu-id="82f1a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82f1a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82f1a-p101">El objeto Index especifica el orden de los registros a los que se tiene acceso desde las tablas de la base de datos y si se aceptan o no los registros duplicados, lo que proporciona un acceso a los datos eficaz. Para bases de datos externas, los objetos Index describen los índices establecidos para tablas externas (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82f1a-p101">Index objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data. For external databases, Index objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="methods"></a><span data-ttu-id="82f1a-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="82f1a-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82f1a-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="82f1a-107">Name</span></span></p></th>
<th><p><span data-ttu-id="82f1a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="82f1a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82f1a-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-110">Crea un nuevo objeto <strong><a href="field-object-dao.md">Field</a></strong> (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82f1a-110">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82f1a-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-112">Crea un nuevo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido por el usuario (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82f1a-112">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="82f1a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82f1a-113">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82f1a-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="82f1a-114">Name</span></span></p></th>
<th><p><span data-ttu-id="82f1a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="82f1a-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82f1a-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-p102">Establece o devuelve un valor que indica si un objeto <strong>Index</strong> representa un índice agrupado para una tabla (sólo áreas de trabajo de Microsoft Access). <strong>Boolean</strong> de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="82f1a-p102">Sets or returns a value that indicates whether an <strong>Index</strong> object represents a clustered index for a table (Microsoft Access workspaces only). Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82f1a-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-120">Devuelve un valor que indica el número de valores únicos del objeto <strong><a href="index-object-dao.md">Index</a></strong> que se incluyen en la tabla asociada (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82f1a-120">Returns a value that indicates the number of unique values for the <strong><a href="index-object-dao.md">Index</a></strong> object that are included in the associated table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82f1a-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-122">Devuelve una colección <strong>Fields</strong> que representa a todos los objetos <strong>Field</strong> almacenados para el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="82f1a-122">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="82f1a-123">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="82f1a-123">Read/write.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82f1a-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-125">Devuelve un valor que indica si un objeto <strong><a href="index-object-dao.md">index</a></strong> representa una clave externa en una tabla (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82f1a-125">Returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a foreign key in a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="82f1a-126">.</span><span class="sxs-lookup"><span data-stu-id="82f1a-126"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82f1a-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-128">Establece o devuelve un valor que indica si los registros con valores Null en sus campos de índice tienen entradas de índice (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82f1a-128">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82f1a-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-p105">Devuelve o establece el nombre del objeto especificado. <strong>String</strong> de lectura y escritura si el objeto no se anexó a una colección. <strong>String</strong> de solo lectura si el objeto se anexó a una colección.</span><span class="sxs-lookup"><span data-stu-id="82f1a-p105">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82f1a-133"><strong><a href="index-primary-property-dao.md">Principal</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-134">Establece o devuelve un valor que indica si un objeto <strong><a href="index-object-dao.md">Index</a></strong> representa un índice de clave principal en una tabla (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82f1a-134">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a primary key index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82f1a-135"><strong><a href="index-properties-property-dao.md">Propiedades</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-136">Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="82f1a-136">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="82f1a-137">Sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="82f1a-137">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82f1a-138"><strong><a href="index-required-property-dao.md">Necesarios</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-138"><strong><a href="index-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-139">Establece o devuelve un valor que indica si un objeto <strong><a href="field-object-dao.md">Field</a></strong> requiere un valor no Null.</span><span class="sxs-lookup"><span data-stu-id="82f1a-139">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82f1a-140"><strong><a href="index-unique-property-dao.md">Única</a></strong></span><span class="sxs-lookup"><span data-stu-id="82f1a-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span></span></p></td>
<td><p><span data-ttu-id="82f1a-141">Establece o devuelve un valor que indica si un objeto <strong><a href="index-object-dao.md">Index</a></strong> representa un índice (clave) único para una tabla (únicamente áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82f1a-141">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

