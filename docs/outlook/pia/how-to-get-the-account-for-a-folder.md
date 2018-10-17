---
title: Obtener la cuenta de una carpeta
TOCTitle: Get the account for a folder
ms:assetid: 3706be15-f746-4d0d-9ffe-d6f46b2004dc
ms:contentKeyID: 55119793
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d83a145b577cbc9be68cdd694f7806da7cdad512
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407208"
---
# <a name="get-the-account-for-a-folder"></a>Obtener la cuenta de una carpeta

Este ejemplo obtiene la cuenta que está asociada a una carpeta en la sesión actual.

## <a name="example"></a>Ejemplo

En el siguiente ejemplo de código, la función DisplayAccountForCurrentFolder llama a la función GetAccountForFolder para identificar la cuenta cuyo almacén de entrega predeterminado hospeda la carpeta actual y después muestra el nombre de la carpeta. GetAccountForFolder relaciona el almacén de la carpeta actual (obtenido de la propiedad [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) con el almacén de entrega predeterminado para cada cuenta (obtenido con la propiedad [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) que está definido en la colección [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) para la sesión. GetAccountForFolder devuelve el objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) si se encuentra una coincidencia; en caso contrario, devuelve una referencia nula.

En una sesión de Microsoft Outlook con varias cuentas definidas en el perfil, la carpeta que se muestra en el explorador activo no debe residir necesariamente en el almacén predeterminado para esa sesión, sino que puede residir en uno de los distintos almacenes asociados a las distintas cuentas. En este tema se muestra cómo identificar la cuenta en la que el almacén de entregas predeterminado es el mismo almacén que hospeda la carpeta.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayAccountForCurrentFolder()
{
    Outlook.Folder myFolder = Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    string msg = "Account for Current Folder:" + "\n" +
        GetAccountForFolder(myFolder).DisplayName;
    MessageBox.Show(msg,
        "GetAccountForFolder",
        MessageBoxButtons.OK,
        MessageBoxIcon.Information);
}

Outlook.Account GetAccountForFolder(Outlook.Folder folder)
{
    // Obtain the store on which the folder resides.
    Outlook.Store store = folder.Store;

    // Enumerate the accounts defined for the session.
    foreach (Outlook.Account account in Application.Session.Accounts)
    {
        // Match the DefaultStore.StoreID of the account
        // with the Store.StoreID for the currect folder.
        if (account.DeliveryStore.StoreID  == store.StoreID)
        {
            // Return the account whose default delivery store
            // matches the store of the given folder.
            return account;
        }
     }
     // No account matches, so return null.
     return null;
}
```

## <a name="see-also"></a>Vea también

- [Accounts](accounts.md) (Cuentas)

