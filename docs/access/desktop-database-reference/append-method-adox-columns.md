---
title: Append (método, Columns de ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa7042f34f4b125c9cd34d31baae538ea3637801
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928540"
---
# <a name="append-method-adox-columns"></a>Append (método, Columns de ADOX)


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


