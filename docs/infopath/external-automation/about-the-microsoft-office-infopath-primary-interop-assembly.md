---
title: Información sobre el conjunto de interoperabilidad principal de InfoPath de Microsoft Office
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2007, ensamblado de interoperabilidad primario, InfoPath ensamblado de interoperabilidad primario, PIA [InfoPath 2007], ensamblados de interoperabilidad primarios [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Para admitir la creación de soluciones de InfoPath que usan los lenguajes de código administrado como Visual C# y Visual Basic, la opción de compatibilidad con programación de .NET en el programa de instalación de InfoPath instala a los ensamblados de interoperabilidad tres.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393358"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Información sobre el conjunto de interoperabilidad principal de InfoPath de Microsoft Office

La aplicación InfoPath se crea como una aplicación de modelo de objetos componentes (COM) que expone sus interfaces de programación para la automatización externa como interfaces COM. Para admitir la creación de soluciones de InfoPath que usan los lenguajes de código administrado como Visual C# y Visual Basic, la opción de **Compatibilidad con programación de .NET** en el programa de instalación de InfoPath instala a los ensamblados de interoperabilidad tres. Los ensamblados de interoperabilidad son ensamblados .NET que actúan como puente entre el código administrado y no administrado, asignando miembros de objetos COM a los miembros administrados .NET equivalentes. 
  
Los archivos de los tres ensamblados de interoperabilidad que instala InfoPath se denominan:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
En este tema se describe el modelo de objetos expuesto a través del ensamblado de interoperabilidad Microsoft.Office.Interop.InfoPath, que se usa exclusivamente para el código de automatización externo. Para obtener información sobre el ensamblado Microsoft.Office.Interop.InfoPath.SemiTrust, que se usa exclusivamente para escribir y ejecutar código administrado que se ejecuta desde dentro de las plantillas de formulario de InfoPath (.xsn), vea [Modelos de objetos compatible con InfoPath 2003](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Información importante sobre la instalación

La opción de instalación predeterminada del programa de instalación de InfoPath instala al ensamblado Microsoft.Office.Interop.InfoPath en la caché de ensamblados Global (GAC) el contenido de los cuales se puede ver desde la carpeta C:\Windows\Assembly (o en C:\Windows\assembly\GAC_ MSIL al ver directamente el sistema de archivos). Este ensamblado se denomina "Microsoft Office InfoPath ensamblado de interoperabilidad primario" y a menudo se utiliza junto con el ensamblado Microsoft.Office.Interop.InfoPath.Xml, que también se instala en la GAC, para automatizar la aplicación InfoPath desde aplicaciones externas que usan código administrado. Para obtener información sobre el ensamblado Microsoft.Office.Interop.InfoPath.Xml, vea [Acerca de que el ensamblado de interoperabilidad InfoPath XML](about-the-infopath-xml-interop-assembly.md).
  
Si el ensamblado Microsoft.Office.Interop.InfoPath no está visible en la GAC, debería confirmar que InfoPath se ha instalado correctamente. De forma predeterminada, se establece la opción de **Compatibilidad con programación de .NET** en el programa de instalación a **Ejecutar desde Mi PC** mientras el paquete redistribuible de .NET Framework 1.1, Kit de desarrollo de Software (SDK) de .NET Framework 1.1 o una versión posterior de .NET Framework está instalado antes de ejecutar el programa de instalación. Si estos ensamblados de interoperabilidad no están disponibles en su equipo, debe confirmar que está instalado .NET Framework 1.1 o posterior y, a continuación, usar **programas y características** del **Panel de Control** para cambiar el programa de instalación mediante la configuración de la programación de .NET ** Compatibilidad con** opción en **Microsoft Office InfoPath** para **Ejecutar desde Mi PC**.
  
Para obtener información acerca de cómo descargar el paquete redistribuible de .NET Framework 1.1, consulte el [Paquete redistribuible de .NET Framework 1.1](https://www.microsoft.com/en-us/download/details.aspx?id=26).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>El Namespace Microsoft.Office.Interop.InfoPath

Aunque administra el proceso de escribir código para una tarea determinada es muy similar a realizar la misma tarea utilizando un lenguaje como Visual Basic para aplicaciones o JScript, el modelo de objetos expuesto al ver el **Microsoft.Office.Interop.InfoPath** espacio de nombres desde el **Examinador de objetos** en Microsoft Visual Studio busca más compleja. Esto es debido a que la interoperabilidad con .NET Framework requiere un servidor COM para exponer todas sus interfaces públicas, así como algunas construcciones adicionales requeridos por el propio .NET Framework. Para obtener más información sobre cómo y por qué el modelo de objetos expuesto por un ensamblado de interoperabilidad aparece más complejo, vea la sección "Cómo COM objetos están expuestos a código administrado" del tema de [Modelos de objetos compatible con InfoPath 2003](../form-templates/infopath-2003-compatible-object-models.md) . 
  
### <a name="using-intellisense"></a>Utilizar IntelliSense

Los ejemplos de esta sección se supone que ha establecido las referencias a los ensamblados Microsoft.Office.Interop.InfoPath y Microsoft.Office.Interop.InfoPath.Xml. Para obtener información acerca de cómo establecer referencias y ejemplos adicionales de automatización externa, vea [escenarios de automatización externo y ejemplos](external-automation-scenarios-and-examples.md).
  
Antes de finalización de instrucciones IntelliSense de Microsoft puede usar en el código de automatización externo, debe crear una variable de objeto de una instancia de la clase de [aplicación](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) tal como se muestra en la siguiente línea de código. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Después de crear la variable de objeto, cuando escriba el nombre de variable seguido de un punto, se muestra una lista desplegable con los miembros de la clase de **aplicación** para seleccionar. 
  
Para trabajar con un formulario de InfoPath, declare una variable de objeto del tipo [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) y, a continuación, inicializarlo abriendo el formulario de la colección [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) de la variable de objeto de **aplicación** tal como se muestra en la siguiente línea de código. 
  
```cs
XDocument myXDoc = myApp.XDocuments.Open(
    "c:\\temp\\Form1.xml",
    (int) XdDocumentVersionMode.xdFailOnVersionOlder);
```

```vb
Dim myXDoc As XDocument = myApp.XDocuments.Open( _
    "c:\\temp\\Form1.xml", _
    XdDocumentVersionMode.xdFailOnVersionOlder)
```

Cuando escriba el nombre de la variable seguido de un período, se mostrará la lista de lista desplegable de finalización de instrucciones de IntelliSense para los miembros de la clase **XDocument** . 
  
Para trabajar con el contenido del documento XML subyacente para el formulario mediante Microsoft XML Core Services (MSXML), debe crear una variable de tipo [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) y, a continuación, usar la propiedad [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) de la clase **XDocument** para asignar el código XML Modelo de objetos de documento (DOM) del formulario a la variable. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

Se mostrará la lista de lista desplegable de finalización de instrucciones de IntelliSense para los miembros de la clase **IXMLDOMDocument2** cuando escriba el nombre de la variable seguido de un período, que le permite usar MSXML para trabajar con el documento XML. 
  
### <a name="using-the-class-library-reference-documentation"></a>Utilizar la documentación de referencia de la Biblioteca de clases

La organización de la documentación de referencia de biblioteca de clases de espacio de nombres de [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) refleja las relaciones entre las interfaces de coclase y las interfaces heredadas que implementan. 
  
Cuando abra un tema de una interfaz de coclase, por ejemplo, la [aplicación](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , el vínculo a los miembros de la interfaz de coclase después de la descripción de la interfaz al principio del tema muestra un tema de vacío. Para mostrar la lista de miembros que la interfaz de coclase implementa, debe abrir el tema de la interfaz más reciente heredado por la coclase y, a continuación, abrir la tabla de sus miembros. Al principio de la sección Observaciones del tema de la interfaz de coclase se proporciona un vínculo a la interfaz heredada. 
  
Cuando se presiona F1 en el Editor de código de Visual Studio, el comportamiento es similar, excepto en que el miembro en el que se invoca ayuda (F1) se mostrará directamente, porque normalmente se trabaja con los miembros de una interfaz. No obstante, puesto que los miembros pueden implementarse desde una interfaz que tiene versión, puede resultar confuso la primera vez que se ve. Por ejemplo, si escribe  `myXDocument.UI.Alert`, coloca el cursor en  `Alert` y pulsa F1, se mostrará un tema titulado "Método UI2.Alert". Ello se debe a que el método **Alert** es una implementación de un miembro de la interfaz **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Pasar parámetros opcionales a los miembros del modelo de objetos de InfoPath

Si un miembro del modelo de objetos de InfoPath contiene un parámetro opcional, y no se especifica un valor de dicho parámetro, debe pasar el campo **Type.Missing** para ese parámetro. Si no se pasa el campo **Type.Missing** al omitir un valor real, se producirá un error de generación. Esto es así para el código escrito en C# y Visual Basic. Por ejemplo, el método [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) de la interfaz [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) incluye dos parámetros opcionales:  _varEndNode_ y  _varViewContext_. Una línea de código que no especifique valores reales para estos parámetros opcionales debería ser como se muestra a continuación.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Vea también

- [Ejemplos y escenarios de automatización externa](external-automation-scenarios-and-examples.md)

