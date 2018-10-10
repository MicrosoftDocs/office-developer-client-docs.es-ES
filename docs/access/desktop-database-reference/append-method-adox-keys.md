---
title: Append (método, claves ADOX)
TOCTitle: Append Method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7e10e272155d2d0377810bf8aa1704a30bad39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486222"
---
# <a name="append-method-adox-keys"></a>Append (método, claves ADOX)


**Se aplica a**: Access 2013 | Office 2013


Agrega un nuevo objeto [Key](key-object-adox.md) a la colección [Keys](keys-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Las claves*. Anexar*clave* \[,*tipo de clave* \] \[,*columna* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]

## <a name="parameters"></a>Parámetros

  - *Key*

  - El objeto **Key** que se anexará o el nombre de la clave que se creará y anexará.

  - *Tipo de clave*

  - Opcional. Un valor **Long** que especifica el tipo de clave. El parámetro *clave* corresponde a la propiedad [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) de un objeto **Key** .

  - *Column*

  - Opcional. Un valor **String** que especifica el nombre de la columna que se va a indizar. El parámetro *Columns* corresponde al valor de la propiedad [Name](name-property-adox.md) de un objeto [Column](column-object-adox.md) .

  - *RelatedTable*

  - Opcional. Un valor **String** que especifica el nombre de la tabla relacionada. El parámetro *RelatedTable* corresponde al valor de la propiedad **Name** de un objeto [Table](table-object-adox.md) .

  - *RelatedColumn*

  - Opcional. Un valor **String** que especifica el nombre de la columna relacionada para una clave externa. El parámetro RelatedColumn corresponde al valor de la propiedad **Name** de un objeto **Column**.

## <a name="remarks"></a>Comentarios

El parámetro *Columns* puede tomar el nombre de una columna o una matriz de nombres de columna.

