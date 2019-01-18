---
title: Aceptar automáticamente una convocatoria de reunión
TOCTitle: Automatically accept a meeting request
ms:assetid: 3c729bcf-4c85-4efa-af79-2c94d55c2042
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184604(v=office.15)
ms:contentKeyID: 55119874
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f546b4e2de2a77034fdfeca4d685d7b7f909f40a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700335"
---
# <a name="automatically-accept-a-meeting-request"></a>Aceptar automáticamente una convocatoria de reunión

En este ejemplo se muestra cómo usar el método [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) para aceptar automáticamente una convocatoria de reunión.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).


Un objeto [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) representa una solicitud para añadir una cita, representada por un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), al calendario de un destinatario. Para responder a una convocatoria de reunión, use el método [GetAssociatedAppointment(Boolean)](https://msdn.microsoft.com/library/bb652725\(v=office.15\)) para obtener el **AppointmentItem** asociado a la convocatoria de reunión. Después use el método [Respond(OlMeetingResponse, Object, Object)](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) del **AppointmentItem** para notificar al organizador de la reunión si la reunión se ha aceptado, rechazado, agregado provisionalmente al calendario del destinatario. El método **Respond** acepta tres parámetros. 

El parámetro *Response* indica si la respuesta es aceptar, rechazar o agregar provisionalmente. Los parámetros fNoUI y fAdditionalTextDialog son valores **booleanos** que determinan si se enviará una respuesta, y si el usuario puede o no editar la respuesta, respectivamente. En el ejemplo de código siguiente, AutoAcceptMeetingRequests enumera todos los objetos **MeetingItem** para obtener el **AppointmentItem** asociado. AutoAcceptMeetingRequests usa después el método **Respond** con el parámetro *fNoUI* establecido en **true** para indicar que se enviará una respuesta automáticamente para aceptar la convocatoria de reunión.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AutoAcceptMeetingRequests()
{
    Outlook.MeetingItem mtgResponse;
    Outlook.Folder folder = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    string filter = "[MessageClass] = " +
        "'IPM.Schedule.Meeting.Request'";
    Outlook.Items items = folder.Items.Restrict(filter);
    foreach (Outlook.MeetingItem request in items)
    {
        Outlook.AppointmentItem appt =
            request.GetAssociatedAppointment(true);
        if (appt != null)
        {
            mtgResponse = appt.Respond(
                Outlook.OlMeetingResponse.olMeetingAccepted,
                true, Type.Missing);
            mtgResponse.Send();
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Meeting requests](meeting-requests.md) (Convocatorias de reunión)

