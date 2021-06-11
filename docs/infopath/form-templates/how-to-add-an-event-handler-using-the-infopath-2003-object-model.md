---
title: Agregar un controlador de eventos con el modelo de objetos de InfoPath
manager: soliver
ms.date: 01/20/2015
ms.audience: Developer
keywords:
- onafterimport event [infopath 2007],OnAfterChange event [InfoPath 2007],OnBeforeChange event [InfoPath 2007],OnSubmitRequest event [InfoPath 2007],OnVersionUpgrade event [InfoPath 2007],InfoPath 2003-compatible form templates, event handlers,OnLoad event [InfoPath 2007],event handlers [InfoPath 2007], adding using InfoPath 2003 object model,OnValidate event [InfoPath 2007],OnContextChange event [InfoPath 2007],OnSaveRequest event [InfoPath 2007],OnClick event [InfoPath 2007],OnSwitchView event [InfoPath 2007],OnSign event [InfoPath 2007],OnMergeRequest event [InfoPath 2007]
localization_priority: Normal
ms.assetid: 0520df55-2d91-4cc5-be31-82144a2db4f6
description: Los comandos de menú para agregar funciones de controlador de eventos a un proyecto de plantilla de formulario compatible con el modelo de objetos de InfoPath 2003 son fundamentalmente los mismos que los utilizados en otros tipos de plantilla de formulario.
ms.openlocfilehash: 8533b6bc11dccdad9d0f05de35406ad3cf68eacd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303671"
---
# <a name="add-an-event-handler-using-the-infopath-object-model"></a>Agregar un controlador de eventos con el modelo de objetos de InfoPath

Los comandos de menú para agregar funciones de controlador de eventos a un proyecto de plantilla de formulario compatible con el modelo de objetos de InfoPath 2003 son fundamentalmente los mismos que los utilizados en otros tipos de plantilla de formulario. Por ejemplo, para agregar un controlador de eventos **OnLoad**, con la plantilla de formulario abierta en el diseñador de InfoPath, haga clic en **Evento Al cargar (OnLoad)** en la ficha **Programador**. En el editor de código de Visual Studio 2012, el foco se desplazará automáticamente al código del formulario relacionado con el controlador de eventos **OnLoad**. 
  
En los proyectos de plantillas de formulario con código administrado compatibles con InfoPath 2003, la clase que contiene funciones de controlador de eventos y los propios controladores de eventos se identifican mediante atributos específicos de InfoPath en el módulo de código.

## <a name="adding-event-handlers"></a>Agregar controladores de eventos

En todos los procedimientos siguientes, se da por supuesto que el usuario tiene abierto un proyecto de plantilla de formulario en Microsoft InfoPath con Visual Studio 2012.
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a>Agregar un controlador de eventos para el evento OnClick de un botón de comando

1. En el panel **Controles**, haga clic en **Botón** para agregar un botón al formulario. 
    
2. En la ficha **Propiedades**, haga clic en **Código personalizado**.
    
   Se desplazará el foco al código auxiliar del controlador de eventos del evento [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) en el editor de código. 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a>Agregar un controlador de eventos para el evento OnBeforeChange, OnValidate u OnAfterChange de un campo o un grupo

1. Haga clic con el botón secundario en un control de entrada de datos enlazado al campo o grupo, como un control de **Cuadro de texto**. 
    
2. Seleccione **Programación** y, a continuación, haga clic en uno de los comandos, como por ejemplo **Evento Al validar (OnValidate)**.
    
   El foco cambia al código auxiliar del controlador de eventos para uno de los siguientes eventos en el editor de código: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)o [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx). 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a>Agregar un controlador de eventos para el evento OnLoad, OnSwitchView, OnContextChange u OnSign de un formulario

- En el menú **Herramientas**, seleccione **Programación** y haga clic en el evento de formularios para el que desee escribir un controlador de eventos.
    
    El foco cambia al código auxiliar del controlador de eventos para uno de los siguientes en el editor de código: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)o [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx). 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a>Agregar un controlador de eventos para el evento OnSubmitRequest de un formulario

1. En la ficha **Datos**, haga clic en **Opciones de envío**.
    
2. Active la casilla **Permitir que los usuarios envíen este formulario** y haga clic en **Realizar acción personalizada mediante el código**.
    
3. Haga clic en **Modificar código** y después en **Aceptar**.
    
   El foco se desplazará al código auxiliar del controlador de eventos del evento [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) en el editor de código. 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a>Agregar un controlador de eventos para el evento OnSaveRequest de un formulario

1. Haga clic en la pestaña **Archivo** y, a continuación, en **Opciones de formulario**.
    
2. En la categoría **Guardar**, haga clic en **Guardar usando código personalizado**, haga clic en **Editar** y después haga clic en **Aceptar**.
    
   El foco se desplazará al código auxiliar del controlador de eventos del evento [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) en el editor de código. 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a>Agregar un controlador de eventos para el evento OnVersionUpgrade de un formulario

