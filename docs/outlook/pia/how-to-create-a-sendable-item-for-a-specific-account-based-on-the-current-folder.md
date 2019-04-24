---
title: Crear un elemento que puede enviarse para una cuenta específica basándose en la carpeta actual
TOCTitle: Create a sendable item for a specific account based on the current folder
ms:assetid: 665ebdc5-2912-4d85-ac40-835c9ef9a439
ms:contentKeyID: 55119796
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ccbbaab10dc88d50c1fad3c1eefeb5c222bc8446
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349535"
---
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a><span data-ttu-id="9db78-102">Crear un elemento que puede enviarse para una cuenta específica basándose en la carpeta actual</span><span class="sxs-lookup"><span data-stu-id="9db78-102">Create a sendable item for a specific account based on the current folder</span></span>

<span data-ttu-id="9db78-103">Este tema contiene dos ejemplos de código que muestran cómo crear un elemento de correo electrónico que se pueda enviar y una convocatoria de reunión y, a continuación, cómo enviarlos usando una cuenta concreta basada en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="9db78-103">This topic contains two code examples that show how to create a sendable email item and meeting request, and then how to send them by using a specific account that is based on the current folder.</span></span>

## <a name="example"></a><span data-ttu-id="9db78-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9db78-104">Example</span></span>

<span data-ttu-id="9db78-105">Cuando usa el método [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) del objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) para crear un elemento de Outlook, el elemento se crea para la cuenta principal de esa sesión.</span><span class="sxs-lookup"><span data-stu-id="9db78-105">When you use the [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) method of the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object to create an Outlook item, the item is created for the primary account for that session.</span></span> <span data-ttu-id="9db78-106">En una sesión donde hay definidas varias cuentas en el perfil, puede crear un elemento para una cuenta de IMAP, POP o Exchange específica.</span><span class="sxs-lookup"><span data-stu-id="9db78-106">In a session where multiple accounts are defined in the profile, you can create an item for a specific IMAP, POP, or Exchange account.</span></span> 

<span data-ttu-id="9db78-107">Si hay varias cuentas en el perfil actual y crea un elemento que se pueda enviar en la interfaz de usuario, por ejemplo, al hacer clic en **Nuevo correo electrónico** o **Nueva reunión**, un inspector muestra un nuevo elemento de correo o convocatoria de reunión en el modo de redacción y, a continuación, puede seleccionar la cuenta desde la que desea enviar el elemento.</span><span class="sxs-lookup"><span data-stu-id="9db78-107">If there are multiple accounts in the current profile and you create a sendable item in the user interface, for example, by clicking **New Email** or **New Meeting**, an inspector displays a new mail item or meeting request in compose mode, and then you can select the account from which to send the item.</span></span> 

<span data-ttu-id="9db78-108">En este tema se muestra cómo crear un elemento que se pueda enviar y enviarlo con una cuenta de envío específica mediante programación.</span><span class="sxs-lookup"><span data-stu-id="9db78-108">This topic shows how to programmatically create a sendable item and send it by using a specific sending account.</span></span> <span data-ttu-id="9db78-109">El tema tiene dos ejemplos de código que muestran cómo crear un objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) y un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) para una cuenta específica que está determinada por la carpeta actual en el explorador activo.</span><span class="sxs-lookup"><span data-stu-id="9db78-109">The topic has two code examples that show how to create a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) and an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) for a specific account that is determined by the current folder in the active explorer.</span></span>

<span data-ttu-id="9db78-110">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="9db78-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="9db78-111">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="9db78-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="9db78-112">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="9db78-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="9db78-113">En este primer método, CreateMailItemFromAccount identifica primero la cuenta adecuada al hacer coincidir el almacén de la carpeta actual (obtenido de la propiedad [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) con el almacén de entrega predeterminado para cada cuenta (obtenido con la propiedad [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) que está definido en la colección [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) para la sesión.</span><span class="sxs-lookup"><span data-stu-id="9db78-113">In the first method, CreateMailItemFromAccount first identifies the appropriate account by matching the store of the current folder (obtained from the [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) property) with the default delivery store of each account (obtained with the [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) property) that is defined in the [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) collection for the session.</span></span> <span data-ttu-id="9db78-114">Después, CreateMailItemFromAccount crea el **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="9db78-114">CreateMailItemFromAccount then creates the **MailItem**.</span></span> 

