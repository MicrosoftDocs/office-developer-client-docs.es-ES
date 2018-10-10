---
title: dinámica Prompt (propiedad, ADO)
TOCTitle: Prompt Property--Dynamic (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb858186942ac026cbf3e1020c4ac658537093a5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486813"
---
# <a name="prompt-property--dynamic-ado"></a><span data-ttu-id="6be12-102">dinámica Prompt (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="6be12-102">Prompt Property--Dynamic (ADO)</span></span>


<span data-ttu-id="6be12-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6be12-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6be12-104">Especifica si el proveedor OLE DB debe solicitar al usuario información de inicialización.</span><span class="sxs-lookup"><span data-stu-id="6be12-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6be12-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="6be12-105">Settings and Return Values</span></span>

<span data-ttu-id="6be12-106">Establece y devuelve un valor [ConnectPromptEnum](connectpromptenum.md).</span><span class="sxs-lookup"><span data-stu-id="6be12-106">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6be12-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6be12-107">Remarks</span></span>

<span data-ttu-id="6be12-p101">**Prompt** es una propiedad dinámica que puede ser anexada a la colección [Properties](connection-object-ado.md) del objeto [Connection](properties-collection-ado.md) por el proveedor OLE DB. Para solicitar información de inicialización, los proveedores OLE DB suelen mostrar un cuadro de diálogo destinado al usuario.</span><span class="sxs-lookup"><span data-stu-id="6be12-p101">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider. To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="6be12-p102">Las propiedades dinámicas de un objeto [Connection](connection-object-ado.md) se pierden al cerrar **Connection**. La propiedad **Prompt** se debe restablecer antes de volver a abrir **Connection** para utilizar un valor distinto al predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6be12-p102">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed. The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6be12-p103">[!NOTA] No especifique que el proveedor deba preguntar al usuario en escenarios en que éste no pueda responder al cuadro de diálogo. Por ejemplo, el usuario no podrá responder si la aplicación se está ejecutando en un sistema de servidores en lugar de en el cliente del usuario, o en un sistema en el que ningún usuario ha iniciado sesión. En estos casos, la aplicación esperará una respuesta indefinidamente y parecerá haberse bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6be12-p103">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box. For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on. In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span></P>



<span data-ttu-id="6be12-115">**Uso**</span><span class="sxs-lookup"><span data-stu-id="6be12-115">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
