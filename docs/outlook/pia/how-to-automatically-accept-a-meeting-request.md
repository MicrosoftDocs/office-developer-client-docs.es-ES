---
title: Aceptar automáticamente una convocatoria de reunión
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f546b4e2de2a77034fdfeca4d685d7b7f909f40a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700335"
---
# <a name="automatically-accept-a-meeting-request"></a><span data-ttu-id="c2f70-102">Aceptar automáticamente una convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="c2f70-102">Automatically accept a meeting request</span></span>

<span data-ttu-id="c2f70-103">En este ejemplo se muestra cómo usar el método [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) para aceptar automáticamente una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="c2f70-103">This example shows how to use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method to automatically accept a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="c2f70-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2f70-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c2f70-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="c2f70-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="c2f70-106">Un objeto [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) representa una solicitud para añadir una cita, representada por un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), al calendario de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="c2f70-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object represents a request to add an appointment, represented by an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, to a recipient’s calendar.</span></span> <span data-ttu-id="c2f70-107">Para responder a una convocatoria de reunión, use el método [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) para obtener el **AppointmentItem** asociado a la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="c2f70-107">To respond to a meeting request, use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to obtain the **AppointmentItem** associated with the meeting request.</span></span> <span data-ttu-id="c2f70-108">Después use el método [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) del **AppointmentItem** para notificar al organizador de la reunión si la reunión se ha aceptado, rechazado, agregado provisionalmente al calendario del destinatario.</span><span class="sxs-lookup"><span data-stu-id="c2f70-108">Then use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the **AppointmentItem** to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient’s calendar.</span></span> <span data-ttu-id="c2f70-109">El método **Respond** acepta tres parámetros.</span><span class="sxs-lookup"><span data-stu-id="c2f70-109">The **Respond** method accepts three parameters.</span></span> 

<span data-ttu-id="c2f70-110">El parámetro *Response* indica si la respuesta es aceptar, rechazar o agregar provisionalmente.</span><span class="sxs-lookup"><span data-stu-id="c2f70-110">The *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="c2f70-111">Los parámetros fNoUI y fAdditionalTextDialog son valores **booleanos** que determinan si se enviará una respuesta, y si el usuario puede o no editar la respuesta, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c2f70-111">The fNoUI and fAdditionalTextDialog parameters are **bool** values that determine whether a response will be sent, and whether the user may or may not edit the response, respectively.</span></span> <span data-ttu-id="c2f70-112">En el ejemplo de código siguiente, AutoAcceptMeetingRequests enumera todos los objetos **MeetingItem** para obtener el **AppointmentItem** asociado.</span><span class="sxs-lookup"><span data-stu-id="c2f70-112">In the following code example, AutoAcceptMeetingRequests enumerates through every **MeetingItem** object to get the associated **AppointmentItem**.</span></span> <span data-ttu-id="c2f70-113">AutoAcceptMeetingRequests usa después el método **Respond** con el parámetro *fNoUI* establecido en **true** para indicar que se enviará una respuesta automáticamente para aceptar la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="c2f70-113">AutoAcceptMeetingRequests then uses the **Respond** method with the *fNoUI* parameter set to **true** to indicate that a response will be sent automatically to accept the meeting request.</span></span>

<span data-ttu-id="c2f70-114">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c2f70-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c2f70-115">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="c2f70-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c2f70-116">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="c2f70-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AutoAcceptMeetingRequests()
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
                true, Type.Missing);
            mtgResponse.Send();
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c2f70-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2f70-117">See also</span></span>

- <span data-ttu-id="c2f70-118">[Meeting requests](meeting-requests.md) (Convocatorias de reunión)</span><span class="sxs-lookup"><span data-stu-id="c2f70-118">[Meeting requests](meeting-requests.md)</span></span>

