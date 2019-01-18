---
title: Propiedad dinámica Prompt (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 261ac5640b5239f27ad91e01d1cb23794f88740a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715189"
---
# <a name="prompt-dynamic-property-ado"></a>Propiedad dinámica Prompt (ADO)

**Se aplica a**: Access 2013, Office 2013

Especifica si el proveedor OLE DB debe solicitar al usuario información de inicialización.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece y devuelve un valor [ConnectPromptEnum](connectpromptenum.md).

## <a name="remarks"></a>Comentarios

**Prompt** es una propiedad dinámica que puede ser anexada a la colección [Properties](connection-object-ado.md) del objeto [Connection](properties-collection-ado.md) por el proveedor OLE DB. Para solicitar información de inicialización, los proveedores OLE DB suelen mostrar un cuadro de diálogo destinado al usuario.

Las propiedades dinámicas de un objeto [Connection](connection-object-ado.md) se pierden al cerrar **Connection**. La propiedad **Prompt** se debe restablecer antes de volver a abrir **Connection** para utilizar un valor distinto al predeterminado.

> [!NOTE]
> [!NOTA] No especifique que el proveedor deba preguntar al usuario en escenarios en que éste no pueda responder al cuadro de diálogo. Por ejemplo, el usuario no podrá responder si la aplicación se está ejecutando en un sistema de servidores en lugar de en el cliente del usuario, o en un sistema en el que ningún usuario ha iniciado sesión. En estos casos, la aplicación esperará una respuesta indefinidamente y parecerá haberse bloqueado.

**Uso**

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
