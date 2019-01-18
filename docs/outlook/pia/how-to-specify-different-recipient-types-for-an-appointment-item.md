---
title: Especificar diferentes tipos de destinatarios de un elemento de reunión
TOCTitle: Specify different recipient types for an appointment item
ms:assetid: 83aedc8f-adc0-453d-8e71-1bb9aacc7993
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184622(v=office.15)
ms:contentKeyID: 55119807
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: beb29c46d590938d1650dac0c862dd5f898333fc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709183"
---
# <a name="specify-different-recipient-types-for-an-appointment-item"></a><span data-ttu-id="2a0d3-102">Especificar diferentes tipos de destinatarios de un elemento de reunión</span><span class="sxs-lookup"><span data-stu-id="2a0d3-102">Specify different recipient types for an appointment item</span></span>

<span data-ttu-id="2a0d3-103">En este ejemplo se muestra cómo usar la enumeración [OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) para especificar diferentes tipos de destinatarios para un elemento de cita.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-103">This example shows how to use the [OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) enumeration to specify different recipient types for an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="2a0d3-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a0d3-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="2a0d3-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="2a0d3-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="2a0d3-106">Para agregar destinatarios a un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa una convocatoria de reunión, use la enumeración OlMeetingRecipientType para especificar si el destinatario del mensaje es un asistente obligatorio u opcional, o un recurso (como una sala o equipos). </span><span class="sxs-lookup"><span data-stu-id="2a0d3-106">To add recipients to an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a meeting request, use the OlMeetingRecipientType enumeration to specify whether the recipient of the message is a required or optional attendee, or a resource (such as a room or equipment).</span></span>

<span data-ttu-id="2a0d3-107">En el siguiente ejemplo de código, SetRecipientTypeForAppt crea un objeto **AppointmentItem**, establece las propiedades del objeto y agrega asistentes obligatorios y opcionales.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-107">In the following code example, SetRecipientTypeForAppt creates an **AppointmentItem** object, sets properties for that object, and adds required and optional attendees.</span></span> <span data-ttu-id="2a0d3-108">También agrega una sala de conferencias para la reunión.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-108">It also adds a conference room for the meeting.</span></span> <span data-ttu-id="2a0d3-109">Tenga en cuenta que la propiedad [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) se establece en [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)), lo que indica que la cita es una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-109">Note that the [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) property is set to [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)), indicating that the appointment is a meeting request.</span></span>

<span data-ttu-id="2a0d3-110">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="2a0d3-111">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="2a0d3-112">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="2a0d3-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void SetRecipientTypeForAppt()
{
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Customer Review";
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Location = "36/2021";
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM");
    appt.End = DateTime.Parse("10/20/2006 11:00 AM");
    Outlook.Recipient recipRequired =
        appt.Recipients.Add("Ryan Gregg");
    recipRequired.Type =
        (int)Outlook.OlMeetingRecipientType.olRequired;
    Outlook.Recipient recipOptional =
        appt.Recipients.Add("Peter Allenspach");
    recipOptional.Type =
        (int)Outlook.OlMeetingRecipientType.olOptional;
    Outlook.Recipient recipConf =
        appt.Recipients.Add("Conf Room 36/2021 (14) AV");
    recipConf.Type =
        (int)Outlook.OlMeetingRecipientType.olResource;
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="2a0d3-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a0d3-113">See also</span></span>

- <span data-ttu-id="2a0d3-114">[Appointments](appointments.md) (Citas)</span><span class="sxs-lookup"><span data-stu-id="2a0d3-114">[Appointments](appointments.md)</span></span>

