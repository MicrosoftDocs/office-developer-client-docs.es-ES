---
title: Obtener el organizador de una reunión
TOCTitle: Get the organizer of a meeting
ms:assetid: 6a33db84-573b-4d1b-a91a-903f30630ec9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184615(v=office.15)
ms:contentKeyID: 55119872
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e19b293b581984e9dbb1fe27c9564cb78a73caa1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542540"
---
# <a name="get-the-organizer-of-a-meeting"></a><span data-ttu-id="5ad24-102">Obtener el organizador de una reunión</span><span class="sxs-lookup"><span data-stu-id="5ad24-102">Get the organizer of a meeting</span></span>

<span data-ttu-id="5ad24-103">Este ejemplo muestra cómo devolver el organizador de una reunión mediante programación.</span><span class="sxs-lookup"><span data-stu-id="5ad24-103">This example shows how to programmatically return the organizer of a meeting.</span></span>

## <a name="example"></a><span data-ttu-id="5ad24-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5ad24-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="5ad24-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="5ad24-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="5ad24-106">En el siguiente ejemplo de código, GetMeetingOrganizer toma un parámetro de tipo [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa una reunión y usa el objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) y el método [GetProperty ( String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) para obtener el [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) para el objeto **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="5ad24-106">In the following code example, GetMeetingOrganizer takes a parameter of type [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) that represents a meeting, and uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object and the [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) method to obtain the [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) for the **AppointmentItem** object.</span></span> <span data-ttu-id="5ad24-107">Una vez obtenga el **EntryID**, el ejemplo usa el método [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) para devolver el objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) que representa el organizador de la reunión.</span><span class="sxs-lookup"><span data-stu-id="5ad24-107">Once the **EntryID** is obtained, the example uses the [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) method to return the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object that represents the organizer of the meeting.</span></span>

<span data-ttu-id="5ad24-108">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5ad24-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="5ad24-109">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="5ad24-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5ad24-110">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="5ad24-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Outlook.AddressEntry GetMeetingOrganizer(Outlook.AppointmentItem appt)
{
    if (appt == null)
    {
        throw new ArgumentNullException();
    }
    string PR_SENT_REPRESENTING_ENTRYID =
        @"http://schemas.microsoft.com/mapi/proptag/0x00410102";
    string organizerEntryID =
        appt.PropertyAccessor.BinaryToString(
            appt.PropertyAccessor.GetProperty(
            PR_SENT_REPRESENTING_ENTRYID));
    Outlook.AddressEntry organizer =
        Application.Session.
        GetAddressEntryFromID(organizerEntryID);
    if (organizer != null)
    {
        return organizer; 
    }
    else
    {
        return null;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="5ad24-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ad24-111">See also</span></span>

- <span data-ttu-id="5ad24-112">[Meeting requests](meeting-requests.md) (Convocatorias de reunión)</span><span class="sxs-lookup"><span data-stu-id="5ad24-112">[Meeting requests](meeting-requests.md)</span></span>

