---
title: Dimension (objeto, ADO MD)
TOCTitle: Dimension object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: afea442aa535660b5bb618297640db8fbd546dec
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712830"
---
# <a name="dimension-object-ado-md"></a><span data-ttu-id="1b709-102">Dimension (objeto, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="1b709-102">Dimension object (ADO MD)</span></span>


<span data-ttu-id="1b709-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b709-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b709-104">Representa una de las dimensiones de un cubo multidimensional, que contiene una o más jerarquías de elementos.</span><span class="sxs-lookup"><span data-stu-id="1b709-104">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b709-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1b709-105">Remarks</span></span>

<span data-ttu-id="1b709-106">Con las colecciones y las propiedades de un objeto **Dimension**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1b709-106">With the collections and properties of a **Dimension** object, you can do the following:</span></span>

  - <span data-ttu-id="1b709-107">Identificar la **dimensión** con las propiedades [Name](name-property-ado-md.md) y [UniqueName](uniquename-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="1b709-107">Identify the **Dimension** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="1b709-108">Devolver una cadena que describa la **dimensión** con la propiedad [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="1b709-108">Return a meaningful string that describes the **Dimension** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="1b709-109">Devolver los objetos [Hierarchy](hierarchy-object-ado-md.md) que componen la **dimensión** con la colección [Hierarchies](hierarchies-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="1b709-109">Return the [Hierarchy](hierarchy-object-ado-md.md) objects that make up the **Dimension** with the [Hierarchies](hierarchies-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="1b709-110">Utilizar la colección [Properties](properties-collection-ado.md) de ADO estándar para obtener información adicional sobre el objeto **Dimension**.</span><span class="sxs-lookup"><span data-stu-id="1b709-110">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Dimension** object.</span></span>

<span data-ttu-id="1b709-p101">La colección **Properties** contiene propiedades proporcionadas por el proveedor. En la tabla siguiente se incluyen las propiedades que pueden estar disponibles. La lista de propiedades reales puede variar en función de la implementación del proveedor. Vea la documentación del proveedor para obtener una lista más completa de las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="1b709-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b709-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="1b709-115">Name</span></span></p></th>
<th><p><span data-ttu-id="1b709-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b709-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b709-117">NombreCatálogo</span><span class="sxs-lookup"><span data-stu-id="1b709-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="1b709-118">Nombre del catálogo al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="1b709-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b709-119">Nombre de cubo</span><span class="sxs-lookup"><span data-stu-id="1b709-119">CubeName</span></span></p></td>
<td><p><span data-ttu-id="1b709-120">Nombre del cubo.</span><span class="sxs-lookup"><span data-stu-id="1b709-120">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b709-121">DefaultHierarchy</span><span class="sxs-lookup"><span data-stu-id="1b709-121">DefaultHierarchy</span></span></p></td>
<td><p><span data-ttu-id="1b709-122">Nombre único de la jerarquía predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1b709-122">The unique name of the default hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b709-123">Description</span><span class="sxs-lookup"><span data-stu-id="1b709-123">Description</span></span></p></td>
<td><p><span data-ttu-id="1b709-124">Descripción del cubo.</span><span class="sxs-lookup"><span data-stu-id="1b709-124">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b709-125">DimensionCaption</span><span class="sxs-lookup"><span data-stu-id="1b709-125">DimensionCaption</span></span></p></td>
<td><p><span data-ttu-id="1b709-126">Etiqueta o título asociado a la dimensión.</span><span class="sxs-lookup"><span data-stu-id="1b709-126">A label or caption associated with the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b709-127">DimensionCardinality</span><span class="sxs-lookup"><span data-stu-id="1b709-127">DimensionCardinality</span></span></p></td>
<td><p><span data-ttu-id="1b709-128">Número de miembros de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="1b709-128">The number of members in the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b709-129">DimensionGUID</span><span class="sxs-lookup"><span data-stu-id="1b709-129">DimensionGUID</span></span></p></td>
<td><p><span data-ttu-id="1b709-130">GUID de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="1b709-130">The GUID of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b709-131">DimensionName</span><span class="sxs-lookup"><span data-stu-id="1b709-131">DimensionName</span></span></p></td>
<td><p><span data-ttu-id="1b709-132">Nombre de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="1b709-132">The name of the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b709-133">DimensionOrdinal</span><span class="sxs-lookup"><span data-stu-id="1b709-133">DimensionOrdinal</span></span></p></td>
<td><p><span data-ttu-id="1b709-134">Número ordinal de la dimensión entre el grupo de dimensiones que forman el cubo.</span><span class="sxs-lookup"><span data-stu-id="1b709-134">The ordinal number of the dimension among the group of dimensions that form the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b709-135">DimensionType</span><span class="sxs-lookup"><span data-stu-id="1b709-135">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="1b709-136">Tipo de dimensión.</span><span class="sxs-lookup"><span data-stu-id="1b709-136">The dimension type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b709-137">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="1b709-137">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="1b709-138">Nombre inequívoco de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="1b709-138">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b709-139">SchemaName</span><span class="sxs-lookup"><span data-stu-id="1b709-139">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="1b709-140">Nombre del esquema al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="1b709-140">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

