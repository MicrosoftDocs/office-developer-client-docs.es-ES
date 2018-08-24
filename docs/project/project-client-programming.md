---
title: Programación de cliente de Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
f1_keywords:
- object model
- Project object model
- Project VBA
- VBA
keywords:
- VBA, project programación de modelo, Project, objeto, programación, proyecto VBA, Visual Basic para aplicaciones, modelo de objetos de un modelo, VBA, Project objeto, VBA, Visual Basic para aplicaciones
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Las aplicaciones de cliente de escritorio de Project 2013, Project Standard 2013 y Project Professional 2013, puede personalizar y extender mediante el uso de VBA para escribir las macros. Puede usar Visual Studio 2012 para personalizar la interfaz de usuario de la cinta de opciones y crear complementos complejo permite a los complementos de Office modelar una nueva extensibilidad para paneles de tareas de proyecto que se basan en una plataforma común de Office 2013. Project Standard 2013 y Project Professional 2013 pueden ejecutar general complementos de Office y utilizar tarea panel complementos que se ha desarrollado específicamente para que Project integrar con SharePoint, otros sitios Web y aplicaciones web y los datos externos.
ms.openlocfilehash: 9e89c5a1f6486ce49ad8b95bcd7a92497b7a2436
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594743"
---
# <a name="project-client-programming"></a>Programación de cliente de Project

Las aplicaciones de cliente de escritorio de Project 2013, Project Standard 2013 y Project Professional 2013, puede personalizar y extender mediante el uso de VBA para escribir las macros. Puede usar Visual Studio 2012 para personalizar la interfaz de usuario de la cinta de opciones y crear complementos complejo permite a los complementos de Office modelar una nueva extensibilidad para paneles de tareas de proyecto que se basan en una plataforma común de Office 2013. Project Standard 2013 y Project Professional 2013 pueden ejecutar general complementos de Office y utilizar tarea panel complementos que se ha desarrollado específicamente para que Project integrar con SharePoint, otros sitios Web y aplicaciones web y los datos externos.
  
 **Mover a Visual Studio** VBA es útil para la grabación de macros y desarrollo de soluciones de automatización relativamente simple. Para desarrollar complementos de panel de tareas, complementos y más complejo, segura, escalable y fácil de implementar soluciones, se recomienda usar Visual Studio 2012. Microsoft .NET Framework 4.0 y el ensamblado de interoperabilidad primario de Project 2013 ofrecen muchas ventajas para desarrollar e implementar soluciones que automatizan e integran a los clientes de escritorio de Project 2013. 
  
> [!NOTE]
> Puede usar Visual Studio 2010 para desarrollar complementos en el proyecto. Sin embargo, Visual Studio 2012 incluye las plantillas y las extensiones que están diseñadas para crear a los clientes de Office Add-ins. 
  
El modelo de objetos de **MSProject** para VBA en Project 2013 es básicamente el mismo que el modelo de objetos **Microsoft.Office.Interop.MSProject** para soluciones de código administrado con Office Developer Tools para Visual Studio 2013 (también conocido como VSTO). Visual Studio 2012 incluye plantillas para el desarrollo de complementos de nivel de la aplicación para Project 2010 y Project 2013 (versiones de Project Standard o Project Professional). VSTO y Office Developer Tools para Visual Studio 2012 simplificar el desarrollo, prueba e implementación de soluciones de integración avanzada que pueden usar el cliente de escritorio de Project y otras aplicaciones de Office 2013 y se integran con los sitios de SharePoint, listas, y flujos de trabajo. 
  
Complementos de panel de tareas y otros complementos para Office y SharePoint se pueden vender en la tienda de Office (consulte [http://office.microsoft.com/store/](http://office.microsoft.com/en-us/store/)) para su uso con instalaciones de Project Online y local. No se puede distribuir las macros de VBA y complementos VSTO en la tienda de Office; están diseñados para su uso local con Project Standard y Project Professional. Puede distribuir las macros de VBA dentro de un proyecto. Archivo MPP, instálelos en el archivo Global.MPT en su equipo o distribuirlas en la plantilla global de empresa en Project Server 2013. Complementos VSTO se pueden distribuir de forma más segura a través de la implementación de [ClickOnce](http://msdn.microsoft.com/en-us/library/t71a733d.aspx) , lo que permite actualizaciones fáciles. 
  
## <a name="reference"></a>Referencia

[Referencia del programador de VBA de Project](http://msdn.microsoft.com/en-us/library/ee861523%28office.15%29.aspx) Contiene una introducción y artículos de Ayuda de VBA. 
  
## <a name="related-sections"></a>Secciones relacionadas

[Arquitectura de Project Server 2013](project-server-2013-architecture.md) Muestra cómo interactúan los clientes de Project con Project Server. 
  
## <a name="see-also"></a>Vea también

- [Project para desarrolladores](http://msdn.microsoft.com/en-us/office/aa905469)
- [Centro para desarrolladores de Office](https://dev.office.com)
- [Centro para desarrolladores de Visual Studio](http://msdn.microsoft.com/en-us/vstudio/aa718325.aspx)
- [Implementación y seguridad de ClickOnce](http://msdn.microsoft.com/en-us/library/t71a733d.aspx)
- [Referencia de los campos disponibles](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