1. Haga clic en la pestaña **Archivo** y, a continuación, en **Opciones de formulario**.
    
2. En la categoría **Control de versiones**, seleccione **Utilizar evento personalizado** en la lista **Actualizar formularios existentes**, haga clic en **Editar** y a continuación haga clic en **Aceptar**.
    
    El foco se desplazará al código auxiliar del controlador de eventos del evento [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) del editor de código. 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a>Agregar un controlador de eventos para el evento OnMergeRequest de un formulario

1. Haga clic en la pestaña **Archivo** y, a continuación, en **Opciones de formulario**.
    
2. En la categoría **Avanzadas**, active las casillas **Habilitar la combinación de formularios** y **Combinar usando código personalizado**, haga clic en **Editar** y a continuación haga clic en **Aceptar**.
    
    El foco se desplazará al código auxiliar del controlador de eventos del evento[OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) en el editor de código. 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a>Agregar un controlador de eventos para el evento OnAfterImport

Para agregar controladores de eventos para el evento [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) , debe abrir el código de formulario de la plantilla de formulario con código administrado y agregar la función de controlador de eventos manualmente. Para obtener información acerca de cómo escribir un controlador de eventos para este evento, haga clic en el vínculo del evento **OnAfterImport**. 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a>Agregar un controlador de eventos para un origen de datos secundario

En el ejemplo siguiente se muestra cómo agregar un controlador de eventos para un origen de datos secundario. En el ejemplo se supone que existe un origen de datos secundario procedente de un archivo de recursos llamado books.xml, que tiene el siguiente esquema:
  
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

La vista del formulario se genera a partir de este origen de datos. El código de formulario crea una tabla hash basándose en los autores y en el número de libros que han escrito. Si actualiza una de las entradas de la tabla que aparece en la vista, el controlador de eventos **OnAfterChange** actualizará la tabla hash. Tenga en cuenta que la propiedad [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) del atributo **InfoPathEventHandler** (implementada por la clase [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) se utiliza para establecer una referencia al origen de datos secundario. 
  
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

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a>Cómo se identifica la clase que contiene controladores de eventos

Al crear un proyecto nuevo de plantillas de formulario de InfoPath compatible con el modelo de objetos de código administrado DE InfoPath 2003, se aplica un atributo de nivel de ensamblado **System.ComponentModel.Description**, a la clase que aparece al principio del módulo de código de formulario, para identificar la clase que contiene todos los controladores de eventos de plantilla de formulario. 
  
> [!IMPORTANT]
> [!IMPORTANTE] No modifique el atributo **System.ComponentModel.Description** de esta clase. Si lo hiciera, la plantilla de formulario no podrá identificar dónde se encuentran los controladores de eventos y éstos no podrán ejecutarse. 
  
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

## <a name="how-event-handlers-are-identified"></a>Cómo se identifican los controladores de eventos

Al agregar un nuevo controlador de eventos utilizando comandos de menú o botones en la interfaz de usuario del modo de diseño de InfoPath, el código auxiliar de la función de controlador de eventos se escribe en el formulario. En el ejemplo siguiente se muestra el controlador de eventos de código auxiliar creado para un evento[OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) agregado para un campo denominado 'total'. 
  
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

A continuación, podrá agregar el código que invoca a los miembros del modelo de objetos de InfoPath utilizando los miembros privados almacenados en la memoria caché de las variables  `thisXDocument` o  `thisApplication`, o usando los miembros a los que se obtiene acceso desde los objetos  `e` **EventArgs** que recibe el controlador de eventos: 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

El atributo **InfoPathEventHandler** (según su definición de la clase [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) es el atributo personalizado de las funciones que se utilizarán como controladores de eventos. 
  
Cuando el evento lo requiera, el parámetro **MatchPath** (tal como lo define la propiedad [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) de la clase **InfoPathEventHandlerAttribute**) especifica una expresión XPath que identifica el origen del evento. El parámetro **EventType** (tal como lo define la propiedad [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) de la clase **InfoPathEventHandlerAttribute**) especifica el tipo de evento. No debe cambiar los valores de estos parámetros. Si lo hace, es posible que el controlador de eventos no se compile correctamente o que la notificación del evento no se produzca como se esperaba. 
  
## <a name="obfuscating-code-in-event-handlers"></a>Ocultación de código en controladores de eventos

Si ejecuta una utilidad de protección en el ensamblado que se genera al compilar una plantilla de formulario con código administrado ( *nombreproyecto*  .dll), InfoPath no podrá cargar el ensamblado cuando un usuario abra el formulario. Si desea proteger el código de los controladores de eventos u otro código de formulario, colóquelo en otro ensamblado, incluya una referencia a ese ensamblado en el proyecto y después llame a los miembros del ensamblado de la referencia desde FormCode.cs o FormCode.vb. Es importante que sólo ejecute la utilidad de protección en el ensamblado de la referencia. 
  
## <a name="see-also"></a>Vea también

- [Responder a eventos de formulario mediante el modelo de objetos de InfoPath 2003](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

