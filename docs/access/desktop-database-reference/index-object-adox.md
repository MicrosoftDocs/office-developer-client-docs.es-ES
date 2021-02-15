---
title: Objeto Index (ADOX)
TOCTitle: Index object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02d12fffa2c766425054e344e9f7d9d7a22cb517
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291778"
---
# <a name="index-object-adox"></a>Objeto Index (ADOX)

**Se aplica a:** Access 2013, Office 2013

Representa un índice de una tabla de base de datos.

## <a name="remarks"></a>Comentarios

El siguiente código crea un nuevo objeto **Index**:

`Dim obj As New Index`

Con las propiedades y las colecciones de un objeto **Index**, se puede:

- Identificar el índice con la propiedad [Name](name-property-adox.md).

- Tener acceso a las columnas de base de datos del índice con la colección [Columns](columns-collection-adox.md).

- Especificar si las claves de índice deben ser únicas con la propiedad [Unique](unique-property-adox.md).

- Especificar si el índice es la clave principal de una tabla con la propiedad [PrimaryKey](primarykey-property-adox.md).

- Especificar si los registros que tienen valores nulos en sus campos de índice tienen entradas de índice con la propiedad [IndexNulls](indexnulls-property-adox.md).

- Especificar si el índice está agrupado con la propiedad [Clustered](clustered-property-adox.md).

- Obtener acceso a propiedades de índice específicas del proveedor con la colección [Properties](properties-collection-ado.md).


> [!NOTE]
> [!NOTA] Si se anexa una [columna](column-object-adox.md) a la colección **Columns** de un **índice** pero la **columna** no existe en un objeto [Table](table-object-adox.md) que ya se ha anexado a la colección [Tables](tables-collection-adox.md), se producirá un error.

Puede que el proveedor de datos no admita todas las propiedades de los objetos **Index**. Se producirá un error si ha definido un valor para una propiedad no admitida por el proveedor. Para los nuevos objetos **Index**, el error se producirá cuando se anexe el objeto a la colección. Para los objetos existentes, el error se producirá al definir la propiedad.

Cuando se crean objetos **Index**, la existencia de un valor predeterminado adecuado para una propiedad opcional no es una garantía de que el proveedor admita la propiedad. Para obtener más información sobre las propiedades admitidas por el proveedor, vea la documentación del proveedor.

