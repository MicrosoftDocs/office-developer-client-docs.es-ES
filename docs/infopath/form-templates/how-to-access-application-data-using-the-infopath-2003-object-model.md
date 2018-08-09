---
title: Obtener acceso a los datos de aplicaciones con el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- form templates [infopath 2007], accessing data using 2003 object model,InfoPath 2003-compatible form templates, accessing application data
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: El modelo de objetos compatible con InfoPath 2003 proporciona objetos y colecciones que se pueden utilizar para obtener acceso a la información sobre la aplicación InfoPath, incluida información relacionada con el documento XML subyacente de un formulario y el archivo de definición de formulario (.xsf). Para obtener acceso a estos datos se utiliza el objeto de nivel superior en la jerarquía del modelo de objetos de InfoPath, del que se crea una instancia utilizando la interfaz Application .
ms.openlocfilehash: e9cf01ff2ffa939fce5af277e756e679478f8b39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815851"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a>Obtener acceso a los datos de aplicaciones con el modelo de objetos de InfoPath 2003

El modelo de objetos compatible con InfoPath 2003 proporciona objetos y colecciones que se pueden utilizar para obtener acceso a la información sobre la aplicación InfoPath, incluida información relacionada con el documento XML subyacente de un formulario y el archivo de definición de formulario (.xsf). Para obtener acceso a estos datos se utiliza el objeto de nivel superior en la jerarquía del modelo de objetos de InfoPath, del que se crea una instancia utilizando la interfaz [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . 
  
Los proyectos de plantilla de formulario con código administrado compatibles con InfoPath 2003 creados con Visual Studio 2012 inicializan la variable  `thisApplication` del método  `_Startup` de la clase de código de formulario, que puede utilizarse para obtener acceso a los miembros de la interfaz [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . En el ejemplo siguiente, se usan las propiedades [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) y [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) de la interfaz [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) para devolver el nombre y el número de versión de la instancia de InfoPath que se está ejecutando. Esta información se muestra en un cuadro de mensaje mediante el método [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) de la interfaz [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) . 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

En el ejemplo de Visual C#, el código no administrado de InfoPath presenta la referencia al carácter  `\n` de la cadena del mensaje de alerta como un salto de línea estándar que hace que el texto aparezca en una nueva línea en el cuadro de mensaje. Para utilizar explícitamente el valor de nueva línea definido para el entorno y la plataforma actuales, use la propiedad **Environment.NewLine** como se muestra en el siguiente ejemplo. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a>Obtener acceso a datos desde el documento XML subyacente de un formulario

Los programadores pueden utilizar la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) para obtener acceso a la información sobre el documento XML subyacente de un formulario, incluida una referencia a un Modelo de objetos de documento (DOM) XML que contiene los datos XML de origen del formulario. 
  
En el ejemplo siguiente, el primer cuadro de mensaje muestra algunos de los datos que están disponibles desde la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , como si se ha cambiado el documento XML subyacente (mediante la propiedad [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) ) y si se ha firmado digitalmente (mediante la propiedad [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) ). El siguiente cuadro de mensaje utiliza la propiedad [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) de la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) para mostrar el código XML de origen del documento XML subyacente del formulario. 
  
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

La propiedad **xml** utilizada en el ejemplo anterior es una propiedad del modelo de objetos de documentos (DOM) XML. Para obtener más información sobre el XML DOM, consulte la documentación de MSXML 5.0 SDK. 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a>Obtener acceso a los datos desde el archivo de definición del formulario

También es posible tener acceso a la información sobre el archivo .xsf de un formulario, incluida la referencia de un DOM XML a los datos de XML de origen que contiene, mediante la interfaz [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . El acceso a esta información se obtiene mediante la propiedad [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) , que devuelve una referencia a la interfaz [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) . 
  
En el ejemplo siguiente, la primera alerta muestra algunos de los datos disponibles a través de la interfaz [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) , como su ubicación de identificador uniforme de recursos (URI) (utilizando la propiedad [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) ) y su número de versión (usando la propiedad [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) ). La siguiente alerta utiliza la propiedad [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) de la interfaz [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) para mostrar el XML de origen del archivo .xsf. 
  
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


