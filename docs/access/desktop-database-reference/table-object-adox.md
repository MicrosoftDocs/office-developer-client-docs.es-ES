---
title: Table (objeto) (ADOX)
TOCTitle: Table Object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b63014a57104d5d31f5ac5620b26712a9f97347b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869298"
---
# <a name="table-object-adox"></a>Table (objeto) (ADOX)


**Se aplica a**: Access 2013, Office 2013

Representa una tabla de base de datos que incluye columnas, índices y claves.

## <a name="remarks"></a>Comentarios

El siguiente código crea un nuevo objeto **Table**:

`Dim obj As New Table`

Con las propiedades y las colecciones de un objeto **Table**, se puede:

  - Identificar la tabla con la propiedad [Name](name-property-adox.md).

  - Determinar el tipo de tabla con la propiedad [Type](https://msdn.microsoft.com/library/jj250042\(v=office.15\)).

  - Tener acceso a las columnas de base de datos de la tabla con la colección [Columns](columns-collection-adox.md).

  - Tener acceso a los índices de la tabla con la colección [Indexes](indexes-collection-adox.md).

  - Tener acceso a las claves de la tabla con la colección [Keys](keys-collection-adox.md).

  - Especificar el [catálogo](catalog-object-adox.md) que contiene la tabla con la propiedad [ParentCatalog](parentcatalog-property-adox.md).

  - Devolver información de fecha con las propiedades [DateCreated](datecreated-property-adox.md) y [DateModified](datemodified-property-adox.md).

  - Obtener acceso a propiedades de tabla específicas del proveedor con la colección [Properties](properties-collection-ado.md).


> [!NOTE]
> <P>[!NOTA] Puede que el proveedor de datos no admita todas las propiedades de los objetos <STRONG>Table</STRONG>. Se producirá un error si ha definido un valor para una propiedad no admitida por el proveedor. Para los nuevos objetos <STRONG>Table</STRONG>, el error se producirá cuando se anexe el objeto a la colección. Para los objetos existentes, el error se producirá al definir la propiedad.</P>



Cuando se crean objetos **Table**, la existencia de un valor predeterminado adecuado para una propiedad opcional no es una garantía de que el proveedor admita la propiedad. Para obtener más información sobre las propiedades admitidas por el proveedor, vea la documentación del proveedor.

