---
title: Colección Columns (ADOX)
TOCTitle: Columns collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1827fe11696e28871bdd03594ff0d7057c377dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296209"
---
# <a name="columns-collection-adox"></a>Colección Columns (ADOX)


**Se aplica a:** Access 2013, Office 2013

Contiene todos los objetos [Column](column-object-adox.md) de una tabla, un índice o una clave.

## <a name="remarks"></a>Comentarios

El método [Append](append-method-adox-columns.md) de una colección **Columns** es único para ADOX. Se puede:

  - Agregar una nueva columna a la colección con el método **Append**.

Los demás métodos o propiedades son estándar en las colecciones ADO. Se puede:

  - Tener acceso a una columna de la colección con la propiedad [Item](item-property-ado.md).

  - Devolver el número de columnas incluido en la colección con la propiedad [Count](count-property-ado.md).

  - Quitar una columna de la colección con el método [Delete](delete-method-adox-collections.md).

  - Actualizar los objetos de la colección de forma que reflejen el esquema de base de datos actual con el método [Refresh](refresh-method-ado.md).


> [!NOTE]
> [!NOTA] Si se anexa una **columna** a la colección **Columns** de un [índice](index-object-adox.md) pero la **columna** no existe en alguna [tabla](table-object-adox.md) que ya se haya anexado a la colección [Tables](tables-collection-adox.md), se producirá un error.


