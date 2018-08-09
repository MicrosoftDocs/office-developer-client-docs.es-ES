---
title: Modelos de objetos compatible de InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, object model,InfoPath 2003-compatible object model,object models [InfoPath 2003], compatible with InfoPath 2007,object models [InfoPath 2007], InfoPath 2003 compatible
localization_priority: Normal
ms.assetid: e4511af6-d7e7-44ad-a50d-1b7ee04f8215
description: Microsoft InfoPath está escrita como una aplicación de modelo de objetos de componentes (COM) y expone sus interfaces de programabilidad para la automatización externa y para la secuencia de comandos de plantillas de formulario como interfaces COM.
ms.openlocfilehash: 09ba36b39e520629764bd57a623e8fb490a63a89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815913"
---
# <a name="infopath-2003-compatible-object-models"></a>Modelos de objetos compatible de InfoPath 2003

Microsoft InfoPath está escrita como una aplicación de modelo de objetos de componentes (COM) y expone sus interfaces de programabilidad para la automatización externa y para la secuencia de comandos de plantillas de formulario como interfaces COM. Para ofrecer compatibilidad con las soluciones de InfoPath creadas en los lenguajes con código administrado Visual C# y Visual Basic, el programa de instalación de InfoPath instala tres ensamblados de interoperabilidad. Los ensamblados de interoperabilidad son ensamblados .NET que actúan como puente entre el código administrado y no administrado, asignando miembros de objetos COM a los miembros administrados .NET equivalentes. 
  
Los archivos de los tres ensamblados de interoperabilidad que instala InfoPath se denominan:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
En este tema se trata el modelo de objetos expuesto a través del ensamblado de interoperabilidad Microsoft.Office.Interop.InfoPath.SemiTrust, que se utiliza exclusivamente para escribir y ejecutar lógica empresarial con código administrado desde dentro de las plantillas de formulario de InfoPath (.xsn). 
  
Para obtener información acerca de los ensamblados Microsoft.Office.Interop.InfoPath y Microsoft.Office.Interop.InfoPath.Xml, consulte la documentación para el [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.aspx) y [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) espacios de nombres. 
  
## <a name="important-installation-information"></a>Información de instalación importantes

De manera predeterminada, la opción **Típica** del programa de instalación de InfoPath instala copias de los ensamblados Microsoft.Office.Interop.InfoPath.SemiTrust y Microsoft.Office.Interop.InfoPath.Xml en C:\Archivos de programa\Microsoft Office\Office14. Los ensamblados Microsoft.Office.Interop.InfoPath y Microsoft.Office.Interop.InfoPath.Xml también se instalan en la memoria caché global de ensamblados (GAC), cuyo contenido puede verse en la carpeta C:\Windows\Assembly. 
  
Si estos ensamblados no están instalados, deberá comprobar si Microsoft InfoPath está correctamente instalado. Siempre que .NET Framework 2.0 (o una versión posterior) esté instalado antes de ejecutar el programa de instalación, la opción **Compatibilidad con programación de .NET** del programa de instalación de InfoPath estará establecida en **Ejecutar desde mi PC** para una instalación **Típica** de InfoPath. Si estos ensamblados de interoperabilidad no están disponibles en su PC, deberá confirmar que .NET Framework 2.0 (o una versión posterior) está instalado y, a continuación, ejecutar **Agregar o quitar programas** desde el **Panel de control** para establecer la opción **Compatibilidad con programación de .NET** en **Ejecutar desde mi PC**.
  
