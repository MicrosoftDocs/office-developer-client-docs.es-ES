---
title: Crear un elemento que puede enviarse para una cuenta específica basándose en la carpeta actual
TOCTitle: Create a sendable item for a specific account based on the current folder
ms:assetid: 665ebdc5-2912-4d85-ac40-835c9ef9a439
ms:contentKeyID: 55119796
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ccbbaab10dc88d50c1fad3c1eefeb5c222bc8446
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702162"
---
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a>Crear un elemento que puede enviarse para una cuenta específica basándose en la carpeta actual

Este tema contiene dos ejemplos de código que muestran cómo crear un elemento de correo electrónico que se pueda enviar y una convocatoria de reunión y, a continuación, cómo enviarlos usando una cuenta concreta basada en la carpeta actual.

## <a name="example"></a>Ejemplo

Cuando usa el método [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) del objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) para crear un elemento de Outlook, el elemento se crea para la cuenta principal de esa sesión. En una sesión donde hay definidas varias cuentas en el perfil, puede crear un elemento para una cuenta de IMAP, POP o Exchange específica. 

Si hay varias cuentas en el perfil actual y crea un elemento que se pueda enviar en la interfaz de usuario, por ejemplo, al hacer clic en **Nuevo correo electrónico** o **Nueva reunión**, un inspector muestra un nuevo elemento de correo o convocatoria de reunión en el modo de redacción y, a continuación, puede seleccionar la cuenta desde la que desea enviar el elemento. 

En este tema se muestra cómo crear un elemento que se pueda enviar y enviarlo con una cuenta de envío específica mediante programación. El tema tiene dos ejemplos de código que muestran cómo crear un objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) y un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) para una cuenta específica que está determinada por la carpeta actual en el explorador activo.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

En este primer método, CreateMailItemFromAccount identifica primero la cuenta adecuada al hacer coincidir el almacén de la carpeta actual (obtenido de la propiedad [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) con el almacén de entrega predeterminado para cada cuenta (obtenido con la propiedad [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) que está definido en la colección [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) para la sesión. Después, CreateMailItemFromAccount crea el **MailItem**. 

Para asociar el elemento con la cuenta, CreateMailItemFromAccount asigna al usuario de la cuenta como el remitente del elemento al configurar la propiedad account.CurrentUser.AddressEntry para la propiedad [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) del **MailItem**. Asignar la propiedad del remitente es el paso importante; si no especifica el remitente, el **MailItem** se crea de forma predeterminada para la cuenta principal. Al final del método, CreateMailItemFromAccount muestra el **MailItem**. Recuerde que si la carpeta actual no está en un almacén de entrega, CreateMailItemFromAccount crea el objeto **MailItem** para la cuenta principal de la sesión.

```csharp
private void CreateMailItemFromAccount()
{
    Outlook.AddressEntry addrEntry = null;
    // Get the Store for CurrentFolder.
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    // Enumerate accounts to find
    // account.DeliveryStore for store.
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID == 
            store.StoreID)
        {
            addrEntry =
                account.CurrentUser.AddressEntry;
            break;
        }
    }
    // Create MailItem.
    Outlook.MailItem mail =
        Application.CreateItem(
        Outlook.OlItemType.olMailItem)
        as Outlook.MailItem;
    if (addrEntry != null)
    {
        // Set Sender property.
        mail.Sender = addrEntry;
        mail.Display(false);
    }
}
```

El siguiente método, CreateMeetingRequestFromAccount, es similar a CreateMailItemFromAccount, excepto que crea un AppointmentItem en lugar de un MailItem. CreateMeetingRequestFromAccount identifica primero la cuenta adecuada al hacer coincidir el almacén de la carpeta actual (obtenido de la propiedad [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) con el almacén de entrega predeterminado para cada cuenta (obtenido de la propiedad [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) que está definido en la colección Accounts para la sesión. A continuación CreateMeetingRequestFromAccount crea el objeto AppointmentItem. 

Para asociar el elemento con la cuenta, CreateMeetingRequestFromAccount asigna esa cuenta como la cuenta de envío del elemento al configurar el objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) para la propiedad [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) del objeto AppointmentItem. Asignar la propiedad SendUsingAccount es el paso importante; si no especifica la cuenta, el AppointmentItem se crea de forma predeterminada para la cuenta principal. Al final del método, CreateMeetingRequestFromAccount muestra el objeto AppointmentItem. Recuerde que si la carpeta actual no está en un almacén de entrega, CreateMeetingRequestFromAccount crea el objeto AppointmentItem para la cuenta principal de la sesión.

```csharp
private void CreateMeetingRequestFromAccount()
{
    Outlook.Account acct = null;
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID ==
            store.StoreID)
        {
            acct = account;
            break;
        }
    }
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = 
        Outlook.OlMeetingStatus.olMeeting;
    if (acct != null)
    {
        // Set SendUsingAccount property.
        appt.SendUsingAccount=acct;
        appt.Display(false);
    }
}
```

## <a name="see-also"></a>Vea también

- [Cuentas](accounts.md)

