---
title: CubeDef (objeto, ADO MD)
TOCTitle: CubeDef object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c82c95a430da76694fe26300e877e86f86a2eb4b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719907"
---
# <a name="cubedef-object-ado-md"></a><span data-ttu-id="61183-102">CubeDef (objeto, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="61183-102">CubeDef object (ADO MD)</span></span>


<span data-ttu-id="61183-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61183-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="61183-104">Representa un cubo de un esquema multidimensional, que contiene un conjunto de dimensiones relacionadas.</span><span class="sxs-lookup"><span data-stu-id="61183-104">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="61183-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61183-105">Remarks</span></span>

<span data-ttu-id="61183-106">Con las colecciones y las propiedades de un objeto **CubeDef**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="61183-106">With the collections and properties of a **CubeDef** object, you can do the following:</span></span>

  - <span data-ttu-id="61183-107">Identificar el objeto **CubeDef** con la propiedad [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="61183-107">Identify a **CubeDef** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="61183-108">Devolver una cadena que describa el cubo con la propiedad [Description](description-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="61183-108">Return a string that describes the cube with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="61183-109">Devolver las dimensiones que conforman el cubo con la colección [Dimensions](dimensions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="61183-109">Return the dimensions that make up the cube with the [Dimensions](dimensions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="61183-110">Obtener información adicional sobre el objeto **CubeDef** con la colección [Properties](properties-collection-ado.md) de ADO estándar.</span><span class="sxs-lookup"><span data-stu-id="61183-110">Obtain additional information about the **CubeDef** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="61183-p101">La colección **Properties** contiene propiedades proporcionadas por el proveedor. En la tabla siguiente se incluyen las propiedades que pueden estar disponibles. La lista de propiedades reales puede variar en función de la implementación del proveedor. Vea la documentación del proveedor para obtener una lista más completa de las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="61183-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61183-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="61183-115">Name</span></span></p></th>
<th><p><span data-ttu-id="61183-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="61183-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61183-117">NombreCatálogo</span><span class="sxs-lookup"><span data-stu-id="61183-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="61183-118">Nombre del catálogo al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="61183-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61183-119">CreatedOn</span><span class="sxs-lookup"><span data-stu-id="61183-119">CreatedOn</span></span></p></td>
<td><p><span data-ttu-id="61183-120">Fecha y hora de creación del cubo.</span><span class="sxs-lookup"><span data-stu-id="61183-120">Date and time of cube creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61183-121">CubeGUID</span><span class="sxs-lookup"><span data-stu-id="61183-121">CubeGUID</span></span></p></td>
<td><p><span data-ttu-id="61183-122">GUID del cubo.</span><span class="sxs-lookup"><span data-stu-id="61183-122">Cube GUID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61183-123">Nombre de cubo</span><span class="sxs-lookup"><span data-stu-id="61183-123">CubeName</span></span></p></td>
<td><p><span data-ttu-id="61183-124">Nombre del cubo.</span><span class="sxs-lookup"><span data-stu-id="61183-124">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61183-125">CubeType</span><span class="sxs-lookup"><span data-stu-id="61183-125">CubeType</span></span></p></td>
<td><p><span data-ttu-id="61183-126">Tipo del cubo.</span><span class="sxs-lookup"><span data-stu-id="61183-126">The type of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61183-127">DataUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="61183-127">DataUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="61183-128">Id. de usuario de la persona que actualizó por última vez los datos.</span><span class="sxs-lookup"><span data-stu-id="61183-128">User ID of the person doing the last data update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61183-129">Description</span><span class="sxs-lookup"><span data-stu-id="61183-129">Description</span></span></p></td>
<td><p><span data-ttu-id="61183-130">Descripción del cubo.</span><span class="sxs-lookup"><span data-stu-id="61183-130">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61183-131">LastSchemaUpdate</span><span class="sxs-lookup"><span data-stu-id="61183-131">LastSchemaUpdate</span></span></p></td>
<td><p><span data-ttu-id="61183-132">Fecha y hora de la última actualización del esquema.</span><span class="sxs-lookup"><span data-stu-id="61183-132">Date and time of last schema update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61183-133">SchemaName</span><span class="sxs-lookup"><span data-stu-id="61183-133">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="61183-134">Nombre del esquema al que pertenece el cubo.</span><span class="sxs-lookup"><span data-stu-id="61183-134">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61183-135">SchemaUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="61183-135">SchemaUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="61183-136">Id. de usuario de la persona que actualizó por última vez el esquema.</span><span class="sxs-lookup"><span data-stu-id="61183-136">User ID of the person doing the last schema update.</span></span></p></td>
</tr>
</tbody>
</table>

