---
title: Column (objeto) (ADOX)
TOCTitle: Column object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 188f70d32237385cd82979589aecb989f18748b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296251"
---
# <a name="column-object-adox"></a><span data-ttu-id="5aa0f-102">Column (objeto) (ADOX)</span><span class="sxs-lookup"><span data-stu-id="5aa0f-102">Column object (ADOX)</span></span>


<span data-ttu-id="5aa0f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5aa0f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5aa0f-104">Representa una columna de una tabla, un índice o una clave.</span><span class="sxs-lookup"><span data-stu-id="5aa0f-104">Represents a column from a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aa0f-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5aa0f-105">Remarks</span></span>

<span data-ttu-id="5aa0f-106">El siguiente código crea un nuevo objeto **Column**:</span><span class="sxs-lookup"><span data-stu-id="5aa0f-106">The following code creates a new **Column**:</span></span>

`Dim obj As New Column`

<span data-ttu-id="5aa0f-107">Con las propiedades y las colecciones de un objeto **Column**, se puede:</span><span class="sxs-lookup"><span data-stu-id="5aa0f-107">With the properties and collections of a **Column** object, you can:</span></span>

  - <span data-ttu-id="5aa0f-108">Identificar la columna con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0f-108">Identify the column with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="5aa0f-109">Especificar el tipo de datos de la columna con la propiedad [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox).</span><span class="sxs-lookup"><span data-stu-id="5aa0f-109">Specify the data type of the column with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property.</span></span>

  - <span data-ttu-id="5aa0f-110">Determinar si la columna tiene una longitud fija o si puede contener valores nulos con la propiedad [Attributes](attributes-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0f-110">Determine if the column is fixed-length, or if it can contain null values with the [Attributes](attributes-property-adox.md) property.</span></span>

  - <span data-ttu-id="5aa0f-111">Especificar el tamaño máximo de la columna con la propiedad [DefinedSize](definedsize-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0f-111">Specify the maximum size of the column with the [DefinedSize](definedsize-property-adox.md) property.</span></span>

  - <span data-ttu-id="5aa0f-112">Para los valores de datos numéricos, especificar la escala con la propiedad [NumericScale](numericscale-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0f-112">For numeric data values, specify the scale with the [NumericScale](numericscale-property-adox.md) property.</span></span>

  - <span data-ttu-id="5aa0f-113">Para los valores de datos numéricos, especificar la precisión máxima con la propiedad [Precision](precision-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0f-113">For numeric data value, specify the maximum precision with the [Precision](precision-property-adox.md) property.</span></span>

  - <span data-ttu-id="5aa0f-114">Especificar el [catálogo](catalog-object-adox.md) que contiene la columna con la propiedad [ParentCatalog](parentcatalog-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0f-114">Specify the [Catalog](catalog-object-adox.md) that owns the column with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

  - <span data-ttu-id="5aa0f-115">Para las columnas clave, especificar el nombre de la columna relacionada en la tabla relacionada con la propiedad [RelatedColumn](relatedcolumn-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0f-115">For key columns, specify the name of the related column in the related table with the [RelatedColumn](relatedcolumn-property-adox.md) property.</span></span>

  - <span data-ttu-id="5aa0f-116">Para las columnas de índices, especificar si el criterio de ordenación es ascendente o descendente con la propiedad [SortOrder](sortorder-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0f-116">For index columns, specify whether the sort order is ascending or descending with the [SortOrder](sortorder-property-adox.md) property.</span></span>

  - <span data-ttu-id="5aa0f-117">Obtener acceso a propiedades específicas del proveedor con la colección [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5aa0f-117">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="5aa0f-p101">[!NOTA] Puede que el proveedor de datos no admita todas las propiedades de los objetos **Column**. Se producirá un error si ha definido un valor para una propiedad no admitida por el proveedor. Para los nuevos objetos **Column**, el error se producirá cuando se anexe el objeto a la colección. Para los objetos existentes, el error se producirá al definir la propiedad.</span><span class="sxs-lookup"><span data-stu-id="5aa0f-p101">Not all properties of **Column** objects may be supported by your data provider. An error will occur if you have set a value for a property that the provider does not support. For new **Column** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>
> 
> <span data-ttu-id="5aa0f-p102">Cuando se crean objetos **Column**, la existencia de un valor predeterminado adecuado para una propiedad opcional no es una garantía de que el proveedor admita la propiedad. Para obtener más información sobre las propiedades admitidas por el proveedor, vea la documentación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="5aa0f-p102">When creating **Column** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

