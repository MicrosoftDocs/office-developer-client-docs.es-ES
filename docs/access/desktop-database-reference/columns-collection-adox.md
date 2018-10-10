---
title: Columns (colección) (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13f9a17d7dfcd9e621e4f4b1f1fcc03e88b4d832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486144"
---
# <a name="columns-collection-adox"></a>Columns (colección) (ADOX)


**Se aplica a**: Access 2013 | Office 2013

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
> <P>[!NOTA] Si se anexa una <STRONG>columna</STRONG> a la colección <STRONG>Columns</STRONG> de un <A href="index-object-adox.md">índice</A> pero la <STRONG>columna</STRONG> no existe en alguna <A href="table-object-adox.md">tabla</A> que ya se haya anexado a la colección <A href="tables-collection-adox.md">Tables</A>, se producirá un error.</P>


