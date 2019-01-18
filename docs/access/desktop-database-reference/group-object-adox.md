---
title: Group (objeto, ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e010ac58ff0b573d42c562ce3be7a99acab5abea
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718171"
---
# <a name="group-object-adox"></a>Group (objeto, ADOX)


**Se aplica a**: Access 2013, Office 2013

Representa una cuenta de grupo que tiene permisos de acceso dentro de una base de datos protegida.

## <a name="remarks"></a>Comentarios

La colección [Groups](groups-collection-adox.md) de un [catálogo](catalog-object-adox.md) representa todas las cuentas de grupo del catálogo. La colección **Groups** para un [usuario](user-object-adox.md) representa sólo el grupo al que pertenece el usuario.

Con las propiedades, las colecciones y los métodos de un objeto **Group**, se puede:

  - Identificar el grupo con la propiedad [Name](name-property-adox.md).

  - Determinar si un grupo tiene permisos de lectura, escritura o eliminación con los métodos [GetPermissions](getpermissions-method-adox.md) y [SetPermissions](setpermissions-method-adox.md).

  - Tener acceso a las cuentas de usuario que pertenecen al grupo con la colección [Users](users-collection-adox.md).

  - Obtener acceso a propiedades específicas del proveedor con la colección [Properties](properties-collection-ado.md).

