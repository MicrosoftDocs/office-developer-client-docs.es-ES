---
title: Crear una cita periódica mediante el patrón de periodicidad predeterminado
TOCTitle: Create a recurring appointment by using the default recurrence pattern
ms:assetid: 157bf1ae-2efe-4783-99ea-606722dde204
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184589(v=office.15)
ms:contentKeyID: 55119809
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: de58523e663349c43cc358f5b76896987a0f23b3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722819"
---
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a>Crear una cita periódica mediante el patrón de periodicidad predeterminado

En este ejemplo se muestra cómo crear una cita periódica con el patrón de periodicidad predeterminado.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Al crear una cita en Outlook, se crea un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). La cita es una cita periódica, si la propiedad [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) de AppointmentItem se establece como verdadera. IsRecurring no puede establecerse directamente. 

Pero, puede crear una cita periódica utilizando el objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Para crear una cita periódica mediante programación, cree un objeto **AppointmentItem**, llame al método [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) del objeto **AppointmentItem** y, luego, guarde el objeto **AppointmentItem**. Se crea una cita que usa el patrón de periodicidad predeterminado que se produce semanalmente en el día de la semana para el que se creó la cita y no tiene fecha de finalización. El objeto RecurrencePattern le permite crear citas periódicas a intervalos específicos: diaria, semanal, mensual o anual. Si no especifica los intervalos para el objeto RecurrencePattern, Outlook utilizará el patrón de periodicidad predeterminado.

Cuando se trabaja con elementos de citas periódicas, debe liberar todas las referencias anteriores, obtener nuevas referencias al elemento de cita periódico antes de tener acceso o modificar el elemento y liberar estas referencias, tan pronto como termine y haya guardado los cambios. Este procedimiento se aplica al objeto periódico **AppointmentItem** y a cualquier objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) o [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Para liberar una referencia en Visual Basic, establezca el objeto existente en Nothing. En C\#, libere explícitamente la memoria para ese objeto.

Tenga en cuenta que incluso después de liberar la referencia e intentar obtener una nueva, si aún hay una referencia activa (retenida por otro complemento o Outlook) a uno de los objetos anteriores, la nueva referencia seguirá apuntando a una copia no actualizada del objeto. Por lo tanto, es importante liberar las referencias cuando termine con la cita periódica.

En el ejemplo siguiente, CreateRecurringAppointment crea un objeto **AppointmentItem**. Luego, llama al GetRecurrencePattern. GetRecurrencePattern devuelve un objeto RecurrencePattern y se guarda el objeto AppointmentItem. Se crea una cita periódica mediante el patrón de periodicidad predeterminado.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de Clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateRecurringAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Weekly Extensibility Team Meeting";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    appt.Save();
}
```

## <a name="see-also"></a>Vea también

- [Citas](appointments.md)

