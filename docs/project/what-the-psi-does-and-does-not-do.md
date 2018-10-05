---
title: Lo que hace y lo que no hace la PSI
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: Project Server Interface (PSI) puede ayudar a automatizar muchos procesos de servidor en instalaciones locales de Project Server 2013. Sin embargo, hay varias funciones requieren el uso de Microsoft Project Professional 2013.
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386344"
---
# <a name="what-the-psi-does-and-does-not-do"></a>Lo que hace y no hace PSI

Project Server Interface (PSI) puede ayudar a automatizar muchos procesos de servidor en instalaciones locales de Project Server 2013. Sin embargo, hay varias funciones requieren el uso de Microsoft Project Professional 2013.
  
|||
|:-----|:-----|
|||
   
La interfaz PSI está diseñada para complementar las capacidades de Project Professional 2013, en lugar de proporcionar una alternativa basada en servidor para todas las funciones de Project Professional. Los programadores de terceros pueden utilizar la interfaz PSI para ayudar a crear elementos Web para instalaciones locales de áreas de trabajo de project y Project Web App, crear aplicaciones personalizadas de Windows y aplicaciones web que interactúan con datos de Project Server local, desarrollar el flujo de trabajo lógica de administración de carteras de proyectos, desarrollar los controladores de eventos de plena confianza local e integrar Project Server con otras aplicaciones. La interfaz PSI no se puede usar para el desarrollo de aplicaciones para la tienda de Office, dispositivos móviles o tabletas; Para ello, puede usar el modelo de objetos de cliente (COM).
  
> [!NOTE]
> La interfaz PSI proporciona una interfaz de mediante programación más integral para Project Server 2013 que proporciona el CSOM. Pero, a menos que el CSOM no proporcionan la funcionalidad que necesita, se recomienda que use el CSOM para desarrollar nuevas aplicaciones. Para obtener más información, vea [el CSOM ¿qué hace y no hace](what-the-csom-does-and-does-not-do.md). 
  
## <a name="usage-scenarios-for-the-psi"></a>Escenarios de uso de la interfaz PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

A continuación se muestran ejemplos de algunas aplicaciones compatibles con PSI para proyectos del servidor y cálculos:
  
- **Automatice la creación o administración de entidades de Project Server** Aunque Project Professional 2013 y Project Web App conjuntamente están diseñados para controlar la administración y la creación de entidades como proyectos, recursos de empresa y campos personalizados, a menudo son los casos donde una aplicación personalizada puede ahorrar tiempo con masiva o tareas repetitivas. La interfaz PSI puede automatizar varios tipos de trabajos que no hace el CSOM, por ejemplo, con cubos OLAP, análisis de cartera de proyectos, los impulsores de negocios, las notificaciones, proveedores de objetos de vínculo, seguridad e interoperabilidad de SharePoint. 
    
- **Obtener datos en el publicado o tablas de archivo de la base de datos de Project** Como base de datos directa el acceso a la borrador, publicada y archivar las tablas no es compatible, puede usar la interfaz PSI para leer datos que no está disponibles en las tablas o vistas de informes. Por ejemplo, obtener información acerca de las versiones del proyecto, las fechas y los cambios que se almacenan en las tablas de archivado y, a continuación, rellenar un control de cuadrícula JS en un elemento web con la información. 
    
- **Validar los datos de estado y partes de horas** Use la PSI en locales gestores para validar los datos de estado o partes de horas de asignación que los usuarios escribir, antes de que los datos se guardan en Project Web App. 
    
- **Proyectos de mantenimiento** Crear proyectos para usar con los planes de recursos de marcador de posición. Reserve tiempo de los recursos para el trabajo de mantenimiento o su negocio base. Proyectos de mantenimiento no suelen tener tareas. 
    
- **Crear proyectos financieros** Creación de proyectos para captura de tiempo a través de la parte de horas para la integración con un sistema financiero. Crear una jerarquía de códigos financieros que reflejen la estructura de desglose de costos del sistema financiero. Proyectos financieros no requieren actualizaciones de estado o programación. 
    
- **Integrar con sistemas de contabilidad** Capturar los costos de recursos y los gastos asociados con proyectos de fuente sistemas financieros y de facturación y con fines de comparación de presupuesto. Sincronizar las tareas, recursos y asignaciones entre los sistemas. Capturar datos del parte de horas en un sistema a la otra fuente (se usa el parte de horas depende de las necesidades de la organización o de proyectos individuales). 
    
- **Actualizaciones de automatizar los miembros del equipo** Para los proyectos que no se administran activamente, actualice automáticamente proyectos en el servidor con progreso y otros cambios de los miembros del equipo de proyecto. Proyectos se pueden actualizar y volver a publicar sin un jefe de proyecto revisar los resultados o realice ajustes en el plan. 
    
