---
title: Column (objeto) (ADOX)
TOCTitle: Column Object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be5af50dd17934ece6ae3a00242a86e691ff337e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485661"
---
# <a name="column-object-adox"></a>Column (objeto) (ADOX)


**Se aplica a**: Access 2013 | Office 2013

Representa una columna de una tabla, un índice o una clave.

## <a name="remarks"></a>Comentarios

El siguiente código crea un nuevo objeto **Column**:

`Dim obj As New Column`

Con las propiedades y las colecciones de un objeto **Column**, se puede:

  - Identificar la columna con la propiedad [Name](name-property-adox.md).

  - Especificar el tipo de datos de la columna con la propiedad [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)).

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

