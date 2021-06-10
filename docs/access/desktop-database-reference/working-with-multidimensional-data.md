---
title: Trabajo con datos multidimensionales
TOCTitle: Working with multidimensional data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 67b22219fdbbec8bf518b7be0fabd9a6adfbcf7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306044"
---
# <a name="working-with-multidimensional-data"></a><span data-ttu-id="a3157-102">Trabajo con datos multidimensionales</span><span class="sxs-lookup"><span data-stu-id="a3157-102">Working with multidimensional data</span></span>

<span data-ttu-id="a3157-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3157-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3157-p101">Un *conjunto de celdas* es el resultado de una consulta de datos multidimensionales. Consta de una colección de ejes, que no suele tener más de cuatro ejes (normalmente, dos o tres). Un *eje* es una colección de miembros de una o varias dimensiones que se utiliza para localizar o filtrar valores específicos de un cubo.</span><span class="sxs-lookup"><span data-stu-id="a3157-p101">A *cellset* is the result of a query on multidimensional data. It consists of a collection of axes, usually no more than four axes and typically only two or three. An *axis* is a collection of members from one or more dimensions, which is used to locate or filter specific values in a cube.</span></span>

<span data-ttu-id="a3157-p102">Una *posición* es un punto a lo largo de un eje. En un eje que consta de una sola dimensión, estas posiciones son un subconjunto de los miembros de una dimensión. Si un eje consta de varias dimensiones, cada posición es una entidad compuesta, que tiene *n* partes donde *n* es el número de dimensiones orientadas a lo largo del eje. Cada parte de la posición es un miembro de una dimensión integrante.</span><span class="sxs-lookup"><span data-stu-id="a3157-p102">A *position* is a point along an axis. For an axis consisting of a single dimension, these positions are a subset of the dimension members. If an axis consists of more than one dimension, then each position is a compound entity, which has *n* parts where *n* is the number of dimensions oriented along that axis. Each part of the position is a member from one constituent dimension.</span></span>

<span data-ttu-id="a3157-p103">Por ejemplo, si las dimensiones Zona geográfica y Producto de un cubo que contiene datos de ventas están orientadas a lo largo del eje x de un conjunto de celdas, una posición a lo largo de este eje puede contener los miembros "EE.UU." y "Equipos". En este ejemplo, para determinar una posición a lo largo del eje x es necesario que los miembros de cada dimensión estén orientados a lo largo del eje.</span><span class="sxs-lookup"><span data-stu-id="a3157-p103">For example, if the Geography and Product dimensions from a cube containing sales data are oriented along the x-axis of a cellset, a position along this axis may contain the members "USA" and "Computers." In this example, determining a position along the x-axis requires that members from each dimension are oriented along the axis.</span></span>

<span data-ttu-id="a3157-p104">Una *celda* es un objeto situado en la intersección de las coordenadas de ejes. Cada celda tiene varios segmentos de información asociados, incluidos los propios datos, una cadena con formato (la forma en que se muestran los datos de la celda) y el valor ordinal de la celda. Cada celda es un valor ordinal único en el conjunto de celdas. El valor ordinal de la primera celda en el conjunto de celdas es cero, mientras que la celda situada en el extremo izquierdo de la segunda fila de un conjunto de celdas con ocho columnas tendría el valor ordinal de ocho.</span><span class="sxs-lookup"><span data-stu-id="a3157-p104">A *cell* is an object positioned at the intersection of axis coordinates. Each cell has multiple pieces of information associated with it, including the data itself, a formatted string (the displayable form of cell data), and the cell ordinal value. (Each cell is a unique ordinal value in the cellset. The ordinal value of the first cell in the cellset is zero, while the leftmost cell in the second row of a cellset with eight columns would have an ordinal value of eight.)</span></span>

<span data-ttu-id="a3157-117">Por ejemplo, un cubo tiene las seis dimensiones siguientes (observe que este esquema de cubo presenta ligeras diferencias con respecto al ejemplo incluido en [Descripción general de esquemas y datos multidimensionales](overview-of-multidimensional-schemas-and-data.md)):</span><span class="sxs-lookup"><span data-stu-id="a3157-117">For example, a cube has the following six dimensions (note that this cube schema differs slightly from the example given in [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md)):</span></span>

