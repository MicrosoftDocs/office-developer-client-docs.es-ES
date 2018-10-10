---
title: Keys (colección) (ADOX)
TOCTitle: Keys Collection (ADOX)
ms:assetid: 0d480c01-1b36-28b9-9135-51958f313995
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248854(v=office.15)
ms:contentKeyID: 48543215
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 837a81058a7d5ba871069a5d8534e870194ba92f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483732"
---
# <a name="keys-collection-adox"></a>Keys (colección) (ADOX)


**Se aplica a**: Access 2013 | Office 2013

Contiene todos los objetos [Key](key-object-adox.md) de una tabla.

## <a name="remarks"></a>Comentarios

El método [Append](append-method-adox-keys.md) de una colección **Keys** es único para ADOX. Se puede:

  - Agregar una nueva clave a la colección con el método **Append**.

Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:

  - Tener acceso a una clave de la colección con la propiedad [Item](item-property-ado.md).

  - Devolver el número de claves incluido en la colección con la propiedad [Count](count-property-ado.md).

  - Quitar una clave de la colección con el método [Delete](delete-method-adox-collections.md).

  - Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).

