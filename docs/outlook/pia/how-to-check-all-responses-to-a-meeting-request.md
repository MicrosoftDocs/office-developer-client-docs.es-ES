---
title: Comprobar todas las respuestas a una convocatoria de reunión
TOCTitle: Check all responses to a meeting request
ms:assetid: ebe10e5a-7f04-447a-bfc1-aa8a726cb0b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184650(v=office.15)
ms:contentKeyID: 55119881
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: a1dbc34cca35306ded436a30691c1cfb0f00fe6c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406165"
---
# <a name="check-all-responses-to-a-meeting-request"></a>Comprobar todas las respuestas a una convocatoria de reunión

Este ejemplo muestra cómo comprobar el estado de respuesta de cada destinatario a una convocatoria de reunión.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

En el siguiente ejemplo de código, CheckAttendeeStatus enumera la colección [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) del objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa una convocatoria de reunión y examina la propiedad [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) de cada objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)). Cada objeto **Recipient** representa un destinatario de la convocatoria de reunión. El valor de la propiedad **MeetingResponseStatus** puede ser uno de los siguientes valores de enumeración [OlResponseStatus](https://msdn.microsoft.com/library/bb644655\(v=office.15\)):

- [olResponseAccepted](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseDeclined](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseNone](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseNotResponded](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseOrganized](https://msdn.microsoft.com/library/bb644655\(v=office.15\))
- [olResponseTentative](https://msdn.microsoft.com/library/bb644655\(v=office.15\))

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CheckAttendeeStatus()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find("[Subject]='Sales Strategy FY2007'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            switch (recip.MeetingResponseStatus)
            {
                case Outlook.OlResponseStatus.olResponseAccepted:
                    Debug.WriteLine("Accepted: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseTentative:
                    Debug.WriteLine("Tentative: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseDeclined:
                    Debug.WriteLine("Declined: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseOrganized:
                    Debug.WriteLine("Organizer: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNone:
                    Debug.WriteLine("None: " + recip.Name);
                    break;
                case Outlook.OlResponseStatus.olResponseNotResponded:
                    Debug.WriteLine("Not responded: " + recip.Name);
                    break;
            }
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Meeting requests](meeting-requests.md) (Convocatorias de reunión)

