---
title: Objeto Key (ADOX - referencia de escritorio de la base de datos de Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 11bd05c4959ba1f3e1819e482ce311fc798bf0e6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929835"
---
# <a name="key-object-adox"></a>Key (objeto, ADOX)


**Se aplica a**: Access 2013, Office 2013

Representa un campo de clave principal, externa o única de una tabla de base de datos.

## <a name="remarks"></a>Comentarios

El siguiente código crea un nuevo objeto **Key**:

`Dim obj As New Key`

Con las propiedades y las colecciones de un objeto **Key**, se puede:

- Identificar la clave con la propiedad [Name](name-property-adox.md).

- Determinar si la clave es principal, externa o única con la propiedad [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)).

- Tener acceso a las columnas de base de datos de la clave con la colección [Columns](columns-collection-adox.md).

- Especificar el nombre de la tabla relacionada con la propiedad [RelatedTable](relatedtable-property-adox.md).

- Determinar la acción realizada al eliminar o actualizar una clave principal con las propiedades [DeleteRule](deleterule-property-adox.md) y [UpdateRule](updaterule-property-adox.md).

