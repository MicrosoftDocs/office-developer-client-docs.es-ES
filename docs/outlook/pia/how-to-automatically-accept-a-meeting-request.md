---
title: Aceptar automáticamente una convocatoria de reunión
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d49044d87cd14c150527d518108f740b9eb319da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405738"
---
# <a name="automatically-accept-a-meeting-request"></a><span data-ttu-id="fb0f0-102">Aceptar automáticamente una convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="fb0f0-102">Automatically accept a meeting request</span></span>

<span data-ttu-id="fb0f0-103">En este ejemplo se muestra cómo usar el método [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) para aceptar automáticamente una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-103">This example shows how to use the M:Microsoft.Office.Interop.Outlook._AppointmentItem.Respond(Microsoft.Office.Interop.Outlook.OlMeetingResponse,System.Object,System.Object) method to automatically accept a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="fb0f0-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb0f0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fb0f0-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="fb0f0-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="fb0f0-106">Un objeto [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) representa una solicitud para añadir una cita, representada por un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), al calendario de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object represents a request to add an appointment, represented by an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, to a recipient’s calendar.</span></span> <span data-ttu-id="fb0f0-107">Para responder a una convocatoria de reunión, use el método [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) para obtener el **AppointmentItem** asociado a la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-107">To respond to a meeting request, use the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to obtain the **AppointmentItem** associated with the meeting request.</span></span> <span data-ttu-id="fb0f0-108">Después use el método [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) del **AppointmentItem** para notificar al organizador de la reunión si la reunión se ha aceptado, rechazado, agregado provisionalmente al calendario del destinatario.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-108">Then use the [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) method of the **AppointmentItem** to notify the meeting organizer whether the meeting has been accepted, declined, or tentatively added to the recipient’s calendar.</span></span> <span data-ttu-id="fb0f0-109">El método **Respond** acepta tres parámetros.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-109">The **GetHiddenRowsOrCols** method accepts three parameters, indicating the following:</span></span> 

<span data-ttu-id="fb0f0-110">El parámetro *Response* indica si la respuesta es aceptar, rechazar o agregar provisionalmente.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-110">The *Response* parameter indicates whether the response is accept, decline, or tentative.</span></span> <span data-ttu-id="fb0f0-111">Los parámetros fNoUI y fAdditionalTextDialog son valores **booleanos** que determinan si se enviará una respuesta, y si el usuario puede o no editar la respuesta, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-111">The fNoUI and fAdditionalTextDialog parameters are **bool** values that determine whether a response will be sent, and whether the user may or may not edit the response, respectively.</span></span> <span data-ttu-id="fb0f0-112">En el ejemplo de código siguiente, AutoAcceptMeetingRequests enumera todos los objetos **MeetingItem** para obtener el **AppointmentItem** asociado.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-112">In the following code example, AutoAcceptMeetingRequests enumerates through every **MeetingItem** object to get the associated **AppointmentItem**.</span></span> <span data-ttu-id="fb0f0-113">AutoAcceptMeetingRequests usa después el método **Respond** con el parámetro *fNoUI* establecido en **true** para indicar que se enviará una respuesta automáticamente para aceptar la convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-113">AutoAcceptMeetingRequests then uses the **Respond** method with the *fNoUI* parameter set to **true** to indicate that a response will be sent automatically to accept the meeting request.</span></span>

<span data-ttu-id="fb0f0-114">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-114">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="fb0f0-115">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="fb0f0-116">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="fb0f0-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="fb0f0-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb0f0-117">See also</span></span>

- <span data-ttu-id="fb0f0-118">[Meeting requests](meeting-requests.md) (Convocatorias de reunión)</span><span class="sxs-lookup"><span data-stu-id="fb0f0-118">[meeting requests](meeting-requests.md)</span></span>

