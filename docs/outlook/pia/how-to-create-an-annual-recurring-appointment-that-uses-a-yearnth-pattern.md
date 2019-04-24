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
# <a name="create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern"></a>Crear una cita de periodicidad anual que usa un patrón YearNth

En este ejemplo se muestra cómo crear una cita para la cual el patrón de periodicidad anual es un día específico, como el primer lunes de junio.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Si desea crear una cita anual que se repita un día específico de la semana durante un mes específico (por ejemplo, el primer lunes de junio), debe usar periodicidades YearNth. Para establecer una periodicidad YearNth, primero debe establecer la propiedad [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) del objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) en olRecursYearNth. Después tiene que establecer la propiedad [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)) para especificar qué día de la semana se debe repetir la cita, y la propiedad [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)) para especificar la periodicidad Nth del día de la semana especificado (por ejemplo, el tercer martes) durante un mes especificado para el patrón anual.

Cuando se trabaja con elementos de citas periódicas, debe liberar todas las referencias anteriores, obtener nuevas referencias al elemento de cita periódico antes de tener acceso o modificar el elemento y liberar estas referencias, tan pronto como termine y haya guardado los cambios. Este procedimiento se aplica al objeto periódico **AppointmentItem** y a cualquier objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) o [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Para liberar una referencia en Visual Basic, establezca el objeto existente en Nothing. En C\#, libere explícitamente la memoria para ese objeto.

Tenga en cuenta que incluso después de liberar la referencia e intentar obtener una nueva, si aún hay una referencia activa (retenida por otro complemento o Outlook) a uno de los objetos anteriores, la nueva referencia seguirá apuntando a una copia no actualizada del objeto. Por lo tanto, es importante liberar las referencias cuando termine con la cita periódica.

En el ejemplo de código siguiente, RecurringYearNthAppointment crea una cita con un patrón de periodicidad YearNth. En primer lugar, RecurringYearNthAppointment crea una cita periódica mediante la creación de un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Después obtiene el patrón de periodicidad de la cita usando el método [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)). Luego establece las siguientes propiedades de RecurrencePattern: RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)) y [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)). La propiedad MonthOfYear puede tomar un valor numérico de 1 a 12, donde cada número representa el mes correspondiente. Una vez que estén establecidas las propiedades, RecurringYearNthAppointment guarda la cita y, después, la muestra con el patrón "Occurs the first Monday of June effective 6/1/2007 until 6/6/2016 from 2:00 PM to 5:00 PM".

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Citas](appointments.md)

