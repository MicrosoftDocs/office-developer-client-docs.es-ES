---
title: Axis (objeto) (ADO MD)
TOCTitle: Axis Object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76fe2e0aa90397b32d95172318f3657741e1b1ec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875024"
---
# <a name="axis-object-ado-md"></a><span data-ttu-id="912a0-102">Axis (objeto) (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="912a0-102">Axis Object (ADO MD)</span></span>


<span data-ttu-id="912a0-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="912a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="912a0-104">Representa un eje de posición o de filtro de un conjunto de celdas, que contiene elementos seleccionados de una o más dimensiones.</span><span class="sxs-lookup"><span data-stu-id="912a0-104">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="912a0-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="912a0-105">Remarks</span></span>

<span data-ttu-id="912a0-106">Un objeto **Axis** puede estar incluido en una colección [Axes](axes-collection-ado-md.md) o ser devuelvo por la propiedad [FilterAxis](filteraxis-property-ado-md.md) de un objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="912a0-106">An **Axis** object can be contained by an [Axes](axes-collection-ado-md.md) collection, or returned by the [FilterAxis](filteraxis-property-ado-md.md) property of a [Cellset](cellset-object-ado-md.md).</span></span>

<span data-ttu-id="912a0-107">Con las colecciones y las propiedades de un objeto **Axis**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="912a0-107">With the collections and properties of an **Axis** object, you can do the following:</span></span>

  - <span data-ttu-id="912a0-108">Identificar el **eje** con la propiedad [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="912a0-108">Identify the **Axis** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="912a0-109">Recorrer en iteración cada posición a lo largo de un **eje** mediante la colección [Positions](positions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="912a0-109">Iterate through each position along an **Axis** using the [Positions](positions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="912a0-110">Obtener el número de dimensiones del **eje** con la propiedad [DimensionCount](dimensioncount-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="912a0-110">Obtain the number of dimensions on the **Axis** with the [DimensionCount](dimensioncount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="912a0-111">Obtener atributos específicos de proveedor del **eje** con la colección [Properties](properties-collection-ado.md) de ADO estándar.</span><span class="sxs-lookup"><span data-stu-id="912a0-111">Obtain provider-specific attributes of the **Axis** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

