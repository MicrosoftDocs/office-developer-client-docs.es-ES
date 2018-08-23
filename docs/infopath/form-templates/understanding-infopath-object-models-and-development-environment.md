---
title: Comprender los modelos de objetos y el entorno de desarrollo de InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, object models,object models [InfoPath 2007],InfoPath 2007, development environments
localization_priority: Normal
ms.assetid: 29415c5b-9a42-46f4-a9e8-6a7d5bb7bdbf
description: Microsoft InfoPath 2013 admite dos tipos de modelos de programación para desarrollar lógica empresarial en plantillas de formulario, además de automatización externa desde un código administrado.
ms.openlocfilehash: 638306eabf9f761ff126953e66228cad8cc5c3ae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579532"
---
# <a name="understanding-infopath-object-models-and-development-environment"></a>Comprender los modelos de objetos y el entorno de desarrollo de InfoPath

Microsoft InfoPath 2013 admite dos tipos de modelos de programación para desarrollar lógica empresarial en plantillas de formulario, además de automatización externa desde un código administrado.
  
InfoPath Forms Services, que está disponible en SharePoint Server 2013, brinda una experiencia de explorador web para completar formularios de InfoPath. Cuando se implementa en un servidor que ejecuta InfoPath Forms Services, los formularios basados en plantillas de formulario compatibles con el explorador (.xsn) se pueden abrir en un explorador web desde PC que no tienen instalado InfoPath, pero se abrirán en InfoPath cuando se instale. InfoPath Forms Services también proporciona un modelo de objeto para la automatización de tareas de servidor relacionadas con la administración y la publicación de plantillas de formulario de InfoPath.
  
InfoPath 2013 admite el entorno de programación de Visual Studio 2012 y los lenguajes de programación asociados, que se describen más adelante en este tema.
  
## <a name="infopath-programming-models"></a>Modelos de programación de InfoPath

InfoPath 2013 admite dos modelos de objetos para desarrollar lógica empresarial en plantillas de formulario:
  
- Modelo de objetos de código administrado de InfoPath
    
- Modelo de objetos de código administrado compatible con InfoPath 2003
    
Además, InfoPath 2013 permite escribir código administrado para automatizar InfoPath desde una aplicación externa.
  
InfoPath Forms Services proporciona un modelo de objetos para automatizar las tareas de servidor, como la comprobación y la carga de plantillas de formulario desde código que se ejecuta en el servidor, que exige permisos y acceso de administrador para el servidor.
  
> [!NOTE]
> [!NOTA] InfoPath Filler 2013 puede abrir e iniciar soluciones de plantilla de formulario de InfoPath creadas en versiones anteriores de InfoPath que usan lógica empresarial escrita con lenguajes de scripting (JScript y VBScript). Pero InfoPath Designer 2010 no admite la creación ni la modificación de plantillas de formulario que usan lógica empresarial escrita con script. 
  
### <a name="the-infopath-managed-code-object-model"></a>Modelo de objetos de código administrado de InfoPath

El modelo de objetos de código administrado de InfoPath 2013 se implementa en dos ensamblados, los dos con el nombre Microsoft.Office.Infopath.dll.
  
Una versión del ensamblado implementa un subconjunto del modelo de objetos de InfoPath que solo contiene los tipos y los miembros compatibles con la lógica empresarial de las plantillas de formulario implementadas como plantillas de formulario habilitadas para el explorador que se ejecutan en SharePoint Server 2013 con InfoPath Forms Services. Las plantillas de formulario con lógica empresarial escrita para este ensamblado pueden abrirse e iniciarse en InfoPath Filler y en un explorador web.
  
La otra versión del ensamblado implementa tipos y miembros adicionales que proporcionan funcionalidad que no es compatible con la lógica empresarial de las plantillas de formulario habilitadas para el explorador. Las plantillas de formulario con lógica empresarial escrita en las clases y los miembros adicionales de este ensamblado sólo se pueden abrir y ejecutar en el editor de InfoPath Filler.
  
> [!NOTE]
> [!NOTA] Se puede escribir lógica condicional que use las propiedades de la clase [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) para determinar el entorno (InfoPath Filler o un explorador web) en que se va a ejecutar la plantilla de formulario. Si se usa esta lógica condicional, la lógica empresarial se puede dividir entre código que funcione en un explorador web y código escrito en clases y miembros que solo funcionen en el editor de InfoPath Filler. Para obtener más información, vea [escribir lógica condicional que determina el entorno de tiempo de ejecución](how-to-write-conditional-logic-that-determines-the-run-time-environment.md)
  
