---
title: Descripción general de esquemas y datos multidimensionales
TOCTitle: Overview of Multidimensional Schemas and Data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef416e62d17b5b4821b5051ecc59cc6e0dfb5739
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486177"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="d6555-102">Descripción general de esquemas y datos multidimensionales</span><span class="sxs-lookup"><span data-stu-id="d6555-102">Overview of Multidimensional Schemas and Data</span></span>


<span data-ttu-id="d6555-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6555-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="d6555-104">Esquemas multidimensionales</span><span class="sxs-lookup"><span data-stu-id="d6555-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="d6555-105">El objeto de metadatos central en ADO MD es el *cubo*, que consiste en un conjunto estructurado de dimensiones, jerarquías, niveles y miembros relacionados.</span><span class="sxs-lookup"><span data-stu-id="d6555-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="d6555-106">Una *dimensión* es una categoría independiente de datos de la base de datos multidimensional, derivado de las entidades empresariales.</span><span class="sxs-lookup"><span data-stu-id="d6555-106">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="d6555-107">Una dimensión suele contener elementos que se utilizan como criterios de consulta para las mediciones de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d6555-107">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="d6555-108">Una *jerarquía* es una ruta de acceso de agregación de una dimensión.</span><span class="sxs-lookup"><span data-stu-id="d6555-108">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="d6555-109">Una dimensión puede tener varios niveles de detalle, con relaciones principal-secundario.</span><span class="sxs-lookup"><span data-stu-id="d6555-109">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="d6555-110">Una jerarquía define cómo están relacionados estos niveles.</span><span class="sxs-lookup"><span data-stu-id="d6555-110">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="d6555-111">Un *nivel* es un paso de agregación de una jerarquía.</span><span class="sxs-lookup"><span data-stu-id="d6555-111">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="d6555-112">En las dimensiones con varias capas de información, cada capa es un nivel.</span><span class="sxs-lookup"><span data-stu-id="d6555-112">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="d6555-113">Un *miembro* es un elemento de datos en una dimensión.</span><span class="sxs-lookup"><span data-stu-id="d6555-113">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="d6555-114">Normalmente, se utilizan miembros para crear un título o describir una medida de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d6555-114">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="d6555-p105">Los cubos se representan mediante objetos [CubeDef](cubedef-object-ado-md.md) en ADO MD. Las dimensiones, jerarquías, niveles y miembros se representan también mediante sus objetos ADO MD correspondientes: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) y [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d6555-p105">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="d6555-117">Dimensiones</span><span class="sxs-lookup"><span data-stu-id="d6555-117">Dimensions</span></span>

<span data-ttu-id="d6555-p106">Las dimensiones de un cubo dependen de las entidades del negocio y de los tipos de datos que se van a diseñar en la base de datos. Normalmente, cada dimensión es un punto de entrada o mecanismo independiente para la selección de datos.</span><span class="sxs-lookup"><span data-stu-id="d6555-p106">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="d6555-p107">Por ejemplo, un cubo que contiene datos de ventas tiene las cinco dimensiones siguientes: Vendedor, Zona geográfica, Fecha, Productos y Medidas. La dimensión Medidas contiene datos de ventas reales, mientras que las otras dimensiones representan formas de clasificar y agrupar los valores de datos de ventas.</span><span class="sxs-lookup"><span data-stu-id="d6555-p107">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="d6555-122">La dimensión Zona geográfica tiene el siguiente conjunto de miembros:</span><span class="sxs-lookup"><span data-stu-id="d6555-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="d6555-123">Jerarquías</span><span class="sxs-lookup"><span data-stu-id="d6555-123">Hierarchies</span></span>

<span data-ttu-id="d6555-p108">Las jerarquías definen el modo en que los niveles de una dimensión se pueden "condensar" o agrupar. Una dimensión puede tener varias jerarquías.</span><span class="sxs-lookup"><span data-stu-id="d6555-p108">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="d6555-126">Niveles</span><span class="sxs-lookup"><span data-stu-id="d6555-126">Levels</span></span>

