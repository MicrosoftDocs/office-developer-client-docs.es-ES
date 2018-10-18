---
title: dinámica Prompt (propiedad, ADO)
TOCTitle: Prompt Property--Dynamic (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 723820a2a1c5300bfdc3e688d693d29e2bddda33
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602517"
---
# <a name="prompt-property--dynamic-ado"></a><span data-ttu-id="b8c0b-102">dinámica Prompt (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="b8c0b-102">Prompt Property--Dynamic (ADO)</span></span>


<span data-ttu-id="b8c0b-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8c0b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b8c0b-104">Especifica si el proveedor OLE DB debe solicitar al usuario información de inicialización.</span><span class="sxs-lookup"><span data-stu-id="b8c0b-104">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span>

<span data-ttu-id="b8c0b-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b8c0b-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="b8c0b-106">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b8c0b-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="b8c0b-107">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b8c0b-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="b8c0b-108">master</span><span class="sxs-lookup"><span data-stu-id="b8c0b-108">master</span></span>

<span data-ttu-id="b8c0b-109">Establece y devuelve un valor [ConnectPromptEnum](connectpromptenum.md).</span><span class="sxs-lookup"><span data-stu-id="b8c0b-109">Sets and returns a [ConnectPromptEnum](connectpromptenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8c0b-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8c0b-110">Remarks</span></span>

<span data-ttu-id="b8c0b-p101">**Prompt** es una propiedad dinámica que puede ser anexada a la colección [Properties](connection-object-ado.md) del objeto [Connection](properties-collection-ado.md) por el proveedor OLE DB. Para solicitar información de inicialización, los proveedores OLE DB suelen mostrar un cuadro de diálogo destinado al usuario.</span><span class="sxs-lookup"><span data-stu-id="b8c0b-p101">**Prompt** is a dynamic property, which may be appended to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection by the OLE DB provider. To prompt for initialization information, OLE DB providers will typically display a dialog box to the user.</span></span>

<span data-ttu-id="b8c0b-p102">Las propiedades dinámicas de un objeto [Connection](connection-object-ado.md) se pierden al cerrar **Connection**. La propiedad **Prompt** se debe restablecer antes de volver a abrir **Connection** para utilizar un valor distinto al predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b8c0b-p102">Dynamic properties of a [Connection](connection-object-ado.md) object are lost when the **Connection** is closed. The **Prompt** property must be reset before re-opening the **Connection** to use a value other than the default.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b8c0b-p103">[!NOTA] No especifique que el proveedor deba preguntar al usuario en escenarios en que éste no pueda responder al cuadro de diálogo. Por ejemplo, el usuario no podrá responder si la aplicación se está ejecutando en un sistema de servidores en lugar de en el cliente del usuario, o en un sistema en el que ningún usuario ha iniciado sesión. En estos casos, la aplicación esperará una respuesta indefinidamente y parecerá haberse bloqueado.</span><span class="sxs-lookup"><span data-stu-id="b8c0b-p103">Do not specify that the provider should prompt the user in scenarios in which the user will not be able to respond to the dialog box. For example, the user will not be able to respond if the application is running on a server system instead of on the user's client, or if the application is running on a system with no user logged on. In these cases, the application will wait indefinitely for a response and seem to lock up.</span></span></P>



<span data-ttu-id="b8c0b-118">**Uso**</span><span class="sxs-lookup"><span data-stu-id="b8c0b-118">**Usage**</span></span>

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
