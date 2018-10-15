---
title: Mostrar un calendario compartido de un destinatario
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 10101a3eff1b0507c1fe562f175bace7026143fb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406886"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a>Mostrar un calendario compartido de un destinatario

Este ejemplo muestra cómo visualizar un calendario compartido de un destinatario utilizando los métodos [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) y [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)).

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Los elementos que se pueden enviar como los objetos [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) siempre exponen la propiedad [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) que, a su vez, le permite acceder a la colección [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) para el elemento que se puede enviar. Para crear un objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) que no está sujeto a la colección **Recipients** de un elemento, use el método [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). Luego, pase este objeto independiente **Recipient** al método [GetSharedDefaultFolderr(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)), que devuelve una carpeta compartida de Exchange. Después, puede abrir la carpeta compartida de Exchange y mostrarla en una ventana del explorador. GetSharedDefaultFolder se utiliza en escenarios delegados de Exchange en los que el delegado tiene permiso para acceder a la carpeta del delegador. Antes de pasar el objeto **Recipient** al método GetSharedDefaultFolder, debe resolverlo. Para resolver un objeto **Recipient**, llame a su método [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)).

En el siguiente ejemplo de código, DisplayManagerCalendar abre y muestra la carpeta Calendario del administrador de usuario actual, llamando a **CreateRecipient** y **GetSharedDefaultFolder**. Se muestra un cuadro de diálogo de alerta si el usuario no tiene permiso para abrir la carpeta Calendario del administrador o si se produce un error. 


> [!NOTE]
> Al crear un objeto **Recipient** utilizando el método **CreateRecipient** del objeto **Namespace** o el método [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) de la colección **Recipients**, debe proporcionar un nombre del destinatario. Luego, el **Recipient** se resuelve con este nombre. Un nombre del destinatario puede tomar cualquiera de los siguientes formatos:
> - Nombre para mostrar
> - Alias
> - Dirección del protocolo simple de transferencia de correo (SMTP)

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de Clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayManagerCalendar()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.Recipient recip =
                Application.Session.CreateRecipient(manager.Name);
            if (recip.Resolve())
            {
                try
                {
                    Outlook.Folder folder =
                        Application.Session.GetSharedDefaultFolder(
                        recip, Outlook.OlDefaultFolders.olFolderCalendar)
                        as Outlook.Folder;
                    folder.Display();
                }
                catch
                {
                    MessageBox.Show("Could not open manager's calendar.",
                        "GetSharedDefaultFolder Example",
                        MessageBoxButtons.OK,
                        MessageBoxIcon.Error);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Calendario](calendar.md)

