---
title: Mostrar las listas de direcciones para un perfil
TOCTitle: Display the address lists for a profile
ms:assetid: ced8230b-110b-4ccb-a699-588798144154
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184643(v=office.15)
ms:contentKeyID: 55119802
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b69ed930241dc058b22b75c6ccc9121f8856d28f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356374"
---
# <a name="display-the-address-lists-for-a-profile"></a><span data-ttu-id="abbd6-102">Mostrar las listas de direcciones para un perfil</span><span class="sxs-lookup"><span data-stu-id="abbd6-102">Display the address lists for a profile</span></span>

<span data-ttu-id="abbd6-103">En este ejemplo se explica cómo mostrar las listas de direcciones para el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="abbd6-103">This example shows how to display the address lists for the current profile.</span></span>

## <a name="example"></a><span data-ttu-id="abbd6-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="abbd6-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="abbd6-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="abbd6-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="abbd6-106">El perfil actual contiene listas de direcciones que se representan mediante la colección [AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="abbd6-106">The current profile contains address lists that are represented by the [AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)) collection.</span></span> <span data-ttu-id="abbd6-107">Para obtener una instancia de la colección AddressLists debe usar la propiedad [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="abbd6-107">To get an instance of the AddressLists collection, you must use the [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span>

<span data-ttu-id="abbd6-108">En el siguiente ejemplo de código, EnumerateAddressLists primero enumera cada objeto [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) de la colección AddressLists utilizando una instrucción.</span><span class="sxs-lookup"><span data-stu-id="abbd6-108">In the following code example, EnumerateAddressLists first enumerates each [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) object in the AddressLists collection by using a foreach statement.</span></span> <span data-ttu-id="abbd6-109">Después, el ejemplo crea una cadena que contiene los valores de las propiedades [Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\)), [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)), [IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\)) e [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="abbd6-109">The example then creates a string that contains the values of the [Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\)), [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)), [IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\)), and [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)) properties.</span></span> <span data-ttu-id="abbd6-110">Por último, EnumerateAddressLists escribe la cadena a los agentes de escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="abbd6-110">Finally, EnumerateAddressLists writes the string to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span> <span data-ttu-id="abbd6-111">Esto muestra cada lista de direcciones para el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="abbd6-111">This displays each address list for the current profile.</span></span>

<span data-ttu-id="abbd6-112">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="abbd6-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="abbd6-113">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="abbd6-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="abbd6-114">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="abbd6-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAddressLists()
{
    Outlook.AddressLists addrLists =
         Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Display Name: " + addrList.Name);
        sb.AppendLine("Resolution Order: "
            + addrList.ResolutionOrder.ToString());
        sb.AppendLine("Read-only : "
            + addrList.IsReadOnly.ToString());
        sb.AppendLine("Initial Address List: "
            + addrList.IsInitialAddressList.ToString());
        sb.AppendLine("");
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="abbd6-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="abbd6-115">See also</span></span>

- [<span data-ttu-id="abbd6-116">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="abbd6-116">Address book</span></span>](address-book.md)

