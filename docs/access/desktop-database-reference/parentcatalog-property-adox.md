---
title: ParentCatalog (propiedad, ADOX)
TOCTitle: ParentCatalog Property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9fdd4b41578b4f185d199a47204faabd0af3ff8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603416"
---
# <a name="parentcatalog-property-adox"></a>ParentCatalog (propiedad, ADOX)


**Se aplica a**: Access 2013 | Office 2013

Especifica el catálogo principal de una tabla o una columna para proporcionar acceso a propiedades específicas del proveedor.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece y devuelve un objeto [Catalog](catalog-object-adox.md). El establecimiento de **ParentCatalog** en un **catálogo** abierto permite el acceso a propiedades específicas del proveedor antes de anexar una tabla o una columna a una colección **Catalog**.

## <a name="remarks"></a>Comentarios

Algunos proveedores de datos permiten la escritura de valores de propiedades específicas del proveedor solo durante la creación (cuando se anexa una tabla o una columna a su colección **Catalog** ). Para tener acceso a estas propiedades antes de anexar estos objetos a un **catálogo**, primero especifique el **catálogo** en la propiedad **ParentCatalog**.

Si la tabla o la columna se anexa a un **catálogo** distinto del **ParentCatalog**, se produce un error.

