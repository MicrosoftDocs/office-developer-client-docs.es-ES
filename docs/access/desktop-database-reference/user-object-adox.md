---
title: 'Objeto User (ADOX: referencia de base de datos de escritorio de Access)'
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3299a6c0742e7fcbbd26532f3522fdc96b7956b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313163"
---
# <a name="user-object-adox"></a><span data-ttu-id="973be-102">Objeto User (ADOX)</span><span class="sxs-lookup"><span data-stu-id="973be-102">User object (ADOX)</span></span>


<span data-ttu-id="973be-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="973be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="973be-104">Representa una cuenta de usuario que tiene permisos de acceso dentro de una base de datos protegida.</span><span class="sxs-lookup"><span data-stu-id="973be-104">Represents a user account that has access permissions within a secured database.</span></span>

## <a name="remarks"></a><span data-ttu-id="973be-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="973be-105">Remarks</span></span>

<span data-ttu-id="973be-p101">La colección [Users](users-collection-adox.md) de un [catálogo](catalog-object-adox.md) representa todos los usuarios del catálogo. La colección **Users** para un [grupo](group-object-adox.md) representa sólo los usuarios del grupo específico.</span><span class="sxs-lookup"><span data-stu-id="973be-p101">The [Users](users-collection-adox.md) collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users of the specific group.</span></span>

<span data-ttu-id="973be-108">Con las propiedades, las colecciones y los métodos de un objeto **User**, se puede:</span><span class="sxs-lookup"><span data-stu-id="973be-108">With the properties, collections, and methods of a **User** object, you can:</span></span>

  - <span data-ttu-id="973be-109">Identificar el usuario con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="973be-109">Identify the user with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="973be-110">Cambiar la contraseña de un usuario con el método [ChangePassword](changepassword-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="973be-110">Change the password for a user with the [ChangePassword](changepassword-method-adox.md) method.</span></span>

  - <span data-ttu-id="973be-111">Determinar si un usuario tiene permisos de lectura, escritura o eliminación con los métodos [GetPermissions](getpermissions-method-adox.md) y [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="973be-111">Determine whether a user has read, write, or delete permissions with the [GetPermissions](getpermissions-method-adox.md) and [SetPermissions](setpermissions-method-adox.md) methods.</span></span>

  - <span data-ttu-id="973be-112">Tener acceso a los grupos a los que pertenece el usuario con la colección [Groups](groups-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="973be-112">Access the groups to which a user belongs with the [Groups](groups-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="973be-113">Obtener acceso a propiedades específicas del proveedor con la colección [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="973be-113">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>

