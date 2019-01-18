---
title: Agregar opciones de votación a un elemento de correo
TOCTitle: Add voting options to a mail item
ms:assetid: 0fb209a8-178d-411e-9551-0a72e041fd65
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424466(v=office.15)
ms:contentKeyID: 55119867
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3befe70363d1e2226b8a3a3a6ebb8db39aa2c6ef
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725997"
---
# <a name="add-voting-options-to-a-mail-item"></a><span data-ttu-id="7013c-102">Agregar opciones de votación a un elemento de correo</span><span class="sxs-lookup"><span data-stu-id="7013c-102">Add voting options to a mail item</span></span>

<span data-ttu-id="7013c-103">Este ejemplo muestra cómo usar la propiedad [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) del objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) para agregar opciones de votación a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7013c-103">This example shows how to use the [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) property of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object to add voting options to an email message.</span></span>

## <a name="example"></a><span data-ttu-id="7013c-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7013c-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7013c-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="7013c-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="7013c-p101">Las opciones de votación en los mensajes se usan para darle a los receptores de mensajes una lista de opciones y hacer un seguimiento de sus respuestas. Para crear opciones de votación mediante programación, establezca una cadena, que es una lista delimitada por punto y comas de valores de la propiedad **VotingOptions** del objeto **MailItem**. Los valores de la propiedad **VotingOptions** aparecerán bajo el comando **Votar** en el grupo \*\*Responder \*\* en la cinta de opciones del mensaje recibido. </span><span class="sxs-lookup"><span data-stu-id="7013c-p101">Voting options on messages are used to give message recipients a list of choices and to track their responses. To create voting options programmatically, set a string that is a semicolon-delimited list of values for the **VotingOptions** property of a **MailItem** object. The values for the **VotingOptions** property will appear under the **Vote** command in the **Respond** group in the ribbon of the received message.</span></span>

<span data-ttu-id="7013c-109">En el siguiente ejemplo, OrderPizza crea opciones de votación en un nuevo mensaje de correo.</span><span class="sxs-lookup"><span data-stu-id="7013c-109">In the following example, OrderPizza creates voting options in a new mail message.</span></span> <span data-ttu-id="7013c-110">OrderPizza primero crea un **MailItem** y establece la propiedad **VotingOptions** en “Queso; Champiñón; Jamón; Combinado; Combinado de verduras” y la propiedad [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) en “Pedido de pizza”.</span><span class="sxs-lookup"><span data-stu-id="7013c-110">OrderPizza first creates a **MailItem**, and then sets the **VotingOptions** property to “Cheese; Mushroom; Sausage; Combo; Veg Combo”, and the [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) property to “Pizza Order”.</span></span> <span data-ttu-id="7013c-111">Cuando se envía el mensaje “Pedido de pizza” se muestran las opciones de votación a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="7013c-111">When the “Pizza Order” message is sent, the voting options appear to recipients.</span></span> <span data-ttu-id="7013c-112">Para cada respuesta recibida, la opción del destinatario se procesará en la página **Tracking** del mensaje en la carpeta Elementos enviados del remitente.</span><span class="sxs-lookup"><span data-stu-id="7013c-112">For each response received, the recipient’s choice will be tallied on the **Tracking** page of the message in the sender’s Sent Items folder.</span></span>

<span data-ttu-id="7013c-113">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="7013c-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7013c-114">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="7013c-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7013c-115">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="7013c-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void OrderPizza()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.CreateItem(
            Outlook.OlItemType.olMailItem);
        mail.VotingOptions = “Cheese; Mushroom; Sausage; Combo; Veg Combo;”
        mail.Subject = “Pizza Order”;
        mail.Display(false);
    }
```

## <a name="see-also"></a><span data-ttu-id="7013c-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="7013c-116">See also</span></span>

- [<span data-ttu-id="7013c-117">Correo</span><span class="sxs-lookup"><span data-stu-id="7013c-117">Mail</span></span>](mail.md)

