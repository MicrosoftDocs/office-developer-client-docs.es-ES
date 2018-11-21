---
title: Implementar un contenedor para inspectores y realizar un seguimiento de eventos al nivel del elemento en cada inspector
TOCTitle: Implement a wrapper for inspectors and track item-level events in each inspector
ms:assetid: 8021dd2b-c36c-492b-b281-783e85140ad8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184620(v=office.15)
ms:contentKeyID: 55119854
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d5fee97e27b616232f2f45eb42faf659eee52cda
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405773"
---
# <a name="implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector"></a><span data-ttu-id="b9ae7-102">Implementar un contenedor para inspectores y realizar un seguimiento de eventos al nivel del elemento en cada inspector</span><span class="sxs-lookup"><span data-stu-id="b9ae7-102">Implement a Wrapper for Inspectors and Track Item-Level Events in Each Inspector</span></span>

<span data-ttu-id="b9ae7-103">Este tema contiene dos ejemplos de código que muestran cómo implementar un contenedor para una colección [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) y cómo usarlo para realizar un seguimiento de eventos al nivel del elemento en cada objeto [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) de la colección.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-103">This topic contains two code examples that show how to implement a wrapper for an [T:Microsoft.Office.Interop.Outlook.Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) collection and to use that wrapper to track item-level events in each [T:Microsoft.Office.Interop.Outlook.Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) object in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="b9ae7-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9ae7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b9ae7-105">El siguiente ejemplo es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="b9ae7-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="b9ae7-106">Los dos siguientes ejemplos de código implementan las clases Connect y OutlookInspector.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-106">The following two code examples implement the Connect and OutlookInspector classes.</span></span> <span data-ttu-id="b9ae7-107">El primer ejemplo implica métodos y controladores de eventos que se incluyen en la clase Connect para implementar un contenedor para una colección **Inspectors**.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-107">The following two code examples implement the Connect and OutlookInspector classes. The first code example involves methods and event handlers you include in the Connect class to implement a wrapper for an **Inspectors** collection. The second code example involves a simple implementation of the OutlookInspector class.</span></span> <span data-ttu-id="b9ae7-108">El segundo ejemplo implica una implementación simple de la clase **OutlookInspector**.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-108">The second code example involves a simple implementation of the **OutlookInspector** class.</span></span>

<span data-ttu-id="b9ae7-109">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-109">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="b9ae7-110">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b9ae7-111">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="b9ae7-112">En el siguiente ejemplo de código, un evento [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) se produce después de haber creado una nueva ventana de inspector y antes de que se muestre.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-112">In the following code example, a [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) event occurs after a new inspector window has been created and before it is displayed.</span></span> <span data-ttu-id="b9ae7-113">Una acción de un usuario también puede crear una nueva ventana de inspector.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-113">A user action may also create a new inspector window.</span></span> <span data-ttu-id="b9ae7-114">Se declara una variable de instancia a nivel de clase denominada inspectores en la clase **Connect** y se enlaza un evento **NewInspector**.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-114">A class-level instance variable named inspectors in the **Connect** class is declared, and a **NewInspector** event is hooked up.</span></span> 

<span data-ttu-id="b9ae7-115">En el método inspectors\_NewInspector, el método **FindOutlookInspector** comprueba si la nueva ventana del inspector ya está en la lista inspectorWindows.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-115">In the inspectors\_NewInspector method, the **FindOutlookInspector** method checks whether the new inspector window is already in the inspectorWindows list.</span></span> <span data-ttu-id="b9ae7-116">Si FindOutlookInspector no encuentra el objeto **Inspector** en inspectorWindows, el método **AddInspector** agrega una instancia de la clase **OutlookInspector** a inspectorWindows.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-116">If FindOutlookInspector does not find the **Inspector** object in inspectorWindows, the **AddInspector** method adds an instance of the **OutlookInspector** class to inspectorWindows.</span></span> <span data-ttu-id="b9ae7-117">Puede usar la clase **OutlookInspector** para provocar eventos para esta ventana de inspector en particular.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-117">You can use the **OutlookInspector** class to raise events for this particular inspector window.</span></span> <span data-ttu-id="b9ae7-118">La implementación de la clase **OutlookInspector** se muestra en el segundo ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-118">The implementation of the **OutlookInspector** class is shown in the second code example.</span></span>

```csharp
class Connect
{
    // Connect class-level Instance Variables
    // Outlook inspectors collection
    private Outlook.Inspectors inspectors;

    // Collection of tracked inspector windows              
    private List<OutlookInspector> inspectorWindows;    

    // Hook up NewInspector event
    inspectors.NewInspector += new 
        Outlook.InspectorsEvents_NewInspectorEventHandler(
        inspectors_NewInspector);

    // NewInspector event creates new instance of OutlookInspector
    void inspectors_NewInspector(Outlook.Inspector Inspector)
    {
        // Check to see if this is a new window you don't
        // already track
        OutlookInspector existingWindow = 
            FindOutlookInspector(Inspector);
        if (existingWindow == null)
        {
            AddInspector(Inspector);
        }
    }

    // Adds an instance of **OutlookInspector** class
    private void AddInspector(Outlook.Inspector inspector)
    {
        OutlookInspector window = new OutlookInspector(inspector);
        window.Close +=
            new EventHandler(WrappedInspectorWindow_Close);
    }

    // Looks up the window wrapper for a given Inspector 
    // window object
    private OutlookInspector FindOutlookInspector(object window)
    {
        foreach (OutlookInspector inspector in inspectorWindows)
        {
            if (inspector.Window == window)
            {
                return inspector;
            }
        }
        return null;
    }
}
```

