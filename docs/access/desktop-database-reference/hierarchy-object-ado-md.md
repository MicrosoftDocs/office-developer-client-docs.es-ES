---
title: Objeto Hierarchy (ADO MD)
TOCTitle: Hierarchy object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6668dfd40f7d0d26bcfa2ca4149acdc713e14c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291932"
---
# <a name="hierarchy-object-ado-md"></a><span data-ttu-id="b7e71-102">Objeto Hierarchy (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="b7e71-102">Hierarchy object (ADO MD)</span></span>


<span data-ttu-id="b7e71-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7e71-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7e71-p101">Representa una forma de agregar o "acumular" los miembros de una [dimensión](dimension-object-ado-md.md). Una dimensión se puede agregar a una o varias jerarquías.</span><span class="sxs-lookup"><span data-stu-id="b7e71-p101">Represents one way in which the members of a [dimension](dimension-object-ado-md.md) can be aggregated or "rolled up." A dimension can be aggregated along one or more hierarchies.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e71-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b7e71-106">Remarks</span></span>

<span data-ttu-id="b7e71-107">Con las colecciones y las propiedades de un objeto **Hierarchy**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b7e71-107">With the collections and properties of a **Hierarchy** object, you can do the following:</span></span>

  - <span data-ttu-id="b7e71-108">Identificar la **jerarquía** con las propiedades [Name](name-property-ado-md.md) y [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="b7e71-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="b7e71-109">Devolver una cadena que describa la **jerarquía** con la propiedad [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="b7e71-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="b7e71-110">Devolver los objetos [Level](level-object-ado-md.md) que componen la **jerarquía** con la colección [Levels](levels-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="b7e71-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="b7e71-111">Utilizar la colección [Properties](properties-collection-ado.md) de ADO estándar para obtener información adicional sobre el objeto **Hierarchy**.</span><span class="sxs-lookup"><span data-stu-id="b7e71-111">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Hierarchy** object.</span></span>

<span data-ttu-id="b7e71-p102">La colección **Properties** contiene propiedades proporcionadas por el proveedor. En la tabla siguiente se incluyen las propiedades que pueden estar disponibles. La lista de propiedades reales puede variar en función de la implementación del proveedor. Vea la documentación del proveedor para obtener una lista más completa de las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="b7e71-p102">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7e71-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="b7e71-116">Name</span></span></p></th>
<th><p><span data-ttu-id="b7e71-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7e71-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7e71-118">AllMember</span><span class="sxs-lookup"><span data-stu-id="b7e71-118">AllMember</span></span></p></td>
<td><p><span data-ttu-id="b7e71-119">Miembro del nivel superior de resumen de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="b7e71-119">The member at the highest level of rollup in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e71-120">CatalogName</span><span class="sxs-lookup"><span data-stu-id="b7e71-120">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="b7e71-121">Nombre del catálogo al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="b7e71-121">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e71-122">CubeName</span><span class="sxs-lookup"><span data-stu-id="b7e71-122">CubeName</span></span></p></td>
<td><p><span data-ttu-id="b7e71-123">Nombre del cubo.</span><span class="sxs-lookup"><span data-stu-id="b7e71-123">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e71-124">DefaultMember</span><span class="sxs-lookup"><span data-stu-id="b7e71-124">DefaultMember</span></span></p></td>
<td><p><span data-ttu-id="b7e71-125">Nombre único del miembro predeterminado de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="b7e71-125">The unique name of the default member for this hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e71-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7e71-126">Description</span></span></p></td>
<td><p><span data-ttu-id="b7e71-127">Descripción de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="b7e71-127">A meaningful description of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e71-128">DimensionType</span><span class="sxs-lookup"><span data-stu-id="b7e71-128">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="b7e71-129">Tipo de dimensión al que pertenece esta jerarquía.</span><span class="sxs-lookup"><span data-stu-id="b7e71-129">The type of dimension to which this hierarchy belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e71-130">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="b7e71-130">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="b7e71-131">Nombre inequívoco de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="b7e71-131">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e71-132">HierarchyCaption</span><span class="sxs-lookup"><span data-stu-id="b7e71-132">HierarchyCaption</span></span></p></td>
<td><p><span data-ttu-id="b7e71-133">Etiqueta o título asociado a la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="b7e71-133">A label or caption associated with the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e71-134">HierarchyCardinality</span><span class="sxs-lookup"><span data-stu-id="b7e71-134">HierarchyCardinality</span></span></p></td>
<td><p><span data-ttu-id="b7e71-135">Número de miembros de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="b7e71-135">The number of members in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e71-136">HierarchyGUID</span><span class="sxs-lookup"><span data-stu-id="b7e71-136">HierarchyGUID</span></span></p></td>
<td><p><span data-ttu-id="b7e71-137">GUID de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="b7e71-137">The GUID of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e71-138">HierarchyName</span><span class="sxs-lookup"><span data-stu-id="b7e71-138">HierarchyName</span></span></p></td>
<td><p><span data-ttu-id="b7e71-139">Nombre de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="b7e71-139">The name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e71-140">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="b7e71-140">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="b7e71-141">Nombre inequívoco de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="b7e71-141">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e71-142">SchemaName</span><span class="sxs-lookup"><span data-stu-id="b7e71-142">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="b7e71-143">Nombre del esquema al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="b7e71-143">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

