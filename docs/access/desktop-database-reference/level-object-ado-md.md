---
title: Objeto Level (ADO MD)
TOCTitle: Level object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70fb359aa4faa0bcfc99f0b1700b0eb51f665bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290117"
---
# <a name="level-object-ado-md"></a><span data-ttu-id="758d4-102">Objeto Level (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="758d4-102">Level object (ADO MD)</span></span>


<span data-ttu-id="758d4-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="758d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="758d4-104">Contiene un conjunto de miembros que tienen el mismo rango dentro de una jerarquía.</span><span class="sxs-lookup"><span data-stu-id="758d4-104">Contains a set of members, each of which has the same rank within a hierarchy.</span></span>

## <a name="remarks"></a><span data-ttu-id="758d4-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="758d4-105">Remarks</span></span>

<span data-ttu-id="758d4-106">Con las colecciones y las propiedades de un objeto **Level**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="758d4-106">With the collections and properties of a **Level** object, you can do the following:</span></span>

  - <span data-ttu-id="758d4-107">Identificar el **nivel** con las propiedades [Name](name-property-ado-md.md) y [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="758d4-107">Identify the **Level** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="758d4-108">Devolver una cadena para utilizarla al mostrar el **nivel** con la propiedad [Caption](caption-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="758d4-108">Return a string to use when displaying the **Level** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="758d4-109">Devolver una cadena que describa el **nivel** con la propiedad [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="758d4-109">Return a meaningful string that describes the **Level** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="758d4-110">Devolver los objetos [Member](member-object-ado-md.md) que componen el **nivel** con la colección [Members](members-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="758d4-110">Return the [Member](member-object-ado-md.md) objects that make up the **Level** with the [Members](members-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="758d4-111">Devolver el número de niveles de la raíz del **nivel** con la propiedad [Depth](depth-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="758d4-111">Return the number of levels from the root of the **Level** with the [Depth](depth-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="758d4-112">Utilizar la colección [Properties](properties-collection-ado.md) de ADO estándar para obtener información adicional sobre el objeto **Level**.</span><span class="sxs-lookup"><span data-stu-id="758d4-112">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="758d4-p101">La colección **Properties** contiene propiedades proporcionadas por el proveedor. En la tabla siguiente se incluyen las propiedades que pueden estar disponibles. La lista de propiedades reales puede variar en función de la implementación del proveedor. Vea la documentación del proveedor para obtener una lista más completa de las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="758d4-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="758d4-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="758d4-117">Name</span></span></p></th>
<th><p><span data-ttu-id="758d4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="758d4-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="758d4-119">CatalogName</span><span class="sxs-lookup"><span data-stu-id="758d4-119">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="758d4-120">Nombre del catálogo al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="758d4-120">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="758d4-121">CubeName</span><span class="sxs-lookup"><span data-stu-id="758d4-121">CubeName</span></span></p></td>
<td><p><span data-ttu-id="758d4-122">Nombre del cubo.</span><span class="sxs-lookup"><span data-stu-id="758d4-122">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="758d4-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="758d4-123">Description</span></span></p></td>
<td><p><span data-ttu-id="758d4-124">Descripción del nivel.</span><span class="sxs-lookup"><span data-stu-id="758d4-124">A meaningful description of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="758d4-125">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="758d4-125">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="758d4-126">Nombre inequívoco de la <a href="dimension-object-ado-md.md">dimensión</a>.</span><span class="sxs-lookup"><span data-stu-id="758d4-126">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="758d4-127">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="758d4-127">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="758d4-128">Nombre inequívoco de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="758d4-128">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="758d4-129">LevelCaption</span><span class="sxs-lookup"><span data-stu-id="758d4-129">LevelCaption</span></span></p></td>
<td><p><span data-ttu-id="758d4-130">Etiqueta o título asociado al nivel.</span><span class="sxs-lookup"><span data-stu-id="758d4-130">A label or caption associated with the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="758d4-131">LevelCardinality</span><span class="sxs-lookup"><span data-stu-id="758d4-131">LevelCardinality</span></span></p></td>
<td><p><span data-ttu-id="758d4-132">Número de miembros del nivel.</span><span class="sxs-lookup"><span data-stu-id="758d4-132">The number of members in the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="758d4-133">LevelGUID</span><span class="sxs-lookup"><span data-stu-id="758d4-133">LevelGUID</span></span></p></td>
<td><p><span data-ttu-id="758d4-134">GUID del nivel.</span><span class="sxs-lookup"><span data-stu-id="758d4-134">The GUID of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="758d4-135">LevelName</span><span class="sxs-lookup"><span data-stu-id="758d4-135">LevelName</span></span></p></td>
<td><p><span data-ttu-id="758d4-136">Nombre del nivel.</span><span class="sxs-lookup"><span data-stu-id="758d4-136">Name of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="758d4-137">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="758d4-137">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="758d4-138">Distancia entre el nivel y la raíz de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="758d4-138">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="758d4-139">LevelType</span><span class="sxs-lookup"><span data-stu-id="758d4-139">LevelType</span></span></p></td>
<td><p><span data-ttu-id="758d4-140">Tipo de nivel.</span><span class="sxs-lookup"><span data-stu-id="758d4-140">The type of level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="758d4-141">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="758d4-141">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="758d4-142">Nombre inequívoco del nivel.</span><span class="sxs-lookup"><span data-stu-id="758d4-142">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="758d4-143">SchemaName</span><span class="sxs-lookup"><span data-stu-id="758d4-143">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="758d4-144">Nombre del esquema al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="758d4-144">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

