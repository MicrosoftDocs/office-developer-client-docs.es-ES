---
title: Append (método, procedimientos ADOX)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483685"
---
# <a name="append-method-adox-procedures"></a>Append (método, procedimientos ADOX)


**Se aplica a**: Access 2013 | Office 2013


Agrega un nuevo objeto [Procedure](procedure-object-adox.md) a la colección [Procedures](procedures-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Los procedimientos*. Anexe el*nombre*, *comando*

## <a name="parameters"></a>Parámetros

  - *Nombre*

  - Un valor **String** que especifica el nombre del procedimiento que se va a crear y anexar.

  - *Command*

  - Un objeto [Command](command-object-ado.md) de ADO que representa el procedimiento que se va a crear y anexar.

## <a name="remarks"></a>Comentarios

Crea un procedimiento nuevo en el origen de datos con el nombre y los atributos especificados en el objeto **Command**.

Si el texto del comando que especifica el usuario representa una vista en vez de un procedimiento, el comportamiento dependerá del proveedor que se utilice. Se producirá un error en **Append** si el proveedor no admite comandos persistentes.


> [!NOTE]
> <P>Cuando se usa el proveedor OLE DB para Microsoft Jet, el método <STRONG>Append</STRONG> de la colección de <STRONG>procedimientos</STRONG> le permitirá especificar una <STRONG>vista</STRONG> en lugar de un <STRONG>procedimiento</STRONG> en el parámetro <EM>Command</EM> . La <STRONG>vista</STRONG> se agregará al origen de datos y a la colección <STRONG>Procedures</STRONG>. Después del proceso <STRONG>Append</STRONG>, si se actualizan las colecciones <STRONG>Procedures</STRONG> y <STRONG>Views</STRONG>, la <STRONG>vista</STRONG> ya no existirá en la colección <STRONG>Procedures</STRONG> y aparecerá en la colección <STRONG>Views</STRONG>.</P>


