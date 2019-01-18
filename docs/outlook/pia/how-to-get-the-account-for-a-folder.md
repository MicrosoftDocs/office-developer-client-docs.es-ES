---
title: Obtener la cuenta de una carpeta
TOCTitle: Get the account for a folder
ms:assetid: 3706be15-f746-4d0d-9ffe-d6f46b2004dc
ms:contentKeyID: 55119793
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8f56f866e71b1080d5b7a6a33fb17e3e71ab9199
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708098"
---
# <a name="get-the-account-for-a-folder"></a><span data-ttu-id="01156-102">Obtener la cuenta de una carpeta</span><span class="sxs-lookup"><span data-stu-id="01156-102">Get the account for a folder</span></span>

<span data-ttu-id="01156-103">Este ejemplo obtiene la cuenta que está asociada a una carpeta en la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="01156-103">This example gets the account that is associated with a folder in the current session.</span></span>

## <a name="example"></a><span data-ttu-id="01156-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01156-104">Example</span></span>

<span data-ttu-id="01156-105">En el siguiente ejemplo de código, la función DisplayAccountForCurrentFolder llama a la función GetAccountForFolder para identificar la cuenta cuyo almacén de entrega predeterminado hospeda la carpeta actual y después muestra el nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="01156-105">In the following code example, the DisplayAccountForCurrentFolder function calls the GetAccountForFolder function to identify the account whose default delivery store hosts the current folder, and then displays the name of the folder.</span></span> <span data-ttu-id="01156-106">GetAccountForFolder relaciona el almacén de la carpeta actual (obtenido de la propiedad [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) con el almacén de entrega predeterminado para cada cuenta (obtenido con la propiedad [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) que está definido en la colección [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) para la sesión.</span><span class="sxs-lookup"><span data-stu-id="01156-106">GetAccountForFolder matches the store of the current folder (obtained from the [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) property) with the default delivery store of each account (obtained with the [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) property) that is defined in the [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) collection for the session.</span></span> <span data-ttu-id="01156-107">GetAccountForFolder devuelve el objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) si se encuentra una coincidencia; en caso contrario, devuelve una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="01156-107">GetAccountForFolder returns the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object if a match is found; otherwise, it returns a null reference.</span></span>

<span data-ttu-id="01156-p102">En una sesión de Microsoft Outlook con varias cuentas definidas en el perfil, la carpeta que se muestra en el explorador activo no debe residir necesariamente en el almacén predeterminado para esa sesión, sino que puede residir en uno de los distintos almacenes asociados a las distintas cuentas. En este tema se muestra cómo identificar la cuenta en la que el almacén de entregas predeterminado es el mismo almacén que hospeda la carpeta.</span><span class="sxs-lookup"><span data-stu-id="01156-p102">In a Microsoft Outlook session that has multiple accounts defined in the profile, the folder that is displayed in the active explorer does not necessarily reside on the default store for that session; instead, it can reside on one of the multiple stores associated with the multiple accounts. This topic shows how to identify the account whose default delivery store is the same store that hosts the folder.</span></span>

<span data-ttu-id="01156-110">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="01156-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="01156-111">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="01156-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="01156-112">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="01156-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="01156-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="01156-113">See also</span></span>

- <span data-ttu-id="01156-114">[Accounts](accounts.md) (Cuentas)</span><span class="sxs-lookup"><span data-stu-id="01156-114">[Accounts](accounts.md)</span></span>

