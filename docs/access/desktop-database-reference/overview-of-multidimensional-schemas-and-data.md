---
title: Información general de los esquemas y datos multidimensionales
TOCTitle: Overview of multidimensional schemas and data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d65378bf964ad8c6e81a08cb653f09bf00a8431c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288157"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="a5b5e-102">Información general de los esquemas y datos multidimensionales</span><span class="sxs-lookup"><span data-stu-id="a5b5e-102">Overview of multidimensional schemas and data</span></span>

<span data-ttu-id="a5b5e-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5b5e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="a5b5e-104">Esquemas multidimensionales</span><span class="sxs-lookup"><span data-stu-id="a5b5e-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="a5b5e-105">El objeto de metadatos central en ADO MD es el *cubo*, que consiste en un conjunto estructurado de dimensiones, jerarquías, niveles y miembros relacionados.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="a5b5e-p101">Una *dimensión* es una categoría independiente de datos de la base de datos multidimensional, que se obtiene de las entidades de negocio. Una dimensión suele contener elementos que se utilizan como criterios de consulta para las mediciones de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p101">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities. A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="a5b5e-p102">Una *jerarquía* es una ruta de agregación de una dimensión. Una dimensión puede tener varios niveles de detalle, con relaciones principal-secundario. Una jerarquía define cómo están relacionados estos niveles.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p102">A *hierarchy* is a path of aggregation of a dimension. A dimension may have multiple levels of granularity, which have parent-child relationships. A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="a5b5e-p103">Un *nivel* es un paso de agregación de una jerarquía. En las dimensiones con varias capas de información, cada capa es un nivel.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p103">A *level* is a step of aggregation in a hierarchy. For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="a5b5e-p104">Un *miembro* es un elemento de datos de una dimensión. Normalmente, se utilizan miembros para crear un título o describir una medida de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p104">A *member* is a data item in a dimension. Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="a5b5e-p105">Los cubos se representan mediante objetos [CubeDef](cubedef-object-ado-md.md) en ADO MD. Las dimensiones, jerarquías, niveles y miembros se representan también mediante sus objetos ADO MD correspondientes: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) y [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p105">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="a5b5e-117">Dimensions</span><span class="sxs-lookup"><span data-stu-id="a5b5e-117">Dimensions</span></span>

<span data-ttu-id="a5b5e-p106">Las dimensiones de un cubo dependen de las entidades del negocio y de los tipos de datos que se van a diseñar en la base de datos. Normalmente, cada dimensión es un punto de entrada o mecanismo independiente para la selección de datos.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p106">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="a5b5e-p107">Por ejemplo, un cubo que contiene datos de ventas tiene las cinco dimensiones siguientes: Vendedor, Zona geográfica, Fecha, Productos y Medidas. La dimensión Medidas contiene datos de ventas reales, mientras que las otras dimensiones representan formas de clasificar y agrupar los valores de datos de ventas.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p107">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="a5b5e-122">La dimensión Zona geográfica tiene el siguiente conjunto de miembros:</span><span class="sxs-lookup"><span data-stu-id="a5b5e-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="a5b5e-123">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="a5b5e-123">Hierarchies</span></span>

<span data-ttu-id="a5b5e-p108">Las jerarquías definen el modo en que los niveles de una dimensión se pueden "condensar" o agrupar. Una dimensión puede tener varias jerarquías.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p108">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="a5b5e-126">Levels</span><span class="sxs-lookup"><span data-stu-id="a5b5e-126">Levels</span></span>

<span data-ttu-id="a5b5e-127">En el ejemplo de la dimensión Zona geográfica mostrado en la ilustración anterior, cada cuadro representa un nivel de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="a5b5e-128">Cada nivel tiene el siguiente conjunto de miembros:</span><span class="sxs-lookup"><span data-stu-id="a5b5e-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="a5b5e-129">El mundo = {All}
</span><span class="sxs-lookup"><span data-stu-id="a5b5e-129">The World = {All}</span></span>

  - <span data-ttu-id="a5b5e-130">Continentes = {Norteamérica, Europa}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="a5b5e-131">Países = {Canadá, EE.UU., Reino Unido, Alemania}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="a5b5e-132">Regiones = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="a5b5e-133">Ciudades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Ángeles, Houston, Shreveport, Miami, Boston, Nueva York, Londres, Dover, Glasgow, Edimburgo, Cardiff, Pembroke, Belfast, Berlin, Hamburgo, Múnich, Stuttgart}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="a5b5e-134">Members</span><span class="sxs-lookup"><span data-stu-id="a5b5e-134">Members</span></span>