El ensamblado que usa InfoPath cuando agrega y compila lógica empresarial para la plantilla de formulario depende de si selecciona la plantilla de formulario **Formulario en blanco** o **Formulario en blanco (InfoPath Filler)** en la ficha **Nuevo** de Microsoft Office Backstage cuando comienza a diseñar un nuevo formulario en InfoPath Designer. Los formularios creados con la plantilla de formulario **Formulario en blanco** usan el ensamblado que contiene solo los tipos y miembros admitidos en la lógica empresarial de plantillas de formularios implementadas como plantillas de formulario habilitadas para el explorador. Los formularios creados con la plantilla de formulario **Formulario en blanco** se pueden abrir en el explorador web y en InfoPath Filler. Los formularios creados con la plantilla de formulario **Formulario en blanco (InfoPath Filler)** usan el ensamblado que implementa tipos y miembros adicionales que proporcionan funcionalidad no admitida en la lógica empresarial de plantillas de formulario habilitadas para el explorador, y solo se pueden abrir en InfoPath Filler. 
  
> [!TIP]
> [!SUGERENCIA] Después de empezar a diseñar una plantilla de formulario, puede cambiar el ensamblado que se usa cambiando la configuración de compatibilidad del formulario. Para ello, haga clic en **Idioma** en la pestaña **Desarrollador** y, después, en **Compatibilidad** en la lista **Categoría**. En la lista **Tipo de formulario**, seleccione **Formulario de explorador web** para crear un formulario que se pueda implementar como formulario compatible con el explorador en SharePoint Server 2013. Seleccione **Formulario de InfoPath Filler** para crear un formulario que solo se pueda iniciar en el editor de InfoPath Filler. Las demás selecciones de la lista **Tipo de formulario** son compatibles con InfoPath 2007 y InfoPath 2003. 
  
Las clases y los miembros de las dos versiones de este modelo de objetos se exponen a través del espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . En la tabla siguiente se indica dónde se encuentran estos ensamblados en los directorios de una instalación de InfoPath 2013. 
  
|**Ensamblado**|**Descripción**|
|:-----|:-----|
|Microsoft.Office.InfoPath.dll (ubicado en C:\Program Files\Microsoft Office\Office15\InfoPathOM\InfoPathOMFormServices)  <br/> |Subconjunto del modelo de objetos que solo contiene tipos y miembros que se ejecutarán en la lógica empresarial de una plantilla de formulario implementada en un servidor que ejecuta InfoPath Forms Services.  <br/> |
|Microsoft.Office.InfoPath.dll (ubicado en C:\Program Files\Microsoft Office\Office15\InfoPathOM)  <br/> |El modelo de objetos "full" con los tipos y miembros que no se ejecutarán en la lógica empresarial de una plantilla de formulario implementada en InfoPath Forms Services.  <br/> |
   
> [!NOTE]
> [!NOTA] Los ensamblados a los que se hace referencia más arriba en esta sección se usan en tiempo de diseño al escribir y compilar código. En tiempo de ejecución, el ensamblado usado al abrir una plantilla de formulario en InfoPath se encuentra en la caché global de ensamblados (GAC) del equipo donde está instalado InfoPath. Al abrir una plantilla de formulario en un explorador web desde un servidor que ejecuta InfoPath Forms Services, el ensamblado usado se encuentra en el servidor. 
  
Al disponer de dos ensamblados, se contribuye a garantizar que la lógica empresarial solo contendrá llamadas a los miembros del modelo de objetos adecuados para los editores de formularios compatibles (explorador web o InfoPath Filler). Por ejemplo, al editar el código, las características de IntelliSense, como la finalización de instrucciones y la documentación en línea, sólo se mostrarán y funcionarán con los miembros del modelo de objetos adecuados para los editores de los formularios de destino.
  
