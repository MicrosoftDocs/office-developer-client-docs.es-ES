---
title: Agregar una acción personalizada como respuesta a un elemento de correo
TOCTitle: Add a custom action as a response to a mail item
ms:assetid: 99e8ba6b-9c47-4b10-968b-436b08d199ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424474(v=office.15)
ms:contentKeyID: 55119870
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6a82b02d357f86ca37d3ec4987ea6323d6d59cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359755"
---
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a><span data-ttu-id="0d3e3-102">Agregar una acción personalizada como respuesta a un elemento de correo</span><span class="sxs-lookup"><span data-stu-id="0d3e3-102">Add a custom action as a response to a mail item</span></span>

<span data-ttu-id="0d3e3-103">Este ejemplo muestra cómo agregar acciones personalizadas como respuesta a un elemento de correo electrónico mediante el método [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) de la colección [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0d3e3-103">This example shows how to add custom actions as a response to an email item by using the [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) method of the [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)) collection.</span></span>

## <a name="example"></a><span data-ttu-id="0d3e3-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0d3e3-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0d3e3-105">El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0d3e3-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="0d3e3-106">Puede crear acciones personalizadas mediante programación para que aparezcan en la cinta del grupo **Acciones** en la ficha **Mensaje** en una respuesta de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0d3e3-106">You can create custom actions programmatically to appear on the ribbon in the **Actions** group on the **Message** tab in an email response.</span></span> <span data-ttu-id="0d3e3-107">En el ejemplo de código siguiente, ReplyWithVoiceMail crea y agrega una acción personalizada denominada "Responder con correo de voz" a la barra de comandos del inspector.</span><span class="sxs-lookup"><span data-stu-id="0d3e3-107">In the following code example, ReplyWithVoiceMail creates and adds a custom action named “Reply with Voice Mail” to the inspector command bar.</span></span> <span data-ttu-id="0d3e3-108">ReplyWithVoiceMail primero obtiene un objeto [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) y, luego, crea un objeto [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) llamando al método **Add** de la colección **Actions** que está asociada al **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="0d3e3-108">ReplyWithVoiceMail first gets a [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) object and then creates an [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) object by calling the **Add** method of the **Actions** collection that is associated with the **MailItem**.</span></span> <span data-ttu-id="0d3e3-109">Después, establece la propiedad [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) del objeto **Action** en "Responder con correo de voz".</span><span class="sxs-lookup"><span data-stu-id="0d3e3-109">It then sets the [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) property of the **Action** object to “Reply with Voice Mail”.</span></span> <span data-ttu-id="0d3e3-110">También se establecen las propiedades [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)), y [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0d3e3-110">The [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)), and [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) properties are also set.</span></span> <span data-ttu-id="0d3e3-111">Por último, se guarda el **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="0d3e3-111">Finally, the **MailItem** is saved.</span></span>


> [!NOTE]
> <span data-ttu-id="0d3e3-112">También puede agregar acciones personalizadas en tiempo de diseño con el Outlook Forms Designer.</span><span class="sxs-lookup"><span data-stu-id="0d3e3-112">You can also add custom actions at design time by using the Outlook Forms Designer.</span></span>


<span data-ttu-id="0d3e3-113">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="0d3e3-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0d3e3-114">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="0d3e3-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0d3e3-115">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="0d3e3-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void ReplyWithVoiceMail()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.ActiveInspector().CurrentItem;
        Outlook.Action action = mail.Actions.Add();
        action.Name = “Reply with Voice Mail”;
        action.ReplyStyle = Outlook.OlActionReplyStyle.olUserPreference;
        action.ResponseStyle = Outlook.OlActionResponseStyle.olOpen;
        action.CopyLike = Outlook.OlActionCopyLike.olReply;
        action.MessageClass = “IPM.Post.Voice Message”;
        mail.Save();
    }
```

## <a name="see-also"></a><span data-ttu-id="0d3e3-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d3e3-116">See also</span></span>

- [<span data-ttu-id="0d3e3-117">Correo</span><span class="sxs-lookup"><span data-stu-id="0d3e3-117">Mail</span></span>](mail.md)

