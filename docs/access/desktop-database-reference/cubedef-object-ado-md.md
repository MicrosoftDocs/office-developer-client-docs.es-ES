---
title: CubeDef (objeto, ADO MD)
TOCTitle: CubeDef object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f48b3ea16e45b3bde12ed9f8584c3218f955eba
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922394"
---
# <a name="cubedef-object-ado-md"></a><span data-ttu-id="0c77c-102">CubeDef (objeto, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="0c77c-102">CubeDef object (ADO MD)</span></span>


<span data-ttu-id="0c77c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c77c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c77c-104">Representa un cubo de un esquema multidimensional, que contiene un conjunto de dimensiones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0c77c-104">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c77c-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0c77c-105">Remarks</span></span>

<span data-ttu-id="0c77c-106">Con las colecciones y las propiedades de un objeto **CubeDef**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0c77c-106">With the collections and properties of a **CubeDef** object, you can do the following:</span></span>

  - <span data-ttu-id="0c77c-107">Identificar el objeto **CubeDef** con la propiedad [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="0c77c-107">Identify a **CubeDef** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="0c77c-108">Devolver una cadena que describa el cubo con la propiedad [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="0c77c-108">Return a string that describes the cube with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="0c77c-109">Devolver las dimensiones que conforman el cubo con la colección [Dimensions](dimensions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="0c77c-109">Return the dimensions that make up the cube with the [Dimensions](dimensions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="0c77c-110">Obtener información adicional sobre el objeto **CubeDef** con la colección [Properties](properties-collection-ado.md) de ADO estándar.</span><span class="sxs-lookup"><span data-stu-id="0c77c-110">Obtain additional information about the **CubeDef** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="0c77c-p101">La colección **Properties** contiene propiedades proporcionadas por el proveedor. En la tabla siguiente se incluyen las propiedades que pueden estar disponibles. La lista de propiedades reales puede variar en función de la implementación del proveedor. Vea la documentación del proveedor para obtener una lista más completa de las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="0c77c-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0c77c-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="0c77c-115">Name</span></span></p></th>
<th><p><span data-ttu-id="0c77c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c77c-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c77c-117">NombreCatálogo</span><span class="sxs-lookup"><span data-stu-id="0c77c-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="0c77c-118">Nombre del catálogo al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="0c77c-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c77c-119">CreatedOn</span><span class="sxs-lookup"><span data-stu-id="0c77c-119">CreatedOn</span></span></p></td>
<td><p><span data-ttu-id="0c77c-120">Fecha y hora de creación del cubo.</span><span class="sxs-lookup"><span data-stu-id="0c77c-120">Date and time of cube creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c77c-121">CubeGUID</span><span class="sxs-lookup"><span data-stu-id="0c77c-121">CubeGUID</span></span></p></td>
<td><p><span data-ttu-id="0c77c-122">GUID del cubo.</span><span class="sxs-lookup"><span data-stu-id="0c77c-122">Cube GUID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c77c-123">Nombre de cubo</span><span class="sxs-lookup"><span data-stu-id="0c77c-123">CubeName</span></span></p></td>
<td><p><span data-ttu-id="0c77c-124">Nombre del cubo.</span><span class="sxs-lookup"><span data-stu-id="0c77c-124">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c77c-125">CubeType</span><span class="sxs-lookup"><span data-stu-id="0c77c-125">CubeType</span></span></p></td>
<td><p><span data-ttu-id="0c77c-126">Tipo del cubo.</span><span class="sxs-lookup"><span data-stu-id="0c77c-126">The type of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c77c-127">DataUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="0c77c-127">DataUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="0c77c-128">Id. de usuario de la persona que actualizó por última vez los datos.</span><span class="sxs-lookup"><span data-stu-id="0c77c-128">User ID of the person doing the last data update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c77c-129">Description</span><span class="sxs-lookup"><span data-stu-id="0c77c-129">Description</span></span></p></td>
<td><p><span data-ttu-id="0c77c-130">Descripción del cubo.</span><span class="sxs-lookup"><span data-stu-id="0c77c-130">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c77c-131">LastSchemaUpdate</span><span class="sxs-lookup"><span data-stu-id="0c77c-131">LastSchemaUpdate</span></span></p></td>
<td><p><span data-ttu-id="0c77c-132">Fecha y hora de la última actualización del esquema.</span><span class="sxs-lookup"><span data-stu-id="0c77c-132">Date and time of last schema update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c77c-133">SchemaName</span><span class="sxs-lookup"><span data-stu-id="0c77c-133">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="0c77c-134">Nombre del esquema al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="0c77c-134">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c77c-135">SchemaUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="0c77c-135">SchemaUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="0c77c-136">Id. de usuario de la persona que actualizó por última vez el esquema.</span><span class="sxs-lookup"><span data-stu-id="0c77c-136">User ID of the person doing the last schema update.</span></span></p></td>
</tr>
</tbody>
</table>

