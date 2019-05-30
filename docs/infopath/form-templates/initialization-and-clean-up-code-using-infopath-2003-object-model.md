---
title: Utilizar código de limpieza e inicialización mediante el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, clean-up code,InfoPath 2003-compatible form templates, initialization code
localization_priority: Normal
ms.assetid: 8d19e8fa-4e5c-40bb-ae89-7a552cc7914d
description: De manera predeterminada, el archivo FormCode.cs o FormCode.vb que se crea para un proyecto nuevo de plantillas de formulario compatible con InfoPath 2003 contiene todo el código fuente de la lógica de programación del formulario. La plantilla del proyecto genera en este archivo una clase parecida a las de los ejemplos siguientes, en los que se puede definir el código de limpieza e inicialización, además de los controladores de los eventos del formulario. Los archivos FormCode.cs y FormCode.vb se aplican a un atributoSystem.ComponentModel.DescriptionAttribute de nivel de ensamblado, que identifica la clase como la única en la que se implementan los controladores de eventos. El atributo InfoPathNamespace (que implementa el tipo InfoPathNamespaceAttribute ) se aplica a una clase para identificar los espacios de nombres de selección del XML DOM que se utilizan dentro de la clase. El sistema de proyectos de InfoPath mantiene los espacios de nombres a los que se hace referencia en InfoPathNamespace.
ms.openlocfilehash: 659214a21dacf75b12f36cb6ad1e7f09c5af8800
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538371"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a><span data-ttu-id="5b23d-108">Utilizar código de limpieza e inicialización mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="5b23d-108">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>

<span data-ttu-id="5b23d-p102">De manera predeterminada, el archivo FormCode.cs o FormCode.vb que se crea para un proyecto nuevo de plantillas de formulario compatible con InfoPath 2003 contiene todo el código fuente de la lógica de programación del formulario. La plantilla del proyecto genera en este archivo una clase parecida a las de los ejemplos siguientes, en los que se puede definir el código de limpieza e inicialización, además de los controladores de los eventos del formulario. Los archivos FormCode.cs y FormCode.vb se aplican a un atributo **System.ComponentModel.DescriptionAttribute** de nivel de ensamblado, que identifica la clase como la única en la que se implementan los controladores de eventos. El atributo **InfoPathNamespace** (que implementa el tipo [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) ) se aplica a una clase para identificar los espacios de nombres de selección del XML DOM que se utilizan dentro de la clase. El sistema de proyectos de InfoPath mantiene los espacios de nombres a los que se hace referencia en **InfoPathNamespace**.</span><span class="sxs-lookup"><span data-stu-id="5b23d-p102">By default, the FormCode.cs or FormCode.vb file that is created for a form template project that is compatible with InfoPath 2003 contains all the source code for the programming logic of the form. The template for the project generates a class in the FormCode.cs or FormCode.vb file much like the classes in the following examples where you can define initialization and clean-up code, as well as handlers for form events. The FormCode.cs and FormCode.vb files apply an assembly-level **System.ComponentModel.DescriptionAttribute** attribute, which identifies the class as the only class where event handlers are implemented. The **InfoPathNamespace** attribute (which is implemented by the [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) type) is applied to a class to identify the XML DOM selection namespaces used within the class. The namespaces referenced in the **InfoPathNamespace** are maintained by the InfoPath project system.</span></span> 
  
