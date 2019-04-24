---
title: Información sobre el conjunto de interoperabilidad principal de InfoPath de Microsoft Office
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2007, ensamblado de interoperabilidad primario, ensamblado de interoperabilidad primario de InfoPath, Pia [InfoPath 2007], ensamblados de interoperabilidad primarios [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Para admitir la creación de soluciones de InfoPath que usan lenguajes de código administrado como Visual C# y Visual Basic, la opción compatibilidad con programación de .NET en el programa de instalación de InfoPath instala tres ensamblados de interoperabilidad.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310139"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Información sobre el conjunto de interoperabilidad principal de InfoPath de Microsoft Office

La aplicación InfoPath se crea como una aplicación de modelo de objetos componentes (COM) que expone sus interfaces de programación para la automatización externa como interfaces COM. Para admitir la creación de soluciones de InfoPath que usan lenguajes de código administrado como Visual C# y Visual Basic, la opción **compatibilidad con programación de .net** en el programa de instalación de InfoPath instala tres ensamblados de interoperabilidad. Los ensamblados de interoperabilidad son ensamblados .NET que actúan como puente entre el código administrado y no administrado, asignando miembros de objetos COM a los miembros administrados .NET equivalentes. 
  
Los archivos de los tres ensamblados de interoperabilidad que instala InfoPath se denominan:
  
- Microsoft. Office. Interop. InfoPath. dll
    
- Microsoft. Office. Interop. InfoPath. semiTrust. dll
    
- Microsoft. Office. Interop. InfoPath. Xml. dll
    
En este tema se describe el modelo de objetos que se expone mediante el ensamblado Microsoft. Office. Interop. InfoPath Interop, que se utiliza exclusivamente para el código de automatización externo. Para obtener información sobre el ensamblado Microsoft. Office. Interop. InfoPath. semiTrust, que se utiliza exclusivamente para escribir y ejecutar código administrado que se ejecuta desde plantillas de formulario de InfoPath (. xsn), consulte [modelos de objetos compatibles con infopath 2003](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Información importante sobre la instalación

La opción de instalación predeterminada del programa de instalación de InfoPath instala el ensamblado Microsoft. Office. Interop. InfoPath en la memoria caché global de ensamblados (GAC), cuyo contenido se puede ver desde la carpeta C:\windows\assembly. (o en C:\Windows\assembly\GAC_ MSIL al ver directamente el sistema de archivos). Este ensamblado se conoce como "ensamblado de interOperabilidad principal de Microsoft Office InfoPath" y se suele usar junto con el ensamblado Microsoft. Office. Interop. InfoPath. XML, que también se instala en la GAC, para automatizar la aplicación InfoPath desde aplicaciones externas que usan código administrado. Para obtener información sobre el ensamblado Microsoft. Office. Interop. InfoPath. XML, vea [acerca del ensamblado de InteroperaBILIDAD XML de InfoPath](about-the-infopath-xml-interop-assembly.md).
  
Si el ensamblado Microsoft. Office. Interop. InfoPath no es visible en la GAC, debe confirmar que InfoPath se instaló correctamente. De forma predeterminada, la opción **compatibilidad con programación de .net** en el programa de instalación se establece en **Ejecutar desde mi PC** siempre que el redistribuible de .NET Framework 1,1, el kit de desarrollo de software (SDK) de .NET Framework 1,1 o una versión posterior de .NET Framework está instalado antes de ejecutar el programa de instalación. Si estos ensamblados de interoperabilidad no están disponibles en el equipo, debe confirmar que .NET Framework 1,1 o posterior está instalado y, a continuación, usar **programas y características** del **Panel de control** para cambiar la configuración mediante la configuración de la **programación de .net Opción soporte técnico** en **Microsoft Office InfoPath** para **Ejecutar desde mi PC**.
  
Para obtener información sobre cómo descargar el paquete redistribuible de .NET Framework 1,1, vea el paquete redistribuible de [.NET framework 1,1](https://www.microsoft.com/en-us/download/details.aspx?id=26).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>El espacio de nombres Microsoft. Office. Interop. InfoPath

Aunque el proceso de escribir código administrado para una tarea determinada es muy similar a realizar la misma tarea con un lenguaje como Visual Basic para aplicaciones o JScript, el modelo de objetos expuesto al ver **Microsoft. Office. Interop. InfoPath** el espacio de nombres del examinador de **objetos** de Microsoft Visual Studio parece más complejo. Esto se debe a que la interoperabilidad con .NET Framework requiere que un servidor COM exponga todas sus interfaces públicas, así como otras construcciones necesarias para .NET Framework. Para obtener más información sobre cómo y por qué el modelo de objetos expuesto por un ensamblado de interoperabilidad parece más complejo, vea la sección "cómo se exPonen los objetos COM en el código administrado" del tema [modelos de objetos compatibles con InfoPath 2003](../form-templates/infopath-2003-compatible-object-models.md) . 
  
### <a name="using-intellisense"></a>Utilizar IntelliSense

En los ejemplos de esta sección se da por supuesto que ha establecido referencias a los ensamblados Microsoft. Office. Interop. InfoPath y Microsoft. Office. Interop. InfoPath. Xml. Para obtener información sobre cómo establecer referencias y ejemplos de automatización externa adicionales, vea [ejemplos y escenarios de automatización externa](external-automation-scenarios-and-examples.md).
  
Para poder usar la finalización de instrucciones de Microsoft IntelliSense en código de automatización externo, debe crear una variable de objeto para una instancia de la clase [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , tal como se muestra en la siguiente línea de código. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

Después de crear la variable de objeto, cuando se escribe el nombre de la variable seguido de un punto, se muestra una lista desplegable con los miembros de la clase de **aplicación** que se van a seleccionar. 
  
Para trabajar con un formulario de InfoPath, declare una variable de objeto de tipo [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) y, a continuación, inicialícela abriendo el formulario de la colección [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) de la variable de objeto **Application** como se muestra en la siguiente línea de código. 
  
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

La lista desplegable de finalización de instrucciones de IntelliSense para los miembros de la clase **XDocument** se mostrará cuando escriba el nombre de la variable seguido de un punto. 
  
Para trabajar con el contenido del documento XML subyacente para el formulario mediante Microsoft XML Core Services (MSXML), debe crear una variable de tipo [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) y, a continuación, usar la propiedad [Dom](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) de la clase **XDOCUMENT** para asignar el código XML Document Object Model (DOM) del formulario a esa variable. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

La lista desplegable de finalización de instrucciones de IntelliSense para los miembros de la clase **IXMLDOMDocument2** se mostrará cuando escriba el nombre de la variable seguido de un punto, lo que le permite usar MSXML para trabajar con el documento XML. 
  
### <a name="using-the-class-library-reference-documentation"></a>Utilizar la documentación de referencia de la Biblioteca de clases

La organización de la documentación de referencia de la biblioteca de clases de espacio de nombres [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) refleja las relaciones entre las interfaces de coclase y las interfaces heredadas que implementan. 
  
Cuando se abre un tema para una interfaz de coclase, como [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , el vínculo a los miembros de la interfaz de coclase que sigue a la descripción de la interfaz al comienzo del tema muestra un tema vacío. Para mostrar la lista de miembros que la interfaz de coclase implementa, debe abrir el tema de la interfaz más reciente heredado por la coclase y, a continuación, abrir la tabla de sus miembros. Al principio de la sección Observaciones del tema de la interfaz de coclase se proporciona un vínculo a la interfaz heredada. 
  
Cuando se presiona la tecla F1 en el editor de código de Visual Studio, el comportamiento es similar, pero el miembro en el que se invoca la ayuda F1 se muestra directamente, ya que se suele trabajar con miembros de una interfaz. No obstante, puesto que los miembros pueden implementarse desde una interfaz que tiene versión, puede resultar confuso la primera vez que se ve. Por ejemplo, si escribe  `myXDocument.UI.Alert`, coloca el cursor en  `Alert` y pulsa F1, se mostrará un tema titulado "Método UI2.Alert". Ello se debe a que el método **Alert** es una implementación de un miembro de la interfaz **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Pasar parámetros opcionales a los miembros del modelo de objetos de InfoPath

Si un miembro del modelo de objetos de InfoPath contiene un parámetro opcional y no especifica un valor para dicho parámetro, debe pasar el campo **Type. Missing** para ese parámetro. Si no se pasa el campo **Type.Missing** al omitir un valor real, se producirá un error de generación. Esto es válido para el código escrito en C# y Visual Basic. Por ejemplo, el método [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) de la interfaz [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) incluye dos parámetros opcionales:  _varEndNode_ y  _varViewContext_. Una línea de código que no especifique valores reales para estos parámetros opcionales debería ser como se muestra a continuación.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>Vea también

- [Ejemplos y escenarios de automatización externa](external-automation-scenarios-and-examples.md)

