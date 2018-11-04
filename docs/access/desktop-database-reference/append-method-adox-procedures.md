---
title: Append (método, Procedures de ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 65a8e0b805bf964ae60bd9de25fc45cf5b04482f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949694"
---
# <a name="append-method-adox-procedures"></a>Append (método, Procedures de ADOX)

**Se aplica a**: Access 2013, Office 2013

Agrega un nuevo objeto [Procedure](procedure-object-adox.md) a la colección [Procedures](procedures-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Los procedimientos*. Anexe el*nombre*, *comando*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Name* |Un valor **String** que especifica el nombre del procedimiento que se va a crear y anexar.|
|*Command* |Un objeto [Command](command-object-ado.md) de ADO que representa el procedimiento que se va a crear y anexar.|

## <a name="remarks"></a>Comentarios

Crea un procedimiento nuevo en el origen de datos con el nombre y los atributos especificados en el objeto **Command**.

Si el texto del comando que especifica el usuario representa una vista en vez de un procedimiento, el comportamiento dependerá del proveedor que se utilice. Se producirá un error en **Append** si el proveedor no admite comandos persistentes.

> [!NOTE]
> Cuando se usa el proveedor OLE DB para Microsoft Jet, el método **Append** de la colección de **procedimientos** le permitirá especificar una **vista** en lugar de un **procedimiento** en el parámetro *Command* . La **vista** se agregará al origen de datos y a la colección **Procedures**. Después del proceso **Append**, si se actualizan las colecciones **Procedures** y **Views**, la **vista** ya no existirá en la colección **Procedures** y aparecerá en la colección **Views**.


