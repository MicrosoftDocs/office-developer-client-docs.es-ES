---
title: Empezar a desarrollar flujos de trabajo de Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Los procesos de administración de propuestas en Project Server 2013 incluyen flujos de trabajo que ayudan a administrar las propuestas de proyecto y los análisis de cartera. Esta sección incluye artículos que muestran cómo crear flujos de trabajo para Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344474"
---
# <a name="getting-started-developing-project-server-workflows"></a>Empezar a desarrollar flujos de trabajo de Project Server

Los procesos de administración de propuestas en Project Server 2013 incluyen flujos de trabajo que ayudan a administrar las propuestas de proyecto y los análisis de cartera. Esta sección incluye artículos que muestran cómo crear flujos de trabajo para Project Server.
  
Los flujos de trabajo de Project Server 2013 usan la plataforma de flujo de trabajo de SharePoint Server 2013, que se basa en la versión 4 de Windows Workflow Foundation (WF4). Los flujos de trabajo basados en WF4 son declarativos, lo que significa que la herramienta de diseño de flujo de trabajo guarda fases de flujo de trabajo, acciones, condiciones y otros elementos en el código XAML, que se interpreta en tiempo de ejecución. Puede usar SharePoint Designer 2013 o Visual Studio 2012 para crear flujos de trabajo declarativos. Un flujo de trabajo requiere el motor de ejecución del cliente 1,0 del administrador de flujos de trabajo, que puede estar en un servidor local para las soluciones locales o en un servidor remoto para las soluciones de Project online.
  
Puede usar SharePoint Designer 2013 para crear flujos de trabajo declarativos relativamente sencillos. Para los flujos de trabajo complejos y las plantillas de flujo de trabajo que se pueden volver a usar, puede usar Visual Studio 2012 para desarrollar y depurar flujos de trabajo de Project Web App. Para obtener más información, vea [crear flujos de trabajo de Project con Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).
  
> [!IMPORTANT]
> Utilice una instalación de prueba de Project Server, no una instalación de producto, para desarrollar y probar los flujos de trabajo. Los flujos de trabajo que se desarrollan para las versiones preliminares de Project Server 2013 deben probarse para la versión de lanzamiento y es posible que tengan que volver a crearse y volver a implementarse. 
  
## <a name="in-this-section"></a>En esta sección

[Crear un flujo de trabajo de Project Server para la administración de propuestas](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a>Vea también



[Actualizar masivamente campos personalizados y crear sitios de proyecto desde un flujo de trabajo de Project online](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[Desarrollo de flujos de trabajo en SharePoint Designer 2013 y Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[Novedades en flujos de trabajo para SharePoint 2013](https://msdn.microsoft.com/library/jj163177.aspx)
  
[Desarrollar de flujos de trabajo de SharePoint 2013 mediante Visual Studio](https://msdn.microsoft.com/library/jj163199.aspx)
  
[Crear flujos de trabajo de Project con Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[Windows Workflow Foundation](https://msdn.microsoft.com/library/dd489441.aspx)
  
[Una introducción para desarrolladores a Windows Workflow Foundation (WF) en .NET 4](https://msdn.microsoft.com/library/ee342461.aspx)
  
[Guía de autoestopistas sobre para la administración de propuestas (notas del producto)](https://msdn.microsoft.com/library/ff973112.aspx)

