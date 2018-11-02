---
title: Catalog (objeto, ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 31a0d2212f063eca013c1668b47e548df1405366
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922576"
---
# <a name="catalog-object-adox"></a>Catalog (objeto, ADOX)


**Se aplica a**: Access 2013, Office 2013

Contiene colecciones ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md) y [Procedures](procedures-collection-adox.md)) que describen el catálogo de esquema de un origen de datos.

## <a name="remarks"></a>Comentarios

Puede modificar el objeto **Catalog** agregando o quitando objetos, o modificando objetos existentes. Puede que algunos proveedores no admitan todos los objetos **Catalog** o que sólo permitan ver la información de esquema.

Con las propiedades y los métodos de un objeto **Catalog**, se puede:

  - Abrir el catálogo estableciendo la propiedad [ActiveConnection](activeconnection-property-adox.md) en un objeto [Connection](connection-object-ado.md) de ADO o en una cadena de conexión válida.

  - Crear un nuevo catálogo con el método [Create](create-method-adox.md).

  - Determinar los propietarios de los objetos de un **catálogo** con los métodos [GetObjectOwner](getobjectowner-method-adox.md) y [SetObjectOwner](https://msdn.microsoft.com/library/jj249006\(v=office.15\)).

