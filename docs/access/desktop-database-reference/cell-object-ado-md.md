---
title: Cell (objeto, ADO MD)
TOCTitle: Cell object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7bb2a479789a8c5bd1825b6cb04e602e0b829dfb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725990"
---
# <a name="cell-object-ado-md"></a><span data-ttu-id="54da7-102">Cell (objeto, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="54da7-102">Cell object (ADO MD)</span></span>


<span data-ttu-id="54da7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54da7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54da7-104">Representa los datos de la intersección de coordenadas de ejes contenidos en un conjunto de celdas.</span><span class="sxs-lookup"><span data-stu-id="54da7-104">Represents the data at the intersection of axis coordinates contained in a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="54da7-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54da7-105">Remarks</span></span>

<span data-ttu-id="54da7-106">El objeto **Cell** lo devuelve la propiedad [Item](item-property-ado-md-cellset.md) de un objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="54da7-106">A **Cell** object is returned by the [Item](item-property-ado-md-cellset.md) property of a [Cellset](cellset-object-ado-md.md) object.</span></span>

<span data-ttu-id="54da7-107">Con las colecciones y las propiedades de un objeto **Cell**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="54da7-107">With the collections and properties of a **Cell** object, you can do the following:</span></span>

- <span data-ttu-id="54da7-108">Devolver los datos de la **celda** con la propiedad [Value](value-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="54da7-108">Return the data in the **Cell** with the [Value](value-property-ado-md.md) property.</span></span>

- <span data-ttu-id="54da7-109">Devolver la cadena que representa la presentación con formato de la propiedad **Value** con la propiedad [FormattedValue](formattedvalue-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="54da7-109">Return the string representing the formatted display of the **Value** property with the [FormattedValue](formattedvalue-property-ado-md.md) property.</span></span>

- <span data-ttu-id="54da7-110">Devolver el valor ordinal de la **celda** incluida en el **conjunto de celdas** con la propiedad [Ordinal](ordinal-property-ado-md-cell.md).</span><span class="sxs-lookup"><span data-stu-id="54da7-110">Return the ordinal value of the **Cell** within the **Cellset** with the [Ordinal](ordinal-property-ado-md-cell.md) property.</span></span>

- <span data-ttu-id="54da7-111">Determinar la posición de la **celda** incluida en el objeto [CubeDef](cubedef-object-ado-md.md) con la colección [Positions](positions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="54da7-111">Determine the position of the **Cell** within the [CubeDef](cubedef-object-ado-md.md) with the [Positions](positions-collection-ado-md.md) collection.</span></span>

- <span data-ttu-id="54da7-112">Recuperar otra información sobre la **celda** con la colección [Properties](properties-collection-ado.md) de ADO estándar.</span><span class="sxs-lookup"><span data-stu-id="54da7-112">Retrieve other information about the **Cell** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="54da7-p101">La colección **Properties** contiene propiedades proporcionadas por el proveedor. En la tabla siguiente se incluyen las propiedades que pueden estar disponibles. La lista de propiedades reales puede variar en función de la implementación del proveedor. Vea la documentación del proveedor para obtener una lista más completa de las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="54da7-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54da7-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="54da7-117">Name</span></span></p></th>
<th><p><span data-ttu-id="54da7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="54da7-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54da7-119">BackColor</span><span class="sxs-lookup"><span data-stu-id="54da7-119">BackColor</span></span></p></td>
<td><p><span data-ttu-id="54da7-120">Color de fondo utilizado al mostrar la celda.</span><span class="sxs-lookup"><span data-stu-id="54da7-120">Background color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54da7-121">FontFlags</span><span class="sxs-lookup"><span data-stu-id="54da7-121">FontFlags</span></span></p></td>
<td><p><span data-ttu-id="54da7-122">Máscara de bits que incluye los efectos de la fuente.</span><span class="sxs-lookup"><span data-stu-id="54da7-122">Bitmask detailing effects on the font.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54da7-123">FontName</span><span class="sxs-lookup"><span data-stu-id="54da7-123">FontName</span></span></p></td>
<td><p><span data-ttu-id="54da7-124">Fuente utilizada para mostrar el valor de la celda.</span><span class="sxs-lookup"><span data-stu-id="54da7-124">Font used to display the cell value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54da7-125">FontSize</span><span class="sxs-lookup"><span data-stu-id="54da7-125">FontSize</span></span></p></td>
<td><p><span data-ttu-id="54da7-126">Tamaño de fuente utilizado para mostrar el valor de la celda.</span><span class="sxs-lookup"><span data-stu-id="54da7-126">Font size used to display the cell value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="54da7-127">ForeColor</span><span class="sxs-lookup"><span data-stu-id="54da7-127">ForeColor</span></span></p></td>
<td><p><span data-ttu-id="54da7-128">Color de primer plano utilizado al mostrar la celda.</span><span class="sxs-lookup"><span data-stu-id="54da7-128">Foreground color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54da7-129">FormatString</span><span class="sxs-lookup"><span data-stu-id="54da7-129">FormatString</span></span></p></td>
<td><p><span data-ttu-id="54da7-130">Valor de la cadena con formato.</span><span class="sxs-lookup"><span data-stu-id="54da7-130">Value in a formatted string.</span></span></p></td>
</tr>
</tbody>
</table>

