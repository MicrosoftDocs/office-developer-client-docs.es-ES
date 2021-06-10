---
title: Objeto Group (ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e010ac58ff0b573d42c562ce3be7a99acab5abea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292121"
---
# <a name="group-object-adox"></a><span data-ttu-id="e2050-102">Objeto Group (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e2050-102">Group object (ADOX)</span></span>


<span data-ttu-id="e2050-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2050-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2050-104">Representa una cuenta de grupo que tiene permisos de acceso dentro de una base de datos protegida.</span><span class="sxs-lookup"><span data-stu-id="e2050-104">Represents a group account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2050-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2050-105">Remarks</span></span>

<span data-ttu-id="e2050-p101">La colección [Groups](groups-collection-adox.md) de un [catálogo](catalog-object-adox.md) representa todas las cuentas de grupo del catálogo. La colección **Groups** para un [usuario](user-object-adox.md) representa sólo el grupo al que pertenece el usuario.</span><span class="sxs-lookup"><span data-stu-id="e2050-p101">The [Groups](groups-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="e2050-108">Con las propiedades, las colecciones y los métodos de un objeto **Group**, se puede:</span><span class="sxs-lookup"><span data-stu-id="e2050-108">With the properties, collections, and methods of a **Group** object, you can:</span></span>

  - <span data-ttu-id="e2050-109">Identificar el grupo con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e2050-109">Identify the group with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="e2050-110">Determinar si un grupo tiene permisos de lectura, escritura o eliminación con los métodos [GetPermissions](getpermissions-method-adox.md) y [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e2050-110">Determine whether a group has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="e2050-111">Tener acceso a las cuentas de usuario que pertenecen al grupo con la colección [Users](users-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e2050-111">Access the user accounts that have memberships in the group with the [Users](users-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="e2050-112">Obtener acceso a propiedades específicas del proveedor con la colección [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e2050-112">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

