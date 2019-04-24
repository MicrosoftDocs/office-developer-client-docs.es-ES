---
title: Obtener información sobre el usuario actual
TOCTitle: Get information about the current user
ms:assetid: 3802523a-3ccf-4cca-a348-abe2645a0d9c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184601(v=office.15)
ms:contentKeyID: 55119840
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b169eb1baadee92c08bcb68726ae4d18a9d79d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349395"
---
# <a name="get-information-about-the-current-user"></a>Obtener información sobre el usuario actual

Este ejemplo muestra cómo obtener información sobre el usuario actual, como su nombre, puesto y número de teléfono.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Para obtener un objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) de un objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)), llame al método [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) del objeto **AddressEntry**. En el siguiente procedimiento, GetCurrentUserInfo obtiene la propiedad [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) del objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) utilizando la propiedad [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)). Si el objeto **AddressEntry** representa un usuario de buzón de Exchange, GetCurrentUserInfo llama al método **GetExchangeUser** y se devuelve un objeto **ExchangeUser**. Las propiedades [Name](https://msdn.microsoft.com/library/bb622941\(v=office.15\)), [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)), [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb611429\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)) y [MobileTelephoneNumber](https://msdn.microsoft.com/library/bb609292\(v=office.15\)) se escriben en los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserInfo()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser currentUser =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser();
        if (currentUser != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + currentUser.Name);
            sb.AppendLine("STMP address: "
                + currentUser.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + currentUser.JobTitle);
            sb.AppendLine("Department: "
                + currentUser.Department);
            sb.AppendLine("Location: "
                + currentUser.OfficeLocation);
            sb.AppendLine("Business phone: "
                + currentUser.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + currentUser.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Exchange users](exchange-users.md) (Usuarios de Exchange)

