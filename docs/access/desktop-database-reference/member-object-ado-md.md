---
title: Member (objeto) (ADO MD)
TOCTitle: Member Object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7eaaa31df9b9bc3678c69e2115a0a58ec41ccf9f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878223"
---
# <a name="member-object-ado-md"></a><span data-ttu-id="85e39-102">Member (objeto) (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="85e39-102">Member Object (ADO MD)</span></span>


<span data-ttu-id="85e39-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85e39-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85e39-104">Representa un miembro de un nivel en un cubo, los miembros secundarios de un miembro de un nivel o un miembro de una posición a lo largo de un eje de un conjunto de celdas.</span><span class="sxs-lookup"><span data-stu-id="85e39-104">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="85e39-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85e39-105">Remarks</span></span>

<span data-ttu-id="85e39-p101">Las propiedades de un **miembro** difieren en función del contexto en el que se utilice. Un **miembro** de un [nivel](level-object-ado-md.md) en un objeto [CubeDef](cubedef-object-ado-md.md) tiene una propiedad [Children](children-property-ado-md.md) que devuelve los **miembros** del siguiente nivel inferior de la jerarquía del **miembro** actual. Para un **miembro** de una [posición](position-object-ado-md.md), la colección **Children** siempre está vacía. Además, la propiedad [Type](type-property-ado-md.md) sólo se aplica a los **miembros** de un **nivel**.</span><span class="sxs-lookup"><span data-stu-id="85e39-p101">The properties of a **Member** differ depending on the context in which it is used. A **Member** of a [Level](level-object-ado-md.md) in a [CubeDef](cubedef-object-ado-md.md) has a [Children](children-property-ado-md.md) property that returns the **Members** on the next lower level in the hierarchy from the current **Member**. For a **Member** of a [Position](position-object-ado-md.md), the **Children** collection is always empty. Also, the [Type](type-property-ado-md.md) property applies only to **Members** of a **Level**.</span></span>

<span data-ttu-id="85e39-p102">Un **miembro** de una **posición** tiene dos propiedades ( [DrilledDown](drilleddown-property-ado-md.md) y [ParentSameAsPrev](parentsameasprev-property-ado-md.md) ) que se usan al mostrar el [conjunto de celdas](cellset-object-ado-md.md). Se producirá un error si se obtiene acceso a estas propiedades en un **miembro** de un **nivel**.</span><span class="sxs-lookup"><span data-stu-id="85e39-p102">A **Member** of **Position** has two properties — [DrilledDown](drilleddown-property-ado-md.md) and [ParentSameAsPrev](parentsameasprev-property-ado-md.md) — that are useful when displaying the [Cellset](cellset-object-ado-md.md). An error will occur if these properties are accessed on a **Member** of a **Level**.</span></span>

