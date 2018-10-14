---
title: Mostrar una notificación al usuario para que responda a una convocatoria de reunión
TOCTitle: Prompt a user to respond to a meeting request
ms:assetid: a0d69f82-8659-457d-9418-1a897a10882f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184630(v=office.15)
ms:contentKeyID: 55119877
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b309252685363774d45ff6f74e581b9be86b042f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407593"
---
# <a name="prompt-a-user-to-respond-to-a-meeting-request"></a>Mostrar una notificación al usuario para que responda a una convocatoria de reunión

En este ejemplo se muestra cómo solicitar al usuario una respuesta a una convocatoria de reunión y cómo habilitar al usuario para que edite la respuesta antes de enviarla.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

El método [Respond](https://msdn.microsoft.com/library/bb647086\(v=office.15\)) del objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) se usa para notificar al organizador de la reunión si la reunión se ha aceptado, rechazado o agregado provisionalmente al calendario del destinatario. Al usar el método **Respond**, puede indicar si quiere que la invitación se envíe automáticamente o si quiere que el usuario pueda editar la respuesta antes de enviarla. El método **Respond** acepta tres parámetros. El parámetro *Response* indica si la respuesta es aceptar, rechazar o agregar provisionalmente. Los parámetros *fNoUI* y *fAdditionalTextDialog* son valores **booleanos** que determinan si se enviará una respuesta al organizador y si el usuario puede o no editar la respuesta, respectivamente. 

En el siguiente ejemplo de código, PromptUserMeetingRequest enumera todos los objetos [MeetingItem](https://msdn.microsoft.com/library/bb645703\(v=office.15\)) para obtener los objetos **AppointmentItem** asociados, y luego llama al método **Respond** con el parámetro *fNoUI* establecido en **false** y el parámetro *fAdditionalTextDialog* establecido en **true**. Esto permite al usuario elegir si desea enviar una respuesta y si quiere editar el cuerpo de la respuesta antes de enviarla.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void PromptUserMeetingRequest()
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
                false, true);
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Convocatorias de reunión](meeting-requests.md)

