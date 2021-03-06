---
title: Colección Tables (ADOX)
TOCTitle: Tables collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e53cd4b6d4a61a226103eb443bac7f3b4f92d908
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314052"
---
# <a name="tables-collection-adox"></a>Colección Tables (ADOX)


**Se aplica a:** Access 2013, Office 2013

Contiene todos los objetos [Table](table-object-adox.md) de un catálogo.

## <a name="remarks"></a>Comentarios

El método [Append](append-method-adox-tables.md) de una colección **Tables** es único para ADOX. Se puede:

  - Agregar una nueva tabla a la colección con el método **Append**.

Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:

  - Tener acceso a una tabla de la colección con la propiedad [Item](item-property-ado.md).

  - Devolver el número de tablas incluido en la colección con la propiedad [Count](count-property-ado.md).

  - Quitar una tabla de la colección con el método [Delete](delete-method-adox-collections.md).

  - Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).

Algunos proveedores pueden devolver otros objetos de esquema, como View, en la colección Tables. Por tanto, algunas colecciones ADOX pueden contener referencias al mismo objeto. Si elimina el objeto de una colección, el cambio no se reflejará en otra colección que haga referencia al objeto eliminado hasta que se llame al método Refresh en la colección. Por ejemplo, con el proveedor OLE DB para Microsoft Jet, se devuelven vistas con la colección Tables. Si borra una vista, debe actualizar la colección Tables para que el cambio quede reflejado en la colección.

