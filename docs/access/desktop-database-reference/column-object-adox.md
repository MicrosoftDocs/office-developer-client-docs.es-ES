---
title: Column (objeto, ADOX)
TOCTitle: Column object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1b7ebd312727e1dc5071964cf1125d1c76bec4d
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026013"
---
# <a name="column-object-adox"></a>Column (objeto, ADOX)


**Se aplica a**: Access 2013, Office 2013

Representa una columna de una tabla, un índice o una clave.

## <a name="remarks"></a>Comentarios

El siguiente código crea un nuevo objeto **Column**:

`Dim obj As New Column`

Con las propiedades y las colecciones de un objeto **Column**, se puede:

  - Identificar la columna con la propiedad [Name](name-property-adox.md).

  - Especificar el tipo de datos de la columna con la propiedad [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox).

  - Determinar si la columna tiene una longitud fija o si puede contener valores nulos con la propiedad [Attributes](attributes-property-adox.md).

  - Especificar el tamaño máximo de la columna con la propiedad [DefinedSize](definedsize-property-adox.md).

  - Para los valores de datos numéricos, especificar la escala con la propiedad [NumericScale](numericscale-property-adox.md).

  - Para los valores de datos numéricos, especificar la precisión máxima con la propiedad [Precision](precision-property-adox.md).

  - Especificar el [catálogo](catalog-object-adox.md) que contiene la columna con la propiedad [ParentCatalog](parentcatalog-property-adox.md).

  - Para las columnas clave, especificar el nombre de la columna relacionada en la tabla relacionada con la propiedad [RelatedColumn](relatedcolumn-property-adox.md).

  - Para las columnas de índices, especificar si el criterio de ordenación es ascendente o descendente con la propiedad [SortOrder](sortorder-property-adox.md).

  - Obtener acceso a propiedades específicas del proveedor con la colección [Properties](properties-collection-ado.md).


> [!NOTE]
> [!NOTA] Puede que el proveedor de datos no admita todas las propiedades de los objetos **Column**. Se producirá un error si ha definido un valor para una propiedad no admitida por el proveedor. Para los nuevos objetos **Column**, el error se producirá cuando se anexe el objeto a la colección. Para los objetos existentes, el error se producirá al definir la propiedad.
> 
> Cuando se crean objetos **Column**, la existencia de un valor predeterminado adecuado para una propiedad opcional no es una garantía de que el proveedor admita la propiedad. Para obtener más información sobre las propiedades admitidas por el proveedor, vea la documentación del proveedor.

