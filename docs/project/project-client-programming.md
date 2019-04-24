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
- VBA, modelo de objetos de Project, proyecto, programación, programación, VBA para Project, Visual Basic para aplicaciones, modelo de objetos de Project, VBA, modelo de objetos, VBA, Visual Basic para aplicaciones
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Las aplicaciones cliente de escritorio de Project 2013 (Project Standard 2013 y Project Professional 2013) se pueden personalizar y extender con VBA para escribir macros. Puede usar Visual Studio 2012 para personalizar la interfaz de usuario de la cinta de características y crear complementos complejos. Office Add-Ins habilita un nuevo modelo de extensibilidad para los paneles de tareas de Project que se basan en una plataforma de Office 2013 común. Project Standard 2013 y Project Professional 2013 pueden ejecutar complementos generales de Office y usar complementos de panel de tareas que se desarrollan específicamente para que Project se integre con SharePoint, otros sitios web y aplicaciones Web, y datos externos.
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301515"
---
# <a name="project-client-programming"></a>Programación de cliente de Project

Las aplicaciones cliente de escritorio de Project 2013 (Project Standard 2013 y Project Professional 2013) se pueden personalizar y extender con VBA para escribir macros. Puede usar Visual Studio 2012 para personalizar la interfaz de usuario de la cinta de características y crear complementos complejos. Office Add-Ins habilita un nuevo modelo de extensibilidad para los paneles de tareas de Project que se basan en una plataforma de Office 2013 común. Project Standard 2013 y Project Professional 2013 pueden ejecutar complementos generales de Office y usar complementos de panel de tareas que se desarrollan específicamente para que Project se integre con SharePoint, otros sitios web y aplicaciones Web, y datos externos.
  
 **Cambiar a Visual Studio** VBA es útil para grabar macros y desarrollar soluciones de automatización relativamente sencillas. Para desarrollar complementos de panel de tareas, complementos y soluciones más complejas, seguras, escalables y de fácil implementación, se recomienda usar Visual Studio 2012. Microsoft .NET Framework 4,0 y el ensamblado de interoperabilidad primario del proyecto 2013 proporcionan muchas ventajas para el desarrollo y la implementación de soluciones que automatizan e integran los clientes de escritorio de Project 2013. 
  
> [!NOTE]
> Puede usar Visual Studio 2010 para desarrollar complementos de Project. Sin embargo, Visual Studio 2012 incluye plantillas y extensiones diseñadas para crear clientes de complementos de Office. 
  
El modelo de objetos **MSProject** para VBA en el proyecto 2013 es esencialmente el mismo que el modelo de objetos **Microsoft. Office. Interop. MSProject** para las soluciones de código administrado con Office Developer Tools para Visual Studio 2013 (también conocido como VSTO). Visual Studio 2012 incluye plantillas para desarrollar complementos de nivel de aplicación para el proyecto 2010 y para el proyecto 2013 (ya sea la versión de Project Standard o Project Professional). VSTO y Office Developer Tools para Visual Studio 2012 simplifican el desarrollo, las pruebas y la implementación de soluciones de integración avanzada que pueden usar el cliente de escritorio de Project y otras aplicaciones de Office 2013, así como integrarse con los sitios, las listas y los sitios de SharePoint flujos. 
  
Los complementos de panel de tareas y otros complementos para Office y SharePoint se pueden vender en la tienda Office ( [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/)consulte) para su uso con instalaciones locales y de Project online. Las macros de VBA y los complementos de VSTO no se pueden distribuir en la tienda Office; están diseñados para su uso local con Project Standard y Project Professional. Puede distribuir macros de VBA dentro de un proyecto. MPP, instálelos en el archivo global. MPT del equipo o distribúyalos en la plantilla global de empresa en Project Server 2013. Los complementos VSTO se pueden distribuir de forma más segura a través de la implementación [ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx) , lo que permite actualizaciones sencillas. 
  
## <a name="reference"></a>Referencia

[Referencia para desarrolladores de VBA para Project](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Contiene artículos de ayuda de VBA y introductorios. 
  
## <a name="related-sections"></a>Secciones relacionadas

[Arquitectura de Project Server 2013](project-server-2013-architecture.md) Muestra cómo interactúan los clientes de Project con Project Server. 
  
## <a name="see-also"></a>Vea también

- [Project para desarrolladores](https://msdn.microsoft.com/office/aa905469)
- [Centro para desarrolladores de Office](https://dev.office.com)
- [Centro para desarrolladores de Visual Studio](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [Seguridad e implementación de ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Referencia de campos disponibles](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

