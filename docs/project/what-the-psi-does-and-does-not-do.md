---
title: Lo que hace y lo que no hace la PSI
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: Project Server Interface (PSI) puede ayudar a automatizar muchos procesos del lado servidor en instalaciones locales de Project Server 2013. Sin embargo, varias funciones requieren el uso de Microsoft Project Professional 2013.
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346532"
---
# <a name="what-the-psi-does-and-does-not-do"></a>Lo que hace y no hace PSI

Project Server Interface (PSI) puede ayudar a automatizar muchos procesos del lado servidor en instalaciones locales de Project Server 2013. Sin embargo, varias funciones requieren el uso de Microsoft Project Professional 2013.
  
|||
|:-----|:-----|
|||
   
Psi está diseñada para complementar las capacidades de Project Professional 2013, en lugar de proporcionar una alternativa basada en servidor para todas las funciones de Project Professional. Los desarrolladores de terceros pueden usar psi para ayudar a crear elementos web para instalaciones locales de Project Web App y áreas de trabajo de proyectos, crear aplicaciones personalizadas de Windows y aplicaciones web que interactúan con datos locales de Project Server, desarrollar lógica de flujo de trabajo para la administración de carteras de proyectos, desarrollar controladores de eventos locales de plena confianza e integrar Project Server con otras aplicaciones. Psi no se puede usar para el desarrollo de aplicaciones para la Tienda Office, dispositivos móviles o tabletas; para ello, puede usar el modelo de objetos del lado cliente (CSOM).
  
> [!NOTE]
> PSI proporciona una interfaz programática más completa para Project Server 2013 que el CSOM proporciona. Sin embargo, a menos que este no proporcione las funciones que requiera, le recomendamos usarlo para desarrollar nuevas aplicaciones. Para obtener más información, consulte [What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md). 
  
## <a name="usage-scenarios-for-the-psi"></a>Escenarios de uso de la interfaz PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

A continuación se muestran ejemplos de algunas aplicaciones compatibles con PSI para proyectos del servidor y cálculos:
  
- **Automatizar la creación o administración de entidades en Project Server** Aunque Project Professional 2013 y Project Web App están diseñados conjuntamente para administrar la administración y la creación de entidades como proyectos, recursos de empresa y campos personalizados, a menudo hay casos en los que una aplicación personalizada puede ahorrar tiempo con trabajos masivos o repetitivos. La interfaz PSI puede automatizar diversos tipos de tareas que no hace el CSOM, por ejemplo, con cubos OLAP, análisis de carteras de proyectos, impulsores de negocios, notificaciones, proveedores de vínculos de objetos, seguridad e interoperabilidad SharePoint. 
    
- **Obtener datos en las tablas publicadas o de archivo de la base de datos de Project** Dado que no se admite el acceso directo a la base de datos a las tablas borrador, publicadas y de archivo, puede usar psi para leer datos que no están disponibles en las tablas o vistas de informes. Por ejemplo, obtenga información sobre las versiones del proyecto, las fechas y los cambios almacenados en las tablas de archivo y, a continuación, rellene un control de js grid en un elemento web con la información. 
    
- **Validar datos de estado y parte de horas** Use psi en controladores locales previos a eventos para validar el estado de asignación o los datos del parte de horas que especifiquen los usuarios, antes de guardar los datos en Project Web App. 
    
- **Proyectos de mantenimiento** Crear proyectos de marcador de posición para usarlos con planes de recursos. Reserve tiempo de los recursos para el trabajo de mantenimiento o de base. Los proyectos de mantenimiento no suelen tener tareas. 
    
- **Crear proyectos financieros** Cree proyectos para obtener tiempo mediante el parte de horas para la integración en un sistema financiero. Cree una jerarquía de códigos financieros que refleje la estructura de desglose de costes del sistema financiero. Los proyectos financieros no requieren actualizaciones de estado o programación. 
    
- **Integrar con sistemas de contabilidad** Obtenga los costes y gastos de los recursos relacionados con los proyectos para enviarlos a los sistemas financieros y de facturación, y para realizar comparaciones de presupuestos. Sincronice tareas, recursos y asignaciones entre los sistemas. Obtenga los datos del parte de horas en un sistema para enviarlos a otro (el parte de horas que se use dependerá de las necesidades de la organización o de proyectos individuales). 
    
