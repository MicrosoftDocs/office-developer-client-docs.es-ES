---
title: Groups (colección, ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b75f6277695c00c251352e0ae2bdcc44f2c86d34
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929156"
---
# <a name="groups-collection-adox"></a><span data-ttu-id="06d96-102">Groups (colección, ADOX)</span><span class="sxs-lookup"><span data-stu-id="06d96-102">Groups collection (ADOX)</span></span>


<span data-ttu-id="06d96-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06d96-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06d96-104">Contiene todos los objetos [Group](group-object-adox.md) almacenados de un catálogo o un usuario.</span><span class="sxs-lookup"><span data-stu-id="06d96-104">Contains all stored [Group](group-object-adox.md) objects of a catalog or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="06d96-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06d96-105">Remarks</span></span>

<span data-ttu-id="06d96-p101">La colección **Groups** de un [catálogo](catalog-object-adox.md) representa todas las cuentas de grupo del catálogo. La colección **Groups** para un [usuario](user-object-adox.md) representa sólo el grupo al que pertenece el usuario.</span><span class="sxs-lookup"><span data-stu-id="06d96-p101">The **Groups** collection of a [Catalog](catalog-object-adox.md) represents all of the catalog's group accounts. The **Groups** collection for a [User](user-object-adox.md) represents only the group to which the user belongs.</span></span>

<span data-ttu-id="06d96-p102">El método [Append](append-method-adox-groups.md) de una colección **Groups** es único para ADOX. Se puede:</span><span class="sxs-lookup"><span data-stu-id="06d96-p102">The [Append](append-method-adox-groups.md) method for a **Groups** collection is unique for ADOX. You can:</span></span>

  - <span data-ttu-id="06d96-110">Agregar un nuevo grupo de seguridad a la colección con el método **Append**.</span><span class="sxs-lookup"><span data-stu-id="06d96-110">Add a new security group to the collection with the **Append** method.</span></span>

<span data-ttu-id="06d96-p103">Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:</span><span class="sxs-lookup"><span data-stu-id="06d96-p103">The remaining properties and methods are standard to ADO collections. You can:</span></span>

  - <span data-ttu-id="06d96-113">Tener acceso a un grupo de la colección con la propiedad [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="06d96-113">Access a group in the collection with the [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="06d96-114">Devolver el número de grupos incluido en la colección con la propiedad [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="06d96-114">Return the number of groups contained in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="06d96-115">Quitar un grupo de la colección con el método [Delete](delete-method-adox-collections.md).</span><span class="sxs-lookup"><span data-stu-id="06d96-115">Remove a group from the collection with the [Delete](delete-method-adox-collections.md) method.</span></span>

  - <span data-ttu-id="06d96-116">Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="06d96-116">Update the objects in the collection to reflect the current database's schema with the [Refresh](refresh-method-ado.md) method.</span></span>


> [!NOTE]
> <P><span data-ttu-id="06d96-117">[!NOTA] Para poder anexar un objeto <STRONG>Group</STRONG> a la colección <STRONG>Groups</STRONG> de un objeto <STRONG>User</STRONG>, debe existir previamente un objeto <STRONG>Group</STRONG> con el mismo <A href="name-property-adox.md">nombre</A> que el que se va a anexar en la colección <STRONG>Groups</STRONG> del <STRONG>catálogo</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="06d96-117">Before appending a <STRONG>Group</STRONG> object to the <STRONG>Groups</STRONG> collection of a <STRONG>User</STRONG> object, a <STRONG>Group</STRONG> object with the same <A href="name-property-adox.md">Name</A> as the one to be appended must already exist in the <STRONG>Groups</STRONG> collection of the <STRONG>Catalog</STRONG>.</span></span></P>


