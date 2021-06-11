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
- vba, project object model,Project, programmability,Programmability, Project VBA,Visual Basic para Aplicaciones, Project object model,VBA, object model,VBA,Visual Basic para Aplicaciones
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Las Project cliente de escritorio de Project Standard 2013 (Project Standard 2013 y Project Profesional 2013) se pueden personalizar y ampliar mediante VBA para escribir macros. Puede usar Visual Studio 2012 para personalizar la interfaz de usuario de la cinta de opciones y crear complementos complejos. Office Los complementos habilitan un nuevo modelo de extensibilidad para los paneles de tareas en Project que se integran en una plataforma Office 2013. Project Standard 2013 y Project Profesional 2013 pueden ejecutar complementos de Office generales y usar complementos de panel de tareas desarrollados específicamente para que Project se integre con SharePoint, otros sitios web y aplicaciones web y datos externos.
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301515"
---
# <a name="project-client-programming"></a>Programación de cliente de Project

Las Project cliente de escritorio de Project Standard 2013 (Project Standard 2013 y Project Profesional 2013) se pueden personalizar y ampliar mediante VBA para escribir macros. Puede usar Visual Studio 2012 para personalizar la interfaz de usuario de la cinta de opciones y crear complementos complejos. Office Los complementos habilitan un nuevo modelo de extensibilidad para los paneles de tareas en Project que se integran en una plataforma Office 2013. Project Standard 2013 y Project Profesional 2013 pueden ejecutar complementos de Office generales y usar complementos de panel de tareas desarrollados específicamente para que Project se integre con SharePoint, otros sitios web y aplicaciones web y datos externos.
  
 **Pasar a Visual Studio** VBA es útil para grabar macros y desarrollar soluciones de automatización relativamente sencillas. Para desarrollar complementos de panel de tareas, complementos y soluciones más complejas, seguras, escalables y fácilmente implementadas, se recomienda usar Visual Studio 2012. Microsoft .NET Framework 4.0 y el ensamblado de interoperabilidad principal de Project 2013 proporcionan muchas ventajas para desarrollar e implementar soluciones que automatizan e integran los clientes de escritorio de Project 2013. 
  
> [!NOTE]
> Puede usar Visual Studio 2010 para desarrollar Project complementos. Sin embargo, Visual Studio 2012 incluye plantillas y extensiones diseñadas para crear Office de complementos. 
  
El modelo de objetos **MSProject** para VBA en Project 2013 es esencialmente el mismo que **microsoft.Office. Modelo de objetos Interop.MSProject** para soluciones de código administrado con Office Developer Tools para Visual Studio 2013 (también conocida como VSTO). Visual Studio 2012 incluye plantillas para desarrollar complementos de nivel de aplicación para Project 2010 y para Project 2013 (ya sea las versiones Project Standard o Project Profesional). VSTO y Office Developer Tools para Visual Studio 2012 simplifican el desarrollo, las pruebas y la implementación de soluciones de integración avanzadas que pueden usar el cliente de escritorio de Project y otras aplicaciones de Office 2013, e integrarse con sitios, listas y flujos de trabajo de SharePoint. 
  
Los complementos de panel de tareas y otros complementos para Office y SharePoint se pueden vender en la Tienda Office (consulte ) para su uso con instalaciones locales y [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/) Project Online. Las macros de VBA VSTO complementos no se pueden distribuir en el Office store; están diseñados para su uso local con Project Standard y Project Profesional. Puede distribuir macros de VBA dentro de un proyecto . MPP, instáleslos en el archivo Global.MPT del equipo o distribuyalos en la plantilla global de empresa en Project Server 2013. VSTO los complementos se pueden distribuir de forma más segura a través [ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx) implementación, lo que permite actualizaciones sencillas. 
  
## <a name="reference"></a>Referencia

[Project de desarrollador de VBA](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Contiene artículos de introducción y ayuda de VBA. 
  
## <a name="related-sections"></a>Secciones relacionadas

[Project server 2013](project-server-2013-architecture.md) Muestra cómo los Project interactúan con Project server. 
  
## <a name="see-also"></a>Vea también

- [Project para desarrolladores](https://msdn.microsoft.com/office/aa905469)
- [Office de desarrolladores](https://dev.office.com)
- [Visual Studio de desarrolladores](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [ClickOnce Seguridad e implementación](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Referencia de campos disponibles](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

