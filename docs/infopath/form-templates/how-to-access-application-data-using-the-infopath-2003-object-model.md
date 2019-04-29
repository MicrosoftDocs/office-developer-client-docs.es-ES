---
title: Obtener acceso a datos de aplicaciones mediante el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- form templates [infopath 2007], accessing data using 2003 object model,InfoPath 2003-compatible form templates, accessing application data
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: El modelo de objetos compatible con InfoPath 2003 proporciona objetos y colecciones que se pueden utilizar para obtener acceso a la información sobre la aplicación InfoPath, incluida información relacionada con el documento XML subyacente de un formulario y el archivo de definición de formulario (.xsf). Para obtener acceso a estos datos se utiliza el objeto de nivel superior en la jerarquía del modelo de objetos de InfoPath, del que se crea una instancia utilizando la interfaz Application .
ms.openlocfilehash: 849882a97109d91a5807a6798d5a62457ab971fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437444"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a><span data-ttu-id="2c919-105">Obtener acceso a datos de aplicaciones mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="2c919-105">Access Application Data Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="2c919-p102">El modelo de objetos compatible con InfoPath 2003 proporciona objetos y colecciones que se pueden utilizar para obtener acceso a la información sobre la aplicación InfoPath, incluida información relacionada con el documento XML subyacente de un formulario y el archivo de definición de formulario (.xsf). Para obtener acceso a estos datos se utiliza el objeto de nivel superior en la jerarquía del modelo de objetos de InfoPath, del que se crea una instancia utilizando la interfaz [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2c919-p102">The InfoPath 2003-compatible object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file. This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> 
  
<span data-ttu-id="2c919-p103">Los proyectos de plantilla de formulario con código administrado compatibles con InfoPath 2003 creados con Visual Studio 2012 inicializan la variable  `thisApplication` del método  `_Startup` de la clase de código de formulario, que puede utilizarse para obtener acceso a los miembros de la interfaz [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . En el ejemplo siguiente, se usan las propiedades [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) y [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) de la interfaz [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) para devolver el nombre y el número de versión de la instancia de InfoPath que se está ejecutando. Esta información se muestra en un cuadro de mensaje mediante el método [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) de la interfaz [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2c919-p103">An InfoPath 2003-compatible managed code form template project created using Visual Studio 2012 initializes the  `thisApplication` variable in the  `_Startup` method of the form code class, which can be used to access the members of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface. In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface are used to return the name and version number of the running instance of InfoPath. This information is displayed in a message box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

<span data-ttu-id="2c919-p104">En el ejemplo de Visual C#, el código no administrado de InfoPath presenta la referencia al carácter  `\n` de la cadena del mensaje de alerta como un salto de línea estándar que hace que el texto aparezca en una nueva línea en el cuadro de mensaje. Para utilizar explícitamente el valor de nueva línea definido para el entorno y la plataforma actuales, use la propiedad **Environment.NewLine** como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2c919-p104">In the Visual C# example, the reference to the  `\n` character in the string for the alert message is rendered by InfoPath unmanaged code as a standard new line feed that causes the text to break and be placed on a new line in the message box. To explicitly use the new line value defined for the current environment and platform, use the **Environment.NewLine** property instead, as shown in the following example.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a><span data-ttu-id="2c919-113">Obtener acceso a datos desde el documento XML subyacente de un formulario</span><span class="sxs-lookup"><span data-stu-id="2c919-113">Accessing Data from the Underlying XML Document of a Form</span></span>

<span data-ttu-id="2c919-114">Los programadores pueden utilizar la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) para obtener acceso a la información sobre el documento XML subyacente de un formulario, incluida una referencia a un Modelo de objetos de documento (DOM) XML que contiene los datos XML de origen del formulario.</span><span class="sxs-lookup"><span data-stu-id="2c919-114">Developers can use the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface to gain access to information about a form's underlying XML document, including a reference to an XML Document Object Model (DOM) that contains the source XML data of the form.</span></span> 
  
<span data-ttu-id="2c919-p105">En el ejemplo siguiente, el primer cuadro de mensaje muestra algunos de los datos que están disponibles desde la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , como si se ha cambiado el documento XML subyacente (mediante la propiedad [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) ) y si se ha firmado digitalmente (mediante la propiedad [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) ). El siguiente cuadro de mensaje utiliza la propiedad [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) de la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) para mostrar el código XML de origen del documento XML subyacente del formulario.</span><span class="sxs-lookup"><span data-stu-id="2c919-p105">In the following example, the first message box displays some of the data that is available from the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, such as whether the underlying XML document has been changed (by using the [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) property) and whether it has been digitally signed (using the [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) property). The next message box uses the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface's [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) property to display the source XML of the form's underlying XML document.</span></span> 
  
