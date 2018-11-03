---
title: Users (colección, ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b44b7b858adca5672266eb1898213d8f28429f2e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931137"
---
# <a name="users-collection-adox"></a><span data-ttu-id="896db-102">Users (colección, ADOX)</span><span class="sxs-lookup"><span data-stu-id="896db-102">Users collection (ADOX)</span></span>


<span data-ttu-id="896db-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="896db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="896db-104">Contiene todos los objetos [User](user-object-adox.md) almacenados de un catálogo o un grupo.</span><span class="sxs-lookup"><span data-stu-id="896db-104">Contains all stored [User](user-object-adox.md) objects of a catalog or group.</span></span>

## <a name="remarks"></a><span data-ttu-id="896db-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="896db-105">Remarks</span></span>

<span data-ttu-id="896db-p101">La colección **Users** de un [catálogo](catalog-object-adox.md) representa todos los usuarios del catálogo. La colección **Users** para un [grupo](group-object-adox.md) representa sólo los usuarios que pertenecen al grupo específico.</span><span class="sxs-lookup"><span data-stu-id="896db-p101">The **Users** collection of a [Catalog](catalog-object-adox.md) represents all the catalog's users. The **Users** collection for a [Group](group-object-adox.md) represents only the users that have a membership in the specific group.</span></span>

<span data-ttu-id="896db-p102">El método [Append](append-method-adox-users.md) de una colección **Users** es único para ADOX. Se puede:</span><span class="sxs-lookup"><span data-stu-id="896db-p102">The [Append](append-method-adox-users.md) method for a **Users** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="896db-110">Agregar un nuevo usuario a la colección con el método **Append**.</span><span class="sxs-lookup"><span data-stu-id="896db-110">Add a new user to the collection with the **Append** method.</span></span>

<span data-ttu-id="896db-p103">Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:</span><span class="sxs-lookup"><span data-stu-id="896db-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="896db-113">Tener acceso a un usuario de la colección con la propiedad [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="896db-113">Access a user in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="896db-114">Devolver el número de usuarios incluido en la colección con la propiedad [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="896db-114">Return the number of users contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="896db-115">Quitar un usuario de la colección con el método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="896db-115">Remove a user from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="896db-116">Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="896db-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="896db-117">[!NOTA] Para poder anexar un objeto <STRONG>User</STRONG> a la colección <STRONG>Users</STRONG> de un objeto <STRONG>Group</STRONG>, debe existir previamente un objeto <STRONG>User</STRONG> con el mismo <A href="name-property-adox.md">nombre</A> que el que se va a anexar en la colección <STRONG>Users</STRONG> del <STRONG>catálogo</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="896db-117">Before appending a <STRONG>User</STRONG> object to the <STRONG>Users</STRONG> collection of a <STRONG>Group</STRONG> object, a <STRONG>User</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Users</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


