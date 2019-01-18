---
title: Catalog (objeto, ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8cc0237d1419c3aba818d54811f1dbdeeaa441c3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714909"
---
# <a name="catalog-object-adox"></a><span data-ttu-id="7e7e6-102">Catalog (objeto, ADOX)</span><span class="sxs-lookup"><span data-stu-id="7e7e6-102">Catalog object (ADOX)</span></span>


<span data-ttu-id="7e7e6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e7e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e7e6-104">Contiene colecciones ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md) y [Procedures](procedures-collection-adox.md)) que describen el catálogo de esquema de un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="7e7e6-104">Contains collections ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md), and [Procedures](procedures-collection-adox.md)) that describe the schema catalog of a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e7e6-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e7e6-105">Remarks</span></span>

<span data-ttu-id="7e7e6-p101">Puede modificar el objeto **Catalog** agregando o quitando objetos, o modificando objetos existentes. Puede que algunos proveedores no admitan todos los objetos **Catalog** o que sólo permitan ver la información de esquema.</span><span class="sxs-lookup"><span data-stu-id="7e7e6-p101">You can modify the **Catalog** object by adding or removing objects or by modifying existing objects. Some providers may not support all of the **Catalog** objects or may support only viewing schema information.</span></span>

<span data-ttu-id="7e7e6-108">Con las propiedades y los métodos de un objeto **Catalog**, se puede:</span><span class="sxs-lookup"><span data-stu-id="7e7e6-108">With the properties and methods of a **Catalog** object, you can:</span></span>

- <span data-ttu-id="7e7e6-109">Abrir el catálogo estableciendo la propiedad [ActiveConnection](activeconnection-property-adox.md) en un objeto [Connection](connection-object-ado.md) de ADO o en una cadena de conexión válida.</span><span class="sxs-lookup"><span data-stu-id="7e7e6-109">Open the catalog by setting the [ActiveConnection](activeconnection-property-adox.md) property to an ADO [Connection](connection-object-ado.md) object or a valid connection string.</span></span>

- <span data-ttu-id="7e7e6-110">Crear un nuevo catálogo con el método [Create](create-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="7e7e6-110">Create a new catalog with the [Create](create-method-adox.md) method.</span></span>

- <span data-ttu-id="7e7e6-111">Determinar los propietarios de los objetos de un **catálogo** con los métodos [GetObjectOwner](getobjectowner-method-adox.md) y [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox).</span><span class="sxs-lookup"><span data-stu-id="7e7e6-111">Determine the owners of the objects in a **Catalog** with the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) methods.</span></span>