<span data-ttu-id="b9ae7-119">El siguiente ejemplo de código es una implementación de la clase **OutlookInspector**.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-119">The following code example is an implementation of the **OutlookInspector** class.</span></span> <span data-ttu-id="b9ae7-120">Esta clase se usa para provocar eventos para la ventana de inspector en el ejemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-120">This class is used to raise events for the inspector window from the preceding code example.</span></span> <span data-ttu-id="b9ae7-121">Se pueden abrir varios inspectores simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-121">Multiple inspector windows can be open simultaneously.</span></span> <span data-ttu-id="b9ae7-122">Se realiza un seguimiento de los eventos de nivel de elemento como [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)) y [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) enlazándolos en el constructor de la clase.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-122">Item-level events such as [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)), and [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) are tracked by hooking them up in this class constructor.</span></span> <span data-ttu-id="b9ae7-123">Un evento [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) para un objeto [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) también se enlaza en el constructor de la clase.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-123">A [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) event for a [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object is also hooked up in this class constructor.</span></span> <span data-ttu-id="b9ae7-124">Puede definir otras variables de instancia del elemento de nivel clase según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-124">You can define other class-level item instance variables as needed.</span></span> <span data-ttu-id="b9ae7-125">Todos los eventos que se enlazaron en el constructor OutlookInspector se desenlazan en el controlador de eventos OutlookInspectorWindow\_Close.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-125">All the events that were hooked up in the OutlookInspector constructor are unhooked in the OutlookInspectorWindow\_Close event handler.</span></span>

<span data-ttu-id="b9ae7-126">Tenga en cuenta que en el nivel de modelo de objetos, un objeto **inspector de Outlook** no es específico para ningún tipo de elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-126">Note that at the object model level, an **Outlook inspector** object is not specific to any Outlook item type.</span></span> <span data-ttu-id="b9ae7-127">Este ejemplo de código utiliza la clase auxiliar OutlookItem, definida en [Crear una clase auxiliar para acceder a los miembros de elementos comunes de Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) para llamar a la propiedad OutlookItem.Class para comprobar la clase de mensaje del elemento actual en el inspector, antes de asumir que el elemento es un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-127">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.Class property to verify the message class of the current item in the inspector, before assuming the item is a contact item.</span></span>

```csharp
// This class tracks the state of an Outlook Inspector window 
// and ensures that what happens in this window is handled correctly.
class OutlookInspector
{
    // OutlookInspector class-level instance variables 
    // wrapped window object
    private Outlook.Inspector m_Window;             

    // Use these instance variables to handle item-level events
    // wrapped MailItem
    private Outlook.MailItem m_Mail;    
    // wrapped AppointmentItem        
    private Outlook.AppointmentItem m_Appointment;  
    // wrapped ContactItem
    private Outlook.ContactItem m_Contact;
    // wrapped TaskItem      
    private Outlook.ContactItem m_Task;             

    // OutlookInspector constructor
    public OutlookInspector(Outlook.Inspector inspector)
    {
        m_Window = inspector;

        // Hook up the close event
        ((Outlook.InspectorEvents_Event)inspector).Close +=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Hook up item-level events as needed
        OutlookItem olItem = new OutlookItem(inspector.CurrentItem);
        if(olItem.Class==Outlook.OlObjectClass.olContact)
        {
            m_Contact = olItem.InnerObject as Outlook.ContactItem;
            m_Contact.Open +=
                new Outlook.ItemEvents_10_OpenEventHandler(
                m_Contact_Open);
            m_Contact.PropertyChange +=
                new Outlook.ItemEvents_10_PropertyChangeEventHandler(
                m_Contact_PropertyChange);
            m_Contact.CustomPropertyChange +=
                new Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
                m_Contact_CustomPropertyChange);
        }
    }

    // Event Handler for the inspector close event.
    private void OutlookInspectorWindow_Close()
    {
        // Unhook events from any item-level instance variables
        m_Contact.Open -= 
            Outlook.ItemEvents_10_OpenEventHandler(
            m_Contact_Open);
        m_Contact.PropertyChange -= 
            Outlook.ItemEvents_10_PropertyChangeEventHandler(
            m_Contact_PropertyChange);
        m_Contact.CustomPropertyChange -= 
            Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
            m_Contact_CustomPropertyChange);
        ((Outlook.ItemEvents_Event)m_Contact).Close -= 
            Outlook.ItemEvents_CloseEventHandler(
            m_Contact_Close);

        // Unhook events from the window
        ((Outlook.InspectorEvents_Event)m_Window).Close -=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Raise the OutlookInspector close event
        if (Close != null)
        {
            Close(this, EventArgs.Empty);
        }
        // Release item-level instance variables
        m_Mail = null;
        m_Appointment = null;
        m_Contact = null;
        m_Task = null;
        m_Window = null;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b9ae7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9ae7-128">See also</span></span>

- [<span data-ttu-id="b9ae7-129">Tareas de ejemplo que usan eventos de Outlook</span><span class="sxs-lookup"><span data-stu-id="b9ae7-129">Sample Tasks Using Outlook Events</span></span>](sample-tasks-using-outlook-events.md)