- **Actualizar el proceso para integrantes del grupo** Si los proyectos no se administran de forma activa, actualícelos automáticamente en el servidor mediante el progreso y otros cambios de los integrantes del grupo del proyecto. Los proyectos se pueden actualizar y volver a publicar sin un jefe de proyecto que revise los resultados o realice ajustes en el plan. 
    
- **Evaluar datos de Project Server en controladores de** eventos locales de plena confianza Un controlador de eventos local para el pre event **ProjectCreating** puede usar datos de Project Server de PSI para ayudar a determinar si se cancela un evento. Por ejemplo, antes de crear un proyecto, compare la propuesta del proyecto con los proyectos existentes. 
    
- **Crear actividades de flujo de trabajo personalizadas para la administración de demandas** Use psi en actividades de flujo de trabajo locales de plena confianza para modificar y actualizar propuestas de proyecto basadas en plantillas de proyecto empresarial. Use campos personalizados de proyecto para etiquetar al proyecto con la información necesaria para el proceso de iniciación y aprobación. Añada tareas para identificar las fases del proyecto para hitos o resultados clave. Cuando se aprueban propuestas de proyectos, un flujo de trabajo puede convertir las propuestas en proyectos a escala completa administrados con Project Professional. 
    
- **Crear extensiones de PSI** **(en desuso.** Las extensiones están en desuso en Project Server 2013 y no se admiten en futuras versiones). Psi se puede extender con servicios personalizados mediante la interfaz de Windows Communication Foundation (WCF). Las extensiones de PSI se ejecutan en el equipo que tiene Project Server y pueden usar la misma infraestructura de seguridad que los servicios de PSI integrados. Las extensiones pueden consultar las tablas de informes, usar tablas de base de datos independientes, consolidar llamadas a PSI para ahorrar ancho de banda e integrarse con aplicaciones de terceros y otros componentes del servidor. Para obtener más información, consulte [Desarrollo de extensiones de PSI](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx).
    
- **Usar la suplantación en aplicaciones locales de plena confianza** Las llamadas a la interfaz WCF de PSI se pueden suplantar, de modo que una aplicación asume los permisos de seguridad del usuario suplantado. La suplantación de personalidad debe usarse con moderación y cuidado. La lectura y actualización de la información de estado para otros usuarios no requiere suplantación de identidad. Las nuevas aplicaciones que requieran la suplantación de identidad deben usar el CSOM y el protocolo OAuth en lugar de la interfaz PSI. Para obtener más información acerca de la suplantación con psi, vea [Usar suplantación con WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).
    
> [!NOTE]
> En algunos casos, psi puede usarse en aplicaciones cliente con el CSOM y Project Online. Si usa un servicio web de PSI basado en ASMX, la aplicación debe incluir un método para autenticar el objeto [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) en el CSOM y un método para autenticar el objeto de cliente **System.Web.Services.Protocols.SoapHttpClientProtocol.** Para ver un ejemplo que usa un servicio web con el CSOM de SharePoint, consulte [Autenticación remota en SharePoint Online mediante la autenticación basada en notificaciones](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx). > debido a los permisos restringidos de nivel de aplicación, psi no se puede usar en aplicaciones diseñadas para su distribución en la Tienda Office pública. En tal caso, solo puede usar el CSOM. 
  
## <a name="what-the-psi-does-not-do"></a>Lo que la interfaz PSI no hace
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Aunque la interfaz PSI puede hacer muchas cosas, hay algunas que no puede hacer. A continuación se indican dos cosas que no puede hacer la interfaz PSI, pero sí el CSOM.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online y receptores de eventos remotos

La limitación principal de PSI es con Project Online. Las aplicaciones que usan la interfaz requieren acceso de confianza plena a una instalación local de Project Server. Por ejemplo, psi no se puede usar en receptores de eventos remotos, donde el receptor de eventos está instalado como servicio en Microsoft Azure.
  
### <a name="workflows-and-claims-authentication"></a>Flujos de trabajo y autenticación de notificaciones

Una definición de flujo de trabajo que usa Windows Workflow Foundation versión 4 (WF4) requiere autenticación de notificaciones, que psi no admite directamente. Esto significa que no puede usar psi para crear un proyecto en Project Server 2013 que tenga un tipo de proyecto empresarial (EPT) con una definición de flujo de trabajo WF4.
  
