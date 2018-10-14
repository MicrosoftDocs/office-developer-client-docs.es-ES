---
title: Crear un recordatorio para un elemento de cita
TOCTitle: Create a reminder for an appointment item
ms:assetid: 85e772f0-65ac-4abc-8286-9099882a2400
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184623(v=office.15)
ms:contentKeyID: 55119814
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 164e744e03ab0984265736673c71d2d0bf57bf45
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405976"
---
# <a name="create-a-reminder-for-an-appointment-item"></a>Crear un recordatorio para un elemento de cita

En este ejemplo se muestra cómo usar la propiedad [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) para crear un recordatorio para un elemento de cita.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).


Outlook permite establecer un recordatorio para una cita mediante la propiedad [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) del objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Esta propiedad indica si se ha creado un recordatorio para la cita. Si se establece la propiedad ReminderSet en true, se crea un recordatorio. Si se establece en false, se elimina el recordatorio.

En el ejemplo de código siguiente, ReminderExample crea un recordatorio en una cita privada para una degustación de vino en Napa, California, y establece que el recordatorio se produzca dos horas antes de que empiece la cita. En primer lugar, ReminderExample crea un objeto **AppointmentItem** de Outlook. Después, establece la propiedad [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) del elemento en [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)). Esto indica que la cita es una cita privada. Después de establecer otras propiedades de la cita, como las propiedades [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) y [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), ReminderExample establece la propiedad [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) para indicar cuántos minutos antes del inicio de la cita aparecerá el recordatorio. En este caso, ReminderMinutesBeforeStart se establece en 120 minutos (dos horas).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Citas](appointments.md)