<span data-ttu-id="85e39-112">Con las colecciones y las propiedades de un objeto **Member** de un **nivel**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="85e39-112">With the collections and properties of a **Member** object of a **Level**, you can do the following:</span></span>

  - <span data-ttu-id="85e39-113">Identificar el **miembro** con las propiedades [Name](name-property-ado-md.md) y [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-113">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="85e39-114">Devolver una cadena para utilizarla al mostrar el **miembro** con la propiedad [Caption](caption-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-114">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="85e39-115">Devolver una cadena que describa un **miembro** de medida o fórmula con la propiedad [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-115">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="85e39-116">Determinar la naturaleza del **miembro** con la propiedad [Type](type-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-116">Determine the nature of the **Member** with the [Type](type-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="85e39-117">Obtener información sobre el **nivel** del **miembro** con las propiedades [LevelDepth](leveldepth-property-ado-md.md) y [LevelName](levelname-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-117">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="85e39-118">Obtener **miembros** relacionados en una [jerarquía](hierarchy-object-ado-md.md) con las propiedades [Parent](parent-property-ado-md.md) y [Children](children-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-118">Obtain related **Members** in a [Hierarchy](hierarchy-object-ado-md.md) with the [Parent](parent-property-ado-md.md) and [Children](children-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="85e39-119">Contar los miembros secundarios de un **miembro** con la propiedad [ChildCount](childcount-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-119">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="85e39-120">Utilizar la colección [Properties](properties-collection-ado.md) de ADO estándar para obtener información adicional sobre el objeto **Level**.</span><span class="sxs-lookup"><span data-stu-id="85e39-120">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="85e39-121">Con las colecciones y las propiedades de un objeto **Member** de una **posición** a lo largo de un [eje](axis-object-ado-md.md), puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="85e39-121">With the collections and properties of a **Member** of a **Position** along an [Axis](axis-object-ado-md.md), you can do the following:</span></span>

  - <span data-ttu-id="85e39-122">Identificar el **miembro** con las propiedades [Name](name-property-ado-md.md) y [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-122">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="85e39-123">Devolver una cadena para utilizarla al mostrar el **miembro** con la propiedad [Caption](caption-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-123">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="85e39-124">Devolver una cadena que describa un **miembro** de medida o fórmula con la propiedad [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-124">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="85e39-125">Obtener información sobre el **nivel** del **miembro** con las propiedades [LevelDepth](leveldepth-property-ado-md.md) y [LevelName](levelname-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-125">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="85e39-126">Contar los miembros secundarios de un **miembro** con la propiedad [ChildCount](childcount-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="85e39-126">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="85e39-127">Utilizar la propiedad [DrilledDown](drilleddown-property-ado-md.md) para determinar si hay al menos un miembro secundario en el **eje** inmediatamente detrás de este **miembro**.</span><span class="sxs-lookup"><span data-stu-id="85e39-127">Use the [DrilledDown](drilleddown-property-ado-md.md) property to determine whether there is at least one child on the **Axis** immediately following this **Member**.</span></span>

  - <span data-ttu-id="85e39-128">Utilizar la propiedad [ParentSameAsPrev](parentsameasprev-property-ado-md.md) para determinar si el miembro principal de este **miembro** es el mismo que el miembro principal del **miembro** inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="85e39-128">Use the [ParentSameAsPrev](parentsameasprev-property-ado-md.md) property to determine whether the parent of this **Member** is the same as the parent of the immediately preceding **Member**.</span></span>

  - <span data-ttu-id="85e39-129">Utilizar la colección [Properties](properties-collection-ado.md) de ADO estándar para obtener información adicional sobre el objeto **Level**.</span><span class="sxs-lookup"><span data-stu-id="85e39-129">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="85e39-p103">La colección **Properties** contiene propiedades proporcionadas por el proveedor. En la tabla siguiente se incluyen las propiedades que pueden estar disponibles. La lista de propiedades reales puede variar en función de la implementación del proveedor. Vea la documentación del proveedor para obtener una lista más completa de las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="85e39-p103">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85e39-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="85e39-134">Name</span></span></p></th>
<th><p><span data-ttu-id="85e39-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="85e39-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85e39-136">NombreCatálogo</span><span class="sxs-lookup"><span data-stu-id="85e39-136">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="85e39-137">Nombre del catálogo al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="85e39-137">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e39-138">ChildrenCardinality</span><span class="sxs-lookup"><span data-stu-id="85e39-138">ChildrenCardinality</span></span></p></td>
<td><p><span data-ttu-id="85e39-139">Número de miembros secundarios que tiene el miembro.</span><span class="sxs-lookup"><span data-stu-id="85e39-139">The number of children that the member has.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e39-140">Nombre de cubo</span><span class="sxs-lookup"><span data-stu-id="85e39-140">CubeName</span></span></p></td>
<td><p><span data-ttu-id="85e39-141">Nombre del cubo.</span><span class="sxs-lookup"><span data-stu-id="85e39-141">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e39-142">Description</span><span class="sxs-lookup"><span data-stu-id="85e39-142">Description</span></span></p></td>
<td><p><span data-ttu-id="85e39-143">Descripción del miembro.</span><span class="sxs-lookup"><span data-stu-id="85e39-143">A meaningful description of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e39-144">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="85e39-144">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="85e39-145">Nombre inequívoco de la <a href="dimension-object-ado-md.md">dimensión</a>.</span><span class="sxs-lookup"><span data-stu-id="85e39-145">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e39-146">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="85e39-146">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="85e39-147">Nombre inequívoco de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="85e39-147">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e39-148">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="85e39-148">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="85e39-149">Distancia entre el nivel y la raíz de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="85e39-149">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e39-150">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="85e39-150">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="85e39-151">Nombre inequívoco del nivel.</span><span class="sxs-lookup"><span data-stu-id="85e39-151">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e39-152">MemberCaption</span><span class="sxs-lookup"><span data-stu-id="85e39-152">MemberCaption</span></span></p></td>
<td><p><span data-ttu-id="85e39-153">Etiqueta o título asociado al miembro.</span><span class="sxs-lookup"><span data-stu-id="85e39-153">A label or caption associated with the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e39-154">MemberGUID</span><span class="sxs-lookup"><span data-stu-id="85e39-154">MemberGUID</span></span></p></td>
<td><p><span data-ttu-id="85e39-155">GUID del miembro.</span><span class="sxs-lookup"><span data-stu-id="85e39-155">The GUID of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e39-156">Nombre de usuario registrado</span><span class="sxs-lookup"><span data-stu-id="85e39-156">MemberName</span></span></p></td>
<td><p><span data-ttu-id="85e39-157">Nombre del miembro.</span><span class="sxs-lookup"><span data-stu-id="85e39-157">The name of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e39-158">MemberOrdinal</span><span class="sxs-lookup"><span data-stu-id="85e39-158">MemberOrdinal</span></span></p></td>
<td><p><span data-ttu-id="85e39-159">Número ordinal del miembro.</span><span class="sxs-lookup"><span data-stu-id="85e39-159">The ordinal number of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e39-160">MemberType</span><span class="sxs-lookup"><span data-stu-id="85e39-160">MemberType</span></span></p></td>
<td><p><span data-ttu-id="85e39-161">Tipo de miembro.</span><span class="sxs-lookup"><span data-stu-id="85e39-161">The type of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e39-162">MemberUniqueName</span><span class="sxs-lookup"><span data-stu-id="85e39-162">MemberUniqueName</span></span></p></td>
<td><p><span data-ttu-id="85e39-163">Nombre inequívoco del miembro.</span><span class="sxs-lookup"><span data-stu-id="85e39-163">The unambiguous name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e39-164">ParentCount</span><span class="sxs-lookup"><span data-stu-id="85e39-164">ParentCount</span></span></p></td>
<td><p><span data-ttu-id="85e39-165">Número de miembros principales que tiene el miembro.</span><span class="sxs-lookup"><span data-stu-id="85e39-165">The count of the number of parents that this member has.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e39-166">ParentLevel</span><span class="sxs-lookup"><span data-stu-id="85e39-166">ParentLevel</span></span></p></td>
<td><p><span data-ttu-id="85e39-167">Número de nivel del miembro principal.</span><span class="sxs-lookup"><span data-stu-id="85e39-167">The level number of the member's parent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85e39-168">ParentUniqueName</span><span class="sxs-lookup"><span data-stu-id="85e39-168">ParentUniqueName</span></span></p></td>
<td><p><span data-ttu-id="85e39-169">Nombre inequívoco del miembro principal.</span><span class="sxs-lookup"><span data-stu-id="85e39-169">The unambiguous name of the member's parent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85e39-170">SchemaName</span><span class="sxs-lookup"><span data-stu-id="85e39-170">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="85e39-171">Nombre del esquema al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="85e39-171">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