- **Datos de evaluación de Project Server en los controladores de eventos de plena confianza local** Un controlador de eventos locales para el evento previo a la **ProjectCreating** puede usar datos de Project Server desde la interfaz PSI para ayudar a determinar si se debe cancelar un evento. Por ejemplo, antes de crear un proyecto, compare la propuesta de proyecto con proyectos existentes. 
    
- **Crear actividades de flujo de trabajo personalizado para la administración de propuestas** Use la interfaz PSI en las actividades del flujo de trabajo local, de plena confianza para modificar y actualizar las propuestas de proyecto en función de las plantillas de proyecto de empresa. Usar campos personalizados de proyecto para etiquetar el proyecto con la información necesaria para el proceso de inicio y aprobación. Agregue tareas para identificar las fases de proyecto para los hitos clave o entregas. Cuando se aprueban las propuestas de proyecto, un flujo de trabajo puede cambiar las propuestas en proyectos a gran escala que se administran con Project Professional. 
    
- **Extensiones de creación de PSI** (**En desuso.** Las extensiones están en desuso en Project Server 2013 y no se admite en versiones futuras). La PSI se puede extender con servicios personalizados mediante la interfaz de Windows Communication Foundation (WCF). Extensiones de PSI ejecutan en el equipo de Project Server y pueden usar la misma infraestructura de seguridad que usan los servicios integrados de PSI. Las extensiones de las tablas de informes de consulta, utilice tablas de base de datos independiente, consolidar las llamadas PSI para ahorrar ancho de banda e integrar con aplicaciones de terceros y otros componentes del lado del servidor. Para obtener más información, vea [Desarrollar extensiones de PSI](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx).
    
- **Usar suplantación en las aplicaciones locales y de plena confianza** Las llamadas a la interfaz WCF de la PSI pueden ser suplantadas, por lo que una aplicación supone que los permisos de seguridad del usuario suplantado. Suplantación debe usarse con moderación y cuidadosamente. Leer y actualizar la información de estado de otros usuarios no requieren suplantación. Nuevas aplicaciones que requieren la suplantación deben usar el protocolo de OAuth y el CSOM en lugar de la PSI. Para obtener más información sobre la suplantación con la interfaz PSI, vea [Usar suplantación con WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).
    
> [!NOTE]
> En algunos casos, se puede usar la interfaz PSI en aplicaciones de cliente con el CSOM y Project Online. Si usa un servicio web PSI basadas en ASMX, la aplicación debe incluir un método para autenticar el objeto [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) en el CSOM y un método para autenticar el ** System.Web.Services.Protocols.SoapHttpClientProtocol** objeto de cliente. Para obtener un ejemplo que usa un servicio web con el CSOM de SharePoint, vea [Autenticación remota en la autenticación SharePoint Online Using Claims-Based](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx). > Porque de permisos de nivel de aplicación limitados, la interfaz PSI no puede usarse en las aplicaciones que están diseñadas para su distribución en la tienda de Office pública. En ese caso, puede usar sólo el CSOM. 
  
## <a name="what-the-psi-does-not-do"></a>Lo que la interfaz PSI no hace
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Aunque la interfaz PSI puede hacer muchas cosas, hay algunas que no puede hacer. A continuación se indican dos cosas que no puede hacer la interfaz PSI, pero sí el CSOM.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online y receptores de eventos remotos

La limitación principal de la PSI es con Project Online. Las aplicaciones que usan la PSI requieren acceso de plena confianza a una instalación local de Project Server. Por ejemplo, la interfaz PSI no puede usarse en receptores de eventos remotos, donde está instalado el receptor de eventos como un servicio en Microsoft Azure.
  
### <a name="workflows-and-claims-authentication"></a>Flujos de trabajo y autenticación de notificaciones

Una definición de flujo de trabajo que use la versión de Windows Workflow Foundation 4 (WF4) requiere la autenticación de notificaciones, que no admite directamente la PSI. Esto significa que no se puede usar la interfaz PSI para crear un proyecto en Project Server 2013 que tiene un tipo de proyecto empresarial (EPT) con una definición de flujo de trabajo WF4.
  
Puede usar la interfaz PSI para crear proyectos con EPT que no tiene ningún flujo de trabajo o utiliza una definición de WF3.5 heredada (la versión del flujo de trabajo en Project Server 2010). Para crear un proyecto con una plantilla EPT que tiene una definición de WF4, use el CSOM.
  
 **Acciones que requieren Project Professional:**
  
La siguiente lista son cosas que no pueden hacer ni la interfaz PSI ni el CSOM.
  
#### <a name="local-data"></a>Datos locales

- Manipulación de datos en proyectos locales (archivos .mpp). Por ejemplo, la definición de tablas de tipos de coste o contornos de disponibilidad para recursos locales. 
    
- Definición o edición de calendarios base locales o calendarios de recursos, incluidas excepciones del calendario.
    
