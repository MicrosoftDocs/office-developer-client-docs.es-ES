---
title: Members (colección, ADO MD)
TOCTitle: Members collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: adc8ed771bcba6a4b6532b33b27980f8aab695c5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721328"
---
# <a name="members-collection-ado-md"></a><span data-ttu-id="4791a-102">Members (colección, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="4791a-102">Members collection (ADO MD)</span></span>


<span data-ttu-id="4791a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4791a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4791a-104">Contiene los objetos [Member](member-object-ado-md.md) de un nivel o una posición a lo largo de un eje.</span><span class="sxs-lookup"><span data-stu-id="4791a-104">Contains the [Member](member-object-ado-md.md) objects from a level or a position along an axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="4791a-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4791a-105">Remarks</span></span>

<span data-ttu-id="4791a-106">La colección **Members** sirve para albergar los siguientes tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4791a-106">A **Members** collection is used to contain the following types of members:</span></span>

  - <span data-ttu-id="4791a-p101">Los miembros que componen un nivel de un cubo. Estos miembros se incluyen en la colección **Members** de un objeto [Level](level-object-ado-md.md). Por ejemplo, en el ejemplo de [Descripción general de esquemas y datos multidimensionales](overview-of-multidimensional-schemas-and-data.md), los cuatro miembros del nivel Countries son Canada, USA, UK y Germany.</span><span class="sxs-lookup"><span data-stu-id="4791a-p101">The members that make up a level in a cube. These are contained in the **Members** collection of a [Level](level-object-ado-md.md) object. For example, using the sample from [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md), the four members of the Countries level are Canada, USA, UK, and Germany.</span></span>

  - <span data-ttu-id="4791a-p102">Los miembros secundarios de un miembro específico en una jerarquía. Estos miembros los devuelve la propiedad [Children](children-property-ado-md.md) del objeto principal **Member**. Por ejemplo, en ese mismo ejemplo, los dos miembros secundarios del miembro Canada son Canada-East y Canada-West.</span><span class="sxs-lookup"><span data-stu-id="4791a-p102">The members that are the children of a specific member within a hierarchy. These members are returned by the [Children](children-property-ado-md.md) property of the parent **Member** object. For example, again using the same sample, the two children of the Canada member are Canada-East and Canada-West.</span></span>

  - <span data-ttu-id="4791a-p103">Los miembros que definen una posición específica a lo largo de un eje de un [conjunto de celdas](cellset-object-ado-md.md). En el conjunto de celdas del ejemplo de [Trabajar con datos multidimensionales](working-with-multidimensional-data.md), los dos miembros de la primera posición en el eje x son Valentine y Seattle. Estos miembros están incluidos en la colección **Members** de un objeto [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="4791a-p103">The members that define a specific position along an axis of a [cellset](cellset-object-ado-md.md). Using the cellset from [Working with Multidimensional Data](working-with-multidimensional-data.md) as an example, the two members of the first position on the x-axis are Valentine and Seattle. These members are contained by the **Members** collection of a [Position](position-object-ado-md.md) object.</span></span>

<span data-ttu-id="4791a-p104">**Members** es una colección de ADO estándar. Con las propiedades y los métodos de una colección, puede realizar las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="4791a-p104">**Members** is a standard ADO collection. With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="4791a-118">Obtener el número de objetos de la colección con la propiedad [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4791a-118">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="4791a-119">Devolver un objeto de la colección con la propiedad [Item](item-property-ado.md) predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4791a-119">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="4791a-120">Actualizar los objetos de la colección del proveedor con el método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4791a-120">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

