---
title: Empezar a desarrollar flujos de trabajo de Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Propuestas en Project Server 2013 los procesos de administración incluyen los flujos de trabajo que le ayudan a administrar las propuestas de proyecto y análisis de cartera. En esta sección se incluye artículos que muestran cómo crear flujos de trabajo de Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384097"
---
# <a name="getting-started-developing-project-server-workflows"></a>Empezar a desarrollar flujos de trabajo de Project Server

Propuestas en Project Server 2013 los procesos de administración incluyen los flujos de trabajo que le ayudan a administrar las propuestas de proyecto y análisis de cartera. En esta sección se incluye artículos que muestran cómo crear flujos de trabajo de Project Server.
  
Flujos de trabajo de Project Server 2013 usan la plataforma de flujo de trabajo de SharePoint Server 2013, que se basa en la versión 4 de Windows Workflow Foundation (WF4). Flujos de trabajo basados en WF4 son declarativos, lo que significa que la herramienta de diseño de flujo de trabajo guarda las etapas de flujo de trabajo, acciones, condiciones y otros elementos en el código XAML, que se interpreta en tiempo de ejecución. Puede usar SharePoint Designer 2013 o Visual Studio 2012 para crear flujos de trabajo declarativos. Un flujo de trabajo requiere el motor de ejecución 1.0 de cliente del Administrador de flujo de trabajo, que puede estar en un servidor local para las soluciones locales o en un servidor remoto para soluciones de Project Online.
  
Puede usar SharePoint Designer 2013 para crear flujos de trabajo declarativos relativamente simples. Para flujos de trabajo complejos y plantillas de flujo de trabajo que se pueden reutilizar, puede usar Visual Studio 2012 para desarrollar y depurar flujos de trabajo de Project Web App. Para obtener más información, vea [creación de flujos de trabajo de proyecto con Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).
  
> [!IMPORTANT]
> Usar una instalación de prueba de Project Server, no es una instalación de producción, para desarrollar y probar los flujos de trabajo. Los flujos de trabajo que se ha desarrollado para versiones anteriores a la versión de Project Server 2013 deben probarse para la versión de lanzamiento y que tenga que se vuelve a crear y volver a implementar. 
  
## <a name="in-this-section"></a>En esta sección

[Crear un flujo de trabajo de Project Server para Administración de propuestas](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>Vea también



[Actualizar los campos personalizados de forma masiva y crear sitios de proyecto desde un flujo de trabajo de Project Online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Desarrollo de flujos de trabajo en SharePoint Designer 2013 y Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[Novedades en flujos de trabajo para SharePoint 2013](https://msdn.microsoft.com/library/jj163177.aspx)
  
[Desarrollar de flujos de trabajo de SharePoint 2013 mediante Visual Studio](https://msdn.microsoft.com/library/jj163199.aspx)
  
[Creación de flujos de trabajo de proyecto con Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](https://msdn.microsoft.com/library/dd489441.aspx)
  
[Introducción para desarrolladores a Windows Workflow Foundation (WF) en .NET 4](https://msdn.microsoft.com/library/ee342461.aspx)
  
[Guía para la administración de propuestas (notas del producto)](https://msdn.microsoft.com/library/ff973112.aspx)

