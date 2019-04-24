---
title: Objeto de usuario (referencia de base de datos de escritorio de Access de ADOX)
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
# <a name="user-object-adox"></a>User (objeto) (ADOX)


**Se aplica a:** Access 2013, Office 2013

Representa una cuenta de usuario que tiene permisos de acceso dentro de una base de datos protegida.

## <a name="remarks"></a>Comentarios

La colección [Users](users-collection-adox.md) de un [catálogo](catalog-object-adox.md) representa todos los usuarios del catálogo. La colección **Users** para un [grupo](group-object-adox.md) representa sólo los usuarios del grupo específico.

Con las propiedades, las colecciones y los métodos de un objeto **User**, se puede:

  - Identificar el usuario con la propiedad [Name](name-property-adox.md).

  - Cambiar la contraseña de un usuario con el método [ChangePassword](changepassword-method-adox.md).

  - Determinar si un usuario tiene permisos de lectura, escritura o eliminación con los métodos [GetPermissions](getpermissions-method-adox.md) y [SetPermissions](setpermissions-method-adox.md).

  - Tener acceso a los grupos a los que pertenece el usuario con la colección [Groups](groups-collection-adox.md).

  - Obtener acceso a propiedades específicas del proveedor con la colección [Properties](properties-collection-ado.md).