En las dos versiones del modelo de objetos de código administrado que expone el ensamblado Microsoft.Office.InfoPath, la exploración y la actualización de los almacenes de datos XML de la lógica empresarial requieren llamadas a los miembros de la clase **System.Xml.XPath.XPathNavigator**. En InfoPath 2003, la exploración y la actualización de los almacenes de datos XML requieren llamadas a miembros de clases de MSXML (para la lógica empresarial creada con JScript o VBScript) o llamadas a través de los contenedores de las clases de MSXML proporcionadas por el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust** (para la lógica empresarial creada con C# o Visual Basic y el Kit de herramientas de Microsoft Office InfoPath 2003 para Visual Studio .NET). 
  
El uso de miembros de la clase **XPathNavigator** permite que el mismo código de lógica empresarial sea compatible con la manipulación de DOM para plantillas de formulario que se abren en el cliente de InfoPath y en los formularios habilitados para Web abiertos desde SharePoint Server 2013 con InfoPath Forms Services en un explorador web. 
  
Para obtener información acerca de cómo trabajar con los miembros de la clase **XPathNavigator** en la lógica empresarial de InfoPath las plantillas de formulario de código administrado, vea [trabajar con las clases XPathNavigator y XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="the-infopath-2003-compatible-managed-code-object-model"></a>Modelo de objetos de código administrado compatible con InfoPath 2003

El modelo de objetos de código administrado compatible con InfoPath 2003 se introdujo en InfoPath 2003 Service Pack 1 con el Kit de herramientas de Microsoft Office InfoPath 2003 para Visual Studio .NET para escribir lógica empresarial en plantillas de formulario con código administrado. InfoPath 2013 aún admite este modelo de objetos por razones de compatibilidad con InfoPath 2003.
  
Las clases y los miembros de este modelo de objetos se exponen a través del espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . Este modelo se implementa en el siguiente archivo de ensamblado, que se encuentra en la carpeta C:\Archivos de programa\Microsoft Office\Office14. 
  
|**Ensamblado**|**Descripción**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.SemiTrust.dll  <br/> |Proporciona la interoperabilidad COM con el modelo de objetos COM de InfoPath para la lógica de negocios de plantilla de formulario escrita con C# o Visual Basic.  <br/> |
   
> [!NOTE]
> [!NOTA] Si bien InfoPath 2013 aún admite crear lógica empresarial con el modelo de objetos de código administrado de interoperabilidad COM que proporciona el ensamblado Microsoft.Office.Interop.InfoPath.SemiTrust, la lógica empresarial escrita con este modelo de objetos no se admite para plantillas de formulario habilitadas para el explorador e implementadas en SharePoint Server 2013 con InfoPath Forms Services. Las plantillas de formulario habilitadas para el explorador deben usar el modelo de objetos de código administrado de InfoPath para la lógica empresarial personalizada. 
  
### <a name="automating-infopath-from-managed-code"></a>Automatizar InfoPath desde código administrado

Además de escribir lógica empresarial con código administrado, los desarrolladores pueden automatizar InfoPath con el código administrado que se inicia en una aplicación externa. Esta funcionalidad y los ensamblados necesarios para escribir código se introdujeron por primera vez en InfoPath 2003 Service Pack 1. Los objetos y los miembros para automatizar InfoPath se actualizaron y ahora proporcionan funciones adicionales cuando se escribe código de automatización externa para InfoPath 2013.
  
Las clases y los miembros usados para automatización externa se exponen con los espacios de nombres [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) y [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml). Los archivos de ensamblado necesarios para escribir código de automatización se encuentran en la carpeta C:\Archivos de programa\Microsoft Office\Office14. 
  
|**Ensamblado**|**Descripción**|
|:-----|:-----|
|Microsoft.Office.Interop.InfoPath.dll  <br/> |Proporciona la interoperabilidad COM con el modelo de objetos COM de InfoPath para el código de automatización externa escrito con C# o Visual Basic.  <br/> |
|Microsoft.Office.Interop.InfoPath.Xml.dll  <br/> |Proporciona la interoperabilidad COM con las operaciones de MSXML para DOM XML en el código de automatización externa escrito con C# o Visual Basic.  <br/> |
   
Para más información sobre los modelos de objetos proporcionados por los espacios de nombres **Microsoft.Office.Interop.InfoPath** y **Microsoft.Office.Interop.InfoPath.Xml**, que se usan exclusivamente para automatizar la aplicación de InfoPath con código administrado de aplicaciones externas, visite el [Centro para desarrolladores de InfoPath Developer](http://msdn.microsoft.com/en-us/office/aa905434.aspx).
  
### <a name="the-infopath-forms-services-object-model"></a>Modelo de objetos de InfoPath Forms Services

El modelo de objetos de código administrado para automatizar las tareas administrativas de InfoPath Forms Services se implementa en Microsoft.Office.InfoPath.Server.dll, que se encuentra en \<unidad\>:\Archivos de programa\Microsoft Office Server\15.0\Bin en una instalación de Microsoft SharePoint Server 2013.
  
|**Ensamblado**|**Descripción**|
|:-----|:-----|
|Microsoft.Office.InfoPath.Server.dll  <br/> |El modelo de objetos para automatizar las tareas de InfoPath Forms Services, como la carga, la activación o desactivación de plantillas de formulario habilitadas para explorador.  <br/> |
   
Para más información sobre el modelo de objetos de InfoPath Forms Services, vea el kit de desarrollo de software (SDK) de SharePoint Server 2013, que puede encontrar en MSDN.
  
## <a name="infopath-development-environment"></a>Entorno de desarrollo de InfoPath

La lógica empresarial puede desarrollarse en plantillas de formulario de InfoPath 2013 con Visual Studio 2012 con el complemento [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) instalado. 
  
> [!NOTE]
> [!NOTA] InfoPath 2013 no permite crear ni modificar plantillas de formulario que usan lógica empresarial escrita con JScript o VBScript, a pesar de que InfoPath Filler permite abrir plantillas de formulario basadas en script creadas en versiones anteriores de InfoPath. 
  
## <a name="see-also"></a>Vea también

- [Tutorial: Crear una plantilla de formulario básica con código](walkthrough-creating-a-basic-form-template-with-code.md)
- [Tutorial: Crear y depurar una plantilla de formulario básica mediante el modelo de objetos de InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)

