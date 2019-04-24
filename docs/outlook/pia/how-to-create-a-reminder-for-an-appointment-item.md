---
title: Crear un recordatorio para un elemento de cita
TOCTitle: Create a reminder for an appointment item
ms:assetid: 85e772f0-65ac-4abc-8286-9099882a2400
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184623(v=office.15)
ms:contentKeyID: 55119814
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1f5f31c480f31b01e53fec9651c8154765b581a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349500"
---
# <a name="create-a-reminder-for-an-appointment-item"></a><span data-ttu-id="dc001-102">Crear un recordatorio para un elemento de cita</span><span class="sxs-lookup"><span data-stu-id="dc001-102">Create a reminder for an appointment item</span></span>

<span data-ttu-id="dc001-103">En este ejemplo se muestra cómo usar la propiedad [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) para crear un recordatorio para un elemento de cita.</span><span class="sxs-lookup"><span data-stu-id="dc001-103">This example shows how to use the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property to create a reminder for an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="dc001-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc001-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="dc001-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="dc001-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="dc001-106">Outlook permite establecer un recordatorio para una cita mediante la propiedad [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) del objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="dc001-106">Outlook provides a way to set a reminder for an appointment by using the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="dc001-107">Esta propiedad indica si se ha creado un recordatorio para la cita.</span><span class="sxs-lookup"><span data-stu-id="dc001-107">This property indicates whether a reminder has been created for the appointment.</span></span> <span data-ttu-id="dc001-108">Si se establece la propiedad ReminderSet en true, se crea un recordatorio. Si se establece en false, se elimina el recordatorio.</span><span class="sxs-lookup"><span data-stu-id="dc001-108">Setting the ReminderSet property to true creates a reminder, and setting it to false removes the reminder.</span></span>

<span data-ttu-id="dc001-109">En el ejemplo de código siguiente, ReminderExample crea un recordatorio en una cita privada para una degustación de vino en Napa, California, y establece que el recordatorio se produzca dos horas antes de que empiece la cita.</span><span class="sxs-lookup"><span data-stu-id="dc001-109">In the following code example, ReminderExample creates a reminder on a private appointment for wine tasting in Napa, California, and sets the reminder to occur two hours before the appointment starts.</span></span> <span data-ttu-id="dc001-110">En primer lugar, ReminderExample crea un objeto **AppointmentItem** de Outlook.</span><span class="sxs-lookup"><span data-stu-id="dc001-110">First, ReminderExample creates an Outlook **AppointmentItem** object.</span></span> <span data-ttu-id="dc001-111">Después, establece la propiedad [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) del elemento en [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="dc001-111">It then sets the [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) property for the item to [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)).</span></span> <span data-ttu-id="dc001-112">Esto indica que la cita es una cita privada.</span><span class="sxs-lookup"><span data-stu-id="dc001-112">This indicates that the appointment is a private appointment.</span></span> <span data-ttu-id="dc001-113">Después de establecer otras propiedades de la cita, como las propiedades [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) y [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), ReminderExample establece la propiedad [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) para indicar cuántos minutos antes del inicio de la cita aparecerá el recordatorio.</span><span class="sxs-lookup"><span data-stu-id="dc001-113">After setting other properties of the appointment, such as [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) times, ReminderExample sets the [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) property to indicate the number of minutes that the reminder will appear before the start of the appointment.</span></span> <span data-ttu-id="dc001-114">En este caso, ReminderMinutesBeforeStart se establece en 120 minutos (dos horas).</span><span class="sxs-lookup"><span data-stu-id="dc001-114">In this case, ReminderMinutesBeforeStart is set to 120 minutes (two hours).</span></span>

<span data-ttu-id="dc001-115">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="dc001-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="dc001-116">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="dc001-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="dc001-117">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="dc001-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void ReminderExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Wine Tasting";
    appt.Location = "Napa CA";
    appt.Sensitivity = Outlook.OlSensitivity.olPrivate;
    appt.Start = DateTime.Parse("10/21/2006 10:00 AM");
    appt.End = DateTime.Parse("10/21/2006 3:00 PM");
    appt.ReminderSet = true;
    appt.ReminderMinutesBeforeStart = 120;
    appt.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="dc001-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc001-118">See also</span></span>

- [<span data-ttu-id="dc001-119">Citas</span><span class="sxs-lookup"><span data-stu-id="dc001-119">Appointments</span></span>](appointments.md)

