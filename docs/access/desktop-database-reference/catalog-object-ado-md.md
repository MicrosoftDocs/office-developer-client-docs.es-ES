---
title: Objeto Catalog (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ee7d2e68df90c8eee4227f949f93ea074b7df97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296594"
---
# <a name="catalog-object-ado-md"></a><span data-ttu-id="259cc-102">Objeto Catalog (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="259cc-102">Catalog object (ADO MD)</span></span>


<span data-ttu-id="259cc-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="259cc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="259cc-104">Contiene información de esquema multidimensional (es decir, cubos y dimensiones subyacentes, jerarquías, niveles y elementos) específica de un proveedor de datos multidimensionales (MDP).</span><span class="sxs-lookup"><span data-stu-id="259cc-104">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span>

## <a name="remarks"></a><span data-ttu-id="259cc-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="259cc-105">Remarks</span></span>

<span data-ttu-id="259cc-106">Con las colecciones y las propiedades de un objeto **Catalog**, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="259cc-106">With the collections and properties of a **Catalog** object, you can do the following:</span></span>

- <span data-ttu-id="259cc-107">Abrir el catálogo estableciendo la propiedad [ActiveConnection](activeconnection-property-ado-md.md) en un objeto [Connection](connection-object-ado.md) de ADO estándar o en una cadena de conexión válida.</span><span class="sxs-lookup"><span data-stu-id="259cc-107">Open the catalog by setting the [ActiveConnection](activeconnection-property-ado-md.md) property to a standard ADO [Connection](connection-object-ado.md) object or to a valid connection string.</span></span>

- <span data-ttu-id="259cc-108">Identificar el **catálogo** con la propiedad [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="259cc-108">Identify the **Catalog** with the [Name](name-property-ado-md.md) property.</span></span>

- <span data-ttu-id="259cc-109">Recorrer en iteración los cubos de un catálogo mediante la colección [CubeDefs](cubedefs-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="259cc-109">Iterate through the cubes in a catalog using the [CubeDefs](cubedefs-collection-ado-md.md) collection.</span></span>

