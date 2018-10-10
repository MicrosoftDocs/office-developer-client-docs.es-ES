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
# <a name="implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector"></a>Implementar un contenedor para inspectores y realizar un seguimiento de eventos al nivel del elemento en cada inspector

Este tema contiene dos ejemplos de código que muestran cómo implementar un contenedor para una colección [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) y cómo usarlo para realizar un seguimiento de eventos al nivel del elemento en cada objeto [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) de la colección.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Los dos siguientes ejemplos de código implementan las clases Connect y OutlookInspector. El primer ejemplo implica métodos y controladores de eventos que se incluyen en la clase Connect para implementar un contenedor para una colección **Inspectors**. El segundo ejemplo implica una implementación simple de la clase **OutlookInspector**.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

En el siguiente ejemplo de código, un evento [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) se produce después de haber creado una nueva ventana de inspector y antes de que se muestre. Una acción de un usuario también puede crear una nueva ventana de inspector. Se declara una variable de instancia a nivel de clase denominada inspectores en la clase **Connect** y se enlaza un evento **NewInspector**. 

En el método inspectors\_NewInspector, el método **FindOutlookInspector** comprueba si la nueva ventana del inspector ya está en la lista inspectorWindows. Si FindOutlookInspector no encuentra el objeto **Inspector** en inspectorWindows, el método **AddInspector** agrega una instancia de la clase **OutlookInspector** a inspectorWindows. Puede usar la clase **OutlookInspector** para provocar eventos para esta ventana de inspector en particular. La implementación de la clase **OutlookInspector** se muestra en el segundo ejemplo de código.

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

El siguiente ejemplo de código es una implementación de la clase **OutlookInspector**. Esta clase se usa para provocar eventos para la ventana de inspector en el ejemplo de código anterior. Se pueden abrir varios inspectores simultáneamente. Se realiza un seguimiento de los eventos de nivel de elemento como [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)) y [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) enlazándolos en el constructor de la clase. Un evento [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) para un objeto [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) también se enlaza en el constructor de la clase. Puede definir otras variables de instancia del elemento de nivel clase según sea necesario. Todos los eventos que se enlazaron en el constructor OutlookInspector se desenlazan en el controlador de eventos OutlookInspectorWindow\_Close.

Tenga en cuenta que en el nivel de modelo de objetos, un objeto **inspector de Outlook** no es específico para ningún tipo de elemento de Outlook. Este ejemplo de código utiliza la clase auxiliar OutlookItem, definida en [Crear una clase auxiliar para acceder a los miembros de elementos comunes de Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) para llamar a la propiedad OutlookItem.Class para comprobar la clase de mensaje del elemento actual en el inspector, antes de asumir que el elemento es un elemento de contacto.

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

## <a name="see-also"></a>Vea también

- [Tareas de ejemplo que usan eventos de Outlook](sample-tasks-using-outlook-events.md)

