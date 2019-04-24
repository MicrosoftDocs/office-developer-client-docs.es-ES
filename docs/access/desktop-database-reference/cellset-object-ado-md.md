---
title: Cellset (objeto, ADO MD)
TOCTitle: Cellset object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8cb75ad7277386cfe81b2edcffa234498318444
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296517"
---
# <a name="cellset-object-ado-md"></a><span data-ttu-id="06ad6-102">Cellset (objeto, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="06ad6-102">Cellset object (ADO MD)</span></span>

<span data-ttu-id="06ad6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06ad6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06ad6-104">Representa los resultados de una consulta multidimensional.</span><span class="sxs-lookup"><span data-stu-id="06ad6-104">Represents the results of a multidimensional query.</span></span> <span data-ttu-id="06ad6-105">Es un conjunto de celdas seleccionadas de cubos u otro conjuntos de celdas.</span><span class="sxs-lookup"><span data-stu-id="06ad6-105">It is a collection of cells selected from cubes or other cellsets.</span></span>

## <a name="remarks"></a><span data-ttu-id="06ad6-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06ad6-106">Remarks</span></span>

<span data-ttu-id="06ad6-p102">Los datos incluidos en un **conjunto de celdas** se recuperan mediante acceso directo en forma de matriz. Puede "profundizar" hasta un miembro específico para obtener datos sobre ese miembro. Por ejemplo, el código siguiente devuelve el título del primer miembro de la primera posición en el primer eje de un conjunto de celdas denominado cst:</span><span class="sxs-lookup"><span data-stu-id="06ad6-p102">Data within a **Cellset** is retrieved using direct, array-like access. You can "drill down" to a specific member to obtain data about that member. For example, the following code returns the caption of the first member in the first position on the first axis of a cellset named cst:</span></span>

`cst.Axes(0).Positions(0).Members(0).Caption`

<span data-ttu-id="06ad6-p103">No hay ninguna indicación de la celda actual dentro de un conjunto de celdas, pero la propiedad [Item](item-property-ado-md-cellset.md) recupera un objeto [Cell](cell-object-ado-md.md) específico del conjunto de celdas. Los argumentos de la propiedad **Item** determinan la celda que se recupera. Puede especificar el valor ordinal único de una celda. Puede también recuperar celdas utilizando sus números de posición a lo largo de cada eje del conjunto de celdas. Para obtener más información sobre cómo recuperar celdas, vea el tema relativo a la propiedad [Item](item-property-ado-md-cellset.md).</span><span class="sxs-lookup"><span data-stu-id="06ad6-p103">There is no notion of a current cell within a cellset. Instead, the [Item](item-property-ado-md-cellset.md) property retrieves a specific [Cell](cell-object-ado-md.md) object from the cellset. The arguments of the **Item** property determine which cell is retrieved. You can specify the unique ordinal value of a cell. You can also retrieve cells by using their position numbers along each axis of the cellset. For more information about retrieving cells, see the [Item](item-property-ado-md-cellset.md) property.</span></span>

<span data-ttu-id="06ad6-116">Con las colecciones, los métodos y las propiedades de un objeto **Cellset**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="06ad6-116">With the collections, methods, and properties of a **Cellset** object, you can do the following:</span></span>

  - <span data-ttu-id="06ad6-117">Asociar una conexión abierta a un objeto **Cellset** estableciendo su propiedad [ActiveConnection](activeconnection-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="06ad6-117">Associate an open connection with a **Cellset** object by setting its [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="06ad6-118">Ejecutar y recuperar los resultados de una consulta multidimensional con el método [Open](open-method-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="06ad6-118">Execute and retrieve the results of a multidimensional query with the [Open](open-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="06ad6-119">Recuperar una **celda** del **conjunto de celdas** con la propiedad [Item](item-property-ado-md-cellset.md).</span><span class="sxs-lookup"><span data-stu-id="06ad6-119">Retrieve a **Cell** from the **Cellset** with the [Item](item-property-ado-md-cellset.md) property.</span></span>

  - <span data-ttu-id="06ad6-120">Devolver los objetos [Axis](axis-object-ado-md.md) que define el **conjunto de celdas** con la colección [Axes](axes-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="06ad6-120">Return the [Axis](axis-object-ado-md.md) objects that define the **Cellset** with the [Axes](axes-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="06ad6-121">Recuperar información sobre las dimensiones utilizadas para filtrar los datos del **conjunto de celdas** con la propiedad [FilterAxis](filteraxis-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="06ad6-121">Retrieve information about the dimensions used to filter the data in the **Cellset** with the [FilterAxis](filteraxis-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="06ad6-122">Devolver o especificar la consulta utilizada para definir el **conjunto de celdas** con la propiedad [Source](source-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="06ad6-122">Return or specify the query used to define the **Cellset** with the [Source](source-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="06ad6-123">Devolver el estado actual del **conjunto de celdas** (abierto, cerrado, en ejecución o en conexión) con la propiedad [State](state-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="06ad6-123">Return the current state of the **Cellset** (open, closed, executing, or connecting) with the [State](state-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="06ad6-124">Cerrar un **conjunto de celdas** abierto con el método [Close](close-method-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="06ad6-124">Close an open **Cellset** with the [Close](close-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="06ad6-125">Obtener información específica del proveedor sobre el **conjunto de celdas** con la colección [Properties](properties-collection-ado.md) de ADO estándar.</span><span class="sxs-lookup"><span data-stu-id="06ad6-125">Retrieve provider-specific information about the **Cellset** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

