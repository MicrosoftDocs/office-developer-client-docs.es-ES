---
title: Axes (colección) (ADO MD)
TOCTitle: Axes collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8183b0bad1dcbaba33088dffcf21959f5b9fd993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296937"
---
# <a name="axes-collection-ado-md"></a><span data-ttu-id="2fab6-102">Axes (colección) (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="2fab6-102">Axes collection (ADO MD)</span></span>


<span data-ttu-id="2fab6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fab6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2fab6-104">Contiene los objetos [Axis](axis-object-ado-md.md) que definen un conjunto de celdas.</span><span class="sxs-lookup"><span data-stu-id="2fab6-104">Contains the [Axis](axis-object-ado-md.md) objects that define a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fab6-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2fab6-105">Remarks</span></span>

<span data-ttu-id="2fab6-p101">Un objeto [Cellset](cellset-object-ado-md.md) contiene una colección **Axes**. Una vez abierta la colección **Cellset**, esta colección contendrá al menos un objeto **Axis**. Vea el tema relativo al objeto [Axis](axis-object-ado-md.md) para obtener una explicación más detallada de cómo usar objetos **Axis**.</span><span class="sxs-lookup"><span data-stu-id="2fab6-p101">A [Cellset](cellset-object-ado-md.md) object contains an **Axes** collection. Once the **Cellset** is opened, this collection will contain at least one **Axis**. See the [Axis](axis-object-ado-md.md) object for a more detailed explanation of how to use **Axis** objects.</span></span>


> [!NOTE]
> <span data-ttu-id="2fab6-p102">[!NOTA] El eje de filtro de un **conjunto de celdas** no está incluido en la colección **Axes**. Vea el tema relativo a la propiedad [FilterAxis](filteraxis-property-ado-md.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2fab6-p102">The filter axis of a **Cellset** is not contained in the **Axes** collection. See the [FilterAxis](filteraxis-property-ado-md.md) property for more information.</span></span>



<span data-ttu-id="2fab6-p103">**Axes** es una colección de ADO estándar. Con las propiedades y los métodos de una colección, puede realizar las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="2fab6-p103">**Axes** is a standard ADO collection. With the properties and methods of a collection, you can do the following:</span></span>

- <span data-ttu-id="2fab6-113">Obtener el número de objetos de la colección con la propiedad [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2fab6-113">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="2fab6-114">Devolver un objeto de la colección con la propiedad [Item](item-property-ado.md) predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2fab6-114">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="2fab6-115">Actualizar los objetos de la colección del proveedor con el método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2fab6-115">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

