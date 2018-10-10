---
title: Append (método, columnas ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f64f3b04df989348173ad2fc975dcefbd1114b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483797"
---
# <a name="append-method-adox-columns"></a>Append (método, columnas ADOX)


**Se aplica a**: Access 2013 | Office 2013

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
> <P>[!NOTA] Si se anexa una <STRONG>columna</STRONG> a la colección <STRONG>Columns</STRONG> de un <A href="index-object-adox.md">índice</A> pero la <STRONG>columna</STRONG> no existe en alguna <A href="table-object-adox.md">tabla</A> que ya se haya anexado a la colección <A href="tables-collection-adox.md">Tables</A>, se producirá un error.</P>


