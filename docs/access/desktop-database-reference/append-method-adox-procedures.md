---
title: Append (método, Procedures de ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2de9dc7d8dccfc4107dbd802c4013ac794acf61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297084"
---
# <a name="append-method-adox-procedures"></a>Append (método, Procedures de ADOX)

**Se aplica a:** Access 2013, Office 2013

Agrega un nuevo objeto [Procedure](procedure-object-adox.md) a la colección [Procedures](procedures-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Procedimientos*. Append *Name*, *Command*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Name* |Un valor **String** que especifica el nombre del procedimiento que se va a crear y anexar.|
|*Command* |Un objeto [Command](command-object-ado.md) de ADO que representa el procedimiento que se va a crear y anexar.|

## <a name="remarks"></a>Comentarios

Crea un procedimiento nuevo en el origen de datos con el nombre y los atributos especificados en el objeto **Command**.

Si el texto del comando que especifica el usuario representa una vista en vez de un procedimiento, el comportamiento dependerá del proveedor que se utilice. Se producirá un error en **Append** si el proveedor no admite comandos persistentes.

> [!NOTE]
> Cuando se utiliza OLE DB Provider para Microsoft Jet, el método **Append** de la colección **Procedures** permite especificar una **vista** en lugar de un **procedimiento** en el parámetro *Command*. La **vista** se agregará al origen de datos y a la colección **Procedures**. Después del proceso **Append**, si se actualizan las colecciones **Procedures** y **Views**, la **vista** ya no existirá en la colección **Procedures** y aparecerá en la colección **Views**.


