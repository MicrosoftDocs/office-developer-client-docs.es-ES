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
# <a name="groups-collection-adox"></a>Groups (colección, ADOX)


**Se aplica a**: Access 2013, Office 2013

Contiene todos los objetos [Group](group-object-adox.md) almacenados de un catálogo o un usuario.

## <a name="remarks"></a>Comentarios

La colección **Groups** de un [catálogo](catalog-object-adox.md) representa todas las cuentas de grupo del catálogo. La colección **Groups** para un [usuario](user-object-adox.md) representa sólo el grupo al que pertenece el usuario.

El método [Append](append-method-adox-groups.md) de una colección **Groups** es único para ADOX. Se puede:

  - Agregar un nuevo grupo de seguridad a la colección con el método **Append**.

Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:

  - Tener acceso a un grupo de la colección con la propiedad [Item](item-property-ado.md).

  - Devolver el número de grupos incluido en la colección con la propiedad [Count](count-property-ado.md).

  - Quitar un grupo de la colección con el método [Delete](delete-method-adox-collections.md).

  - Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).


> [!NOTE]
> <P>[!NOTA] Para poder anexar un objeto <STRONG>Group</STRONG> a la colección <STRONG>Groups</STRONG> de un objeto <STRONG>User</STRONG>, debe existir previamente un objeto <STRONG>Group</STRONG> con el mismo <A href="name-property-adox.md">nombre</A> que el que se va a anexar en la colección <STRONG>Groups</STRONG> del <STRONG>catálogo</STRONG>.</P>


