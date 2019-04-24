---
title: Consultar la respuesta de un administrador a una convocatoria de reunión
TOCTitle: Check a manager's response to a meeting request
ms:assetid: 7bdb2163-17e3-47b4-95e5-e051b90506c6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184618(v=office.15)
ms:contentKeyID: 55119847
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba54ba740182eaffc92a0e1932a6fbed1d3804c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359713"
---
# <a name="check-a-managers-response-to-a-meeting-request"></a>Consultar la respuesta de un administrador a una convocatoria de reunión.

En este ejemplo se muestra cómo usar los métodos [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) y [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) para comprobar el estado de respuesta del administrador del usuario actual a una convocatoria de reunión.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Para determinar si un destinatario específico ha aceptado o rechazado una reunión solicitada, use la propiedad [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) del objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) desde la colección [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) asociada con el objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).

En el ejemplo siguiente, CheckManagerResponseStatus toma un objeto **AppointmentItem** como parámetro. CheckManagerResponseStatus obtiene el objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) llamando al método **GetExchangeUser** del usuario actual. CheckManagerResponseStatus obtiene luego el objeto **ExchangeUser** que está asociado con el administrador del usuario actual llamando al método **GetExchangeUserManager**. Usando el método [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), en el ejemplo se comprueba si el objeto **Recipient** asociado con el objeto **AppointmentItem** es el mismo que el objeto **ExchangeUser** que representa el administrador del usuario. Si **CompareEntryIDs** devuelve **verdadero**, el administrador del usuario se encuentra en la colección de **Recipients** y CheckManagerResponseStatus devuelve el **MeetingResponseStatus** del administrador. Si **CompareEntryIDs** devuelve **falso**, CheckManagerResponseStatus devuelve una referencia nula.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Object CheckManagerResponseStatus(Outlook.AppointmentItem appt)
{
    try
    {
        if (appt == null)
        {
            throw new ArgumentNullException();
        }
        Outlook.AddressEntry user =
            Application.Session.CurrentUser.AddressEntry;
        Outlook.ExchangeUser userEx = user.GetExchangeUser();
        if (userEx == null)
        {
            return null;
        }
        Outlook.ExchangeUser manager =
            userEx.GetExchangeUserManager();
        if (manager == null)
        {
            return null;
        }
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            if (Application.Session.CompareEntryIDs(
                recip.AddressEntry.ID, manager.ID))
            {
                return recip.MeetingResponseStatus;
            }
        }
        return null;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
        return null;
    }
}
```

## <a name="see-also"></a>Vea también

- [Exchange users](exchange-users.md) (Usuarios de Exchange)

