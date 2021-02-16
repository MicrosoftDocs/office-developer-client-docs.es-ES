---
title: Crear una excepción para una cita en una serie de citas periódicas
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70e491069fd3f178371e9e8e3e6bcd8dc08e729e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356437"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a><span data-ttu-id="2f939-102">Crear una excepción para una cita en una serie de citas periódicas</span><span class="sxs-lookup"><span data-stu-id="2f939-102">Create an exception appointment in a recurring appointment series</span></span>

<span data-ttu-id="2f939-103">En este ejemplo se usa un objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) para crear una excepción en un patrón de periodicidad estándar de una cita.</span><span class="sxs-lookup"><span data-stu-id="2f939-103">This example uses an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object to create an exception to a standard recurrence pattern for an appointment.</span></span>

## <a name="example"></a><span data-ttu-id="2f939-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2f939-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="2f939-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="2f939-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="2f939-106">Una vez que se elimina o cambia una instancia de cita de una cita periódica, Outlook crea un objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="2f939-106">Once you delete or change one appointment instance of a recurring appointment, Outlook creates an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object.</span></span> <span data-ttu-id="2f939-107">El objeto Exception le permite crear una excepción en un patrón de periodicidad estándar de una cita.</span><span class="sxs-lookup"><span data-stu-id="2f939-107">The Exception object allows you to create an exception to a standard recurrence pattern.</span></span> <span data-ttu-id="2f939-108">Las propiedades del objeto contienen los cambios realizados en la instancia de la cita.</span><span class="sxs-lookup"><span data-stu-id="2f939-108">The object’s properties contain the changes that were made to the appointment instance.</span></span> <span data-ttu-id="2f939-109">La colección [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) contiene todos los objetos Exception de una cita periódica y está asociada al objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) de la cita.</span><span class="sxs-lookup"><span data-stu-id="2f939-109">The [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) collection contains all of the Exception objects for a recurring appointment, and is associated with the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span>

<span data-ttu-id="2f939-110">Para obtener el objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa la excepción en el patrón de periodicidad original de la cita periódica, use la propiedad [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) del objeto Exception.</span><span class="sxs-lookup"><span data-stu-id="2f939-110">To get the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents the exception to the original recurrence pattern of the recurring appointment, use the [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) property of the Exception.</span></span> <span data-ttu-id="2f939-111">Al usar los métodos y propiedades del objeto AppointmentItem devuelto, puede establecer las propiedades de la excepción de la cita.</span><span class="sxs-lookup"><span data-stu-id="2f939-111">By using the methods and properties of the returned AppointmentItem, you can set the properties of the appointment exception.</span></span>

<span data-ttu-id="2f939-112">Cuando se trabaja con elementos de citas periódicas, debe liberar todas las referencias anteriores, obtener nuevas referencias al elemento de cita periódico antes de tener acceso o modificar el elemento y liberar estas referencias, tan pronto como termine y haya guardado los cambios.</span><span class="sxs-lookup"><span data-stu-id="2f939-112">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="2f939-113">Este procedimiento se aplica al objeto periódico **AppointmentItem** y a cualquier objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) o [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="2f939-113">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="2f939-114">Para liberar una referencia en Visual Basic, establezca el objeto existente en Nothing.</span><span class="sxs-lookup"><span data-stu-id="2f939-114">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="2f939-115">En C\#, libere explícitamente la memoria para ese objeto.</span><span class="sxs-lookup"><span data-stu-id="2f939-115">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="2f939-p104">Tenga en cuenta que incluso después de liberar la referencia e intentar obtener una nueva, si aún hay una referencia activa a uno de los objetos anteriores, mantenida por otro complemento o Outlook, la nueva referencia puede apuntar a una copia obsoleta del objeto. Por lo tanto, es importante liberar las referencias cuando termine con la cita periódica.</span><span class="sxs-lookup"><span data-stu-id="2f939-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference, held by another add-in or Outlook, to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="2f939-118">En el siguiente ejemplo de código, CreateExceptionExample cambia el asunto de la cita periódica que se creó en el tema [Buscar una cita específica de una serie de citas periódicas](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md) y, a continuación, usa la propiedad AppointmentItem del objeto Exception resultante para recuperar el AppointmentItem que corresponde a la excepción de la cita.</span><span class="sxs-lookup"><span data-stu-id="2f939-118">In the following code example, CreateExceptionExample changes the subject of the recurring appointment that was created in the topic [Find a Specific Appointment in a Recurring Appointment Series](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md), and then uses the AppointmentItem property of the resulting Exception object to retrieve the AppointmentItem that corresponds to the appointment exception.</span></span> <span data-ttu-id="2f939-119">Después, CreateExceptionExample cambia las horas de inicio y fin de la excepción de la cita.</span><span class="sxs-lookup"><span data-stu-id="2f939-119">CreateExceptionExample then changes the start and end times of the appointment exception.</span></span>

<span data-ttu-id="2f939-120">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="2f939-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="2f939-121">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="2f939-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="2f939-122">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="2f939-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateExceptionExample()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find(
        "[Subject]='Recurring Appointment DaysOfWeekMask Example'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        try
        {
            Outlook.RecurrencePattern pattern =
                appt.GetRecurrencePattern();
            Outlook.AppointmentItem myInstance =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (myInstance != null)
            {
                myInstance.Subject = "My Exception";
                myInstance.Save();
                Outlook.RecurrencePattern newPattern =
                    appt.GetRecurrencePattern();
                Outlook.Exception myException =
                    newPattern.Exceptions[1];
                if (myException != null)
                {
                    Outlook.AppointmentItem myNewInstance =
                        myException.AppointmentItem;
                    myNewInstance.Start =
                        DateTime.Parse("7/21/2006 1:00 PM");
                    myNewInstance.End =
                        DateTime.Parse("7/21/2006 2:00 PM");
                    myNewInstance.Save();
                }
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="2f939-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f939-123">See also</span></span>

- [<span data-ttu-id="2f939-124">Citas</span><span class="sxs-lookup"><span data-stu-id="2f939-124">Appointments</span></span>](appointments.md)

