---
title: Append (método, Views de ADOX)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9e1a6e14542f267af6a9f5bc58bb2d75a11aac77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297049"
---
# <a name="append-method-adox-views"></a>Append (método, Views de ADOX)

**Se aplica a:** Access 2013, Office 2013

Crea un nuevo objeto [View](view-object-adox.md) y lo anexa a la colección [Views](views-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Vistas*. Anexar*nombre*, *comando*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Nombre* |Un valor **String** que especifica el nombre de la vista que se va a crear.|
|*Command* |Un objeto [Command](command-object-ado.md) de ADO que representa la vista que se va a crear.|

## <a name="remarks"></a>Comentarios

Crea una vista nueva en el origen de datos con el nombre y los atributos especificados en el objeto **Command**.

Si el texto del comando que especifica el usuario representa un procedimiento en vez de una vista, el comportamiento dependerá del proveedor. **Se producirá un error en Append** si el proveedor no admite comandos persistentes.

> [!NOTE]
> Cuando se utiliza OLE DB Provider para Microsoft Jet, el método **Append** de la colección **Views** permite especificar un **procedimiento** en lugar de una **vista** en el parámetro *Command*. El **procedimiento** se agregará al origen de datos y a la colección **Views**. Después del proceso **Append**, si se actualizan las colecciones **Procedures** y **Views**, el **procedimiento** ya no estará en la colección **Views** y aparecerá en la colección **Procedures**.


