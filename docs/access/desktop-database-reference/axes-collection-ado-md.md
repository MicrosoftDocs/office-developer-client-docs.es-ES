---
title: Axes (colección, ADO MD)
TOCTitle: Axes collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c88bf27f406a439d051112afb9abf94697a13b12
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922238"
---
# <a name="axes-collection-ado-md"></a><span data-ttu-id="46a21-102">Axes (colección, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="46a21-102">Axes collection (ADO MD)</span></span>


<span data-ttu-id="46a21-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46a21-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46a21-104">Contiene los objetos [Axis](axis-object-ado-md.md) que definen un conjunto de celdas.</span><span class="sxs-lookup"><span data-stu-id="46a21-104">Contains the [Axis](axis-object-ado-md.md) objects that define a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="46a21-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46a21-105">Remarks</span></span>

<span data-ttu-id="46a21-p101">Un objeto [Cellset](cellset-object-ado-md.md) contiene una colección **Axes**. Una vez abierta la colección **Cellset**, esta colección contendrá al menos un objeto **Axis**. Vea el tema relativo al objeto [Axis](axis-object-ado-md.md) para obtener una explicación más detallada de cómo usar objetos **Axis**.</span><span class="sxs-lookup"><span data-stu-id="46a21-p101">A [Cellset](cellset-object-ado-md.md) object contains an **Axes** collection. Once the **Cellset** is opened, this collection will contain at least one **Axis**. See the [Axis](axis-object-ado-md.md) object for a more detailed explanation of how to use **Axis** objects.</span></span>


> [!NOTE]
> <span data-ttu-id="46a21-p102">[!NOTA] El eje de filtro de un **conjunto de celdas** no está incluido en la colección **Axes**. Vea el tema relativo a la propiedad [FilterAxis](filteraxis-property-ado-md.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="46a21-p102">The filter axis of a **Cellset** is not contained in the **Axes** collection. See the [FilterAxis](filteraxis-property-ado-md.md) property for more information.</span></span>



<span data-ttu-id="46a21-p103">**Axes** es una colección de ADO estándar. Con las propiedades y los métodos de una colección, puede realizar las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="46a21-p103">**Axes** is a standard ADO collection. With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="46a21-113">Obtener el número de objetos de la colección con la propiedad [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="46a21-113">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="46a21-114">Devolver un objeto de la colección con la propiedad [Item](item-property-ado.md) predeterminada.</span><span class="sxs-lookup"><span data-stu-id="46a21-114">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="46a21-115">Actualizar los objetos de la colección del proveedor con el método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="46a21-115">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

