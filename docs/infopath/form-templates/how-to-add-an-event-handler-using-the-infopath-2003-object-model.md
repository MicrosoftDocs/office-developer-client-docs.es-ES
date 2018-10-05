---
title: Agregar un controlador de eventos con el modelo de objetos de InfoPath
manager: soliver
ms.date: 01/20/2015
ms.audience: Developer
keywords:
- onafterimport event [infopath 2007],OnAfterChange event [InfoPath 2007],OnBeforeChange event [InfoPath 2007],OnSubmitRequest event [InfoPath 2007],OnVersionUpgrade event [InfoPath 2007],InfoPath 2003-compatible form templates, event handlers,OnLoad event [InfoPath 2007],event handlers [InfoPath 2007], adding using InfoPath 2003 object model,OnValidate event [InfoPath 2007],OnContextChange event [InfoPath 2007],OnSaveRequest event [InfoPath 2007],OnClick event [InfoPath 2007],OnSwitchView event [InfoPath 2007],OnSign event [InfoPath 2007],OnMergeRequest event [InfoPath 2007]
localization_priority: Normal
ms.assetid: 0520df55-2d91-4cc5-be31-82144a2db4f6
description: Los comandos de menú para agregar funciones de controlador de eventos de un proyecto de plantilla de formulario que sea compatible con el modelo de objetos de InfoPath 2003 esencialmente son los mismos que los de otros tipos de plantillas de formulario.
ms.openlocfilehash: 8533b6bc11dccdad9d0f05de35406ad3cf68eacd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386708"
---
# <a name="add-an-event-handler-using-the-infopath-object-model"></a><span data-ttu-id="d6d5e-104">Agregar un controlador de eventos con el modelo de objetos de InfoPath</span><span class="sxs-lookup"><span data-stu-id="d6d5e-104">Add an event handler using the InfoPath object model</span></span>

<span data-ttu-id="d6d5e-p101">Los comandos de menú para agregar funciones de controlador de eventos a un proyecto de plantilla de formulario compatible con el modelo de objetos de InfoPath 2003 son fundamentalmente los mismos que los utilizados en otros tipos de plantilla de formulario. Por ejemplo, para agregar un controlador de eventos **OnLoad**, con la plantilla de formulario abierta en el diseñador de InfoPath, haga clic en **Evento Al cargar (OnLoad)** en la ficha **Programador**. En el editor de código de Visual Studio 2012, el foco se desplazará automáticamente al código del formulario relacionado con el controlador de eventos **OnLoad**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-p101">The menu commands for adding event handler functions in a form template project that is compatible with the InfoPath 2003 object model are essentially the same as those for other types of form templates. For example, in order to add an **OnLoad** event handler, with the form template open in the InfoPath designer, click the **On Load Event** command on the **Developer** tab. The focus automatically switches to the form code for the **OnLoad** event handler in the Visual Studio 2012 code editor.</span></span> 
  
<span data-ttu-id="d6d5e-107">En los proyectos de plantillas de formulario con código administrado compatibles con InfoPath 2003, la clase que contiene funciones de controlador de eventos y los propios controladores de eventos se identifican mediante atributos específicos de InfoPath en el módulo de código.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-107">In managed-code form template projects compatible with InfoPath 2003, the class that contains event handler functions and the event handlers themselves are identified by attributes specific to InfoPath in the code module.</span></span>

## <a name="adding-event-handlers"></a><span data-ttu-id="d6d5e-108">Adición de controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="d6d5e-108">Adding event handlers</span></span>

<span data-ttu-id="d6d5e-109">En todos los procedimientos siguientes, se da por supuesto que el usuario tiene abierto un proyecto de plantilla de formulario en Microsoft InfoPath con Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-109">All of the following procedures assume that you have a form template project open in Microsoft InfoPath with Visual Studio 2012.</span></span>
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a><span data-ttu-id="d6d5e-110">Agregar un controlador de eventos para el evento OnClick de un botón de comando</span><span class="sxs-lookup"><span data-stu-id="d6d5e-110">Add an event handler for the OnClick event of a command button</span></span>

1. <span data-ttu-id="d6d5e-111">En el panel **Controles**, haga clic en **Botón** para agregar un botón al formulario.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-111">In the **Controls** pane, click **Button** to add a button to the form.</span></span> 
    
