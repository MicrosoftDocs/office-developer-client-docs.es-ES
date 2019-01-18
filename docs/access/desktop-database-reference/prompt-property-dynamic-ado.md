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
# <a name="prompt-dynamic-property-ado"></a><span data-ttu-id="60522-102">Propiedad dinámica Prompt (ADO)</span><span class="sxs-lookup"><span data-stu-id="60522-102">Prompt dynamic property (ADO)</span></span>

<span data-ttu-id="60522-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60522-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60522-104">Especifica si el proveedor OLE DB debe solicitar al usuario información de inicialización.</span><span class="sxs-lookup"><span data-stu-id="60522-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="60522-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="60522-105">Settings and return values</span></span>

<span data-ttu-id="60522-106">Establece y devuelve un valor [ConnectPromptEnum](connectpromptenum.md).</span><span class="sxs-lookup"><span data-stu-id="60522-106">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60522-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60522-107">Remarks</span></span>

<span data-ttu-id="60522-p101">**Prompt** es una propiedad dinámica que puede ser anexada a la colección [Properties](connection-object-ado.md) del objeto [Connection](properties-collection-ado.md) por el proveedor OLE DB. Para solicitar información de inicialización, los proveedores OLE DB suelen mostrar un cuadro de diálogo destinado al usuario.</span><span class="sxs-lookup"><span data-stu-id="60522-p101">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider. To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="60522-p102">Las propiedades dinámicas de un objeto [Connection](connection-object-ado.md) se pierden al cerrar **Connection**. La propiedad **Prompt** se debe restablecer antes de volver a abrir **Connection** para utilizar un valor distinto al predeterminado.</span><span class="sxs-lookup"><span data-stu-id="60522-p102">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed. The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>

> [!NOTE]
> <span data-ttu-id="60522-p103">[!NOTA] No especifique que el proveedor deba preguntar al usuario en escenarios en que éste no pueda responder al cuadro de diálogo. Por ejemplo, el usuario no podrá responder si la aplicación se está ejecutando en un sistema de servidores en lugar de en el cliente del usuario, o en un sistema en el que ningún usuario ha iniciado sesión. En estos casos, la aplicación esperará una respuesta indefinidamente y parecerá haberse bloqueado.</span><span class="sxs-lookup"><span data-stu-id="60522-p103">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box. For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on. In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span>

<span data-ttu-id="60522-115">**Uso**</span><span class="sxs-lookup"><span data-stu-id="60522-115">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
