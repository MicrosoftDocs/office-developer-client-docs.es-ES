---
title: Programar plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- form templates [infopath 2007], using infopath 2003 object model,InfoPath 2003-compatible form templates,InfoPath 2007, developing form templates using InfoPath 2003 object model,object models [InfoPath 2003], developing managed code form templates
localization_priority: Normal
ms.assetid: c74cbcd0-4fe6-4eb7-a05c-f61e1868c42b
description: Microsoft InfoPath sigue siendo compatible con los proyectos de plantillas de formulario creados con el Kit de herramientas de Microsoft Office InfoPath 2003 para Visual Studio .NET o con Visual Studio 2005 Tools para Microsoft Office System que tienen lógica empresarial escrita en miembros del espacio de nombres Microsoft.Office.Interop.InfoPath.SemiTrust . Los temas de esta sección se refieren a los tipos y miembros de este espacio de nombres como el modelo de objetos compatible con InfoPath 2003 o sencillamente el modelo de objetos de InfoPath 2003. InfoPath también es compatible con los proyectos de plantillas de formulario creados con Microsoft Office InfoPath 2007 que usan el modelo de objetos compatible con InfoPath 2003. Asimismo, puede usar InfoPath para crear nuevos proyectos de plantillas de formulario que usen el modelo de objetos compatible con InfoPath 2003 para que los usuarios de Office InfoPath 2007 dispongan de compatibilidad con versiones anteriores. En todos los temas de esta sección, se describe la creación y el desarrollo de plantillas de formulario que funcionen con el modelo de objetos compatible con InfoPath 2003 proporcionado por el espacio de nombres Microsoft.Office.Interop.InfoPath.SemiTrust .
ms.openlocfilehash: 5d949242068586c752e7a92fa53792cda9ececea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815850"
---
# <a name="developing-form-templates-using-the-infopath-2003-object-model"></a>Programar plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003

Microsoft InfoPath sigue siendo compatible con los proyectos de plantillas de formulario creados con el Kit de herramientas de Microsoft Office InfoPath 2003 para Visual Studio .NET o con Visual Studio 2005 Tools para Microsoft Office System que tienen lógica empresarial escrita en miembros del espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . Los temas de esta sección se refieren a los tipos y miembros de este espacio de nombres como el modelo de objetos compatible con InfoPath 2003 o sencillamente el modelo de objetos de InfoPath 2003. InfoPath también es compatible con los proyectos de plantillas de formulario creados con Microsoft Office InfoPath 2007 que usan el modelo de objetos compatible con InfoPath 2003. Asimismo, puede usar InfoPath para crear nuevos proyectos de plantillas de formulario que usen el modelo de objetos compatible con InfoPath 2003 para que los usuarios de Office InfoPath 2007 dispongan de compatibilidad con versiones anteriores. En todos los temas de esta sección, se describe la creación y el desarrollo de plantillas de formulario que funcionen con el modelo de objetos compatible con InfoPath 2003 proporcionado por el espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
> [!IMPORTANT]
> [!IMPORTANTE] Si bien la creación de lógica empresarial con el modelo de objetos de código administrado proporcionado por el espacio de nombres [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) sigue siendo compatible con InfoPath, la lógica empresarial escrita con este modelo de objetos no se admite en plantillas de formulario habilitadas para el explorador e implementadas en Microsoft SharePoint Server 2010 con InfoPath Forms Services. Las plantillas de formulario habilitadas para el explorador deben usar el nuevo modelo de objetos de código administrado de InfoPath proporcionado por los miembros del espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) para la lógica empresarial personalizada. Para obtener más información acerca de la creación de plantillas de formulario con lógica empresarial escrita con miembros del espacio de nombres [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , vea [Desarrollo de plantillas de formulario de InfoPath con código](developing-infopath-form-templates-with-code.md). > Tenga en cuenta también que los usuarios de plantillas de formulario compiladas con Visual Studio 2012 deben tener Microsoft .NET Framework 2.0 (o versión posterior) instalado en el equipo. Los usuarios de plantillas de formulario compiladas con Visual Studio .NET 2003 solo necesitan disponer de Microsoft .NET Framework 1.1 en el equipo. 
  
## <a name="in-this-section"></a>En esta sección

[Introducción al desarrollo de plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003](get-started-developing-form-templates-using-infopath-object-model.md)
  
> Proporciona información sobre cómo empezar a crear plantillas de formulario con código administrado que funcionen con el modelo de objetos compatible con InfoPath 2003.
    
[Crear plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
  
> Trata el código de limpieza e inicialización, cómo agregar controladores de eventos, cómo depurar e implementar plantillas de formulario con código administrado, la compatibilidad con los subprocesos y cómo trabajar con Microsoft XML Core Services (MSXML) desde soluciones de código administrado de InfoPath.
    
[Seguridad en las plantillas de formulario con código](security-in-infopath-form-templates-with-code.md)
  
> Trata el modelo de seguridad de las plantillas de formulario de InfoPath que usan código administrado, la depuración de plantillas de formulario de InfoPath de plena confianza y procedimientos de seguridad relacionados.
    
[Comprender el modelo de objetos de InfoPath 2003](understanding-the-infopath-2003-object-model.md)
  
> Describe el modelo de objetos compatible con InfoPath 2003 y las tareas de programación más comunes para plantillas de formulario con código administrado que funcionan con dicho modelo de objetos.
    
[Solución de problemas de las plantillas de formulario con código que usan el modelo de objetos de InfoPath 2003](troubleshoot-form-templates-that-use-infopath-object-model.md)
  
> Contiene sugerencias para resolver los problemas más comunes que pueden plantearse al crear plantillas de formulario con código administrado que funcionan con el modelo de objetos compatible con InfoPath 2003.
    
## <a name="related-sections"></a>Secciones relacionadas

[Portal de programadores de InfoPath](http://go.microsoft.com/fwlink?LinkID=11689)
  
> Contiene vínculos a artículos técnicos, ejemplos de código, descargas, soporte técnico y documentación de MSDN relacionada con la creación de soluciones personalizadas de InfoPath.
    
[Centro de programadores de Microsoft Office](http://go.microsoft.com/fwlink?LinkID=27128)
  
> Contiene vínculos a artículos técnicos, ejemplos de código, descargas, soporte técnico y documentación de MSDN relacionada con la creación de soluciones personalizadas de Office.
    

