---
title: Crear una cita periódica con un patrón semanal
TOCTitle: Create a recurring appointment that has a weekly pattern
ms:assetid: 20b46b26-e278-451b-9e35-36683205d164
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184595(v=office.15)
ms:contentKeyID: 55119810
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b326ad23f8cbe47e5141775eacdd2bc9302db3cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359174"
---
# <a name="create-a-recurring-appointment-that-has-a-weekly-pattern"></a><span data-ttu-id="3e5b9-102">Crear una cita periódica con un patrón semanal</span><span class="sxs-lookup"><span data-stu-id="3e5b9-102">Create a recurring appointment that has a weekly pattern</span></span>

<span data-ttu-id="3e5b9-103">En este ejemplo se muestra cómo crear una cita periódica que tenga un patrón semanal (por ejemplo, una cita que se produzca todos los lunes, miércoles y viernes).</span><span class="sxs-lookup"><span data-stu-id="3e5b9-103">This example shows how to create a recurring appointment that has a weekly pattern (for example, an appointment that occurs every Monday, Wednesday, and Friday).</span></span>

## <a name="example"></a><span data-ttu-id="3e5b9-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3e5b9-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="3e5b9-105">El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="3e5b9-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="3e5b9-106">Cuando se crea una nueva cita periódica, el patrón de periodicidad se basa en el tiempo que especifique al crear la cita.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-106">When you create a new recurring appointment, the recurrence pattern is based on the time you specify when you create the appointment.</span></span> <span data-ttu-id="3e5b9-107">Por ejemplo, si crea una cita que se repite cada día a las 13:00, la cita se repetirá solo a las 13:00 cada día.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-107">For example, if you create an appointment that recurs daily at 1:00 PM, the appointment will recur only at 1:00 PM on a daily basis.</span></span> <span data-ttu-id="3e5b9-108">Para cambiar el patrón de periodicidad de una cita, establezca las propiedades del objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) de la cita.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-108">To change the recurrence pattern of an appointment, set the properties of the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="3e5b9-109">Establezca la propiedad [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) del objeto RecurrencePattern antes de establecer otras propiedades RecurrencePattern.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-109">Set the [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) property of the RecurrencePattern object before setting other RecurrencePattern properties.</span></span> <span data-ttu-id="3e5b9-110">La siguiente tabla muestra las propiedades de RecurrencePattern válidas para un determinado RecurrenceType (especificada por la enumeración [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="3e5b9-110">The following table shows valid RecurrencePattern properties for a given RecurrenceType (specified by the [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\)) enumeration).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3e5b9-111">El valor OlRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="3e5b9-111">OlRecurrenceType value</span></span></p></th>
<th><p><span data-ttu-id="3e5b9-112">Propiedades válidas de RecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="3e5b9-112">Valid RecurrencePattern properties</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e5b9-113">olRecursDaily</span><span class="sxs-lookup"><span data-stu-id="3e5b9-113">olRecursDaily</span></span></p></td>
<td><p><span data-ttu-id="3e5b9-114"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></span><span class="sxs-lookup"><span data-stu-id="3e5b9-114"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e5b9-115">olRecursWeekly</span><span class="sxs-lookup"><span data-stu-id="3e5b9-115">olRecursWeekly</span></span></p></td>
<td><p><span data-ttu-id="3e5b9-116"><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="3e5b9-116"><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e5b9-117">olRecursMonthly</span><span class="sxs-lookup"><span data-stu-id="3e5b9-117">olRecursMonthly</span></span></p></td>
<td><p><span data-ttu-id="3e5b9-118"><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="3e5b9-118"><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e5b9-119">olRecursMonthNth</span><span class="sxs-lookup"><span data-stu-id="3e5b9-119">olRecursMonthNth</span></span></p></td>
<td><p><span data-ttu-id="3e5b9-120">DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="3e5b9-120">DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e5b9-121">olRecursYearly</span><span class="sxs-lookup"><span data-stu-id="3e5b9-121">olRecursYearly</span></span></p></td>
<td><p><span data-ttu-id="3e5b9-122">DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="3e5b9-122">DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e5b9-123">olRecursYearNth</span><span class="sxs-lookup"><span data-stu-id="3e5b9-123">olRecursYearNth</span></span></p></td>
<td><p><span data-ttu-id="3e5b9-124">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="3e5b9-124">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3e5b9-125">Cuando se trabaja con elementos de citas periódicas, debe liberar todas las referencias anteriores, obtener nuevas referencias al elemento de cita periódico antes de tener acceso o modificar el elemento y liberar estas referencias, tan pronto como termine y haya guardado los cambios.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-125">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="3e5b9-126">Este procedimiento se aplica al objeto periódico **AppointmentItem** y a cualquier objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) o [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3e5b9-126">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="3e5b9-127">Para liberar una referencia en Visual Basic, establezca el objeto existente en Nothing.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-127">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="3e5b9-128">En C\#, libere explícitamente la memoria para ese objeto.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-128">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="3e5b9-p103">Tenga en cuenta que incluso después de liberar la referencia e intentar obtener una nueva, si aún hay una referencia activa (retenida por otro complemento o Outlook) a uno de los objetos anteriores, la nueva referencia seguirá apuntando a una copia no actualizada del objeto. Por lo tanto, es importante liberar las referencias cuando termine con la cita periódica.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-p103">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="3e5b9-131">En el ejemplo de código siguiente, RecurringAppointmentEveryMondayWednesdayFriday crea un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) y, luego, llama a [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) para el recién creado objeto RecurrencePattern de la cita.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-131">In the following code example, RecurringAppointmentEveryMondayWednesdayFriday creates an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, and then calls [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) to get the newly created appointment’s RecurrencePattern object.</span></span> <span data-ttu-id="3e5b9-132">Luego, RecurringAppointmentEveryMondayWednesdayFriday establece las propiedades RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime y Subject, guarda la cita y, por último, muestra la cita con el patrón "Se produce los lunes, los miércoles y los viernes desde el 10/7/2006 hasta el 25/8/2006 de 14:00 a 15:00."</span><span class="sxs-lookup"><span data-stu-id="3e5b9-132">RecurringAppointmentEveryMondayWednesdayFriday then sets the RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime, and Subject properties, saves the appointment, and finally displays the appointment with the pattern "Occurs every Monday, Wednesday, and Friday effective 7/10/2006 until 8/25/2006 from 2:00 PM to 3:00 PM."</span></span>

<span data-ttu-id="3e5b9-133">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-133">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3e5b9-134">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-134">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3e5b9-135">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="3e5b9-135">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringAppointmentEveryMondayWednesdayFriday()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring Appointment DaysOfWeekMask Example";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursWeekly;
    // Logical OR for DayOfWeekMask creates pattern
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday |
        Outlook.OlDaysOfWeek.olWednesday |
        Outlook.OlDaysOfWeek.olFriday;
    pattern.PatternStartDate = DateTime.Parse("7/10/2006");
    pattern.PatternEndDate = DateTime.Parse("8/25/2006");
    pattern.Duration = 60;
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("3:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="3e5b9-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e5b9-136">See also</span></span>

- [<span data-ttu-id="3e5b9-137">Citas</span><span class="sxs-lookup"><span data-stu-id="3e5b9-137">Appointments</span></span>](appointments.md)