Puede usar psi para crear proyectos con ETS que no tienen flujo de trabajo o usar una definición wf3.5 heredada (la versión de flujo de trabajo en Project Server 2010). Para crear un proyecto con un tipo EPT que tenga una definición de WF4, use el CSOM.
  
 **Acciones que requieren Project Professional:**
  
La siguiente lista son cosas que no pueden hacer ni la interfaz PSI ni el CSOM.
  
#### <a name="local-data"></a>Datos locales

- Manipulación de datos en proyectos locales (archivos .mpp). Por ejemplo, la definición de tablas de tipos de coste o contornos de disponibilidad para recursos locales. 
    
- Definición o edición de calendarios base locales o calendarios de recursos, incluidas excepciones del calendario.
    
- Definición de campos personalizados locales. (La interfaz PSI no admite la edición de valores de campos personalizados locales en tareas, recursos y asignaciones.)
    
#### <a name="enterprise-data"></a>Datos de la empresa

- Desprotección o edición de la plantilla global de la empresa. Los datos globales de empresa de Project Server 2013 son un conjunto de tablas de datos binarios de la base de datos de Project, no una plantilla de proyecto como en Office Project Server 2007 y versiones anteriores.
    
- Definición o edición de calendarios de la empresa. Los [métodos calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) administran solo excepciones de calendario. 
    
#### <a name="master-projects-and-cross-project-links"></a>Proyectos maestros y vínculos entre proyectos

- Creación de proyectos maestros e inserción de subproyectos.
    
- Programación de una ruta crítica a través de un proyecto maestro. 
    
- Creación de vínculos entre proyectos.
    
#### <a name="resources"></a>Recursos

- Solicitud o realización de nivelación de recursos.
    
- Cambio del recurso en una asignación. (Puede usar la interfaz PSI para eliminar la asignación y crear una nueva.)
    
- Eliminación o sustitución de un recurso que tiene el trabajo real aceptado (datos reales).
    
- Cambio de un tipo de recurso entre trabajo, material y costo.
    
- Creación o edición de calendarios de recursos.
    
- Cuando se añade un recurso a una tarea, la interfaz PSI no redistribuye automáticamente el trabajo del modo que lo hace Project Professional. Depende del programador elegir y definir de manera explícita la distribución de trabajo en las asignaciones.
    
#### <a name="cost-resources"></a>Cost resources

- Edición, creación o eliminación de asignaciones y recursos de costo mediante los métodos [de Project.](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) Los [métodos Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) pueden crear recursos de costo, pero no pueden editarlos. 
    
#### <a name="work-contours"></a>Perfiles de trabajo

- Edición de datos con fases temporales.
    
    > [!NOTE]
    > El [método UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) del servicio **web** de estado puede editar los datos reales de fases tiempo en las asignaciones después de que el jefe de proyecto actualice y publique los datos de asignación. 
  
- Configuración o cambio del tipo de contorno de la asignación (como plano, creciente o decreciente).
    
#### <a name="baselines-and-earned-value"></a>Referencias y valor acumulado

- Guardar una referencia o edición de los datos de referencia. 
    
- Configuración de una fecha de progreso.
    
- Cálculo de variación y valor acumulado. 
    
#### <a name="interactive-scheduling"></a>Programación interactiva

- Compatibilidad con la programación interactiva. (Dado que Project Server gestiona las interacciones de manera asincrónica, la programación interactiva debe realizarse con Project Professional.)
    
    > [!NOTE]
    > Para evitar cambiar el comportamiento mediante programación, los métodos de PSI que se han presentado desde Project Server 2010 actúan del mismo modo en Project Server 2013. Por ejemplo, [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) sigue teniendo las mismas limitaciones y usa el motor de programación anterior del lado servidor. El nuevo método [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) elimina muchas de estas limitaciones y usa el nuevo motor de programación del lado servidor de Project Server 2013, que es el mismo motor de programación que en Project Professional 2013. 
  
#### <a name="wbs"></a>WBS

- Definición de una máscara de código de estructura de desglose del trabajo (EDT). 
    
#### <a name="tasks"></a>Tareas

- Cambio del tipo de tarea (trabajo fijo, duración o unidades).
    
- Cambio de si una tarea está condicionada por el esfuerzo.
    
- Cambio de acumulación de costos fijos de tareas.
    
