---
title: Crear una convocatoria de reunión, agregar destinatarios y especificar una ubicación
TOCTitle: Create a meeting request, add recipients, and specify a location
ms:assetid: 3053c27e-34d9-440e-9b66-06de940c2813
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644964(v=office.15)
ms:contentKeyID: 55119873
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 0f637d3d21f79ec538d10cf509fb09f5abf0b0ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351432"
---
# <a name="create-a-meeting-request-add-recipients-and-specify-a-location"></a><span data-ttu-id="ed705-102">Crear una convocatoria de reunión, agregar destinatarios y especificar una ubicación</span><span class="sxs-lookup"><span data-stu-id="ed705-102">Create a meeting request, add recipients, and specify a location</span></span>

<span data-ttu-id="ed705-103">En este ejemplo se crea un elemento de cita como una convocatoria de reunión, se especifica la hora, los destinatarios y la ubicación de la reunión; además, se muestra la cita en un inspector.</span><span class="sxs-lookup"><span data-stu-id="ed705-103">This example creates an appointment item as a meeting request, specifies the time, recipients, and location of the meeting, and displays the appointment in an inspector.</span></span>

## <a name="example"></a><span data-ttu-id="ed705-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed705-104">Example</span></span>

<span data-ttu-id="ed705-105">En Outlook, una convocatoria de reunión es un [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ed705-105">In Outlook, a meeting request is an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span></span> <span data-ttu-id="ed705-106">Para configurar un elemento de reunión como una convocatoria de reunión, debe establecer la propiedad [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) en **olMeeting**.</span><span class="sxs-lookup"><span data-stu-id="ed705-106">To set an appointment item as a meeting request, you must set the [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) property to **olMeeting**.</span></span> <span data-ttu-id="ed705-107">Use la propiedad [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) del objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) para especificar si asistir a la reunión es opcional o si un destinatario es un recurso de la reunión en lugar de un asistente.</span><span class="sxs-lookup"><span data-stu-id="ed705-107">Use the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of the [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object to specify if the meeting attendee is optional, or if a recipient is actually a meeting resource instead of an attendee.</span></span>

<span data-ttu-id="ed705-108">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ed705-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ed705-109">La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="ed705-109">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ed705-110">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="ed705-110">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SetRecipientTypeForAppt()
    Dim appt As Outlook.AppointmentItem = _
        CType(Application.CreateItem( _
        Outlook.OlItemType.olAppointmentItem), Outlook.AppointmentItem)
    appt.Subject = "Customer Review"
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting
    appt.Location = "36/2021"
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM")
    appt.End = DateTime.Parse("10/20/2006 11:00 AM")
    Dim recipRequired As Outlook.Recipient = _
        appt.Recipients.Add("Ryan Gregg")
    recipRequired.Type = _
        Outlook.OlMeetingRecipientType.olRequired
    Dim recipOptional As Outlook.Recipient = _
        appt.Recipients.Add("Peter Allenspach")
    recipOptional.Type = _
        Outlook.OlMeetingRecipientType.olOptional
    Dim recipConf As Outlook.Recipient = _
        appt.Recipients.Add("Conf Room 36/2021 (14) AV")
    recipConf.Type = _
        Outlook.OlMeetingRecipientType.olResource
    appt.Recipients.ResolveAll()
    appt.Display(False)
End Sub
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

## <a name="see-also"></a><span data-ttu-id="ed705-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed705-111">See also</span></span>

- <span data-ttu-id="ed705-112">[Meeting requests](meeting-requests.md) (Convocatorias de reunión)</span><span class="sxs-lookup"><span data-stu-id="ed705-112">[Meeting requests](meeting-requests.md)</span></span>

