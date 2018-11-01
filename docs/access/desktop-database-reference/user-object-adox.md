---
title: Objeto de usuario) (ADOX - referencia de escritorio de la base de datos de Access)
TOCTitle: User Object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c37e43f09fb4187de246e687d81dbd72463d390
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889318"
---
# <a name="user-object-adox"></a>User (objeto) (ADOX)


**Se aplica a**: Access 2013, Office 2013

Representa una cuenta de usuario que tiene permisos de acceso dentro de una base de datos protegida.

## <a name="remarks"></a>Comentarios

La colección [Users](users-collection-adox.md) de un [catálogo](catalog-object-adox.md) representa todos los usuarios del catálogo. La colección **Users** para un [grupo](group-object-adox.md) representa sólo los usuarios del grupo específico.

Con las propiedades, las colecciones y los métodos de un objeto **User**, se puede:

  - Identificar el usuario con la propiedad [Name](name-property-adox.md).

  - Cambiar la contraseña de un usuario con el método [ChangePassword](changepassword-method-adox.md).

  - Determinar si un usuario tiene permisos de lectura, escritura o eliminación con los métodos [GetPermissions](getpermissions-method-adox.md) y [SetPermissions](setpermissions-method-adox.md).

  - Tener acceso a los grupos a los que pertenece el usuario con la colección [Groups](groups-collection-adox.md).

  - Obtener acceso a propiedades específicas del proveedor con la colección [Properties](properties-collection-ado.md).

