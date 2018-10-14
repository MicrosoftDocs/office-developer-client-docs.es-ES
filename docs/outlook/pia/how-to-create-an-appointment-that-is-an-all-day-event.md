---
title: Crear una cita que sea un evento de todo el día
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 79bffb9185db43395df7254bc353ac24b65d717a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405941"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a>Crear una cita que sea un evento de todo el día

En este ejemplo se muestra cómo usar la propiedad [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) para crear una cita que sea un evento de día completo.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Un evento difiere de una cita regular en que es una actividad que dura 24 horas o más. Como ejemplos de eventos se encuentran las ferias comerciales, los seminarios o las vacaciones. Los eventos y los eventos anuales no aparecen como bloques de tiempo ocupado en el calendario del usuario, sino que aparecen como titulares. Puede ver los titulares en la parte superior de una vista de calendario diaria o semanal. En las citas de día completo, de forma predeterminada, la hora del usuario se muestra como ocupada cuando otras personas la visualizan, pero se muestra como libre para un evento o evento anual.

Para crear un evento de todo el día mediante programación, establezca la propiedad [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) del objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) en true. Después, establezca las propiedades [Starr](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) y [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) del objeto AppointmentItem. Si establece la propiedad AllDayEvent en true y no establece las propiedades Start y End, el evento se producirá en el día de hoy, y será una cita que mostrará el estado Ocupado en el calendario. Debe establecer las propiedades Start y End si quiere que el evento se produzca en una fecha futura.

> [!NOTE]
> Para hacer que la cita sea un evento de todo el día, debe establecer la propiedad Start en 12:00 A. M. (medianoche) del día en el que quiere que se inicie el evento, y la propiedad End en 12:00 A. M. del día en el que quiere que finalice el evento. Si establece la hora de inicio o finalización en un valor de fecha y hora que no sea las 12:00 A. M., la cita se convertirá en una cita de varios días en lugar de un evento de todo el día. 
>
> Por ejemplo, si la duración del evento es de un solo día, establezca la propiedad Start en 12:00 A. M. del día en el que quiere que se inicie el evento, y establezca la propiedad End en 12:00 A. M. del día siguiente. Debe establecer siempre la propiedad End en 12:00 A. M. en una fecha que sea más de un día después de la fecha de inicio.

En el siguiente ejemplo de código, AllDayEventExample crea un evento de día completo que comienza el 11 de junio de 2007 y finaliza el 15 de junio de 2007. Observe que la propiedad End de la cita está ajustada en 12:00 a.m. del día 16 de junio de 2007.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Citas](appointments.md)