<span data-ttu-id="d6555-127">En el ejemplo de la dimensión Zona geográfica mostrado en la ilustración anterior, cada cuadro representa un nivel de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="d6555-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="d6555-128">Cada nivel tiene el siguiente conjunto de miembros:</span><span class="sxs-lookup"><span data-stu-id="d6555-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="d6555-129">El mundo = {All}
</span><span class="sxs-lookup"><span data-stu-id="d6555-129">The World = {All}</span></span>

  - <span data-ttu-id="d6555-130">Continentes = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="d6555-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="d6555-131">Países = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="d6555-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="d6555-132">Regiones = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="d6555-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="d6555-133">Ciudades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="d6555-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="d6555-134">Miembros</span><span class="sxs-lookup"><span data-stu-id="d6555-134">Members</span></span>

<span data-ttu-id="d6555-p109">Los miembros en el nivel de hoja de una jerarquía no tienen miembros secundarios y los miembros en el nivel raíz no tienen miembros principales. Todos los demás miembros tienen al menos un miembro principal y un miembro secundario. Por ejemplo, un recorrido transversal parcial del árbol jerárquico de la dimensión Zona geográfica da lugar a las siguientes relaciones principal-secundario:</span><span class="sxs-lookup"><span data-stu-id="d6555-p109">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

  - <span data-ttu-id="d6555-138">{All} (elemento principal de) {Europa, Norteamérica}</span><span class="sxs-lookup"><span data-stu-id="d6555-138">{All} (parent of) {Europe, North America}</span></span>

  - <span data-ttu-id="d6555-139">{North America} (elemento principal de) {Canada, USA}</span><span class="sxs-lookup"><span data-stu-id="d6555-139">{North America} (parent of) {Canada, USA}</span></span>

  - <span data-ttu-id="d6555-140">{EE.} (elemento principal de) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="d6555-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

  - <span data-ttu-id="d6555-141">{USA-NW} (elemento principal de) {Boise, Seattle}</span><span class="sxs-lookup"><span data-stu-id="d6555-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="d6555-142">Los miembros se pueden consolidar en una o varias jerarquías para cada dimensión.</span><span class="sxs-lookup"><span data-stu-id="d6555-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="d6555-p110">Este ejemplo ilustra también otra característica: algunos miembros del nivel Semana de la jerarquía Año-Semana no aparecen en ningún nivel de la jerarquía Año-Trimestre. Por tanto, una jerarquía no incluye necesariamente todos los miembros de una dimensión.</span><span class="sxs-lookup"><span data-stu-id="d6555-p110">This example also illustrates another characteristic: Some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy. Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="d6555-145">Esquemas multidimensionales</span><span class="sxs-lookup"><span data-stu-id="d6555-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="d6555-146">El objeto de metadatos central en ADO MD es el *cubo*, que consiste en un conjunto estructurado de dimensiones, jerarquías, niveles y miembros relacionados.</span><span class="sxs-lookup"><span data-stu-id="d6555-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="d6555-147">Una *dimensión* es una categoría independiente de datos de la base de datos multidimensional, derivado de las entidades empresariales.</span><span class="sxs-lookup"><span data-stu-id="d6555-147">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="d6555-148">Una dimensión suele contener elementos que se utilizan como criterios de consulta para las mediciones de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d6555-148">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="d6555-149">Una *jerarquía* es una ruta de acceso de agregación de una dimensión.</span><span class="sxs-lookup"><span data-stu-id="d6555-149">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="d6555-150">Una dimensión puede tener varios niveles de detalle, con relaciones principal-secundario.</span><span class="sxs-lookup"><span data-stu-id="d6555-150">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="d6555-151">Una jerarquía define cómo están relacionados estos niveles.</span><span class="sxs-lookup"><span data-stu-id="d6555-151">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="d6555-152">Un *nivel* es un paso de agregación de una jerarquía.</span><span class="sxs-lookup"><span data-stu-id="d6555-152">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="d6555-153">En las dimensiones con varias capas de información, cada capa es un nivel.</span><span class="sxs-lookup"><span data-stu-id="d6555-153">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="d6555-154">Un *miembro* es un elemento de datos en una dimensión.</span><span class="sxs-lookup"><span data-stu-id="d6555-154">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="d6555-155">Normalmente, se utilizan miembros para crear un título o describir una medida de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d6555-155">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="d6555-p115">Los cubos se representan mediante objetos [CubeDef](cubedef-object-ado-md.md) en ADO MD. Las dimensiones, jerarquías, niveles y miembros se representan también mediante sus objetos ADO MD correspondientes: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) y [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d6555-p115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="d6555-158">Dimensiones</span><span class="sxs-lookup"><span data-stu-id="d6555-158">Dimensions</span></span>

<span data-ttu-id="d6555-p116">Las dimensiones de un cubo dependen de las entidades del negocio y de los tipos de datos que se van a diseñar en la base de datos. Normalmente, cada dimensión es un punto de entrada o mecanismo independiente para la selección de datos.</span><span class="sxs-lookup"><span data-stu-id="d6555-p116">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="d6555-p117">Por ejemplo, un cubo que contiene datos de ventas tiene las cinco dimensiones siguientes: Vendedor, Zona geográfica, Fecha, Productos y Medidas. La dimensión Medidas contiene datos de ventas reales, mientras que las otras dimensiones representan formas de clasificar y agrupar los valores de datos de ventas.</span><span class="sxs-lookup"><span data-stu-id="d6555-p117">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="d6555-163">La dimensión Zona geográfica tiene el siguiente conjunto de miembros:</span><span class="sxs-lookup"><span data-stu-id="d6555-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="d6555-164">Jerarquías</span><span class="sxs-lookup"><span data-stu-id="d6555-164">Hierarchies</span></span>

<span data-ttu-id="d6555-p118">Las jerarquías definen el modo en que los niveles de una dimensión se pueden "condensar" o agrupar. Una dimensión puede tener varias jerarquías.</span><span class="sxs-lookup"><span data-stu-id="d6555-p118">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="d6555-167">Niveles</span><span class="sxs-lookup"><span data-stu-id="d6555-167">Levels</span></span>

<span data-ttu-id="d6555-168">En el ejemplo de la dimensión Zona geográfica mostrado en la ilustración anterior, cada cuadro representa un nivel de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="d6555-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="d6555-169">Cada nivel tiene el siguiente conjunto de miembros:</span><span class="sxs-lookup"><span data-stu-id="d6555-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="d6555-170">El mundo = {All}
</span><span class="sxs-lookup"><span data-stu-id="d6555-170">The World = {All}</span></span>

- <span data-ttu-id="d6555-171">Continentes = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="d6555-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="d6555-172">Países = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="d6555-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="d6555-173">Regiones = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="d6555-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="d6555-174">Ciudades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="d6555-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="d6555-175">Miembros</span><span class="sxs-lookup"><span data-stu-id="d6555-175">Members</span></span>

<span data-ttu-id="d6555-p119">Los miembros en el nivel de hoja de una jerarquía no tienen miembros secundarios y los miembros en el nivel raíz no tienen miembros principales. Todos los demás miembros tienen al menos un miembro principal y un miembro secundario. Por ejemplo, un recorrido transversal parcial del árbol jerárquico de la dimensión Zona geográfica da lugar a las siguientes relaciones principal-secundario:</span><span class="sxs-lookup"><span data-stu-id="d6555-p119">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="d6555-179">{All} (elemento principal de) {Europa, Norteamérica}</span><span class="sxs-lookup"><span data-stu-id="d6555-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="d6555-180">{North America} (elemento principal de) {Canada, USA}</span><span class="sxs-lookup"><span data-stu-id="d6555-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="d6555-181">{EE.} (elemento principal de) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="d6555-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="d6555-182">{USA-NW} (elemento principal de) {Boise, Seattle}</span><span class="sxs-lookup"><span data-stu-id="d6555-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="d6555-183">Los miembros se pueden consolidar en una o varias jerarquías para cada dimensión.</span><span class="sxs-lookup"><span data-stu-id="d6555-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="d6555-p120">Este ejemplo ilustra también otra característica: algunos miembros del nivel Semana de la jerarquía Año-Semana no aparecen en ningún nivel de la jerarquía Año-Trimestre. Por tanto, una jerarquía no incluye necesariamente todos los miembros de una dimensión.</span><span class="sxs-lookup"><span data-stu-id="d6555-p120">This example also illustrates another characteristic: Some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy. Thus, a hierarchy need not include all members of a dimension.</span></span>

