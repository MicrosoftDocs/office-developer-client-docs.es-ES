---
title: Crear una cita de periodicidad anual que usa un patrón YearNth
TOCTitle: Create an annual recurring appointment that uses a YearNth pattern
ms:assetid: 5fb2ad0b-248c-417d-8868-52e0550d970f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184611(v=office.15)
ms:contentKeyID: 55119811
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc50166674ee7b9699ef8e29c5ff1e54db705ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349507"
---
# <a name="create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern"></a><span data-ttu-id="d1a6b-102">Crear una cita de periodicidad anual que usa un patrón YearNth</span><span class="sxs-lookup"><span data-stu-id="d1a6b-102">Create an annual recurring appointment that uses a YearNth pattern</span></span>

<span data-ttu-id="d1a6b-103">En este ejemplo se muestra cómo crear una cita para la cual el patrón de periodicidad anual es un día específico, como el primer lunes de junio.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-103">This example shows how to create an appointment for which the annual recurrence pattern is a specific day such as the first Monday in June.</span></span>

## <a name="example"></a><span data-ttu-id="d1a6b-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d1a6b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d1a6b-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="d1a6b-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="d1a6b-106">Si desea crear una cita anual que se repita un día específico de la semana durante un mes específico (por ejemplo, el primer lunes de junio), debe usar periodicidades YearNth.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-106">If you want to create an annual appointment that recurs on a specific day of the week during a specific month (for example, the first Monday in June), you must use YearNth recurrences.</span></span> <span data-ttu-id="d1a6b-107">Para establecer una periodicidad YearNth, primero debe establecer la propiedad [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) del objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) en olRecursYearNth.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-107">To set a YearNth recurrence, you must first set the [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) property of the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object to olRecursYearNth.</span></span> <span data-ttu-id="d1a6b-108">Después tiene que establecer la propiedad [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)) para especificar qué día de la semana se debe repetir la cita, y la propiedad [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)) para especificar la periodicidad Nth del día de la semana especificado (por ejemplo, el tercer martes) durante un mes especificado para el patrón anual.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-108">Then set the [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)) property to specify on which day of the week the appointment should recur, and the [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)) property to specify the Nth occurrence of the specified day of the week (for example, the third Tuesday) during a specified month for the yearly pattern.</span></span>

<span data-ttu-id="d1a6b-109">Cuando se trabaja con elementos de citas periódicas, debe liberar todas las referencias anteriores, obtener nuevas referencias al elemento de cita periódico antes de tener acceso o modificar el elemento y liberar estas referencias, tan pronto como termine y haya guardado los cambios.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-109">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="d1a6b-110">Este procedimiento se aplica al objeto periódico **AppointmentItem** y a cualquier objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) o [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d1a6b-110">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="d1a6b-111">Para liberar una referencia en Visual Basic, establezca el objeto existente en Nothing.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-111">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="d1a6b-112">En C\#, libere explícitamente la memoria para ese objeto.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-112">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="d1a6b-p103">Tenga en cuenta que incluso después de liberar la referencia e intentar obtener una nueva, si aún hay una referencia activa (retenida por otro complemento o Outlook) a uno de los objetos anteriores, la nueva referencia seguirá apuntando a una copia no actualizada del objeto. Por lo tanto, es importante liberar las referencias cuando termine con la cita periódica.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-p103">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="d1a6b-115">En el ejemplo de código siguiente, RecurringYearNthAppointment crea una cita con un patrón de periodicidad YearNth.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-115">In the following code example, RecurringYearNthAppointment creates an appointment that has a YearNth recurrence pattern.</span></span> <span data-ttu-id="d1a6b-116">En primer lugar, RecurringYearNthAppointment crea una cita periódica mediante la creación de un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d1a6b-116">RecurringYearNthAppointment first creates a recurring appointment by creating an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="d1a6b-117">Después obtiene el patrón de periodicidad de la cita usando el método [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d1a6b-117">Next, it gets the appointment’s recurrence pattern by using the [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) method.</span></span> <span data-ttu-id="d1a6b-118">Luego establece las siguientes propiedades de RecurrencePattern: RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)) y [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d1a6b-118">It then sets the following RecurrencePattern properties: RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)), and [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)).</span></span> <span data-ttu-id="d1a6b-119">La propiedad MonthOfYear puede tomar un valor numérico de 1 a 12, donde cada número representa el mes correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-119">The MonthOfYear property can take a numerical value of 1 through 12, where each number represents the corresponding month.</span></span> <span data-ttu-id="d1a6b-120">Una vez que estén establecidas las propiedades, RecurringYearNthAppointment guarda la cita y, después, la muestra con el patrón "Occurs the first Monday of June effective 6/1/2007 until 6/6/2016 from 2:00 PM to 5:00 PM".</span><span class="sxs-lookup"><span data-stu-id="d1a6b-120">Once the properties are set, RecurringYearNthAppointment saves the appointment, and then displays it with the pattern "Occurs the first Monday of June effective 6/1/2007 until 6/6/2016 from 2:00 PM to 5:00 PM."</span></span>

<span data-ttu-id="d1a6b-121">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="d1a6b-122">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="d1a6b-123">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="d1a6b-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringYearNthAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring YearNth Appointment";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearNth;
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday;
    pattern.MonthOfYear = 6;
    pattern.Instance = 1;
    pattern.Occurrences = 10;
    pattern.Duration = 180;
    pattern.PatternStartDate = DateTime.Parse("6/1/2007");
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("5:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="d1a6b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1a6b-124">See also</span></span>

- [<span data-ttu-id="d1a6b-125">Citas</span><span class="sxs-lookup"><span data-stu-id="d1a6b-125">Appointments</span></span>](appointments.md)