<span data-ttu-id="5b23d-114">La clase FormCode proporciona los métodos  `_Startup` y  `_Shutdown`, que se emplean para llevar a cabo rutinas de inicialización y limpieza de cualquier componente que sea necesario para complementar la funcionalidad estándar de InfoPath mientras está abierto el formulario.</span><span class="sxs-lookup"><span data-stu-id="5b23d-114">The FormCode class itself provides  `_Startup` and  `_Shutdown` methods that are used to perform initialization and clean-up routines for any components that are required in addition to standard InfoPath functionality while the form is open.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5b23d-p103">[!IMPORTANTE] No llame a los miembros del modelo de objetos de InfoPath desde los métodos  `_Startup` y  `_Shutdown`. Sólo debe inicializar y llamar a miembros de componentes externos de estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5b23d-p103">Do not call members of the InfoPath object model from within the  `_Startup` and  `_Shutdown` methods. You should initialize and call only members of external components in these methods.</span></span> 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-27-27'")]
    public partial class FormCode
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // You can add additional initialization code here.
        }
        public void _Shutdown()
        {
        }
    }
}
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
    ' The namespace prefixes defined in this attribute must remain synchronized with
    ' those in the form definition file (.xsf).
    <InfoPathNamespace( _
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-36-40'")> _
    Public Class FormCode
        Private thisXDocument As XDocument
        Private thisApplication As Application
        Public Sub _Startup(app As Application, doc As XDocument)
            thisXDocument = doc
            thisApplication = app
            ' You can add additional initialization code here.
        End Sub
        Public Sub _Shutdown()
        End Sub
    End Class
End Namespace
```

## <a name="the-startup-method"></a><span data-ttu-id="5b23d-117">Método _Startup</span><span class="sxs-lookup"><span data-stu-id="5b23d-117">The _Startup Method</span></span>

<span data-ttu-id="5b23d-p104">Además de proporcionar una ubicación para escribir el código de inicialización de los componentes adicionales, el método  `_Startup` inicializa las variables  `thisXDocument` y  `thisApplication`, que se pueden emplear en el código del formulario para obtener acceso a los miembros de las clases [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) y [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) del modelo de objetos de InfoPath. La plantilla de proyectos genera automáticamente el código necesario para inicializar las dos variables.</span><span class="sxs-lookup"><span data-stu-id="5b23d-p104">In addition to providing a place to write initialization code for additional components, the  `_Startup` method initializes the  `thisXDocument` and  `thisApplication` variables that can be used in your form code to access the members of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) and [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) classes in the InfoPath object model. The code necessary to initialize the two variables is generated automatically by the project template.</span></span> 
  
```cs
    private XDocument thisXDocument;
    private Application thisApplication;
    public void _Startup(Application app, XDocument doc)
    {
        thisXDocument = doc;
        thisApplication = app;
        // You can add additional initialization code here.
    }
```

```vb
    Private thisXDocument As XDocument
    Private thisApplication As Application
    Public Sub _Startup(app As Application, doc As XDocument)
        thisXDocument = doc
        thisApplication = app
        ' You can add additional initialization code here.
    End Sub

```

<span data-ttu-id="5b23d-120">Los ejemplos siguientes muestran un controlador de eventos simple para un botón que utiliza la variable  `thisXDocument` para obtener acceso al método [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) del tipo [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5b23d-120">The following examples show a simple event handler for a button that uses the  `thisXDocument` variable to access the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) type.</span></span> 
  
```cs
[InfoPathEventHandler(MatchPath="CTRL1_5", EventType=InfoPathEventType.OnClick)]
public void CTRL1_5_OnClick(DocActionEvent e)
{
    // Write your code here.
    thisXDocument.UI.Alert("Hello!");
}
```

```vb
<InfoPathEventHandler(MatchPath:="CTRL1_5", EventType:=InfoPathEventType.OnClick)> _
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
    ' Write your code here.
    thisXDocument.UI.Alert("Hello!")
End Sub
```

<span data-ttu-id="5b23d-121">Para obtener información sobre cómo crear un controlador de eventos, vea [Agregar un controlador de eventos mediante el modelo de objetos de InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="5b23d-121">For information on how to create an event handler, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
  
## <a name="the-shutdown-method"></a><span data-ttu-id="5b23d-122">Método _ShutDown</span><span class="sxs-lookup"><span data-stu-id="5b23d-122">The _ShutDown Method</span></span>

<span data-ttu-id="5b23d-p105">El método  `_Shutdown` es el último método al que se llama cuando se cierra un formulario. Puede escribir cualquier tipo de código en este método necesario para limpiar o finalizar los componentes utilizados en el formulario.</span><span class="sxs-lookup"><span data-stu-id="5b23d-p105">The  `_Shutdown` method is the last method called when a form is closed. You can write any code in this method that is needed to clean up or finalize components used in the form.</span></span> 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a><span data-ttu-id="5b23d-125">Ejemplo de código de limpieza e inicialización</span><span class="sxs-lookup"><span data-stu-id="5b23d-125">Initialization and Clean-up Code Example</span></span>

<span data-ttu-id="5b23d-p106">En el ejemplo siguiente, se muestra cómo inicializar una conexión a una base de datos de Microsoft SQL Server en el método  `_Startup` y cerrar la conexión en el método  `_Shutdown`. Para que este ejemplo funcione correctamente, primero debe establecer una referencia al ensamblado System.Data de .NET Framework, haciendo clic en la opción **Agregar referencia** del menú **Proyecto** y, después, debe seleccionar el componente System.Data.dll en la ficha **.NET**. Tenga en cuenta, además, que la directiva  `using System.Data.SqlClient` (o  `Imports System.Data.SqlClient)`) se agrega al principio del archivo de código del formulario para reducir el número de pulsaciones.</span><span class="sxs-lookup"><span data-stu-id="5b23d-p106">The following example shows how to initialize a connection to a Microsoft SQL Server database in the  `_Startup` method and close the connection in the  `_Shutdown` method. In order for this example to work correctly, you must first set a reference to the System.Data assembly of the .NET Framework by clicking **Add Reference** on the **Project** menu, and then selecting the System.Data.dll component on the **.NET** tab. Also note that the  `using System.Data.SqlClient` (or  `Imports System.Data.SqlClient)` directive was added at the top of the form code file to reduce keystrokes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5b23d-128">[!NOTA] Puede que los usuarios de un formulario de InfoPath que contenga código que se conecte a una base de datos de SQL necesiten permisos de seguridad según la forma en que se implemente el formulario y cómo se defina la directiva de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5b23d-128">Users of an InfoPath form that contains form code that connects to a SQL Server database may require security permissions depending on how the form is deployed and security policy is defined.</span></span> <span data-ttu-id="5b23d-129">Para obtener más información sobre seguridad, vea [el modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md) y [configurar las opciones de seguridad de las plantillas de formulario con código](how-to-configure-security-settings-for-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="5b23d-129">For more information on security see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md) and [Configure Security Settings for Form Templates with Code](how-to-configure-security-settings-for-form-templates-with-code.md).</span></span> 
  
```cs
using System;
using System.Data.SqlClient;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-05T20-56-13'")]
    public partial class Template1
    {
        private XDocument    thisXDocument;
        private Application    thisApplication;
        private SqlConnection sqlConnect;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // Initialize variable for SQL Server connection.
            sqlConnect= new SqlConnection("server=localhost;Trusted_Connection=yes;database=Northwind");
        }
        public void _Shutdown()
        {
            // Close SQL Server connection at shut down.
            sqlConnect.Close();
        }
    }
}
```

```vb
Imports System
Imports System.Data.SqlClient
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
        ' The namespace prefixes defined in this attribute must remain synchronized with
        ' those in the form definition file (.xsf).
        <InfoPathNamespace( _
            "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-08T18-47-33'")>        _
        Public Class Template1
            Private thisXDocument As XDocument
            Private thisApplication As Application
            Private sqlConnect As SqlConnection
            Public Sub _Startup(app As Application, doc As XDocument)
                thisXDocument = doc
                thisApplication = app
                ' Initialize variable for SQL Server connection.
                sqlConnect = New SqlConnection _("server=localhost;Trusted_Connection=yes;database=Northwind")
            End Sub
        Public Sub _Shutdown()
            ' Close SQL Server connection.
            sqlConnect.Close()
        End Sub
    End Class
End Namespace
```

## <a name="see-also"></a><span data-ttu-id="5b23d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b23d-130">See also</span></span>



[<span data-ttu-id="5b23d-131">Adición de un controlador de eventos mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="5b23d-131">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

