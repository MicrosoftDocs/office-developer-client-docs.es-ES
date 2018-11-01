---
title: Group (objeto) (ADOX)
TOCTitle: Group Object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6f98e65522ebefdb8f3897234d04e54d9599dda
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883683"
---
# <a name="group-object-adox"></a><span data-ttu-id="97273-102">Group (objeto) (ADOX)</span><span class="sxs-lookup"><span data-stu-id="97273-102">Group Object (ADOX)</span></span>


<span data-ttu-id="97273-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97273-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97273-104">Representa una cuenta de grupo que tiene permisos de acceso dentro de una base de datos protegida.</span><span class="sxs-lookup"><span data-stu-id="97273-104">Represents a group account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="97273-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97273-105">Remarks</span></span>

<span data-ttu-id="97273-p101">La colección [Groups](groups-collection-adox.md) de un [catálogo](catalog-object-adox.md) representa todas las cuentas de grupo del catálogo. La colección **Groups** para un [usuario](user-object-adox.md) representa sólo el grupo al que pertenece el usuario.</span><span class="sxs-lookup"><span data-stu-id="97273-p101">The [Groups](groups-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="97273-108">Con las propiedades, las colecciones y los métodos de un objeto **Group**, se puede:</span><span class="sxs-lookup"><span data-stu-id="97273-108">With the properties, collections, and methods of a **Group** object, you can:</span></span>

  - <span data-ttu-id="97273-109">Identificar el grupo con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="97273-109">Identify the group with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="97273-110">Determinar si un grupo tiene permisos de lectura, escritura o eliminación con los métodos [GetPermissions](getpermissions-method-adox.md) y [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="97273-110">Determine whether a group has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="97273-111">Tener acceso a las cuentas de usuario que pertenecen al grupo con la colección [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="97273-111">Access the user accounts that have memberships in the group with the [Users](users-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="97273-112">Obtener acceso a propiedades específicas del proveedor con la colección [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="97273-112">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