- <span data-ttu-id="a3157-118">Vendedor</span><span class="sxs-lookup"><span data-stu-id="a3157-118">Salesperson</span></span>
- <span data-ttu-id="a3157-119">Zona geográfica (jerarquía natural): Continentes, Países, Estados, etc.</span><span class="sxs-lookup"><span data-stu-id="a3157-119">Geography (natural hierarchy) — Continents, Countries, States, and so on</span></span>
- <span data-ttu-id="a3157-120">Trimestres: Trimestres, Meses, Días</span><span class="sxs-lookup"><span data-stu-id="a3157-120">Quarters — Quarters, Months, Days</span></span>
- <span data-ttu-id="a3157-121">Años</span><span class="sxs-lookup"><span data-stu-id="a3157-121">Years</span></span>
- <span data-ttu-id="a3157-122">Medidas: Ventas, CambioPorcentual, VentasPresupuestadas</span><span class="sxs-lookup"><span data-stu-id="a3157-122">Measures — Sales, PercentChange, BudgetedSales</span></span>
- <span data-ttu-id="a3157-123">Productos</span><span class="sxs-lookup"><span data-stu-id="a3157-123">Products</span></span>

> [!NOTE]
> <span data-ttu-id="a3157-124">Los valores de celda del ejemplo pueden considerarse pares ordenados de ordinales de posiciones de eje, donde el primer dígito representa la posición en el eje x y el segundo dígito, la posición en el eje y.</span><span class="sxs-lookup"><span data-stu-id="a3157-124">The cell values in the example can be viewed as ordered pairs of axis position ordinals where the first digit represents the x-axis position and the second digit the y-axis position.</span></span>

<span data-ttu-id="a3157-125">Las características de este conjunto de celdas son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3157-125">The characteristics of this cellset are as follows:</span></span>

- <span data-ttu-id="a3157-126">Dimensiones de eje: Trimestres, Vendedor, Zona geográfica</span><span class="sxs-lookup"><span data-stu-id="a3157-126">Axis dimensions: Quarters, Salesperson, Geography</span></span>

- <span data-ttu-id="a3157-127">Dimensiones de filtro: Medidas, Años, Productos</span><span class="sxs-lookup"><span data-stu-id="a3157-127">Filter dimensions: Measures, Years, Products</span></span>

- <span data-ttu-id="a3157-128">Dos ejes: COLUMNA (x o Eje 0) y FILA (y o Eje 1)</span><span class="sxs-lookup"><span data-stu-id="a3157-128">Two axes: COLUMN (x, or Axis 0) and ROW (y, or Axis 1)</span></span>

- <span data-ttu-id="a3157-129">Eje x: dos dimensiones anidadas, Vendedor y Zona geográfica</span><span class="sxs-lookup"><span data-stu-id="a3157-129">x-axis: two nested dimensions, Salesperson and Geography</span></span>

- <span data-ttu-id="a3157-130">Eje y: dimensión Trimestres</span><span class="sxs-lookup"><span data-stu-id="a3157-130">y-axis: Quarters dimension</span></span>

<span data-ttu-id="a3157-p105">El eje x tiene dos dimensiones anidadas, Vendedor y Zona geográfica. De Zona geográfica se seleccionan cuatro miembros: Seattle, Boston, USA-South y Japan. De Vendedor se seleccionan dos miembros: Valentine y Nash. Esto produce un total de ocho posiciones en este eje (8 = 4\*2).</span><span class="sxs-lookup"><span data-stu-id="a3157-p105">The x-axis has two nested dimensions: Salesperson and Geography. From Geography, four members are selected: Seattle, Boston, USA-South, and Japan. Two members are selected from Salesperson: Valentine and Nash. This yields a total of eight positions on this axis (8 = 4\*2).</span></span>

<span data-ttu-id="a3157-135">Cada coordenada se representa como una posición con dos miembros: uno de la dimensión Vendedor y otro de la dimensión Zona geográfica:</span><span class="sxs-lookup"><span data-stu-id="a3157-135">Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:</span></span>

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

<span data-ttu-id="a3157-136">El eje y sólo tiene una dimensión, que contiene las ocho posiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3157-136">The y-axis has only one dimension, containing the following eight positions:</span></span>

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

<span data-ttu-id="a3157-137">Los conjuntos de celdas, celdas, ejes y posiciones se representan en ADO MD mediante los objetos correspondientes: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md) y [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a3157-137">Cellsets, cells, axes, and positions are all represented in ADO MD by corresponding objects: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), and [Position](position-object-ado-md.md).</span></span>

