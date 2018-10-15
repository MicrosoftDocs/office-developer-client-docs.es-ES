---
title: Consultar la respuesta de un administrador a una convocatoria de reunión.
TOCTitle: Check a manager's response to a meeting request
ms:assetid: 7bdb2163-17e3-47b4-95e5-e051b90506c6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184618(v=office.15)
ms:contentKeyID: 55119847
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 14d78a88a0df514bca6782a84bd2c030fc140093
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406354"
---
# <a name="check-a-managers-response-to-a-meeting-request"></a><span data-ttu-id="9f4f4-102">Consultar la respuesta de un administrador a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="9f4f4-102">Check a manager's response to a meeting request</span></span>

<span data-ttu-id="9f4f4-103">En este ejemplo se muestra cómo usar los métodos [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) y [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) para comprobar el estado de respuesta del administrador del usuario actual a una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="9f4f4-103">This example illustrates how to use the [M:Microsoft.Office.Interop.Outlook.AddressEntry.GetExchangeUser](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) and [M:Microsoft.Office.Interop.Outlook._ExchangeUser.GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) methods to check the status of the response of the current user's manager to a meeting request.</span></span>

## <a name="example"></a><span data-ttu-id="9f4f4-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f4f4-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="9f4f4-105">El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="9f4f4-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="9f4f4-106">Para determinar si un destinatario específico ha aceptado o rechazado una reunión solicitada, use la propiedad [MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) del objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) desde la colección [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) asociada con el objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="9f4f4-106">To determine whether a given recipient has accepted or declined a requested meeting, use the [P:Microsoft.Office.Interop.Outlook.Recipient.MeetingResponseStatus](https://msdn.microsoft.com/library/bb645283\(v=office.15\)) property of the [T:Microsoft.Office.Interop.Outlook.Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object from the [T:Microsoft.Office.Interop.Outlook.Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection associated with the [T:Microsoft.Office.Interop.Outlook.AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="9f4f4-107">En el ejemplo siguiente, CheckManagerResponseStatus toma un objeto **AppointmentItem** como parámetro.</span><span class="sxs-lookup"><span data-stu-id="9f4f4-107">In the following code example, CheckManagerResponseStatus takes in an **AppointmentItem** object as a parameter.</span></span> <span data-ttu-id="9f4f4-108">CheckManagerResponseStatus obtiene el objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) llamando al método **GetExchangeUser** del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="9f4f4-108">CheckManagerResponseStatus gets the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object by calling the **GetExchangeUser** method on the current user.</span></span> <span data-ttu-id="9f4f4-109">CheckManagerResponseStatus obtiene luego el objeto **ExchangeUser** que está asociado con el administrador del usuario actual llamando al método **GetExchangeUserManager**.</span><span class="sxs-lookup"><span data-stu-id="9f4f4-109">CheckManagerResponseStatus then gets the **ExchangeUser** object that is associated with the current user’s manager by calling the **GetExchangeUserManager** method.</span></span> <span data-ttu-id="9f4f4-110">Usando el método [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), en el ejemplo se comprueba si el objeto **Recipient** asociado con el objeto **AppointmentItem** es el mismo que el objeto **ExchangeUser** que representa el administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="9f4f4-110">By using the [CompareEntryIDs(String, String)](https://msdn.microsoft.com/library/bb646919\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object, the example then checks whether the **Recipient** object associated with the **AppointmentItem** object is the same as the **ExchangeUser** object that represents the user’s manager.</span></span> <span data-ttu-id="9f4f4-111">Si **CompareEntryIDs** devuelve **verdadero**, el administrador del usuario se encuentra en la colección de **Recipients** y CheckManagerResponseStatus devuelve el **MeetingResponseStatus** del administrador.</span><span class="sxs-lookup"><span data-stu-id="9f4f4-111">If **CompareEntryIDs** returns **true**, the user’s manager is found in the **Recipients** collection, and CheckManagerResponseStatus returns the manager’s **MeetingResponseStatus**.</span></span> <span data-ttu-id="9f4f4-112">Si **CompareEntryIDs** devuelve **falso**, CheckManagerResponseStatus devuelve una referencia nula.</span><span class="sxs-lookup"><span data-stu-id="9f4f4-112">If **CompareEntryIDs** returns **false**, CheckManagerResponseStatus returns a null reference.</span></span>

<span data-ttu-id="9f4f4-113">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="9f4f4-113">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="9f4f4-114">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de Clase pública.</span><span class="sxs-lookup"><span data-stu-id="9f4f4-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="9f4f4-115">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="9f4f4-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Object CheckManagerResponseStatus(Outlook.AppointmentItem appt)
{
    try
    {
        if (appt == null)
        {
            throw new ArgumentNullException();
        }
        Outlook.AddressEntry user =
            Application.Session.CurrentUser.AddressEntry;
        Outlook.ExchangeUser userEx = user.GetExchangeUser();
        if (userEx == null)
        {
            return null;
        }
        Outlook.ExchangeUser manager =
            userEx.GetExchangeUserManager();
        if (manager == null)
        {
            return null;
        }
        foreach (Outlook.Recipient recip in appt.Recipients)
        {
            if (Application.Session.CompareEntryIDs(
                recip.AddressEntry.ID, manager.ID))
            {
                return recip.MeetingResponseStatus;
            }
        }
        return null;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
        return null;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="9f4f4-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f4f4-116">See also</span></span>

- [<span data-ttu-id="9f4f4-117">Usuarios de Exchange</span><span class="sxs-lookup"><span data-stu-id="9f4f4-117">exchange users</span></span>](exchange-users.md)

