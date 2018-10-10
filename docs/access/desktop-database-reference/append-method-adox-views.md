---
title: Append (método, vistas ADOX)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485066"
---
# <a name="append-method-adox-views"></a>Append (método, vistas ADOX)


**Se aplica a**: Access 2013 | Office 2013


Crea un nuevo objeto [View](view-object-adox.md) y lo anexa a la colección [Views](views-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Las vistas*. Anexe el*nombre*, *comando*

## <a name="parameters"></a>Parámetros

  - *Nombre*

  - Un valor **String** que especifica el nombre de la vista que se va a crear.

  - *Command*

  - Un objeto [Command](command-object-ado.md) de ADO que representa la vista que se va a crear.

## <a name="remarks"></a>Comentarios

Crea una vista nueva en el origen de datos con el nombre y los atributos especificados en el objeto **Command**.

Si el texto del comando que especifica el usuario representa un procedimiento en vez de una vista, el comportamiento dependerá del proveedor. **Se producirá un error en Append** si el proveedor no admite comandos persistentes.


> [!NOTE]
> <P>Cuando se usa el proveedor OLE DB para Microsoft Jet, el método <STRONG>Append</STRONG> de la colección de <STRONG>vistas</STRONG> permiten especificar un <STRONG>procedimiento</STRONG> en lugar de una <STRONG>vista</STRONG> en el parámetro <EM>Command</EM> . El <STRONG>procedimiento</STRONG> se agregará al origen de datos y a la colección <STRONG>Views</STRONG>. Después del proceso <STRONG>Append</STRONG>, si se actualizan las colecciones <STRONG>Procedures</STRONG> y <STRONG>Views</STRONG>, el <STRONG>procedimiento</STRONG> ya no estará en la colección <STRONG>Views</STRONG> y aparecerá en la colección <STRONG>Procedures</STRONG>.</P>


