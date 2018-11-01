---
title: Append (método, columnas ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec64241bf63719fe4f5c547d60a93f7804f181ca
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877663"
---
# <a name="append-method-adox-columns"></a>Append (método, columnas ADOX)


**Se aplica a**: Access 2013, Office 2013

Agrega un nuevo objeto [Column](column-object-adox.md) a la colección [Columns](columns-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Las columnas*. Anexar la*columna* \[,*tipo* \] \[,*DefinedSize*\]

## <a name="parameters"></a>Parámetros

  - *Column*

  - El objeto **Column** que se anexará o el nombre de la columna que se creará y anexará.

  - *Type*

  - Opcional. Un valor **Long** que especifica el tipo de datos de la columna. El parámetro *Type* corresponde a la propiedad [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) de un objeto **Column** .

  - *DefinedSize*

  - Opcional. Un valor **Long** que especifica el tamaño de la columna. El parámetro *DefinedSize* corresponde a la propiedad [DefinedSize](definedsize-property-adox.md) de un objeto **Column** .


> [!NOTE]
> [!NOTA] Si se anexa una **columna** a la colección **Columns** de un [índice](index-object-adox.md) pero la **columna** no existe en alguna [tabla](table-object-adox.md) que ya se haya anexado a la colección [Tables](tables-collection-adox.md), se producirá un error.


