---
title: Crear una cita que sea un evento de todo el día
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5065395afe39247f8113bc5223b0e3e403a02fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349479"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a><span data-ttu-id="f4469-102">Crear una cita que sea un evento de todo el día</span><span class="sxs-lookup"><span data-stu-id="f4469-102">Create an appointment that is an all-day event</span></span>

<span data-ttu-id="f4469-103">En este ejemplo se muestra cómo usar la propiedad [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) para crear una cita que sea un evento de día completo.</span><span class="sxs-lookup"><span data-stu-id="f4469-103">This example shows how use the [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) property to create an appointment that is an all-day event.</span></span>

## <a name="example"></a><span data-ttu-id="f4469-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4469-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f4469-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="f4469-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="f4469-p101">Un evento difiere de una cita regular en que es una actividad que dura 24 horas o más. Como ejemplos de eventos se encuentran las ferias comerciales, los seminarios o las vacaciones. Los eventos y los eventos anuales no aparecen como bloques de tiempo ocupado en el calendario del usuario, sino que aparecen como titulares. Puede ver los titulares en la parte superior de una vista de calendario diaria o semanal. En las citas de día completo, de forma predeterminada, la hora del usuario se muestra como ocupada cuando otras personas la visualizan, pero se muestra como libre para un evento o evento anual.</span><span class="sxs-lookup"><span data-stu-id="f4469-p101">An event is different from a regular appointment because it is an activity that lasts 24 hours or longer. Examples of events include trade shows, seminars, or vacations. Events and annual events do not appear as occupied blocks of time in the user’s calendar. Instead, they appear as banners. You can see the banners at the top of a calendar day or week view. For an all-day appointment, by default, the user’s time is displayed as busy when viewed by other people, but the user’s time is displayed as free for an event or annual event.</span></span>

<span data-ttu-id="f4469-112">Para crear un evento de todo el día mediante programación, establezca la propiedad [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) del objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) en true.</span><span class="sxs-lookup"><span data-stu-id="f4469-112">To create an all-day event programmatically, set the [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) property of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object to true.</span></span> <span data-ttu-id="f4469-113">Después, establezca las propiedades [Starr](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) y [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) del objeto AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="f4469-113">Then set the [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) properties of the AppointmentItem.</span></span> <span data-ttu-id="f4469-114">Si establece la propiedad AllDayEvent en true y no establece las propiedades Start y End, el evento se producirá en el día de hoy, y será una cita que mostrará el estado Ocupado en el calendario.</span><span class="sxs-lookup"><span data-stu-id="f4469-114">If you set the AllDayEvent property to true and do not set the Start and End properties, the event will occur today, and it will be an appointment, showing a busy status on your calendar.</span></span> <span data-ttu-id="f4469-115">Debe establecer las propiedades Start y End si quiere que el evento se produzca en una fecha futura.</span><span class="sxs-lookup"><span data-stu-id="f4469-115">You must set the Start and End properties if you want the event to occur on a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="f4469-116">Para hacer que la cita sea un evento de todo el día, debe establecer la propiedad Start en 12:00 A. M.</span><span class="sxs-lookup"><span data-stu-id="f4469-116">To make the appointment an all-day event, you must set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="f4469-117">(medianoche) del día en el que quiere que se inicie el evento, y la propiedad End en 12:00 A. M.</span><span class="sxs-lookup"><span data-stu-id="f4469-117">(midnight) on the day you want the event to begin, and set End property to 12:00 A.M.</span></span> <span data-ttu-id="f4469-118">del día en el que quiere que finalice el evento.</span><span class="sxs-lookup"><span data-stu-id="f4469-118">on the day after you want the event to end.</span></span> <span data-ttu-id="f4469-119">Si establece la hora de inicio o finalización en un valor de fecha y hora que no sea las 12:00 A. M., la cita se convertirá en una cita de varios días en lugar de un evento de todo el día.</span><span class="sxs-lookup"><span data-stu-id="f4469-119">If you set the Start or End time to a date and time value other than 12:00 A.M., the appointment will become a multiday appointment instead of an all-day event.</span></span> 
>
> <span data-ttu-id="f4469-120">Por ejemplo, si la duración del evento es de un solo día, establezca la propiedad Start en 12:00 A. M.</span><span class="sxs-lookup"><span data-stu-id="f4469-120">For example, if your event duration is only one day, set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="f4469-121">del día en el que quiere que se inicie el evento, y establezca la propiedad End en 12:00 A. M.</span><span class="sxs-lookup"><span data-stu-id="f4469-121">on the day you want the event to begin, and set the End property to 12:00 A.M.</span></span> <span data-ttu-id="f4469-122">del día siguiente.</span><span class="sxs-lookup"><span data-stu-id="f4469-122">on the following day.</span></span> <span data-ttu-id="f4469-123">Debe establecer siempre la propiedad End en 12:00 A. M.</span><span class="sxs-lookup"><span data-stu-id="f4469-123">You should always set the End property to 12:00 A.M.</span></span> <span data-ttu-id="f4469-124">en una fecha que sea más de un día después de la fecha de inicio.</span><span class="sxs-lookup"><span data-stu-id="f4469-124">on a date that is more than one day after the start date.</span></span>

<span data-ttu-id="f4469-p105">En el siguiente ejemplo de código, AllDayEventExample crea un evento de día completo que comienza el 11 de junio de 2007 y finaliza el 15 de junio de 2007. Observe que la propiedad End de la cita está ajustada en 12:00 a.m. del día 16 de junio de 2007.</span><span class="sxs-lookup"><span data-stu-id="f4469-p105">In the following code example, AllDayEventExample creates an all-day event that begins on June 11, 2007, and ends on June 15, 2007. Note that the End property for the appointment is set to 12:00 A.M. on June 16, 2007.</span></span>

<span data-ttu-id="f4469-128">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f4469-128">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="f4469-129">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="f4469-129">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="f4469-130">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="f4469-130">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AllDayEventExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Developer's Conference";
    appt.AllDayEvent = true;
    appt.Start = DateTime.Parse("6/11/2007 12:00 AM");
    appt.End = DateTime.Parse("6/16/2007 12:00 AM");
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="f4469-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4469-131">See also</span></span>

- [<span data-ttu-id="f4469-132">Citas</span><span class="sxs-lookup"><span data-stu-id="f4469-132">Appointments</span></span>](appointments.md)

