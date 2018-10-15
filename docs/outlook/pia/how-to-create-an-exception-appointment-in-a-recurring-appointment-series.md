---
title: Crear una excepción para una cita en una serie de citas periódicas
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1344188ad8947245ec0a6d54efff603b9e7755e7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405983"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a>Crear una excepción para una cita en una serie de citas periódicas

En este ejemplo se usa un objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) para crear una excepción en un patrón de periodicidad estándar de una cita.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Una vez que se elimina o cambia una instancia de cita de una cita periódica, Outlook crea un objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)). El objeto Exception le permite crear una excepción en un patrón de periodicidad estándar de una cita. Las propiedades del objeto contienen los cambios realizados en la instancia de la cita. La colección [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) contiene todos los objetos Exception de una cita periódica y está asociada al objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) de la cita.

Para obtener el objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa la excepción en el patrón de periodicidad original de la cita periódica, use la propiedad [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) del objeto Exception. Al usar los métodos y propiedades del objeto AppointmentItem devuelto, puede establecer las propiedades de la excepción de la cita.

Cuando se trabaja con elementos de citas periódicas, debe liberar todas las referencias anteriores, obtener nuevas referencias al elemento de cita periódico antes de tener acceso o modificar el elemento y liberar estas referencias, tan pronto como termine y haya guardado los cambios. Este procedimiento se aplica al objeto periódico **AppointmentItem** y a cualquier objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) o [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Para liberar una referencia en Visual Basic, establezca el objeto existente en Nothing. En C\#, libere explícitamente la memoria para ese objeto.

Tenga en cuenta que incluso después de liberar la referencia e intentar obtener una nueva, si aún hay una referencia activa a uno de los objetos anteriores, mantenida por otro complemento o Outlook, la nueva referencia puede apuntar a una copia obsoleta del objeto. Por lo tanto, es importante liberar las referencias cuando termine con la cita periódica.

En el siguiente ejemplo de código, CreateExceptionExample cambia el asunto de la cita periódica que se creó en el tema [Buscar una cita específica de una serie de citas periódicas](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md) y, a continuación, usa la propiedad AppointmentItem del objeto Exception resultante para recuperar el AppointmentItem que corresponde a la excepción de la cita. Después, CreateExceptionExample cambia las horas de inicio y fin de la excepción de la cita.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateExceptionExample()
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
            Outlook.AppointmentItem myInstance =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (myInstance != null)
            {
                myInstance.Subject = "My Exception";
                myInstance.Save();
                Outlook.RecurrencePattern newPattern =
                    appt.GetRecurrencePattern();
                Outlook.Exception myException =
                    newPattern.Exceptions[1];
                if (myException != null)
                {
                    Outlook.AppointmentItem myNewInstance =
                        myException.AppointmentItem;
                    myNewInstance.Start =
                        DateTime.Parse("7/21/2006 1:00 PM");
                    myNewInstance.End =
                        DateTime.Parse("7/21/2006 2:00 PM");
                    myNewInstance.Save();
                }
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

