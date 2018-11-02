---
title: Keys (colección, ADOX)
TOCTitle: Keys collection (ADOX)
ms:assetid: 0d480c01-1b36-28b9-9135-51958f313995
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248854(v=office.15)
ms:contentKeyID: 48543215
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92ab4da50d8dceb98adac7ea585ebe0028d983fe
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929128"
---
# <a name="keys-collection-adox"></a>Keys (colección, ADOX)


**Se aplica a**: Access 2013, Office 2013

Contiene todos los objetos [Key](key-object-adox.md) de una tabla.

## <a name="remarks"></a>Comentarios

El método [Append](append-method-adox-keys.md) de una colección **Keys** es único para ADOX. Se puede:

  - Agregar una nueva clave a la colección con el método **Append**.

Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:

  - Tener acceso a una clave de la colección con la propiedad [Item](item-property-ado.md).

  - Devolver el número de claves incluido en la colección con la propiedad [Count](count-property-ado.md).

  - Quitar una clave de la colección con el método [Delete](delete-method-adox-collections.md).

  - Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).

