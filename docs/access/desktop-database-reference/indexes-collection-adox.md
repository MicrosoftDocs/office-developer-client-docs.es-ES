---
title: Indexes (colección) (ADOX)
TOCTitle: Indexes Collection (ADOX)
ms:assetid: ab04bdd1-7c4a-44cb-dfc6-add3a52f502f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249793(v=office.15)
ms:contentKeyID: 48546963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a3dbc32da7580aa4e4c222c20131cda2adefdb50
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483354"
---
# <a name="indexes-collection-adox"></a>Indexes (colección) (ADOX)


**Se aplica a**: Access 2013 | Office 2013

Contiene todos los objetos [Index](index-object-adox.md) de una tabla.

## <a name="remarks"></a>Comentarios

El método [Append](append-method-adox-indexes.md) de una colección **Indexes** es único para ADOX. Se puede:

  - Agregar un nuevo índice a la colección con el método **Append**.

Los demás métodos y propiedades son estándar en las colecciones ADO. Se puede:

  - Tener acceso a un índice de la colección con la propiedad [Item](item-property-ado.md).

  - Devolver el número de índices incluido en la colección con la propiedad [Count](count-property-ado.md).

  - Quitar un índice de la colección con el método [Delete](delete-method-adox-collections.md).

  - Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).

