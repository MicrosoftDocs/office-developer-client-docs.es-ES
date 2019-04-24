---
title: Index (objeto) (ADOX)
TOCTitle: Index object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02d12fffa2c766425054e344e9f7d9d7a22cb517
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291778"
---
# <a name="index-object-adox"></a><span data-ttu-id="8b710-102">Index (objeto) (ADOX)</span><span class="sxs-lookup"><span data-stu-id="8b710-102">Index object (ADOX)</span></span>

<span data-ttu-id="8b710-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b710-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b710-104">Representa un índice de una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="8b710-104">Represents an index from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b710-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8b710-105">Remarks</span></span>

<span data-ttu-id="8b710-106">El siguiente código crea un nuevo objeto **Index**:</span><span class="sxs-lookup"><span data-stu-id="8b710-106">The following code creates a new **Index**:</span></span>

`Dim obj As New Index`

<span data-ttu-id="8b710-107">Con las propiedades y las colecciones de un objeto **Index**, se puede:</span><span class="sxs-lookup"><span data-stu-id="8b710-107">With the properties and collections of an **Index** object, you can:</span></span>

- <span data-ttu-id="8b710-108">Identificar el índice con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="8b710-108">Identify the index with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="8b710-109">Tener acceso a las columnas de base de datos del índice con la colección [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="8b710-109">Access the database columns of the index with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="8b710-110">Especificar si las claves de índice deben ser únicas con la propiedad [Unique](unique-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="8b710-110">Specify whether the index keys must be unique with the [Unique](unique-property-adox.md) property.</span></span>

- <span data-ttu-id="8b710-111">Especificar si el índice es la clave principal de una tabla con la propiedad [PrimaryKey](primarykey-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="8b710-111">Specify whether the index is the primary key for a table with the [PrimaryKey](primarykey-property-adox.md) property.</span></span>

- <span data-ttu-id="8b710-112">Especificar si los registros que tienen valores nulos en sus campos de índice tienen entradas de índice con la propiedad [IndexNulls](indexnulls-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="8b710-112">Specify whether records that have null values in their index fields have index entries with the [IndexNulls](indexnulls-property-adox.md) property.</span></span>

- <span data-ttu-id="8b710-113">Especificar si el índice está agrupado con la propiedad [Clustered](clustered-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="8b710-113">Specify whether the index is clustered with the [Clustered](clustered-property-adox.md) property.</span></span>

- <span data-ttu-id="8b710-114">Obtener acceso a propiedades de índice específicas del proveedor con la colección [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8b710-114">Access provider-specific index properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="8b710-115">[!NOTA] Si se anexa una [columna](column-object-adox.md) a la colección **Columns** de un **índice** pero la **columna** no existe en un objeto [Table](table-object-adox.md) que ya se ha anexado a la colección [Tables](tables-collection-adox.md), se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="8b710-115">An error will occur when appending a [Column](column-object-adox.md) to the **Columns** collection of an **Index** if the **Column** does not exist in a [Table](table-object-adox.md) object already appended to the [Tables](tables-collection-adox.md) collection.</span></span>

<span data-ttu-id="8b710-p101">Puede que el proveedor de datos no admita todas las propiedades de los objetos **Index**. Se producirá un error si ha definido un valor para una propiedad no admitida por el proveedor. Para los nuevos objetos **Index**, el error se producirá cuando se anexe el objeto a la colección. Para los objetos existentes, el error se producirá al definir la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8b710-p101">Your data provider may not support all properties of **Index** objects. An error will occur if you have set a value for a property that is not supported by the provider. For new **Index** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="8b710-p102">Cuando se crean objetos **Index**, la existencia de un valor predeterminado adecuado para una propiedad opcional no es una garantía de que el proveedor admita la propiedad. Para obtener más información sobre las propiedades admitidas por el proveedor, vea la documentación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8b710-p102">When creating **Index** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

