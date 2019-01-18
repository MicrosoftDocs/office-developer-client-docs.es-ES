---
title: Table (objeto, ADOX)
TOCTitle: Table object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6475621d711881b0187031aa037c8284e155546d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710443"
---
# <a name="table-object-adox"></a>Table (objeto, ADOX)

**Se aplica a**: Access 2013, Office 2013

Representa una tabla de base de datos que incluye columnas, índices y claves.

## <a name="remarks"></a>Comentarios

El siguiente código crea un nuevo objeto **Table**:

`Dim obj As New Table`

Con las propiedades y las colecciones de un objeto **Table**, se puede:

- Identificar la tabla con la propiedad [Name](name-property-adox.md).

- Determinar el tipo de tabla con la propiedad [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox).

- Tener acceso a las columnas de base de datos de la tabla con la colección [Columns](columns-collection-adox.md).

- Tener acceso a los índices de la tabla con la colección [Indexes](indexes-collection-adox.md).

- Tener acceso a las claves de la tabla con la colección [Keys](keys-collection-adox.md).

- Especificar el [catálogo](catalog-object-adox.md) que contiene la tabla con la propiedad [ParentCatalog](parentcatalog-property-adox.md).

- Devolver información de fecha con las propiedades [DateCreated](datecreated-property-adox.md) y [DateModified](datemodified-property-adox.md).

- Obtener acceso a propiedades de tabla específicas del proveedor con la colección [Properties](properties-collection-ado.md).


> [!NOTE]
> [!NOTA] Puede que el proveedor de datos no admita todas las propiedades de los objetos **Table**. Se producirá un error si ha definido un valor para una propiedad no admitida por el proveedor. Para los nuevos objetos **Table**, el error se producirá cuando se anexe el objeto a la colección. Para los objetos existentes, el error se producirá al definir la propiedad.

Cuando se crean objetos **Table**, la existencia de un valor predeterminado adecuado para una propiedad opcional no es una garantía de que el proveedor admita la propiedad. Para obtener más información sobre las propiedades admitidas por el proveedor, vea la documentación del proveedor.

