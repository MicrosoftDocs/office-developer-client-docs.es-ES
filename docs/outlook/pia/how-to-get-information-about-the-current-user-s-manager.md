---
title: Obtener información sobre el administrador del usuario actual
TOCTitle: Get information about the current user's manager
ms:assetid: 3a77fa51-e2e3-4544-849f-4267b1762270
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184603(v=office.15)
ms:contentKeyID: 55119846
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 89da7df4aac29b7d308dd0b0f432d8652c5f0127
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407313"
---
# <a name="get-information-about-the-current-users-manager"></a><span data-ttu-id="8565d-102">Obtener información sobre el administrador del usuario actual</span><span class="sxs-lookup"><span data-stu-id="8565d-102">Get information about the current user's manager</span></span>

<span data-ttu-id="8565d-103">Este ejemplo muestra cómo obtener información sobre el usuario actual, como su nombre, puesto y número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="8565d-103">This example shows how to get information (such as name, job title, and phone numbers) about the current user’s manager.</span></span>

## <a name="example"></a><span data-ttu-id="8565d-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8565d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="8565d-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="8565d-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="8565d-106">En el siguiente procedimiento, GetManagerInfo llama al método [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) para obtener un objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) que representa el administrador de un **ExchangeUser** en la jerarquía de la organización.</span><span class="sxs-lookup"><span data-stu-id="8565d-106">In the following procedure, GetManagerInfo calls the [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method to obtain an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object that represents the manager of an **ExchangeUser** in the organizational hierarchy.</span></span> <span data-ttu-id="8565d-107">El procedimiento comprueba si el usuario que ha iniciado sesión está conectado para asegurarse de que **GetExchangeUserManager** puede devolver un objeto **ExchangeUser**.</span><span class="sxs-lookup"><span data-stu-id="8565d-107">The procedure tests whether the logged-on user is online to ensure that **GetExchangeUserManager** can return an **ExchangeUser** object.</span></span> <span data-ttu-id="8565d-108">Si el usuario no está conectado, **GetExchangeUserManager** devolverá una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="8565d-108">If the user is not online, **GetExchangeUserManager** will return a null reference.</span></span> <span data-ttu-id="8565d-109">Después, GetManagerInfo escribe información de administrador para los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="8565d-109">GetManagerInfo then writes manager information to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="8565d-110">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="8565d-110">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="8565d-111">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="8565d-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="8565d-112">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="8565d-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerInfo()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + manager.Name);
            sb.AppendLine("STMP address: "
                + manager.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + manager.JobTitle);
            sb.AppendLine("Department: "
                + manager.Department);
            sb.AppendLine("Location: "
                + manager.OfficeLocation);
            sb.AppendLine("Business phone: "
                + manager.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + manager.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="8565d-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="8565d-113">See also</span></span>

- <span data-ttu-id="8565d-114">[Exchange users](exchange-users.md) (Usuarios de Exchange)</span><span class="sxs-lookup"><span data-stu-id="8565d-114">[exchange users](exchange-users.md)</span></span>

