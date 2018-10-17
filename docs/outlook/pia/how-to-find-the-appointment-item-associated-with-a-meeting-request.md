---
title: Buscar el elemento de cita asociado a una convocatoria de reunión
TOCTitle: Find the appointment item associated with a meeting request
ms:assetid: ff356fcf-0980-4567-8570-4bbcb14381e7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184658(v=office.15)
ms:contentKeyID: 55119875
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 5fa3822206d86b976bcfa2360cecf3ef22602e96
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407502"
---
# <a name="find-the-appointment-item-associated-with-a-meeting-request"></a><span data-ttu-id="7dbc7-102">Buscar el elemento de cita asociado a una convocatoria de reunión</span><span class="sxs-lookup"><span data-stu-id="7dbc7-102">Find the appointment item associated with a meeting request</span></span>

<span data-ttu-id="7dbc7-103">Este ejemplo muestra cómo usar el método [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) para buscar la cita asociada a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="7dbc7-103">This example shows how to use the [M:Microsoft.Office.Interop.Outlook._MeetingItem.GetAssociatedAppointment(System.Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method to find the appointment that is associated with a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="7dbc7-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7dbc7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7dbc7-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="7dbc7-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="7dbc7-106">Un objeto [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) no representa una cita, sino un mensaje que contiene una solicitud para agregar una cita al calendario del destinatario.</span><span class="sxs-lookup"><span data-stu-id="7dbc7-106">A [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) object does not represent an appointment, but a message that contains a request to add an appointment to the recipient’s calendar.</span></span> <span data-ttu-id="7dbc7-107">En el siguiente ejemplo de código, MeetingRequestExample usa el método [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) del objeto **MeetingItem** en cada **MeetingItem** recuperado desde la Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="7dbc7-107">In the following code example, MeetingRequestExample uses the [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) method of the **MeetingItem** object on each **MeetingItem** retrieved from the user’s Inbox.</span></span> <span data-ttu-id="7dbc7-108">Después, el objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) devuelto se utiliza para escribir el asunto de la cita para los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="7dbc7-108">The returned [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object is then used to write the subject of the appointment to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="7dbc7-109">Tenga en cuenta que el argumento **GetAssociatedAppointment** se establece en **false** para que no se agregue la cita al calendario del usuario.</span><span class="sxs-lookup"><span data-stu-id="7dbc7-109">Note that **GetAssociatedAppointment** argument is set to **false** so that the appointment is not added to the user’s calendar.</span></span>

<span data-ttu-id="7dbc7-110">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="7dbc7-110">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="7dbc7-111">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="7dbc7-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7dbc7-112">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="7dbc7-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void MeetingRequestsExample()
{
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(false);
        if (appt != null)
        {
            Debug.WriteLine(appt.Subject);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="7dbc7-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="7dbc7-113">See also</span></span>

- <span data-ttu-id="7dbc7-114">[Meeting requests](meeting-requests.md) (Convocatorias de reunión)</span><span class="sxs-lookup"><span data-stu-id="7dbc7-114">[meeting requests](meeting-requests.md)</span></span>

