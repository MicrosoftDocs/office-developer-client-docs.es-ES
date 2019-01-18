---
title: Table (objeto, ADOX)
TOCTitle: Table object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6475621d711881b0187031aa037c8284e155546d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710443"
---
# <a name="table-object-adox"></a><span data-ttu-id="94696-102">Table (objeto, ADOX)</span><span class="sxs-lookup"><span data-stu-id="94696-102">Table object (ADOX)</span></span>

<span data-ttu-id="94696-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="94696-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94696-104">Representa una tabla de base de datos que incluye columnas, índices y claves.</span><span class="sxs-lookup"><span data-stu-id="94696-104">Represents a database table including columns, indexes, and keys.</span></span>

## <a name="remarks"></a><span data-ttu-id="94696-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94696-105">Remarks</span></span>

<span data-ttu-id="94696-106">El siguiente código crea un nuevo objeto **Table**:</span><span class="sxs-lookup"><span data-stu-id="94696-106">The following code creates a new **Table**:</span></span>

`Dim obj As New Table`

<span data-ttu-id="94696-107">Con las propiedades y las colecciones de un objeto **Table**, se puede:</span><span class="sxs-lookup"><span data-stu-id="94696-107">With the properties and collections of a **Table** object, you can:</span></span>

- <span data-ttu-id="94696-108">Identificar la tabla con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="94696-108">Identify the table with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="94696-109">Determinar el tipo de tabla con la propiedad [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox).</span><span class="sxs-lookup"><span data-stu-id="94696-109">Determine the type of table with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox) property.</span></span>

- <span data-ttu-id="94696-110">Tener acceso a las columnas de base de datos de la tabla con la colección [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="94696-110">Access the database columns of the table with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="94696-111">Tener acceso a los índices de la tabla con la colección [Indexes](indexes-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="94696-111">Access the indexes of the table with the [Indexes](indexes-collection-adox.md) collection.</span></span>

- <span data-ttu-id="94696-112">Tener acceso a las claves de la tabla con la colección [Keys](keys-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="94696-112">Access the keys of the table with the [Keys](keys-collection-adox.md) collection.</span></span>

- <span data-ttu-id="94696-113">Especificar el [catálogo](catalog-object-adox.md) que contiene la tabla con la propiedad [ParentCatalog](parentcatalog-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="94696-113">Specify the [Catalog](catalog-object-adox.md) that owns the table with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

- <span data-ttu-id="94696-114">Devolver información de fecha con las propiedades [DateCreated](datecreated-property-adox.md) y [DateModified](datemodified-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="94696-114">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

- <span data-ttu-id="94696-115">Obtener acceso a propiedades de tabla específicas del proveedor con la colección [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="94696-115">Access provider-specific table properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="94696-p101">[!NOTA] Puede que el proveedor de datos no admita todas las propiedades de los objetos **Table**. Se producirá un error si ha definido un valor para una propiedad no admitida por el proveedor. Para los nuevos objetos **Table**, el error se producirá cuando se anexe el objeto a la colección. Para los objetos existentes, el error se producirá al definir la propiedad.</span><span class="sxs-lookup"><span data-stu-id="94696-p101">Your data provider may not support all properties of **Table** objects. An error will occur if you have set a value for a property that the provider does not support. For new **Table** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="94696-p102">Cuando se crean objetos **Table**, la existencia de un valor predeterminado adecuado para una propiedad opcional no es una garantía de que el proveedor admita la propiedad. Para obtener más información sobre las propiedades admitidas por el proveedor, vea la documentación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="94696-p102">When creating **Table** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

