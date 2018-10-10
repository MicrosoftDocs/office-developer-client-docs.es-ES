---
title: Users (colección) (ADOX)
TOCTitle: Users Collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d68dc2dd368523e8ca3dd04a06008cea9bef337e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483794"
---
# <a name="users-collection-adox"></a>Users (colección) (ADOX)


**Se aplica a**: Access 2013 | Office 2013

Contiene todos los objetos [User](user-object-adox.md) almacenados de un catálogo o un grupo.

## <a name="remarks"></a>Comentarios

La colección **Users** de un [catálogo](catalog-object-adox.md) representa todos los usuarios del catálogo. La colección **Users** para un [grupo](group-object-adox.md) representa sólo los usuarios que pertenecen al grupo específico.

El método [Append](append-method-adox-users.md) de una colección **Users** es único para ADOX. Se puede:

  - Agregar un nuevo usuario a la colección con el método **Append**.

Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:

  - Tener acceso a un usuario de la colección con la propiedad [Item](item-property-ado.md).

  - Devolver el número de usuarios incluido en la colección con la propiedad [Count](count-property-ado.md).

  - Quitar un usuario de la colección con el método [Delete](delete-method-adox-collections.md).

  - Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).


> [!NOTE]
> <P>[!NOTA] Para poder anexar un objeto <STRONG>User</STRONG> a la colección <STRONG>Users</STRONG> de un objeto <STRONG>Group</STRONG>, debe existir previamente un objeto <STRONG>User</STRONG> con el mismo <A href="name-property-adox.md">nombre</A> que el que se va a anexar en la colección <STRONG>Users</STRONG> del <STRONG>catálogo</STRONG>.</P>


