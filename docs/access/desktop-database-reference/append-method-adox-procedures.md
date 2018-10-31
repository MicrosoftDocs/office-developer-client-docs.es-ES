---
title: Append (método, procedimientos ADOX)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 195cb08fb0b195b63cdddaa848554f24d028b498
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861879"
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
> Cuando se usa el proveedor OLE DB para Microsoft Jet, el método **Append** de la colección de **procedimientos** le permitirá especificar una **vista** en lugar de un **procedimiento** en el parámetro *Command* . La **vista** se agregará al origen de datos y a la colección **Procedures**. Después del proceso **Append**, si se actualizan las colecciones **Procedures** y **Views**, la **vista** ya no existirá en la colección **Procedures** y aparecerá en la colección **Views**.