- Definición de campos personalizados locales. (La interfaz PSI no admite la edición de valores de campos personalizados locales en tareas, recursos y asignaciones.)
    
#### <a name="enterprise-data"></a>Datos de la empresa

- Desprotección o edición de la plantilla global de empresa. Los datos globales de empresa en Project Server 2013 están un conjunto de tablas de datos binarios de la base de datos de Project, no una plantilla de proyecto como en Office Project Server 2007 y versiones anteriores.
    
- Definición o edición de calendarios de empresa. Los métodos de [calendario](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) administran sólo las excepciones de calendario. 
    
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
    
#### <a name="cost-resources"></a>Recursos de costo

- Editar, crear o eliminar recursos de costo y las asignaciones mediante los métodos del [proyecto](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) . Los métodos de [recursos](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) pueden crear recursos de costo, pero no pueden editarlos. 
    
#### <a name="work-contours"></a>Perfiles de trabajo

- Edición de datos con fases temporales.
    
    > [!NOTE]
    > El método [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) en el servicio Web de **administración de Estados** puede editar datos reales de fase temporal de asignaciones una vez que el jefe de proyecto actualiza y publica los datos de asignación. 
  
- Configuración o cambio del tipo de contorno de la asignación (como plano, creciente o decreciente).
    
#### <a name="baselines-and-earned-value"></a>Referencias y valor acumulado

- Guardar una referencia o edición de los datos de referencia. 
    
- Configuración de una fecha de progreso.
    
- Cálculo de variación y valor acumulado. 
    
#### <a name="interactive-scheduling"></a>Programación interactiva

- Compatibilidad con la programación interactiva. (Dado que Project Server gestiona las interacciones de manera asincrónica, la programación interactiva debe realizarse con Project Professional.)
    
    > [!NOTE]
    > Para evitar cambiar el comportamiento de programación, los métodos PSI que pasan desde Project Server 2010 actúan del mismo modo en Project Server 2013. Por ejemplo, [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) todavía tiene las mismas limitaciones y usa el motor de programación de servidor anterior. El nuevo método [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) quita muchas de las limitaciones y usa el nuevo Project Server 2013 servidor motor de programación, que es el mismo motor de programación que se encuentra en Project Professional 2013. 
  
#### <a name="wbs"></a>EDT

- Definición de una máscara de código de estructura de desglose del trabajo (EDT). 
    
#### <a name="tasks"></a>Tareas

- Cambio del tipo de tarea (trabajo fijo, duración o unidades).
    
- Cambio de si una tarea está condicionada por el esfuerzo.
    
- Cambio de acumulación de costos fijos de tareas.
    
- Cambiar el contenido del campo [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) . La interfaz PSI puede leer sólo la parte de texto de las notas de tarea, que son datos binarios .rtf. Sin embargo, puede editar notas de la asignación ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ), que son datos de texto. La base de datos de informes no incluye notas de la tarea o asignación. 
    
- Creación o edición de tareas recurrentes.
    
- Asignación o cambio del calendario de tareas en tareas existentes.
    
- Creación de una tarea nueva con un calendario de tareas.
    
- Al cambiar el valor del campo [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) (la tarea ignora el calendario de recursos). 
    
- Cambio del estado activo de una tarea mediante el uso de [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , si se realizan cambios adicionales en la misma llamada. Para obtener más información, vea la sección *Programación de proyectos en el servidor* en la [programación de Project Server](project-server-programmability.md).
    
#### <a name="summary-tasks"></a>Tareas de resumen

- Creación o cambio de asignaciones en tareas de resumen.
    
    > [!NOTE]
    > Se recomienda no realizar asignaciones en tareas de resumen de uso de Project Professional o cualquier otro medio. Para obtener más información, vea la sección *Programación de proyectos en el servidor* en la [programación de Project Server](project-server-programmability.md). 
  
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
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (establecer el valor sólo cuando se crea la tarea) 
    
  - [COLUMNAS TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
Para la tarea de resumen del proyecto, las limitaciones de PSI son las mismas que para Project Professional. La interfaz PSI puede editar asignaciones de presupuesto (incluidos presupuestos de costos).
  
#### <a name="project-level-calculation-options"></a>Opciones de cálculo en el nivel de proyecto

- Cambio de un tipo de proyecto entre Programar desde el comienzo (SFS) y Programar desde el fin (SFF). (La interfaz PSI puede crear un proyecto como SFS o como SFF, pero, una vez creado, solo se puede cambiar en Project Professional.)
    
- Cambio del calendario de base de proyecto ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) después de la creación del proyecto. 
    
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
    
## <a name="see-also"></a>Vea también

- [Lo que hace y no hace CSOM](what-the-csom-does-and-does-not-do.md)  
- [Programación de Project Server](project-server-programmability.md)   
- [Autenticación remota en SharePoint Online mediante la autenticación basada en notificaciones](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)  
- [Crear aplicaciones para Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) 
    