<span data-ttu-id="a5b5e-p109">Los miembros en el nivel de hoja de una jerarquía no tienen miembros secundarios y los miembros en el nivel raíz no tienen miembros principales. Todos los demás miembros tienen al menos un miembro principal y un miembro secundario. Por ejemplo, un recorrido transversal parcial del árbol jerárquico de la dimensión Zona geográfica da lugar a las siguientes relaciones principal-secundario:</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p109">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="a5b5e-138">{All} (primario de) {Europa, Norteamérica}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-138">{All} (parent of) {Europe, North America}</span></span>
- <span data-ttu-id="a5b5e-139">{Norteamérica} (primario de) {Canada, USA}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-139">{North America} (parent of) {Canada, USA}</span></span>
- <span data-ttu-id="a5b5e-140">{USA} (primario de) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>
- <span data-ttu-id="a5b5e-141">{USA-NW} (primario de) {Boise, Seattle}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="a5b5e-142">Los miembros se pueden consolidar en una o varias jerarquías para cada dimensión.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="a5b5e-143">Este ejemplo también ilustra otra característica: algunos miembros del nivel semana de la jerarquía Year-Week no aparecen en ningún nivel de la Year-Quarter jerarquía.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-143">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="a5b5e-144">Por tanto, una jerarquía no incluye necesariamente todos los miembros de una dimensión.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-144">Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="a5b5e-145">Esquemas multidimensionales</span><span class="sxs-lookup"><span data-stu-id="a5b5e-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="a5b5e-146">El objeto de metadatos central en ADO MD es el *cubo*, que consiste en un conjunto estructurado de dimensiones, jerarquías, niveles y miembros relacionados.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="a5b5e-p111">Una *dimensión* es una categoría independiente de datos de la base de datos multidimensional, que se obtiene de las entidades de negocio. Una dimensión suele contener elementos que se utilizan como criterios de consulta para las mediciones de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p111">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities. A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="a5b5e-p112">Una *jerarquía* es una ruta de agregación de una dimensión. Una dimensión puede tener varios niveles de detalle, con relaciones principal-secundario. Una jerarquía define cómo están relacionados estos niveles.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p112">A *hierarchy* is a path of aggregation of a dimension. A dimension may have multiple levels of granularity, which have parent-child relationships. A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="a5b5e-p113">Un *nivel* es un paso de agregación de una jerarquía. En las dimensiones con varias capas de información, cada capa es un nivel.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p113">A *level* is a step of aggregation in a hierarchy. For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="a5b5e-p114">Un *miembro* es un elemento de datos de una dimensión. Normalmente, se utilizan miembros para crear un título o describir una medida de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p114">A *member* is a data item in a dimension. Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="a5b5e-p115">Los cubos se representan mediante objetos [CubeDef](cubedef-object-ado-md.md) en ADO MD. Las dimensiones, jerarquías, niveles y miembros se representan también mediante sus objetos ADO MD correspondientes: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) y [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="a5b5e-158">Dimensions</span><span class="sxs-lookup"><span data-stu-id="a5b5e-158">Dimensions</span></span>

<span data-ttu-id="a5b5e-p116">Las dimensiones de un cubo dependen de las entidades del negocio y de los tipos de datos que se van a diseñar en la base de datos. Normalmente, cada dimensión es un punto de entrada o mecanismo independiente para la selección de datos.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p116">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="a5b5e-p117">Por ejemplo, un cubo que contiene datos de ventas tiene las cinco dimensiones siguientes: Vendedor, Zona geográfica, Fecha, Productos y Medidas. La dimensión Medidas contiene datos de ventas reales, mientras que las otras dimensiones representan formas de clasificar y agrupar los valores de datos de ventas.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p117">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="a5b5e-163">La dimensión Zona geográfica tiene el siguiente conjunto de miembros:</span><span class="sxs-lookup"><span data-stu-id="a5b5e-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="a5b5e-164">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="a5b5e-164">Hierarchies</span></span>

<span data-ttu-id="a5b5e-p118">Las jerarquías definen el modo en que los niveles de una dimensión se pueden "condensar" o agrupar. Una dimensión puede tener varias jerarquías.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p118">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="a5b5e-167">Levels</span><span class="sxs-lookup"><span data-stu-id="a5b5e-167">Levels</span></span>

<span data-ttu-id="a5b5e-168">En el ejemplo de la dimensión Zona geográfica mostrado en la ilustración anterior, cada cuadro representa un nivel de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="a5b5e-169">Cada nivel tiene el siguiente conjunto de miembros:</span><span class="sxs-lookup"><span data-stu-id="a5b5e-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="a5b5e-170">El mundo = {All}
</span><span class="sxs-lookup"><span data-stu-id="a5b5e-170">The World = {All}</span></span>

- <span data-ttu-id="a5b5e-171">Continentes = {Norteamérica, Europa}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="a5b5e-172">Países = {Canadá, EE.UU., Reino Unido, Alemania}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="a5b5e-173">Regiones = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="a5b5e-174">Ciudades = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Ángeles, Houston, Shreveport, Miami, Boston, Nueva York, Londres, Dover, Glasgow, Edimburgo, Cardiff, Pembroke, Belfast, Berlin, Hamburgo, Múnich, Stuttgart}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="a5b5e-175">Members</span><span class="sxs-lookup"><span data-stu-id="a5b5e-175">Members</span></span>

<span data-ttu-id="a5b5e-p119">Los miembros en el nivel de hoja de una jerarquía no tienen miembros secundarios y los miembros en el nivel raíz no tienen miembros principales. Todos los demás miembros tienen al menos un miembro principal y un miembro secundario. Por ejemplo, un recorrido transversal parcial del árbol jerárquico de la dimensión Zona geográfica da lugar a las siguientes relaciones principal-secundario:</span><span class="sxs-lookup"><span data-stu-id="a5b5e-p119">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="a5b5e-179">{All} (primario de) {Europa, Norteamérica}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="a5b5e-180">{Norteamérica} (primario de) {Canada, USA}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="a5b5e-181">{USA} (primario de) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="a5b5e-182">{USA-NW} (primario de) {Boise, Seattle}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="a5b5e-183">Los miembros se pueden consolidar en una o varias jerarquías para cada dimensión.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="a5b5e-184">Este ejemplo también ilustra otra característica: algunos miembros del nivel semana de la jerarquía Year-Week no aparecen en ningún nivel de la Year-Quarter jerarquía.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-184">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="a5b5e-185">Por tanto, una jerarquía no incluye necesariamente todos los miembros de una dimensión.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-185">Thus, a hierarchy need not include all members of a dimension.</span></span>

