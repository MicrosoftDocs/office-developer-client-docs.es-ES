---
title: Append (método, Keys de ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297091"
---
# <a name="append-method-adox-keys"></a>Append (método, Keys de ADOX)

**Se aplica a:** Access 2013, Office 2013

Agrega un nuevo objeto [Key](key-object-adox.md) a la colección [Keys](keys-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Claves*. Anexar*clave* \[,*KeyType* \] \[,*columna* \] \[, \[*RelatedTable* \] ,*RelatedColumn*\]

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Key* |El objeto **Key** que se anexará o el nombre de la clave que se creará y anexará.|
|*KeyType* |Opcional. Un valor **Long** que especifica el tipo de clave. El parámetro *KeyType* corresponde a la propiedad [Tipo](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) de un objeto **Key**.|
|*Columna* |Opcional. Un valor **String** que especifica el nombre de la columna que se va a indizar. El parámetro *Columns* corresponde al valor de la propiedad [Name](name-property-adox.md) de un objeto [Column](column-object-adox.md).|
|*RelatedTable* |Opcional. Un valor **String** que especifica el nombre de la tabla relacionada. El parámetro *RelatedTable* corresponde al valor de la propiedad **Name** de un objeto [Table](table-object-adox.md).|
|*RelatedColumn* |Opcional. Un valor **String** que especifica el nombre de la columna relacionada para una clave externa. El parámetro RelatedColumn corresponde al valor de la propiedad **Name** de un objeto **Column**.|

## <a name="remarks"></a>Comentarios

El parámetro *Columns* puede tomar el nombre de una columna, o bien, de una matriz de nombres de columna.