```cs
thisXDocument.UI.Alert("\nIsDirty: " + thisXDocument.IsDirty +
   "\nIsDOMReadOnly: " + thisXDocument.IsDOMReadOnly +
   "\nIsNew: " + thisXDocument.IsNew +
   "\nIsReadOnly: " + thisXDocument.IsReadOnly +
   "\nIsSigned: " + thisXDocument.IsSigned);
thisXDocument.UI.Alert(thisXDocument.DOM.xml);
```

```vb
thisXDocument.UI.Alert("IsDirty: " &amp; thisXDocument.IsDirty &amp; vbNewLine &amp; _
   "IsDOMReadOnly: " &amp; thisXDocument.IsDOMReadOnly &amp; vbNewLine &amp; _
   "IsNew: " &amp; thisXDocument.IsNew &amp; vbNewLine &amp; _
   "IsReadOnly: " &amp; thisXDocument.IsReadOnly &amp; vbNewLine &amp; _
   "IsSigned: " &amp; thisXDocument.IsSigned)
thisXDocument.UI.Alert(thisXDocument.DOM.xml)
```

<span data-ttu-id="2c919-p106">La propiedad **xml** utilizada en el ejemplo anterior es una propiedad del modelo de objetos de documentos (DOM) XML. Para obtener más información sobre el XML DOM, consulte la documentación de MSXML 5.0 SDK.</span><span class="sxs-lookup"><span data-stu-id="2c919-p106">The **xml** property used in the previous example is a property of the XML Document Object Model (DOM). For more information about the XML DOM, see the MSXML 5.0 SDK documentation.</span></span> 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a><span data-ttu-id="2c919-119">Obtener acceso a los datos desde el archivo de definición del formulario</span><span class="sxs-lookup"><span data-stu-id="2c919-119">Accessing Data from a Form's Form Definition File</span></span>

<span data-ttu-id="2c919-p107">También es posible tener acceso a la información sobre el archivo .xsf de un formulario, incluida la referencia de un DOM XML a los datos de XML de origen que contiene, mediante la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . El acceso a esta información se obtiene mediante la propiedad [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) , que devuelve una referencia a la interfaz [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2c919-p107">Information about a form's .xsf file, including an XML DOM reference to the source XML data that it contains, can also be accessed using the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface. This information is accessed using the [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) property, which returns a reference to the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface.</span></span> 
  
<span data-ttu-id="2c919-p108">En el ejemplo siguiente, la primera alerta muestra algunos de los datos disponibles a través de la interfaz [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) , como su ubicación de identificador uniforme de recursos (URI) (utilizando la propiedad [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) ) y su número de versión (usando la propiedad [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) ). La siguiente alerta utiliza la propiedad [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) de la interfaz [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) para mostrar el XML de origen del archivo .xsf.</span><span class="sxs-lookup"><span data-stu-id="2c919-p108">In the following example, the first alert displays some of the data that is available through the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface, such as its Uniform Resource Identifier (URI) location (using the [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) property) and its version number (using the [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) property). The next alert uses the [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) property of the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface to display the source XML of the .xsf file.</span></span> 
  
```cs
thisXDocument.UI.Alert("PackageURL: " +
   thisXDocument.Solution.PackageURL +
   "\nURI: " + thisXDocument.Solution.URI +
   "\nVersion: " + thisXDocument.Solution.Version);
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml);
```

```vb
thisXDocument.UI.Alert("PackageURL: " &amp; _
   thisXDocument.Solution.PackageURL &amp; vbNewLine &amp; _
   "URI: " &amp; thisXDocument.Solution.URI &amp; vbNewLine &amp; _
   "Version: " &amp; thisXDocument.Solution.Version)
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml)
```


