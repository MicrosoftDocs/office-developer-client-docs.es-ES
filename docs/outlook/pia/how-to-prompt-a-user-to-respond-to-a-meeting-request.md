---
title: Mostrar una notificación al usuario para que responda a una convocatoria de reunión
TOCTitle: Prompt a user to respond to a meeting request
ms:assetid: a0d69f82-8659-457d-9418-1a897a10882f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184630(v=office.15)
ms:contentKeyID: 55119877
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26e59cca7431e9f11f3fea5fa058548b9a5903a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320051"
---
# <a name="prompt-a-user-to-respond-to-a-meeting-request"></a><span data-ttu-id="c0831-102">Mostrar una notificación al usuario para que responda a una convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="c0831-102">Prompt a user to respond to a meeting request</span></span>

<span data-ttu-id="c0831-103">En este ejemplo se muestra cómo solicitar al usuario una respuesta a una convocatoria de reunión y cómo habilitar al usuario para que edite la respuesta antes de enviarla.</span><span class="sxs-lookup"><span data-stu-id="c0831-103">This example shows how to prompt the user for a response to a meeting request, and to enable the user to edit the response before sending it.</span></span>

## <a name="example"></a><span data-ttu-id="c0831-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0831-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c0831-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="c0831-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="c0831-106">El método [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) del objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) se usa para notificar al organizador de la reunión si la reunión se ha aceptado, rechazado o agregado provisionalmente al calendario del destinatario.</span><span class="sxs-lookup"><span data-stu-id="c0831-106">The [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object is used to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient’s calendar.</span></span> <span data-ttu-id="c0831-107">Al usar el método **Respond**, puede indicar si quiere que la invitación se envíe automáticamente o si quiere que el usuario pueda editar la respuesta antes de enviarla.</span><span class="sxs-lookup"><span data-stu-id="c0831-107">By using the **Respond** method, you can indicate whether you want to send the notification automatically, or whether you want to allow the user to edit the response before sending it.</span></span> <span data-ttu-id="c0831-108">El método **Respond** acepta tres parámetros.</span><span class="sxs-lookup"><span data-stu-id="c0831-108">The **Respond** method accepts three parameters.</span></span> <span data-ttu-id="c0831-109">El parámetro *Response* indica si la respuesta es aceptar, rechazar o agregar provisionalmente.</span><span class="sxs-lookup"><span data-stu-id="c0831-109">The *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="c0831-110">Los parámetros *fNoUI* y *fAdditionalTextDialog* son valores **booleanos** que determinan si se enviará una respuesta al organizador y si el usuario puede o no editar la respuesta, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c0831-110">The *fNoUI* and *fAdditionalTextDialog* parameters are **bool** values that indicate whether the response will be sent to the organizer, and whether the user can edit the body of the response before sending it, respectively.</span></span> 

<span data-ttu-id="c0831-111">En el siguiente ejemplo de código, PromptUserMeetingRequest enumera todos los objetos [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) para obtener los objetos **AppointmentItem** asociados, y luego llama al método **Respond** con el parámetro *fNoUI* establecido en **false** y el parámetro *fAdditionalTextDialog* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="c0831-111">In the following code example, PromptUserMeetingRequest enumerates through the [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) objects to get the associated **AppointmentItem** objects, and then calls the **Respond** method with the *fNoUI* parameter set to **false** and the *fAdditionalTextDialog* parameter set to **true**.</span></span> <span data-ttu-id="c0831-112">Esto permite al usuario elegir si desea enviar una respuesta y si quiere editar el cuerpo de la respuesta antes de enviarla.</span><span class="sxs-lookup"><span data-stu-id="c0831-112">This allows the user to choose whether to send a response, and whether to edit the body of the response before sending it.</span></span>

<span data-ttu-id="c0831-113">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c0831-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c0831-114">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="c0831-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c0831-115">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="c0831-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void PromptUserMeetingRequest()
{
    Outlook.MeetingItem mtgResponse;
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(true);
        if (appt != null)
        {
            mtgResponse = appt.Respond(
                Outlook.OlMeetingResponse.olMeetingAccepted,
                false, true);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c0831-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0831-116">See also</span></span>

- <span data-ttu-id="c0831-117">[Meeting requests](meeting-requests.md) (Convocatorias de reunión)</span><span class="sxs-lookup"><span data-stu-id="c0831-117">[Meeting requests](meeting-requests.md)</span></span>