<span data-ttu-id="9db78-115">Para asociar el elemento con la cuenta, CreateMailItemFromAccount asigna al usuario de la cuenta como el remitente del elemento al configurar la propiedad account.CurrentUser.AddressEntry para la propiedad [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) del **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="9db78-115">To associate the item with the account, CreateMailItemFromAccount assigns the user of the account as the sender of the item by setting the account.CurrentUser.AddressEntry property to the [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) property of the **MailItem**.</span></span> <span data-ttu-id="9db78-116">Asignar la propiedad del remitente es el paso importante; si no especifica el remitente, el **MailItem** se crea de forma predeterminada para la cuenta principal.</span><span class="sxs-lookup"><span data-stu-id="9db78-116">Assigning the Sender property is the important step; if you do not specify the sender, the **MailItem** is created for the primary account by default.</span></span> <span data-ttu-id="9db78-117">Al final del método, CreateMailItemFromAccount muestra el **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="9db78-117">At the end of the method, CreateMailItemFromAccount displays the **MailItem**.</span></span> <span data-ttu-id="9db78-118">Recuerde que si la carpeta actual no está en un almacén de entrega, CreateMailItemFromAccount crea el objeto **MailItem** para la cuenta principal de la sesión.</span><span class="sxs-lookup"><span data-stu-id="9db78-118">Note that if the current folder is not on a delivery store, CreateMailItemFromAccount creates the **MailItem** for the primary account for the session.</span></span>

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

<span data-ttu-id="9db78-119">El siguiente método, CreateMeetingRequestFromAccount, es similar a CreateMailItemFromAccount, excepto que crea un AppointmentItem en lugar de un MailItem.</span><span class="sxs-lookup"><span data-stu-id="9db78-119">The next method, CreateMeetingRequestFromAccount, is similar to CreateMailItemFromAccount except that it creates an AppointmentItem instead of a MailItem.</span></span> <span data-ttu-id="9db78-120">CreateMeetingRequestFromAccount identifica primero la cuenta adecuada al hacer coincidir el almacén de la carpeta actual (obtenido de la propiedad [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) con el almacén de entrega predeterminado para cada cuenta (obtenido de la propiedad [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) que está definido en la colección Accounts para la sesión.</span><span class="sxs-lookup"><span data-stu-id="9db78-120">CreateMeetingRequestFromAccount first identifies the appropriate account by matching the store of the current folder (obtained from the [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) property) with the default delivery store of each account (obtained from the [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) property) that is defined in the Accounts collection for the session.</span></span> <span data-ttu-id="9db78-121">A continuación CreateMeetingRequestFromAccount crea el objeto AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="9db78-121">CreateMeetingRequestFromAccount then creates the AppointmentItem.</span></span> 

<span data-ttu-id="9db78-122">Para asociar el elemento con la cuenta, CreateMeetingRequestFromAccount asigna esa cuenta como la cuenta de envío del elemento al configurar el objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) para la propiedad [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) del objeto AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="9db78-122">To associate the item with the account, CreateMeetingRequestFromAccount assigns that account as the item's sending account by setting the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object to the [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) property of the AppointmentItem.</span></span> <span data-ttu-id="9db78-123">Asignar la propiedad SendUsingAccount es el paso importante; si no especifica la cuenta, el AppointmentItem se crea de forma predeterminada para la cuenta principal.</span><span class="sxs-lookup"><span data-stu-id="9db78-123">Assigning the SendUsingAccount property is the important step; if you do not specify the account, the AppointmentItem is created for the primary account by default.</span></span> <span data-ttu-id="9db78-124">Al final del método, CreateMeetingRequestFromAccount muestra el objeto AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="9db78-124">At the end of the method, CreateMeetingRequestFromAccount displays the AppointmentItem.</span></span> <span data-ttu-id="9db78-125">Recuerde que si la carpeta actual no está en un almacén de entrega, CreateMeetingRequestFromAccount crea el objeto AppointmentItem para la cuenta principal de la sesión.</span><span class="sxs-lookup"><span data-stu-id="9db78-125">Note that if the current folder is not on a delivery store, CreateMeetingRequestFromAccount creates the AppointmentItem for the primary account for the session.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="9db78-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9db78-126">See also</span></span>

- [<span data-ttu-id="9db78-127">Cuentas</span><span class="sxs-lookup"><span data-stu-id="9db78-127">Accounts</span></span>](accounts.md)

