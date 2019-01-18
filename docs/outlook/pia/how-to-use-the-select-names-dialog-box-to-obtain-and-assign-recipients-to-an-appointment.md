---
title: Usar el cuadro de diálogo Seleccionar nombres para obtener y asignar destinatarios a una cita
TOCTitle: Use the Select Names dialog box to obtain and assign recipients to an appointment
ms:assetid: b9bcb341-1912-425c-8d75-ed5be233145a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184636(v=office.15)
ms:contentKeyID: 55119878
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 408d2fbdc3c89b7f2bad1fe9c2c76c1f47ae05ff
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722770"
---
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a>Usar el cuadro de diálogo Seleccionar nombres para obtener y asignar destinatarios a una cita

En este ejemplo se muestra cómo usar el cuadro de diálogo **Seleccionar nombres** para obtener y asignar destinatarios a un elemento de cita.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Para mostrar el cuadro de diálogo **Seleccionar nombres**, llame al método [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) del objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)). Una vez que se muestra al usuario el cuadro de diálogo **Seleccionar nombres**, se detiene la ejecución de código hasta que el usuario hace clic en **Aceptar** o cierra el cuadro de diálogo. Para establecer los destinatarios iniciales que se muestran en el cuadro de diálogo, o para que los destinatarios sean seleccionados en el cuadro de diálogo, use la propiedad [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) del objeto **SelectNamesDialog**. Esto devuelve una colección [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) asociada al objeto **SelectNamesDialog**. Para añadir un objeto de [destinatario](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) a la colección **Recipients** del **SelectNamesDialog**, use el método [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) de la colección y especifique la propiedad [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) del objeto de **destinatario**.

En el ejemplo siguiente, DemoSelectNamesDialogRecipients crea un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) y establece algunas de sus propiedades. A continuación, crea un **SelectNamesDialog** y usa el método [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) para configurar un modo de presentación de la reunión para el cuadro de diálogo **Seleccionar nombres**. En el ejemplo se rellena el selector de destinatario **Resource** con la cadena "Sala de conferencias 36/2739". Una vez que se muestra el cuadro de diálogo al usuario, el código enumera la colección **Recipients** asociada a esta instancia del **SelectNamesDialog** y agrega los destinatarios a la cita que se había creado. Por último, en el ejemplo se muestra la convocatoria de reunión para el usuario.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoSelectNamesDialogRecipients()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Subject = "Team Morale Event";
    appt.Start = DateTime.Parse("5/17/2007 11:00 AM");
    appt.End = DateTime.Parse("5/17/2007 12:00 PM");
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    snd.SetDefaultDisplayMode(
        Outlook.OlDefaultSelectNamesDisplayMode.olDefaultMeeting);
    Outlook.Recipient confRoom =
        snd.Recipients.Add("Conf Room 36/2739");
    // Explicitly specify Recipient.Type.
    confRoom.Type = (int)Outlook.OlMeetingRecipientType.olResource;
    snd.Recipients.ResolveAll();
    snd.Display();
    // Add Recipients to meeting request.
    Outlook.Recipients recips = snd.Recipients;
    if (recips.Count > 0)
    {
        foreach (Outlook.Recipient recip in recips)
        {
            appt.Recipients.Add(recip.Name);
        }
    }
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a>Vea también

- [Destinatarios](recipients.md)

