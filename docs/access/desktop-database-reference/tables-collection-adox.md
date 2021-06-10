---
title: Colección Tables (ADOX)
TOCTitle: Tables collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e53cd4b6d4a61a226103eb443bac7f3b4f92d908
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314052"
---
# <a name="tables-collection-adox"></a><span data-ttu-id="9945d-102">Colección Tables (ADOX)</span><span class="sxs-lookup"><span data-stu-id="9945d-102">Tables collection (ADOX)</span></span>


<span data-ttu-id="9945d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9945d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9945d-104">Contiene todos los objetos [Table](table-object-adox.md) de un catálogo.</span><span class="sxs-lookup"><span data-stu-id="9945d-104">Contains all [Table](table-object-adox.md) objects of a catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="9945d-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9945d-105">Remarks</span></span>

<span data-ttu-id="9945d-p101">El método [Append](append-method-adox-tables.md) de una colección **Tables** es único para ADOX. Se puede:</span><span class="sxs-lookup"><span data-stu-id="9945d-p101">The [Append](append-method-adox-tables.md) method for a **Tables** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="9945d-108">Agregar una nueva tabla a la colección con el método **Append**.</span><span class="sxs-lookup"><span data-stu-id="9945d-108">Add a new table to the collection with the **Append** method.</span></span>

<span data-ttu-id="9945d-p102">Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:</span><span class="sxs-lookup"><span data-stu-id="9945d-p102">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="9945d-111">Tener acceso a una tabla de la colección con la propiedad [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9945d-111">Access a table in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="9945d-112">Devolver el número de tablas incluido en la colección con la propiedad [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9945d-112">Return the number of tables contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="9945d-113">Quitar una tabla de la colección con el método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="9945d-113">Remove a table from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="9945d-114">Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9945d-114">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>

<span data-ttu-id="9945d-p103">Algunos proveedores pueden devolver otros objetos de esquema, como View, en la colección Tables. Por tanto, algunas colecciones ADOX pueden contener referencias al mismo objeto. Si elimina el objeto de una colección, el cambio no se reflejará en otra colección que haga referencia al objeto eliminado hasta que se llame al método Refresh en la colección. Por ejemplo, con el proveedor OLE DB para Microsoft Jet, se devuelven vistas con la colección Tables. Si borra una vista, debe actualizar la colección Tables para que el cambio quede reflejado en la colección.</span><span class="sxs-lookup"><span data-stu-id="9945d-p103">Some providers may return other schema objects, such as a View, in the Tables collection. Therefore, some ADOX collections may contain references to the same object. Should you delete the object from one collection, the change will not be visible in another collection that references the deleted object until the Refresh method is called on the collection. For example, with the OLE DB Provider for Microsoft Jet, Views are returned with the Tables collection. If you drop a View, you must Refresh the Tables collection before the collection will reflect the change.</span></span>

