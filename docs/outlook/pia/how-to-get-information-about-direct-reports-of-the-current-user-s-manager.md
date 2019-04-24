---
title: Obtener información sobre los subordinados directos del administrador del usuario actual
TOCTitle: Get information about direct reports of the current user's manager
ms:assetid: 768bf573-1b10-4776-8947-a7f8dc3ebde0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184617(v=office.15)
ms:contentKeyID: 55119842
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d49e96138d8cd2d857c49cc293258e1493afc747
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349437"
---
# <a name="get-information-about-direct-reports-of-the-current-users-manager"></a><span data-ttu-id="afb56-102">Obtener información sobre los subordinados directos del administrador del usuario actual</span><span class="sxs-lookup"><span data-stu-id="afb56-102">Get information about direct reports of the current user's manager</span></span>

<span data-ttu-id="afb56-103">En este ejemplo se obtienen los subordinados directos del administrador del usuario actual, si existen, y se muestra información sobre cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="afb56-103">This example gets the direct reports of the current user’s manager, if any, and then displays information about each of the manager’s direct reports.</span></span>

## <a name="example"></a><span data-ttu-id="afb56-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="afb56-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="afb56-105">El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="afb56-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="afb56-106">En el ejemplo siguiente el procedimiento GetManagerDirectReports llama al método [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) para obtener el administrador del usuario, representado por un objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="afb56-106">In the following example, the GetManagerDirectReports procedure calls the [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method to get the user’s manager, represented by an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object.</span></span> <span data-ttu-id="afb56-107">Si el usuario actual tiene un administrador, se llama a [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) para devolver una colección [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) que representa las entradas de dirección para todos los subordinados directos del administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="afb56-107">If the current user has a manager, [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) is called to return an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection that represents the address entries for all the direct reports of user’s manager.</span></span> <span data-ttu-id="afb56-108">Si el administrador no tiene ningún subordinado directo, **GetDirectReports** devuelve una colección **AddressEntries** con un total de cero.</span><span class="sxs-lookup"><span data-stu-id="afb56-108">If the manager has no direct reports, **GetDirectReports** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="afb56-109">Cuando se obtienen los subordinados directos del administrador, GetManagerDirectReports escribe información sobre cada uno de ellos en las escucha de seguimiento de la colección [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="afb56-109">Once the manager’s direct reports are obtained, GetManagerDirectReports writes information about each of the manager’s direct reports to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="afb56-110">El usuario que ha iniciado sesión debe estar en línea para que este método devuelva una colección **AddressEntries**; en caso contrario, **GetDirectReports** devuelve una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="afb56-110">The signed-in user must be online for this method to return an **AddressEntries** collection; otherwise, **GetDirectReports** returns a null reference.</span></span> <span data-ttu-id="afb56-111">Para el código de producción, debe probar si el usuario está desconectado usando la propiedad [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) o [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) para varios escenarios de Exchange.</span><span class="sxs-lookup"><span data-stu-id="afb56-111">For production code, you must test for the user being offline by using the [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) property, or the [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) property for multiple Exchange scenarios.</span></span>

<span data-ttu-id="afb56-112">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="afb56-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="afb56-113">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="afb56-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="afb56-114">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="afb56-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerDirectReports()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.AddressEntries addrEntries =
                manager.GetDirectReports();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Outlook.ExchangeUser exchUser =
                        addrEntry.GetExchangeUser();
                    StringBuilder sb = new StringBuilder();
                    sb.AppendLine("Name: "
                        + exchUser.Name);
                    sb.AppendLine("Title: "
                        + exchUser.JobTitle);
                    sb.AppendLine("Department: "
                        + exchUser.Department);
                    sb.AppendLine("Location: "
                        + exchUser.OfficeLocation);
                    Debug.WriteLine(sb.ToString());
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="afb56-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="afb56-115">See also</span></span>

- <span data-ttu-id="afb56-116">[Exchange users](exchange-users.md) (Usuarios de Exchange)</span><span class="sxs-lookup"><span data-stu-id="afb56-116">[Exchange users](exchange-users.md)</span></span>

