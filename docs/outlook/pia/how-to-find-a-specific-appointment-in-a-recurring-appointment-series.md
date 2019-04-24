---
title: Buscar una cita específica de una serie de citas periódicas
TOCTitle: Find a specific appointment in a recurring appointment series
ms:assetid: 01f55f04-7245-4325-a354-50a6eb270a31
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184586(v=office.15)
ms:contentKeyID: 55119812
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 19502895996d4777f2d1a6887aa80883a5398a09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320255"
---
# <a name="find-a-specific-appointment-in-a-recurring-appointment-series"></a>Buscar una cita específica de una serie de citas periódicas

En este ejemplo se muestra cómo devolver un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa una cita específica de una serie de citas periódicas.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Para buscar una instancia de una cita periódica que se produce en una fecha y hora especificadas, use el método [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) del objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) para devolver un objeto **AppointmentItem**.

Cuando se trabaja con elementos de citas periódicas, debe liberar todas las referencias anteriores, obtener nuevas referencias al elemento de cita periódico antes de tener acceso o modificar el elemento y liberar estas referencias, tan pronto como termine y haya guardado los cambios. Este procedimiento se aplica al objeto periódico **AppointmentItem** y a cualquier objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) o [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Para liberar una referencia en Visual Basic, establezca el objeto existente en Nothing. En C\#, libere explícitamente la memoria para ese objeto.

Tenga en cuenta que incluso después de liberar la referencia e intentar obtener una nueva, si aún hay una referencia activa (retenida por otro complemento o Outlook) a uno de los objetos anteriores, la nueva referencia seguirá apuntando a una copia no actualizada del objeto. Por lo tanto, es importante liberar las referencias cuando termine con la cita periódica.

En el ejemplo siguiente, CheckOccurrenceExample usa la cita periódica que se creó en el ejemplo de código en [Crear una cita periódica con un patrón semanal](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md). Después, llama al método GetOccurrence para determinar si la cita periódica comienza en la fecha y hora especificadas. Para garantizar que continúe el proceso incluso aunque la información proporcionada no coincida con la fecha y hora de inicio de una instancia de la cita periódica, el ejemplo usa un bloque try... catch. Tras llamar al método GetOccurrence en todas las citas de la serie de citas periódicas, CheckOccurrenceExample comprueba la variable singleAppt para determinar si está establecida en una referencia nula, lo que indica que el método no se ejecutó correctamente y no devolvió un objeto **AppointmentItem**.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CheckOccurrenceExample()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find(
        "[Subject]='Recurring Appointment DaysOfWeekMask Example'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        try
        {
            Outlook.RecurrencePattern pattern =
                appt.GetRecurrencePattern();
            Outlook.AppointmentItem singleAppt =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (singleAppt != null)
            {
                Debug.WriteLine("7/21/2006 2:00 PM occurrence found.");
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Citas](appointments.md)

