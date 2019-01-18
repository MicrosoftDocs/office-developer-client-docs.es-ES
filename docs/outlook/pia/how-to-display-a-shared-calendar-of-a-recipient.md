---
title: Mostrar un calendario compartido de un destinatario
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9230a63af66e8143a7da488ce41dadafe359429
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709218"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a><span data-ttu-id="6c343-102">Mostrar un calendario compartido de un destinatario</span><span class="sxs-lookup"><span data-stu-id="6c343-102">Display a shared calendar of a recipient</span></span>

<span data-ttu-id="6c343-103">Este ejemplo muestra cómo visualizar un calendario compartido de un destinatario utilizando los métodos [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) y [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="6c343-103">This example shows how to display a recipient's shared calendar by using the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) and [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) methods.</span></span>

## <a name="example"></a><span data-ttu-id="6c343-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c343-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6c343-105">El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="6c343-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="6c343-106">Los elementos que se pueden enviar como los objetos [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) siempre exponen la propiedad [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) que, a su vez, le permite acceder a la colección [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) para el elemento que se puede enviar.</span><span class="sxs-lookup"><span data-stu-id="6c343-106">Sendable items such as [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) objects always expose the [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) property which, in turn, enables you to access the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection for the sendable item.</span></span> <span data-ttu-id="6c343-107">Para crear un objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) que no está sujeto a la colección **Recipients** de un elemento, use el método [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="6c343-107">To create a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object that is not bound to the **Recipients** collection of an item, use the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="6c343-108">Luego, pase este objeto independiente **Recipient** al método [GetSharedDefaultFolderr(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)), que devuelve una carpeta compartida de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6c343-108">Then pass this unbound **Recipient** object to the [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) method, which returns a shared Exchange folder.</span></span> <span data-ttu-id="6c343-109">Después, puede abrir la carpeta compartida de Exchange y mostrarla en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="6c343-109">You can then open the shared Exchange folder and display that folder in an explorer window.</span></span> <span data-ttu-id="6c343-110">GetSharedDefaultFolder se utiliza en escenarios delegados de Exchange en los que el delegado tiene permiso para acceder a la carpeta del delegador.</span><span class="sxs-lookup"><span data-stu-id="6c343-110">GetSharedDefaultFolder is used in Exchange delegate scenarios where the delegate has permission to access the folder of the delegator.</span></span> <span data-ttu-id="6c343-111">Antes de pasar el objeto **Recipient** al método GetSharedDefaultFolder, debe resolverlo.</span><span class="sxs-lookup"><span data-stu-id="6c343-111">Before you pass the **Recipient** object to the GetSharedDefaultFolder method, you must resolve it.</span></span> <span data-ttu-id="6c343-112">Para resolver un objeto **Recipient**, llame a su método [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="6c343-112">To resolve a **Recipient** object, call its [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) method.</span></span>

<span data-ttu-id="6c343-p102">En el siguiente ejemplo de código, DisplayManagerCalendar abre y muestra la carpeta Calendario del administrador de usuario actual, llamando a **CreateRecipient** y **GetSharedDefaultFolder**. Se muestra un cuadro de diálogo de alerta si el usuario no tiene permiso para abrir la carpeta Calendario del administrador o si se produce un error. </span><span class="sxs-lookup"><span data-stu-id="6c343-p102">In the following code example, DisplayManagerCalendar opens and displays the Calendar folder of the current user’s manager by calling **CreateRecipient** and **GetSharedDefaultFolder**. An alert dialog box is displayed if the user does not have permission to open the manager’s Calendar folder or an error occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="6c343-115">Al crear un objeto **Recipient** utilizando el método **CreateRecipient** del objeto **Namespace** o el método [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) de la colección **Recipients**, debe proporcionar un nombre del destinatario.</span><span class="sxs-lookup"><span data-stu-id="6c343-115">When you create a **Recipient** object by using the **CreateRecipient** method of the **Namespace** object or the [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) method of the **Recipients** collection, you must provide a recipient name.</span></span> <span data-ttu-id="6c343-116">Luego, el **Recipient** se resuelve con este nombre.</span><span class="sxs-lookup"><span data-stu-id="6c343-116">The **Recipient** is then resolved against this name.</span></span> <span data-ttu-id="6c343-117">Un nombre del destinatario puede tomar cualquiera de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="6c343-117">A recipient name can take any of the following formats:</span></span>
> - <span data-ttu-id="6c343-118">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="6c343-118">Display name</span></span>
> - <span data-ttu-id="6c343-119">Alias</span><span class="sxs-lookup"><span data-stu-id="6c343-119">Alias</span></span>
> - <span data-ttu-id="6c343-120">Dirección del protocolo simple de transferencia de correo (SMTP)</span><span class="sxs-lookup"><span data-stu-id="6c343-120">Simple Mail Transfer Protocol (SMTP) address</span></span>

<span data-ttu-id="6c343-121">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6c343-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="6c343-122">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de Clase pública.</span><span class="sxs-lookup"><span data-stu-id="6c343-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6c343-123">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="6c343-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="6c343-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c343-124">See also</span></span>

- [<span data-ttu-id="6c343-125">Calendario</span><span class="sxs-lookup"><span data-stu-id="6c343-125">Calendar</span></span>](calendar.md)

