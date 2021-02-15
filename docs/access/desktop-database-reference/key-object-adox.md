---
title: 'Objeto Key (ADOX: referencia de base de datos de escritorio de Access)'
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f56a90b7accd1b64c9a52e0a7cf5385f83fd10d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290755"
---
# <a name="key-object-adox"></a>Objeto Key (ADOX)


**Se aplica a:** Access 2013, Office 2013

Representa un campo de clave principal, externa o única de una tabla de base de datos.

## <a name="remarks"></a>Comentarios

El siguiente código crea un nuevo objeto **Key**:

`Dim obj As New Key`

Con las propiedades y las colecciones de un objeto **Key**, se puede:

- Identificar la clave con la propiedad [Name](name-property-adox.md).

- Determinar si la clave es principal, externa o única con la propiedad [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox).

- Tener acceso a las columnas de base de datos de la clave con la colección [Columns](columns-collection-adox.md).

- Especificar el nombre de la tabla relacionada con la propiedad [RelatedTable](relatedtable-property-adox.md).

- Determinar la acción realizada al eliminar o actualizar una clave principal con las propiedades [DeleteRule](deleterule-property-adox.md) y [UpdateRule](updaterule-property-adox.md).

