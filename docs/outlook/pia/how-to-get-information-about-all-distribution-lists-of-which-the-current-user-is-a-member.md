---
title: Obtener información sobre todas las listas de distribución de las que el usuario actual es un miembro
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f98d7a338866624e67d745e66a66e864fb9bbf99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406767"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a><span data-ttu-id="1fc8f-102">Obtener información sobre todas las listas de distribución de las que el usuario actual es un miembro</span><span class="sxs-lookup"><span data-stu-id="1fc8f-102">Uses the M:Microsoft.Office.Interop.Outlook._ExchangeUser.GetMemberOfList method to get information about all distribution lists of which the current user is a member.</span></span>

<span data-ttu-id="1fc8f-103">En este ejemplo se usa el método [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) para obtener información sobre todas las listas de distribución de las que el usuario actual es miembro.</span><span class="sxs-lookup"><span data-stu-id="1fc8f-103">This example uses the [M:Microsoft.Office.Interop.Outlook._ExchangeUser.GetMemberOfList](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) method to get information about all distribution lists of which the current user is a member.</span></span>

## <a name="example"></a><span data-ttu-id="1fc8f-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fc8f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1fc8f-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="1fc8f-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="1fc8f-106">En el ejemplo siguiente, GetCurrentUserMembership llama al método **GetMemberOfList** para obtener una colección [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) de todas las listas de distribución de las que el usuario de Exchange es miembro.</span><span class="sxs-lookup"><span data-stu-id="1fc8f-106">In the following example, GetCurrentUserMembership calls the **GetMemberOfList** method to get an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection for all distribution lists of which the Exchange user is a member.</span></span> <span data-ttu-id="1fc8f-107">Si el usuario no es miembro de ninguna lista de distribución, **GetMemberOfList** devuelve una colección **AddressEntries**con un total de cero.</span><span class="sxs-lookup"><span data-stu-id="1fc8f-107">If the user is not a member of any distribution lists, **GetMemberOfList** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="1fc8f-108">El usuario debe estar en línea para que el método **GetMemberOfList** devuelva una colección **AddressEntries**; en caso contrario, **GetMemberOfList** devuelve una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="1fc8f-108">The user must be online for **GetMemberOfList** to return an **AddressEntries** collection; otherwise, **GetMemberOfList** returns a null reference.</span></span> <span data-ttu-id="1fc8f-109">GetCurrentUserMembership usa el método [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)), que devuelve el objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) actual, para comprobar si el usuario está en línea.</span><span class="sxs-lookup"><span data-stu-id="1fc8f-109">GetCurrentUserMembership uses the [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) method, which returns the current [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object, to test whether the user is online.</span></span> <span data-ttu-id="1fc8f-110">Una vez que se obtienen las entradas de direcciones, el ejemplo escribe información sobre cada una de las listas de distribución del usuario en los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="1fc8f-110">Once the address entries are obtained, the example writes information about each of the user’s distribution lists to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="1fc8f-111">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1fc8f-111">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="1fc8f-112">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="1fc8f-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1fc8f-113">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="1fc8f-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserMembership()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser exchUser =
            currentUser.GetExchangeUser();
        if (exchUser != null)
        {
            Outlook.AddressEntries addrEntries =
                exchUser.GetMemberOfList();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Debug.WriteLine(addrEntry.Name);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="1fc8f-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fc8f-114">See also</span></span>

- [<span data-ttu-id="1fc8f-115">Usuarios de Exchange</span><span class="sxs-lookup"><span data-stu-id="1fc8f-115">exchange users</span></span>](exchange-users.md)

