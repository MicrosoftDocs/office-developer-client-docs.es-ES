---
title: Usar el cuadro de diálogo Seleccionar nombres para obtener y asignar destinatarios a una cita
TOCTitle: Use the Select Names dialog box to obtain and assign recipients to an appointment
ms:assetid: b9bcb341-1912-425c-8d75-ed5be233145a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184636(v=office.15)
ms:contentKeyID: 55119878
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 408d2fbdc3c89b7f2bad1fe9c2c76c1f47ae05ff
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722770"
---
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a><span data-ttu-id="fb08b-102">Usar el cuadro de diálogo Seleccionar nombres para obtener y asignar destinatarios a una cita</span><span class="sxs-lookup"><span data-stu-id="fb08b-102">Use the Select Names dialog box to obtain and assign recipients to an appointment</span></span>

<span data-ttu-id="fb08b-103">En este ejemplo se muestra cómo usar el cuadro de diálogo **Seleccionar nombres** para obtener y asignar destinatarios a un elemento de cita.</span><span class="sxs-lookup"><span data-stu-id="fb08b-103">This example shows how to use the **Select Names** dialog box to obtain and assign recipients to an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="fb08b-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb08b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fb08b-105">El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="fb08b-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="fb08b-106">Para mostrar el cuadro de diálogo **Seleccionar nombres**, llame al método [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) del objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="fb08b-106">To display the **Select Names** dialog box, call the [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) method of the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object.</span></span> <span data-ttu-id="fb08b-107">Una vez que se muestra al usuario el cuadro de diálogo **Seleccionar nombres**, se detiene la ejecución de código hasta que el usuario hace clic en **Aceptar** o cierra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fb08b-107">Once the **Select Names** dialog box is displayed to the user, code execution halts until the user clicks **OK** or closes the dialog box.</span></span> <span data-ttu-id="fb08b-108">Para establecer los destinatarios iniciales que se muestran en el cuadro de diálogo, o para que los destinatarios sean seleccionados en el cuadro de diálogo, use la propiedad [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) del objeto **SelectNamesDialog**.</span><span class="sxs-lookup"><span data-stu-id="fb08b-108">To set initial recipients to display in the dialog box, or to get the recipients selected in the dialog box, use the [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) property of the **SelectNamesDialog** object.</span></span> <span data-ttu-id="fb08b-109">Esto devuelve una colección [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) asociada al objeto **SelectNamesDialog**.</span><span class="sxs-lookup"><span data-stu-id="fb08b-109">This returns a [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that is associated with the **SelectNamesDialog**.</span></span> <span data-ttu-id="fb08b-110">Para añadir un objeto de [destinatario](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) a la colección **Recipients** del **SelectNamesDialog**, use el método [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) de la colección y especifique la propiedad [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) del objeto de **destinatario**.</span><span class="sxs-lookup"><span data-stu-id="fb08b-110">To add a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object to the **Recipients** collection for the **SelectNamesDialog**, use the [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) method for the collection and specify the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of the **Recipient** object.</span></span>

<span data-ttu-id="fb08b-111">En el ejemplo siguiente, DemoSelectNamesDialogRecipients crea un objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) y establece algunas de sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="fb08b-111">In the following code example, DemoSelectNamesDialogRecipients creates an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object and sets some of its properties.</span></span> <span data-ttu-id="fb08b-112">A continuación, crea un **SelectNamesDialog** y usa el método [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) para configurar un modo de presentación de la reunión para el cuadro de diálogo **Seleccionar nombres**.</span><span class="sxs-lookup"><span data-stu-id="fb08b-112">It then creates a **SelectNamesDialog** and uses the [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) method to set a meeting display mode for the **Select Names** dialog box.</span></span> <span data-ttu-id="fb08b-113">En el ejemplo se rellena el selector de destinatario **Resource** con la cadena "Sala de conferencias 36/2739".</span><span class="sxs-lookup"><span data-stu-id="fb08b-113">The example populates the **Resource** recipient selector with the string "Conf Room 36/2739".</span></span> <span data-ttu-id="fb08b-114">Una vez que se muestra el cuadro de diálogo al usuario, el código enumera la colección **Recipients** asociada a esta instancia del **SelectNamesDialog** y agrega los destinatarios a la cita que se había creado.</span><span class="sxs-lookup"><span data-stu-id="fb08b-114">Once the dialog box is displayed to the user, the code enumerates the **Recipients** collection that is associated with this instance of **SelectNamesDialog** and adds those recipients to the appointment that was created.</span></span> <span data-ttu-id="fb08b-115">Por último, en el ejemplo se muestra la convocatoria de reunión para el usuario.</span><span class="sxs-lookup"><span data-stu-id="fb08b-115">Finally, the example displays the meeting request to the user.</span></span>

<span data-ttu-id="fb08b-116">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="fb08b-116">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="fb08b-117">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="fb08b-117">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="fb08b-118">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="fb08b-118">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoSelectNamesDialogRecipients()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Subject = "Team Morale Event";
    appt.Start = DateTime.Parse("5/17/2007 11:00 AM");
    appt.End = DateTime.Parse("5/17/2007 12:00 PM");
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    snd.SetDefaultDisplayMode(
        Outlook.OlDefaultSelectNamesDisplayMode.olDefaultMeeting);
    Outlook.Recipient confRoom =
        snd.Recipients.Add("Conf Room 36/2739");
    // Explicitly specify Recipient.Type.
    confRoom.Type = (int)Outlook.OlMeetingRecipientType.olResource;
    snd.Recipients.ResolveAll();
    snd.Display();
    // Add Recipients to meeting request.
    Outlook.Recipients recips = snd.Recipients;
    if (recips.Count > 0)
    {
        foreach (Outlook.Recipient recip in recips)
        {
            appt.Recipients.Add(recip.Name);
        }
    }
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="fb08b-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb08b-119">See also</span></span>

- [<span data-ttu-id="fb08b-120">Destinatarios</span><span class="sxs-lookup"><span data-stu-id="fb08b-120">Recipients</span></span>](recipients.md)