Para obtener información sobre la descarga del redistribuible .NET Framework 2.0, vea [.NET Framework 2.0 Redistributable.](http://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=0856eacb-4362-4b0d-8edd-aab15c5e04f5)
  
## <a name="the-microsoftofficeinteropinfopathsemitrust-namespace"></a>El espacio de nombres Microsoft.Office.Interop.InfoPath.SemiTrust

Antes del lanzamiento de Microsoft Office InfoPath 2003 Service Pack 1 y el Kit de herramientas de Microsoft Office InfoPath 2003 para Visual Studio® .NET, toda la lógica de programación de las plantillas de formulario de InfoPath se creaba utilizando código Microsoft JScript o Microsoft VBScript, que se escribía en el entorno de desarrollo de Microsoft Script Editor (MSE) integrado en InfoPath. Los scripts escritos en MSE se interpretan en tiempo de ejecución y obtienen acceso al modelo de objetos COM que expone la biblioteca de vínculos dinámicos IPEDITOR.dll.
  
Para permitir la creación de plantillas de formulario que usen lenguajes de código administrado como Visual C# y Visual Basic para la lógica de programación, se agregó a InfoPath una funcionalidad que permite el hospedaje de Common Language Runtime (CLR). Además, se creó el ensamblado de interoperabilidad Microsoft.Office.Interop.InfoPath.SemiTrust para permitir al código administrado interoperar con el modelo de objetos COM que expone InfoPath de una forma segura. Para obtener información sobre el modelo de seguridad aplicable a las plantillas de formulario con código administrado de InfoPath, vea [Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md). 
  
Aunque el proceso de escribir código administrado para una tarea determinada en una plantilla de formulario de InfoPath es muy parecido al de llevar a cabo la misma tarea de programación escribiendo scripts, el modelo de objetos compatible con InfoPath 2003 que se expone al ver el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust** desde el **Examinador de objetos** en Visual Studio 2012 parece mucho más complejo. Esto se debe a que la tecnología de interoperabilidad con .NET Framework usada por compatibilidad con el modelo de objetos compatible con InfoPath 2003 requiere un servidor COM para exponer todas las interfaces públicas, además de otros constructores adicionales que requiere el propio .NET Framework. 
  
### <a name="how-com-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>¿Cómo se exponen los objetos COM al modelo de objetos compatible con InfoPath 2003

Al trabajar de forma nativa con un servidor COM desde lenguajes de alto nivel como JScript, VBScript o Visual Basic (pero no la versión .NET de Visual Basic y Visual C#), el modelo de objetos que se expone es más sencillo que las interfaces y clases COM subyacentes. Por ejemplo, al trabajar con estos lenguajes, el objeto **UI** de InfoPath expone un conjunto de siete métodos, como el método **Alert** para mostrar un cuadro de mensaje a los usuarios. 
  
Sin embargo, los constructores COM subyacentes que admiten el objeto **UI** se componen en realidad de tres entidades: dos interfaces denominadas **UI** y **UI2** y una coclase COM que implementa los miembros de estas dos interfaces. Existen dos versiones de la interfaz **UI** porque el marco de trabajo COM necesita que la definición de una interfaz permanezca fija para mantener la compatibilidad con versiones anteriores de los programas y componentes que llaman a la implementación de esa interfaz. 
  
En este caso, la interfaz **UI**, que se definió en la versión inicial de InfoPath, proporciona cuatro métodos, incluido el método **Alert**. La interfaz **UI2** puede considerarse una segunda versión de la interfaz **UI**, ya que se definió para la versión Service Pack 1 de InfoPath. La interfaz **UI2** ha heredado los cuatro métodos de la interfaz **UI** original y se le han agregado tres nuevos métodos, como **Confirm**. Aunque una línea de código se puede escribir, tanto con secuencias de comandos como con código administrado que llame al método **Confirm** mediante  `XDocument.UI.Confirm`, el código subyacente está realmente llamando al método **Confirm** de la interfaz **UI2** desde la implementación del método en la coclase COM. 
  
El modelo de objetos, tal como se expone a las secuencias de comandos, oculta estos detalles, pero el ensamblado de interoperabilidad necesario para trabajar con un servidor COM desde código administrado expone la coclase y ambas interfaces públicamente. Para el único objeto **UI** que se utiliza en el entorno de secuencias de comandos MSE, el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust** expone los tres elementos siguientes: 
  
- Interfaz [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI.aspx) 
    
- Interfaz [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) 
    
- Interfaz de coclase [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) 
    
Aunque estas tres interfaces se exponen en el **Examinador de objetos** y están incluidas en la documentación de la biblioteca de clases del espacio de nombres, solo se ocupa de la interfaz de coclase **UIObject**, ya que ésta implementa el objeto **UI** y los miembros de la interfaz **UI2**, que es la versión más actualizada de la interfaz que implementa la interfaz de coclase **UIObject**. Para obtener acceso a la interfaz de coclase **UIObject** desde el objeto [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) principal de ésta, utilice la propiedad de descriptor de acceso [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) , como en los scripts. Exceptuando algunos casos señalados, éste es el modelo de todos los objetos de la versión original de InfoPath que se actualizaron en InfoPath Service Pack 1. 
  
Aunque el modelo es básicamente el mismo, la situación de los objetos totalmente nuevos que fueron agregados a InfoPath Service Pack 1, como el objeto **Certificate** es algo más sencilla. En este caso, sólo es necesario ocuparse de dos elementos: la interfaz de coclase [CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) y los miembros de la interfaz [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Certificate.aspx) , que es la más reciente y la única que implementa la interfaz de coclase **CertificateObject**. Como sucede al utilizar objetos COM de InfoPath tomados de secuencias de comandos, la propiedad de descriptor de acceso [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Certificate.aspx) se utiliza para obtener acceso al objeto desde el principal de éste. 
  
Este mismo modelo se aplica a las interfaces para colecciones, exceptuando los casos en los que la interfaz de coclase de una colección tiene la cadena "Collection" unida a su nombre en lugar de la cadena "Object". Por ejemplo, la interfaz de coclase de la colección COM **DataAdapters** se denomina [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) y la interfaz que implementa es la interfaz [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdapters.aspx) . De forma parecida, la propiedad de descriptor de acceso [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) del objeto principal **XDocument** se utiliza para obtener acceso a la colección. 
  
Este modelo de nomenclatura tiene tres excepciones. Las interfaces de coclase de los objetos COM **Application** y **XDocument** no tienen la cadena "Object" unida a sus nombres. Sus nombres son idénticos a los de los objetos COM correspondientes: [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) y **XDocument**. Además, los nombres de las interfaces que implementan las interfaces de coclase **Application** y **XDocument** llevan el signo de subrayado como prefijo (_): [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) y [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) . La tercera excepción es el objeto COM **DataObject**. La interfaz de coclase de este objeto se denomina [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) , pero como sucede con otros objetos COM de InfoPath, la interfaz que implementa es la interfaz [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.aspx) . 
  
### <a name="how-microsoft-xml-core-services-msxml-50-for-microsoft-office-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>¿Cómo se exponen Microsoft XML Core Services (MSXML) 5.0 para objetos de Microsoft Office al modelo de objetos compatible con InfoPath 2003

Un subconjunto de los objetos y miembros del modelo de objetos que proporciona Microsoft XML Core Services (MSXML), que también es servidor COM, se ajusta mediante las interfaces que expone el ensamblado de interoperabilidad Microsoft.Office.Interop.InfoPath.SemiTrust. Esto es necesario porque algunos miembros del modelo de objetos COM de InfoPath se basan en MSXML y deben tener capacidad para obtener acceso a estos miembros de una forma segura. Los nombres de las interfaces del espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust** que ajustan los objetos y miembros del modelo de objetos de MSXML 5.0 son los mismos que los nombres que expone el servidor COM MSXML. En la mayoría de los casos, estos nombres llevan el prefijo "IXMLDOM", ya que se utilizan para trabajar con Document Object Model (DOM) XML. Por ejemplo, la propiedad [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) de la interfaz **XDocument**, que se utiliza para devolver una referencia al documento XML subyacente del formulario, devuelve la interfaz [IXMLDOMDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.IXMLDOMDocument.aspx) que se ajusta mediante el ensamblado de interoperabilidad Microsoft.Office.Interop.InfoPath.SemiTrust. Los miembros de la interfaz **IXMLDOMDocument** se llaman y utilizan básicamente de la misma manera que cuando se utilizan scripts en las plantillas de formulario que no utilizan código administrado. 
  
Para obtener más información sobre el uso de los miembros del modelo de objetos de Microsoft XML Core Services (MSXML) para Microsoft Office en plantillas de formulario con código administrado, vea [Trabajar con MSXML y System.Xml con el modelo de objetos de InfoPath 2003](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md).
  
### <a name="using-intellisense"></a>Utilizar IntelliSense

Para la mayor parte del código que se escribe frente al modelo de objetos compatible con InfoPath 2003 en las plantillas de formulario con código administrado, se utilizan las variables  `thisXDocument` y  `thisApplication` que se inicializan en el método  `_Startup` del archivo de clase FormCode.cs o FormCode.vb predeterminado. Puede utilizar las variables  `thisXDocument` y  `thisApplication` para obtener acceso a los miembros de las interfaces de coclase [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) y [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . Una vez escrito el nombre de cualquier variable seguido de punto, la finalización automática de instrucciones de IntelliSense mostrará la lista de miembros de la interfaz de coclase correspondiente. Puede continuar de esta forma para obtener acceso al miembro del modelo de objetos con el que desee trabajar. 
  
A continuación, se muestra un ejemplo sencillo que utiliza la variable  `thisXDocument` para obtener acceso al método [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) y mostrar la versión de la aplicación InfoPath mediante la propiedad [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) a la que se obtiene acceso desde la variable  `thisApplication`. 
  
```cs
thisXDocument.UI.Alert(thisApplication.Version);
```

```vb
thisXDocument.UI.Alert(thisApplication.Version)
```

### <a name="using-the-class-library-reference-documentation"></a>Uso de la documentación de referencia de biblioteca de clases

La organización de la documentación de referencia de la biblioteca de clases del espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust** es un reflejo de las relaciones entre las interfaces de coclase y las interfaces heredadas que aquéllas implementan, como se describe en la sección "Cómo se exponen los objetos COM al código administrado" de este tema. 
  
Aunque la organización y la nomenclatura de la documentación de referencia del espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust** parezca confusa al principio, los temas se organizan básicamente de la misma manera que la Referencia del modelo de objetos de InfoPath, que forma parte de la Referencia del programador de InfoPath incluida en InfoPath. Exceptuando los que tratan de las interfaces **Application** y **XDocument**, todos los temas de la interfaz de coclase COM están asignados a los temas "Objeto" y "Colección" equivalentes de la referencia de secuencias de comandos de InfoPath. Por ejemplo, los temas "Interfaz UIObject" e "Interfaz WindowsCollection" de la documentación de referencia del espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust** corresponden a un contenido similar en los temas "Objeto UI" y "Colección Windows" de la referencia de secuencias de comandos Referencia del modelo de objetos de InfoPath. 
  
Sin embargo, el vínculo a los miembros de la interfaz de coclase que siguen a la descripción de la interfaz al principio del tema lleva a un tema vacío. Para mostrar la lista de miembros que la interfaz de coclase implementa, debe abrir el tema de la interfaz más reciente heredado por la coclase y, a continuación, abrir la tabla de sus miembros. Al principio de la sección Observaciones del tema de la interfaz de coclase se proporciona un vínculo a la interfaz heredada.
  
Al presionar F1 en el Editor de código de Visual Studio, se produce un resultado parecido, excepto que el miembro para el que se invoca la Ayuda F1 se muestra directamente, ya que lo más habitual es trabajar con miembros de una interfaz. No obstante, puesto que los miembros pueden implementarse desde una interfaz que tiene versión, puede resultar confuso la primera vez que se ve. Por ejemplo, si escribe  `thisXDocument.UI.Alert`, coloca el cursor en  `Alert` y pulsa F1, se mostrará un tema titulado "Método UI2.Alert". Ello se debe a que el método **Alert** es una implementación de un miembro de la interfaz **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Pasar parámetros opcionales a miembros del modelo de objetos de InfoPath

Si un miembro del modelo de objetos compatible con InfoPath 2003 contiene un parámetro opcional y no se especifica un valor para ese parámetro, deberá pasar el campo **Type.Missing** de ese parámetro. Si no se pasa el campo **Type.Missing** al omitir un valor real, se producirá un error de generación. Esto es aplicable tanto al código escrito en Visual C# como al escrito en Visual Basic. Por ejemplo, el método [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) de la interfaz [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) incluye dos parámetros opcionales:  _varEndNode_ y  _varViewContext_. Una línea de código que no especifique valores reales para estos parámetros opcionales debería ser como se muestra a continuación.
  
```cs
IXMLDOMNode group1 = 
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1");
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
Dim group1 As IXMLDOMNode = _
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1")
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

### <a name="about-common-language-specification-compliance"></a>Sobre con common language specification

Internamente, todos los miembros e interfaces del ensamblado Microsoft.Office.Interop.InfoPath.SemiTrust tienen un atributo **CLSCompliant** establecido en **false**. Puesto que la documentación de referencia se genera en parte utilizando **System.Reflection**, la descripción de todos los miembros e interfaces lleva unida la frase "Esta interfaz/método/propiedad no es compatible con CLS". No obstante, la mayoría de las interfaces y miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) son en realidad compatibles con CLS. 
  
## <a name="see-also"></a>Vea también

- [Tareas comunes en el desarrollo de plantillas de formulario mediante el modelo de objetos de InfoPath 2003](common-tasks-for-developing-form-templates-using-infopath-object-model.md)
- [Acerca del modelo de seguridad de las plantillas de formulario con código](about-the-security-model-for-form-templates-with-code.md)
- [Crear plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
- [Comprender el modelo de objetos de InfoPath 2003](understanding-the-infopath-2003-object-model.md)

