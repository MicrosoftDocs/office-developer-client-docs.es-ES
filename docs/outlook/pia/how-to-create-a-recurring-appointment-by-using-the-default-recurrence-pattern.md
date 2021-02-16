---
title: Crear una cita periódica mediante el patrón de periodicidad predeterminado
TOCTitle: Create a recurring appointment by using the default recurrence pattern
ms:assetid: 157bf1ae-2efe-4783-99ea-606722dde204
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184589(v=office.15)
ms:contentKeyID: 55119809
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: de58523e663349c43cc358f5b76896987a0f23b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332119"
---
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a><span data-ttu-id="ec12f-102">Crear una cita periódica mediante el patrón de periodicidad predeterminado</span><span class="sxs-lookup"><span data-stu-id="ec12f-102">Create a recurring appointment by using the default recurrence pattern</span></span>

<span data-ttu-id="ec12f-103">En este ejemplo se muestra cómo crear una cita periódica con el patrón de periodicidad predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ec12f-103">This example shows how to create a recurring appointment by using the default recurrence pattern.</span></span>

## <a name="example"></a><span data-ttu-id="ec12f-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec12f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ec12f-105">El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="ec12f-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="ec12f-106">Al crear una cita en Outlook, se crea un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ec12f-106">When you create an appointment in Outlook, you are creating an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="ec12f-107">La cita es una cita periódica, si la propiedad [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) de AppointmentItem se establece como verdadera.</span><span class="sxs-lookup"><span data-stu-id="ec12f-107">Your appointment is a recurring appointment if the [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) property of the AppointmentItem is set to true.</span></span> <span data-ttu-id="ec12f-108">IsRecurring no puede establecerse directamente.</span><span class="sxs-lookup"><span data-stu-id="ec12f-108">IsRecurring cannot be set directly.</span></span> 

<span data-ttu-id="ec12f-109">Pero, puede crear una cita periódica utilizando el objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ec12f-109">However, you can create a recurring appointment by using the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="ec12f-110">Para crear una cita periódica mediante programación, cree un objeto **AppointmentItem**, llame al método [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) del objeto **AppointmentItem** y, luego, guarde el objeto **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="ec12f-110">To create a recurring appointment programmatically, create an **AppointmentItem** object, call the [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) method of the **AppointmentItem** object, and then save the **AppointmentItem** object.</span></span> <span data-ttu-id="ec12f-111">Se crea una cita que usa el patrón de periodicidad predeterminado que se produce semanalmente en el día de la semana para el que se creó la cita y no tiene fecha de finalización.</span><span class="sxs-lookup"><span data-stu-id="ec12f-111">This creates an appointment that uses the default recurrence pattern, which occurs weekly on the day of the week for which the appointment was created, and has no end date.</span></span> <span data-ttu-id="ec12f-112">El objeto RecurrencePattern le permite crear citas periódicas a intervalos específicos: diaria, semanal, mensual o anual.</span><span class="sxs-lookup"><span data-stu-id="ec12f-112">The RecurrencePattern object allows you to create recurring appointments at specified intervals—daily, weekly, monthly, or yearly.</span></span> <span data-ttu-id="ec12f-113">Si no especifica los intervalos para el objeto RecurrencePattern, Outlook utilizará el patrón de periodicidad predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ec12f-113">If you do not specify intervals for the RecurrencePattern object, Outlook will use the default recurrence pattern.</span></span>

<span data-ttu-id="ec12f-114">Cuando se trabaja con elementos de citas periódicas, debe liberar todas las referencias anteriores, obtener nuevas referencias al elemento de cita periódico antes de tener acceso o modificar el elemento y liberar estas referencias, tan pronto como termine y haya guardado los cambios.</span><span class="sxs-lookup"><span data-stu-id="ec12f-114">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="ec12f-115">Este procedimiento se aplica al objeto periódico **AppointmentItem** y a cualquier objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) o [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ec12f-115">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="ec12f-116">Para liberar una referencia en Visual Basic, establezca el objeto existente en Nothing.</span><span class="sxs-lookup"><span data-stu-id="ec12f-116">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="ec12f-117">En C\#, libere explícitamente la memoria para ese objeto.</span><span class="sxs-lookup"><span data-stu-id="ec12f-117">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="ec12f-p104">Tenga en cuenta que incluso después de liberar la referencia e intentar obtener una nueva, si aún hay una referencia activa (retenida por otro complemento o Outlook) a uno de los objetos anteriores, la nueva referencia seguirá apuntando a una copia no actualizada del objeto. Por lo tanto, es importante liberar las referencias cuando termine con la cita periódica.</span><span class="sxs-lookup"><span data-stu-id="ec12f-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="ec12f-120">En el ejemplo siguiente, CreateRecurringAppointment crea un objeto **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="ec12f-120">In the following example, CreateRecurringAppointment creates an **AppointmentItem** object.</span></span> <span data-ttu-id="ec12f-121">Luego, llama al GetRecurrencePattern.</span><span class="sxs-lookup"><span data-stu-id="ec12f-121">It then calls GetRecurrencePattern.</span></span> <span data-ttu-id="ec12f-122">GetRecurrencePattern devuelve un objeto RecurrencePattern y se guarda el objeto AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="ec12f-122">GetRecurrencePattern returns a RecurrencePattern object, and the AppointmentItem is saved.</span></span> <span data-ttu-id="ec12f-123">Se crea una cita periódica mediante el patrón de periodicidad predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ec12f-123">This creates a recurring appointment that uses the default recurrence pattern.</span></span>

<span data-ttu-id="ec12f-124">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ec12f-124">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ec12f-125">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="ec12f-125">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ec12f-126">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="ec12f-126">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateRecurringAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Weekly Extensibility Team Meeting";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    appt.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="ec12f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec12f-127">See also</span></span>

- [<span data-ttu-id="ec12f-128">Citas</span><span class="sxs-lookup"><span data-stu-id="ec12f-128">Appointments</span></span>](appointments.md)

