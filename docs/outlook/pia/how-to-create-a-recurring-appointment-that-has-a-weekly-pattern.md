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
# <a name="create-a-recurring-appointment-that-has-a-weekly-pattern"></a>Crear una cita periódica con un patrón semanal

En este ejemplo se muestra cómo crear una cita periódica que tenga un patrón semanal (por ejemplo, una cita que se produzca todos los lunes, miércoles y viernes).

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Cuando se crea una nueva cita periódica, el patrón de periodicidad se basa en el tiempo que especifique al crear la cita. Por ejemplo, si crea una cita que se repite cada día a las 13:00, la cita se repetirá solo a las 13:00 cada día. Para cambiar el patrón de periodicidad de una cita, establezca las propiedades del objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) de la cita. Establezca la propiedad [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) del objeto RecurrencePattern antes de establecer otras propiedades RecurrencePattern. La siguiente tabla muestra las propiedades de RecurrencePattern válidas para un determinado RecurrenceType (especificada por la enumeración [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\))).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>El valor OlRecurrenceType</p></th>
<th><p>Propiedades válidas de RecurrencePattern</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>olRecursDaily</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></p></td>
</tr>
<tr class="even">
<td><p>olRecursWeekly</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="odd">
<td><p>olRecursMonthly</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="even">
<td><p>olRecursMonthNth</p></td>
<td><p>DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="odd">
<td><p>olRecursYearly</p></td>
<td><p>DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="even">
<td><p>olRecursYearNth</p></td>
<td><p>DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
</tbody>
</table>


Cuando se trabaja con elementos de citas periódicas, debe liberar todas las referencias anteriores, obtener nuevas referencias al elemento de cita periódico antes de tener acceso o modificar el elemento y liberar estas referencias, tan pronto como termine y haya guardado los cambios. Este procedimiento se aplica al objeto periódico **AppointmentItem** y a cualquier objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) o [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Para liberar una referencia en Visual Basic, establezca el objeto existente en Nothing. En C\#, libere explícitamente la memoria para ese objeto.

Tenga en cuenta que incluso después de liberar la referencia e intentar obtener una nueva, si aún hay una referencia activa (retenida por otro complemento o Outlook) a uno de los objetos anteriores, la nueva referencia seguirá apuntando a una copia no actualizada del objeto. Por lo tanto, es importante liberar las referencias cuando termine con la cita periódica.

En el ejemplo de código siguiente, RecurringAppointmentEveryMondayWednesdayFriday crea un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) y, luego, llama a [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) para el recién creado objeto RecurrencePattern de la cita. Luego, RecurringAppointmentEveryMondayWednesdayFriday establece las propiedades RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime y Subject, guarda la cita y, por último, muestra la cita con el patrón "Se produce los lunes, los miércoles y los viernes desde el 10/7/2006 hasta el 25/8/2006 de 14:00 a 15:00."

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Citas](appointments.md)

