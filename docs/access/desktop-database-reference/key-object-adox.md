---
title: Objeto Key (ADOX - referencia de escritorio de la base de datos de Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7722130c76516eaa7dcaf0598a5e1c040e21ba25
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025948"
---
# <a name="key-object-adox"></a>Key (objeto, ADOX)


**Se aplica a**: Access 2013, Office 2013

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