- Cambio del contenido del [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) campo. La interfaz PSI solo puede leer la parte de texto de las notas de tareas, que son datos binarios .rtf. Sin embargo, puede editar notas de [asignación](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ( ASSN_NOTES ), que son datos de texto. La base de datos de informes no incluye notas de tareas o de asignaciones. 
    
- Creación o edición de tareas recurrentes.
    
- Asignación o cambio del calendario de tareas en tareas existentes.
    
- Creación de una tarea nueva con un calendario de tareas.
    
- Cambio del valor del campo [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) (la tarea omite el calendario de recursos). 
    
- Cambiar el estado activo de una tarea mediante [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , si se realizan cambios adicionales en la misma llamada. Para obtener más información, vea la sección  *Programación de proyectos en el servidor*  en [Programación de Project Server](project-server-programmability.md).
    
#### <a name="summary-tasks"></a>Tareas de resumen

- Creación o cambio de asignaciones en tareas de resumen.
    
    > [!NOTE]
    > Recomendamos que no realice asignaciones en tareas de resumen mediante Project Professional o de ningún otro modo. Para obtener más información, vea la sección  *Programación de proyectos en el servidor*  en [Programación de Project Server](project-server-programmability.md). 
  
- Edición de campos de tareas de resumen que normalmente se acumulan desde la subtarea. Los proyectos del servidor siempre acumulan información de resumen, en lugar de configurar información sobre la tarea de resumen y aplicarla a las subtareas. Solo se pueden editar los siguientes niveles en tareas de resumen:
    
  - Dependencias de tareas
    
  - Campos personalizados sin fórmulas
    
  - [TASK_NAME](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [TASK_OUTLINE_LEVEL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [TASK_IS_MARKED](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [TASK_CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [TASK_CONSTRAINT_DATE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [TASK_PRIORITY](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [TASK_DEADLINE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [TASK_FIXED_COST](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (establecer el valor solo al crear la tarea) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
Para la tarea de resumen del proyecto, las limitaciones de PSI son las mismas que para Project Professional. La interfaz PSI puede editar asignaciones de presupuesto (incluidos presupuestos de costos).
  
#### <a name="project-level-calculation-options"></a>Opciones de cálculo en el nivel de proyecto

- Cambio de un tipo de proyecto entre Programar desde el comienzo (SFS) y Programar desde el fin (SFF). (La interfaz PSI puede crear un proyecto como SFS o como SFF, pero, una vez creado, solo se puede cambiar en Project Professional.)
    
- Cambiar el calendario base del proyecto ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) después de la creación del proyecto. 
    
- Cambio de opciones para cálculos. Puede usar la interfaz PSI para definir las siguientes opciones de cálculo cuando se crea el proyecto, pero el cambio de las opciones requiere Project Professional. (En la vista Backstage, elija **Opciones** y seleccione la ficha **Programa** en el cuadro de diálogo **Opciones de proyecto**.) 
    
  - [PROJ_OPT_CALC_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CALC_ACT_COSTS.aspx)
    
  - [PROJ_OPT_CRITICAL_SLACK_LIMIT](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CRITICAL_SLACK_LIMIT.aspx)
    
  - [PROJ_OPT_HONOR_CONSTRAINTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_HONOR_CONSTRAINTS.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_IF_LATER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_IF_LATER.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_TO_STATUS.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_IF_EARLIER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_IF_EARLIER.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_TO_STATUS.aspx)
    
  - [PROJ_OPT_MULT_CRITICAL_PATHS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MULT_CRITICAL_PATHS.aspx)
    
  - [PROJ_OPT_SPLIT_IN_PROGRESS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPLIT_IN_PROGRESS.aspx)
    
  - [PROJ_OPT_SPREAD_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_ACT_COSTS.aspx)
    
  - [PROJ_OPT_SPREAD_PCT_COMP](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_PCT_COMP.aspx)
    
  - [PROJ_OPT_TASK_UPDATES_RES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_TASK_UPDATES_RES.aspx)
    
## <a name="see-also"></a>Consulte también

- [Qué hace y qué no hace el CSOM](what-the-csom-does-and-does-not-do.md)  
- [Programación de Project Server](project-server-programmability.md)   
- [Autenticación remota en SharePoint Online mediante la autenticación basada en notificaciones](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)  
- [Complementos de Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) 
    