2. <span data-ttu-id="d6d5e-112">En la ficha **Propiedades**, haga clic en **Código personalizado**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-112">On the **Properties** tab, click **Custom Code**.</span></span>
    
   <span data-ttu-id="d6d5e-113">Se desplazará el foco al código auxiliar del controlador de eventos del evento [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) en el editor de código.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-113">The focus switches to the stub for the event handler for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a><span data-ttu-id="d6d5e-114">Agregar un controlador de eventos para el evento OnBeforeChange, OnValidate u OnAfterChange de un campo o un grupo</span><span class="sxs-lookup"><span data-stu-id="d6d5e-114">Add an event handler for the OnBeforeChange, OnValidate, or OnAfterChange event of a field or group</span></span>

1. <span data-ttu-id="d6d5e-115">Haga clic con el botón secundario en un control de entrada de datos enlazado al campo o grupo, como un control de **Cuadro de texto**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-115">Right-click a data-entry control bound to the field or group, such as a **Text Box** control.</span></span> 
    
2. <span data-ttu-id="d6d5e-116">Seleccione **Programación** y, a continuación, haga clic en uno de los comandos, como por ejemplo **Evento Al validar (OnValidate)**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-116">Point to **Programming**, and then click one of the commands, such as **On Validate Event**.</span></span>
    
   <span data-ttu-id="d6d5e-117">Se desplazará el foco al código auxiliar del controlador de eventos para uno de los siguientes eventos en el editor de código: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)u [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx).</span><span class="sxs-lookup"><span data-stu-id="d6d5e-117">The focus switches to the stub for the event handler for one of the following events in the code editor: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx), or [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a><span data-ttu-id="d6d5e-118">Agregar un controlador de eventos para el evento OnLoad, OnSwitchView, OnContextChange u OnSign de un formulario</span><span class="sxs-lookup"><span data-stu-id="d6d5e-118">Add an event handler for the OnLoad, OnSwitchView, OnContextChange, or OnSign event of a form</span></span>

- <span data-ttu-id="d6d5e-119">En el menú **Herramientas**, seleccione **Programación** y haga clic en el evento de formularios para el que desee escribir un controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-119">On the **Tools** menu, point to **Programming**, and then click the form event that you want to write an event handler for.</span></span>
    
    <span data-ttu-id="d6d5e-120">Se desplazará el foco al código auxiliar del controlador de eventos para uno de los siguientes procedimientos en el editor de código: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)u [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx).</span><span class="sxs-lookup"><span data-stu-id="d6d5e-120">The focus switches to the stub for the event handler for one of the following in the code editor: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx), or [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a><span data-ttu-id="d6d5e-121">Agregar un controlador de eventos para el evento OnSubmitRequest de un formulario</span><span class="sxs-lookup"><span data-stu-id="d6d5e-121">Add an event handler for the OnSubmitRequest event of a form</span></span>

1. <span data-ttu-id="d6d5e-122">En la ficha **Datos**, haga clic en **Opciones de envío**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-122">On the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="d6d5e-123">Active la casilla **Permitir que los usuarios envíen este formulario** y haga clic en **Realizar acción personalizada mediante el código**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-123">Select the **Allow users to submit this form** check box, and then click **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="d6d5e-124">Haga clic en **Modificar código** y después en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-124">Click **Edit Code**, and then click **OK**.</span></span>
    
   <span data-ttu-id="d6d5e-125">El foco se desplazará al código auxiliar del controlador de eventos del evento [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) en el editor de código.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-125">The focus switches to the stub for the event handler for the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a><span data-ttu-id="d6d5e-126">Agregar un controlador de eventos para el evento OnSaveRequest de un formulario</span><span class="sxs-lookup"><span data-stu-id="d6d5e-126">Add an event handler for the OnSaveRequest event of a form</span></span>

1. <span data-ttu-id="d6d5e-127">Haga clic en la pestaña **Archivo** y, a continuación, en **Opciones de formulario**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-127">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="d6d5e-128">En la categoría **Guardar**, haga clic en **Guardar usando código personalizado**, haga clic en **Editar** y después haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-128">In the **Save** category, click **Save using custom code**, click **Edit**, and then click **OK**.</span></span>
    
   <span data-ttu-id="d6d5e-129">El foco se desplazará al código auxiliar del controlador de eventos del evento [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) en el editor de código.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-129">The focus switches to the stub for the event handler for the [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a><span data-ttu-id="d6d5e-130">Agregar un controlador de eventos para el evento OnVersionUpgrade de un formulario</span><span class="sxs-lookup"><span data-stu-id="d6d5e-130">Add an event handler for the OnVersionUpgrade event of a form</span></span>

1. <span data-ttu-id="d6d5e-131">Haga clic en la pestaña **Archivo** y, a continuación, en **Opciones de formulario**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-131">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="d6d5e-132">En la categoría **Control de versiones**, seleccione **Utilizar evento personalizado** en la lista **Actualizar formularios existentes**, haga clic en **Editar** y a continuación haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-132">In the **Versioning** category, select **Use custom event** from the **Update existing forms** list, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="d6d5e-133">El foco se desplazará al código auxiliar del controlador de eventos del evento [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) del editor de código.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-133">The focus switches to the stub for the event handler for the [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a><span data-ttu-id="d6d5e-134">Agregar un controlador de eventos para el evento OnMergeRequest de un formulario</span><span class="sxs-lookup"><span data-stu-id="d6d5e-134">Add an event handler for the OnMergeRequest event of a form</span></span>

1. <span data-ttu-id="d6d5e-135">Haga clic en la pestaña **Archivo** y, a continuación, en **Opciones de formulario**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-135">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="d6d5e-136">En la categoría **Avanzadas**, active las casillas **Habilitar la combinación de formularios** y **Combinar usando código personalizado**, haga clic en **Editar** y a continuación haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-136">In the **Advanced** category, select the **Enable Form merging** and the **Merge using custom code** check boxes, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="d6d5e-137">El foco se desplazará al código auxiliar del controlador de eventos del evento[OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) en el editor de código.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-137">The focus switches to the stub for the event handler for the [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) event in the code editor.</span></span> 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a><span data-ttu-id="d6d5e-138">Adición de un controlador de eventos para el evento OnAfterImport</span><span class="sxs-lookup"><span data-stu-id="d6d5e-138">Adding an event handler for the OnAfterImport event</span></span>

<span data-ttu-id="d6d5e-p102">Para agregar controladores de eventos para el evento [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) , debe abrir el código de formulario de la plantilla de formulario con código administrado y agregar la función de controlador de eventos manualmente. Para obtener información acerca de cómo escribir un controlador de eventos para este evento, haga clic en el vínculo del evento **OnAfterImport**.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-p102">To add event handlers for the [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) event, you must open the form code for your managed-code form template and add the event handler function manually. For information on how to write an event handler for this event, click the link for the **OnAfterImport** event.</span></span> 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a><span data-ttu-id="d6d5e-141">Adición de un controlador de eventos para un origen de datos secundario</span><span class="sxs-lookup"><span data-stu-id="d6d5e-141">Adding an event handler for a secondary data source</span></span>

<span data-ttu-id="d6d5e-p103">En el ejemplo siguiente se muestra cómo agregar un controlador de eventos para un origen de datos secundario. En el ejemplo se supone que existe un origen de datos secundario procedente de un archivo de recursos llamado books.xml, que tiene el siguiente esquema:</span><span class="sxs-lookup"><span data-stu-id="d6d5e-p103">The following example shows how to add an event handler for a secondary data source. The example assumes a secondary data source from a resource file named books.xml, which has the following schema:</span></span>
  
```xml
<?xml version="1.0"?>
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema">
    <xsd:element name="catalog">
        <xsd:complexType>
            <xsd:sequence>
                <xsd:element ref="book" minOccurs="0" maxOccurs="unbounded"></xsd:element>
            </xsd:sequence>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="genre" type="xsd:string"></xsd:element>
    <xsd:element name="author" type="xsd:string"></xsd:element>
    <xsd:element name="book">
        <xsd:complexType>
            <xsd:all>
                <xsd:element ref="author" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="title" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="genre" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="price" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="publish_date" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="description" minOccurs="0" maxOccurs="1"></xsd:element>
            </xsd:all>
            <xsd:attribute ref="id"></xsd:attribute>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="price" type="xsd:string"></xsd:element>
    <xsd:element name="title" type="xsd:string"></xsd:element>
    <xsd:element name="publish_date" type="xsd:string"></xsd:element>
    <xsd:element name="description" type="xsd:string"></xsd:element>
    <xsd:attribute name="id" type="xsd:string"></xsd:attribute>
</xsd:schema>

```

<br/>

<span data-ttu-id="d6d5e-p104">La vista del formulario se genera a partir de este origen de datos. El código de formulario crea una tabla hash basándose en los autores y en el número de libros que han escrito. Si actualiza una de las entradas de la tabla que aparece en la vista, el controlador de eventos **OnAfterChange** actualizará la tabla hash. Tenga en cuenta que la propiedad [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) del atributo **InfoPathEventHandler** (implementada por la clase [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) se utiliza para establecer una referencia al origen de datos secundario.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-p104">The form's view is built from this data source. The form code creates a hash table based on the authors and the number of books they have written. You can update an entry from the table shown in the view and the **OnAfterChange** event handler updates the hash table. Note that the [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) property of the **InfoPathEventHandler** attribute (which is implemented by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is used to reference the secondary data source.</span></span> 
  
```cs
namespace AuxDom
{
    // InfoPathNamespace attribute goes here.
    public class AuxDom
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        private Hashtable authors;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            authors = new Hashtable();
        }
        public void _Shutdown()
        {
            authors.Clear();
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
        public void OnLoad(DocReturnEvent e)
        {
            IXMLDOMDocument books = thisXDocument.GetDOM("books");
            DOMNodeList externalAuthors = books.selectNodes("/catalog/book/author");
            foreach (IXMLDOMNode authorNode in externalAuthors)
            {
                AddBookFromAuthor(authorNode.text);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="/catalog/book/author", EventType=InfoPathEventType.OnAfterChange, DataObject="books")]
        public void books__author_OnAfterChange(DataDOMEvent e)
        {
            if (e.IsUndoRedo)
            {
                // An undo or redo operation has occurred and the DOM 
                // is read-only.
                return;
            }
            
            if (e.Source.text != e.NewValue.ToString())
            {
                RemoveBookFromAuthor(e.OldValue.ToString());
                AddBookFromAuthor(e.NewValue.ToString());
            }
        }
        private void AddBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] + 1;
            }
            else
            {
                authors.Add(authorName, 1);
            }
        }
        private void RemoveBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] - 1;
            }
            if ((int)authors[authorName] == 0)
            {
                authors.Remove(authorName);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="ShowAuthors", EventType=InfoPathEventType.OnClick)]
        public void ShowAuthors_OnClick(DocActionEvent e)
        {
            // Write your code here.
            StringBuilder report = new StringBuilder();
            foreach (string authorName in authors.Keys)
            {
                report.Append(authorName + ",\t\t\t");
                report.Append(authors[authorName] + "\n");
            }
            thisXDocument.UI.Alert(report.ToString());
        }
    }
}

```

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a><span data-ttu-id="d6d5e-148">¿Cómo se identifica la clase que contiene los controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="d6d5e-148">How the class that contains event handlers is identified</span></span>

<span data-ttu-id="d6d5e-149">Al crear un proyecto nuevo de plantillas de formulario de InfoPath compatible con el modelo de objetos de código administrado DE InfoPath 2003, se aplica un atributo de nivel de ensamblado **System.ComponentModel.Description**, a la clase que aparece al principio del módulo de código de formulario, para identificar la clase que contiene todos los controladores de eventos de plantilla de formulario.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-149">When you create a new InfoPath form template project that is compatible with the InfoPath 2003 managed code object model, an assembly-level **System.ComponentModel.Description** attribute is applied to the class at the beginning of the form code module to identify the class that contains all event handlers for the form template.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d6d5e-p105">[!IMPORTANTE] No modifique el atributo **System.ComponentModel.Description** de esta clase. Si lo hiciera, la plantilla de formulario no podrá identificar dónde se encuentran los controladores de eventos y éstos no podrán ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-p105">Do not modify the **System.ComponentModel.Description** attribute in this class. If you do so, your form template will not be able to identify where event handlers are located, and the event handlers will fail to run.</span></span> 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the // form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute(    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
' Office integration attribute. Identifies the startup class for the form. Do not modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
```

## <a name="how-event-handlers-are-identified"></a><span data-ttu-id="d6d5e-152">¿Cómo se identifican los controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="d6d5e-152">How event handlers are identified</span></span>

<span data-ttu-id="d6d5e-p106">Al agregar un nuevo controlador de eventos utilizando comandos de menú o botones en la interfaz de usuario del modo de diseño de InfoPath, el código auxiliar de la función de controlador de eventos se escribe en el formulario. En el ejemplo siguiente se muestra el controlador de eventos de código auxiliar creado para un evento[OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) agregado para un campo denominado 'total'.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-p106">When you add a new event handler using menu commands or buttons in the InfoPath design mode user interface, the stub for the event handler function is written into the form. The following example shows the stub event handler created for an [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) added for a field named 'total'.</span></span> 
  
```cs
[InfoPathEventHandler(MatchPath="/invoice/total", EventType=InfoPathEventType.OnValidate)]
public void total_OnValidate(DataDOMEvent e)
{
    // Write your code here.
}

```

```vb
<InfoPathEventHandler(MatchPath:="/invoice/total",EventType:= OnValidate)> Public Sub total_OnValidate(ByVal e As EventArgs)
    ' Write your code here.
End Sub

```

<span data-ttu-id="d6d5e-155">A continuación, podrá agregar el código que invoca a los miembros del modelo de objetos de InfoPath utilizando los miembros privados almacenados en la memoria caché de las variables  `thisXDocument` o  `thisApplication`, o usando los miembros a los que se obtiene acceso desde los objetos  `e` **EventArgs** que recibe el controlador de eventos:</span><span class="sxs-lookup"><span data-stu-id="d6d5e-155">You can then add code that invokes members of the InfoPath object model using the private cached members of the  `thisXDocument` or  `thisApplication` variables, or by using the members accessed from the  `e` **EventArgs** object received by the event handler:</span></span> 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

<span data-ttu-id="d6d5e-156">El atributo **InfoPathEventHandler** (según su definición de la clase [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) es el atributo personalizado de las funciones que se utilizarán como controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-156">The **InfoPathEventHandler** attribute (as defined by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is the custom attribute for functions that will be used as event handlers.</span></span> 
  
<span data-ttu-id="d6d5e-p107">Cuando el evento lo requiera, el parámetro **MatchPath** (tal como lo define la propiedad [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) de la clase **InfoPathEventHandlerAttribute**) especifica una expresión XPath que identifica el origen del evento. El parámetro **EventType** (tal como lo define la propiedad [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) de la clase **InfoPathEventHandlerAttribute**) especifica el tipo de evento. No debe cambiar los valores de estos parámetros. Si lo hace, es posible que el controlador de eventos no se compile correctamente o que la notificación del evento no se produzca como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-p107">When required by the event, the **MatchPath** parameter (as defined by the [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies an XPath expression that identifies the event source. The **EventType** parameter (as defined by the [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies the type of event. You should not change the values of these parameters. If the values of these parameters are changed, the event handler may not compile correctly, or event notification will not occur as expected.</span></span> 
  
## <a name="obfuscating-code-in-event-handlers"></a><span data-ttu-id="d6d5e-161">Ofuscar código en controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="d6d5e-161">Obfuscating code in event handlers</span></span>

<span data-ttu-id="d6d5e-p108">Si ejecuta una utilidad de protección en el ensamblado que se genera al compilar una plantilla de formulario con código administrado ( *nombreproyecto*  .dll), InfoPath no podrá cargar el ensamblado cuando un usuario abra el formulario. Si desea proteger el código de los controladores de eventos u otro código de formulario, colóquelo en otro ensamblado, incluya una referencia a ese ensamblado en el proyecto y después llame a los miembros del ensamblado de la referencia desde FormCode.cs o FormCode.vb. Es importante que sólo ejecute la utilidad de protección en el ensamblado de la referencia.</span><span class="sxs-lookup"><span data-stu-id="d6d5e-p108">If you run an obfuscator utility on the assembly that is generated when a managed-code form template is compiled ( *projectname*  .dll), InfoPath will not be able to load the assembly when a user opens the form. If you want to obfuscate the code for your event handlers or other form code, you must put the code that you want to obfuscate in a separate assembly, and reference that assembly in your project, and then call members of the referenced assembly from FormCode.cs or FormCode.vb. It is important that you run the obfuscator utility only on the referenced assembly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6d5e-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6d5e-165">See also</span></span>

- [<span data-ttu-id="d6d5e-166">Responder a eventos de formulario con el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="d6d5e-166">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

