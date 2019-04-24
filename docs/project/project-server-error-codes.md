---
title: Códigos de error de Project Server
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- error codes
- errors
- Project Server errors
- PSErrorID
- PSI errors
keywords:
- PSI, códigos de error, códigos de error, Project Server, PSErrorID, Project Server Interface, códigos de error, Project Server, códigos de error
ms.assetid: db78a09c-ebef-47cc-8623-40abe117aa08
description: Este tema contiene las tablas con los códigos de error de Project Server Interface (PSI) en Project Server 2013. Las tablas están organizadas por áreas funcionales y por intervalos de los códigos de error.
localization_priority: Priority
ms.openlocfilehash: c61821bcb85fa3bd83601659850577eaa93eda61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301480"
---
# <a name="project-server-error-codes"></a>Códigos de error de Project Server

Este tema contiene las tablas con los códigos de error de Project Server Interface (PSI) en Project Server 2013. Las tablas están organizadas por áreas funcionales y por intervalos de los códigos de error.
   
Los procesos de Project Server 2013 y los métodos de PSI tienen números de códigos de error que se suelen organizar según el área funcional. La enumeración [Microsoft.Office.Project.Server.Library.PSErrorID](https://msdn.microsoft.com/library/microsoft.office.project.server.library.pserrorid_di_pj14mref(v=office.14).aspx) está duplicada en [WebSvcProject.PSErrorID](https://msdn.microsoft.com/library/office/websvcproject.pserrorid_di_pj14mref.aspx), los códigos de error se enumeran en orden alfabético por nombre. En este tema se enumeran los códigos de error en tablas, las cuales están organizadas por la clase de PSI o por el área funcional y el número de identificación (id.) del error. 
  
> [!NOTE]
>  Muchos de los códigos de error son generales y pueden tener varias causas posibles. Si desea obtener más información sobre los errores, puede hacer lo siguiente: 
> - Para las aplicaciones basadas en ASMX, use **System.Web.Services.Protocols.SoapException** con el objeto **PSClientError** para mostrar una lista o jerarquía de errores en una llamada de método PSI. Vea [Ejemplo de códigos de error de ASMX](#pj15_ErrorCodes_ASMXExample). 
> - Para las aplicaciones basadas en WCF, puede usar **System.ServiceModel.FaultException** para obtener un objeto **PSClientError** y también para obtener información adicional sobre el error. Vea [Ejemplo de códigos de error de WCF](#pj15_ErrorCodes_WCFExample). 
> - Use el registro de eventos de la aplicación en el equipo de Project Server.
> - Use los registros de seguimiento del Servicio de registro unificado (ULS). Para obtener una explicación, consulte la sección de *comprobación de errores* del artículo [Getting Started with Development for Project 2010](https://msdn.microsoft.com/library/gg607685.aspx) (Introducción al desarrollo para Project 2010). 
> - Para obtener más información acerca del uso de los registros del ULS, vea el artículo del blog de soporte técnico de Project titulado [Project Server 2010: What to Expect when you get the Unexpected](https://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx) (Project Server 2010: Qué esperar cuando ocurre lo inesperado) y busque en el blog “reading ULS logs” (lectura de registros del ULS). 
> - Para buscar o controlar problemas específicos en los datos del ULS, use el [Visor del ULS](https://www.codeproject.com/Articles/458052/ULS-Log-Viewer). 
> - Use Microsoft SQL Server Profiler para detectar o supervisar errores de la base de datos. Para obtener más información, vea [SQL Server Profiler](https://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx). 
> - Muchos de los códigos de error solo se usan internamente. Por ejemplo, como los servicios web **ExchangeSync** y **PWA** no se pueden usar para el desarrollo de terceros, no es probable que vea los códigos de error de métodos de esas áreas, como, por ejemplo, los métodos **Rules** y **StatusReports**. Sin embargo, las tablas de este artículo incluyen todos los códigos de error de Project Server con la pretensión de ser exhaustivas. 
  
## <a name="table-1-error-code-functional-areas-and-related-number-ranges"></a>Tabla 1. Áreas funcionales de los códigos de error con los intervalos de números correspondientes

|Área funcional de Project Server|Intervalos de números de los códigos de error|
|:-----|:-----|
|[Tabla 3: Códigos de error generales](#pj15_ErrorCodes_General) <br/> |0 - 99; 500 - 999; 9131; 10000 - 10099; 20000 - 20099; 26000 - 26099  <br/> |
|[Tabla 4: Caché activa](#pj15_ErrorCodes_ActiveCache) <br/> |12000 - 12099  <br/> |
|[Tabla 5: Sincronización de Active Directory](#pj15_ErrorCodes_ActiveDirectory) <br/> |27000 - 27999  <br/> |
|[Tabla 6: Servicio web de administración](#pj15_ErrorCodes_Admin) <br/> |16600 - 16699; 19011, 19012 y 19032; 20003 y 25000 - 25099  <br/> |
|[Tabla 7: Archivo (copia de seguridad y restauración)](#pj15_ErrorCodes_Archive) <br/> |25000 - 25999 y 29000 - 29099  <br/> |
|[Tabla 8: Asignaciones](#pj15_ErrorCodes_Assignments) <br/> |120 - 199  <br/> |
|[Tabla 9: Calendario](#pj15_ErrorCodes_Calendar) <br/> |77 y 13000 - 13999  <br/> |
|[Tabla 10: Cube Build Service (CBS)](#pj15_ErrorCodes_CBS) <br/> |17000 - 17999  <br/> |
|[Tabla 11: Protección y desprotección](#pj15_ErrorCodes_CICO) <br/> |10100 - 10199  <br/> |
|[Tabla 12: Campos personalizados](#pj15_ErrorCodes_CustomFields) <br/> |11500 - 11999  <br/> |
|[Tabla 13: Tablas de búsqueda](#pj15_ErrorCodes_LookupTables) <br/> |11000 - 11499  <br/> |
|[Tabla 14: Miscelánea](#pj15_ErrorCodes_Miscellaneous) <br/> |11000 - 11499  <br/> |
|[Tabla 15: Notificaciones](#pj15_ErrorCodes_Notifications) <br/> |16000 - 16599  <br/> |
|[Tabla 16: Optimizador](#pj15_ErrorCodes_Optimizer) (análisis de la cartera de proyectos)  <br/> |29000 - 29999  <br/> |
|[Tabla 17: Planner](#pj15_ErrorCodes_Planner) (análisis de la cartera de proyectos)  <br/> |28000 - 28999  <br/> |
|[Tabla 18: Proyectos](#pj15_ErrorCodes_Projects) <br/> |100 - 499; 1000 - 1199; 9100 - 9199 y 23000 - 23999  <br/> |
|[Tabla 19: Servicio de datos de informes](#pj15_ErrorCodes_RDS) (RDS)  <br/> |24000 - 24999  <br/> |
|[Tabla 20: Recursos](#pj15_ErrorCodes_Resources) <br/> |2000 - 2999  <br/> |
|[Tabla 21: Planeamiento de recursos](#pj15_ErrorCodes_ResourcePlans) <br/> |30000 - 30999  <br/> |
|[Tabla 22: Reglas](#pj15_ErrorCodes_Rules) <br/> |21000 - 21099  <br/> |
|[Tabla 23: Seguridad](#pj15_ErrorCodes_Security) <br/> |19000 - 19099  <br/> |
|[Tabla 24: Eventos de servidor](#pj15_ErrorCodes_Events) <br/> |19033 y 22000 - 22999  <br/> |
|[Tabla 25: Estado](#pj15_ErrorCodes_Statusing) <br/> |3100 - 3199  <br/> |
|[tabla 26: Informes de estado](#pj15_ErrorCodes_StatusReports) <br/> |12100 - 12299  <br/> |
|[Tabla 27: Tareas](#pj15_ErrorCodes_Tasks) <br/> |7000 - 7099  <br/> |
|[Tabla 28: Partes de horas](#pj15_ErrorCodes_Timesheets) <br/> |3200 - 3299  <br/> |
|[Tabla 29: Delegación de usuarios](#pj15_ErrorCodes_UserDelegation) <br/> |43000 - 43500  <br/> |
|[Tabla 30: Flujo de trabajo](#pj15_ErrorCodes_Workflow) <br/> |35000 - 35999: Flujo de trabajo  <br/> |
|[Tabla 31: Códigos de error de WssInterop y ObjectLinkProvider (integración de SharePoint)](#pj15_ErrorCodes_WSS) <br/> |16400 - 16499: Áreas de trabajo de proyectos e integración de SharePoint  <br/> 18000 - 18099: Proveedor de vínculos a objetos e importación de proyectos de SharePoint  <br/> |
   
## <a name="table-2-error-code-table-by-number-range"></a>Tabla 2. Tabla de códigos de error ordenados por el intervalo de números

|Intervalo de códigos de error|Tabla de códigos de error|
|:-----|:-----|
|0 - 99  <br/> |[Tabla 3: Códigos de error generales](#pj15_ErrorCodes_General), excepto 77 que está en la [Tabla 9: Calendario](#pj15_ErrorCodes_Calendar) <br/> |
|100 - 119  <br/> |[Tabla 18: Proyectos](#pj15_ErrorCodes_Projects) <br/> |
|120 - 199  <br/> |[Tabla 8: Asignaciones](#pj15_ErrorCodes_Assignments) <br/> |
|500 - 999  <br/> |[Tabla 3: Códigos de error generales](#pj15_ErrorCodes_General) <br/> |
|1000 - 1199  <br/> |[Tabla 18: Proyectos](#pj15_ErrorCodes_Projects) <br/> |
|2000 - 2999  <br/> |[Tabla 20: Recursos](#pj15_ErrorCodes_Resources) <br/> |
|3100 - 3199  <br/> |[Tabla 25: Estado](#pj15_ErrorCodes_Statusing) <br/> |
|3200 - 3299  <br/> |[Tabla 28: Partes de horas](#pj15_ErrorCodes_Timesheets) <br/> |
|7000 - 7099  <br/> |[Tabla 27: Tareas](#pj15_ErrorCodes_Tasks) <br/> |
|9100 - 9199  <br/> |[Tabla 18: Proyectos](#pj15_ErrorCodes_Projects), excepto 9131 que está en la [Tabla 3: Códigos de error generales](#pj15_ErrorCodes_General) <br/> |
|10000 - 10099  <br/> |[Tabla 3: Códigos de error generales](#pj15_ErrorCodes_General) <br/> |
|10100 - 10199  <br/> |[Tabla 11: Protección y desprotección](#pj15_ErrorCodes_CICO) <br/> |
|11000 - 11499  <br/> |[Tabla 13: Tablas de búsqueda](#pj15_ErrorCodes_LookupTables) <br/> |
|11500 - 11999  <br/> |[Tabla 12: Campos personalizados](#pj15_ErrorCodes_CustomFields) <br/> |
|12000 - 12099  <br/> |[Tabla 4: Caché activa](#pj15_ErrorCodes_ActiveCache) <br/> |
|12100 - 12299  <br/> |[tabla 26: Informes de estado](#pj15_ErrorCodes_StatusReports) <br/> |
|13000 - 13999  <br/> |[Tabla 9: Calendario](#pj15_ErrorCodes_Calendar) <br/> |
|16000 - 16399  <br/> |[Tabla 15: Notificaciones](#pj15_ErrorCodes_Notifications) <br/> |
|16400 - 16499  <br/> |[Tabla 31: Códigos de error de WssInterop y Object Link Provider (integración de SharePoint)](#pj15_ErrorCodes_WSS) <br/> |
|16600 - 16699  <br/> |[Tabla 6: Servicio web de administración](#pj15_ErrorCodes_Admin) <br/> |
|17000 - 17999  <br/> |[Tabla 10: Cube Build Service (CBS)](#pj15_ErrorCodes_CBS) <br/> |
|18000 - 18099  <br/> |[Tabla 31: Integración de SharePoint](#pj15_ErrorCodes_WSS) <br/> |
|19000 - 19099  <br/> |[Tabla 23: Seguridad](#pj15_ErrorCodes_Security), excepto 19011, 19012 y 19032 que son códigos relacionados con la seguridad y están en la [Tabla 6: Servicio web de administración](#pj15_ErrorCodes_Admin) <br/> |
|20000 - 20099  <br/> |[Tabla 3: Códigos de error generales](#pj15_ErrorCodes_General), excepto 20003 que está en la [Tabla 6: Servicio web de administración](#pj15_ErrorCodes_Admin) <br/> |
|21000 - 21099  <br/> |[Tabla 22: Reglas](#pj15_ErrorCodes_Rules) <br/> |
|22000 - 22999  <br/> |[Tabla 24: Eventos de servidor](#pj15_ErrorCodes_Events) <br/> |
|23000 - 23999  <br/> |[Tabla 18: Proyectos](#pj15_ErrorCodes_Projects) <br/> |
|24000 - 24999  <br/> |[Tabla 19: Servicio de datos de informes](#pj15_ErrorCodes_RDS) (RDS)  <br/> |
|25000 - 25999  <br/> |[Tabla 7: Archivo (copia de seguridad y restauración)](#pj15_ErrorCodes_Archive), excepto 25004 y 25006 que están en la [Tabla 6: Servicio web de administración](#pj15_ErrorCodes_Admin) <br/> |
|26000 - 26099  <br/> |[Tabla 3: Códigos de error generales](#pj15_ErrorCodes_General) <br/> |
|27000 - 27999  <br/> |[Tabla 5: Sincronización de Active Directory](#pj15_ErrorCodes_ActiveDirectory) <br/> |
|28000 - 28999  <br/> |[Tabla 17: Planner](#pj15_ErrorCodes_Planner) (análisis de la cartera de proyectos)  <br/> |
|29000 - 29999  <br/> |[Tabla 16: Optimizador](#pj15_ErrorCodes_Optimizer) (análisis de la cartera de Project), excepto 29021 que está en la [Tabla 7: Archivo](#pj15_ErrorCodes_Archive) <br/> |
|30000 - 30999  <br/> |[Tabla 21: Planeamiento de recursos](#pj15_ErrorCodes_ResourcePlans) <br/> |
|31000 - 31999  <br/> 32000 - 32100  <br/> |[Tabla 14: Miscelánea](#pj15_ErrorCodes_Miscellaneous) (Auditoría; no se usa)  <br/> Páginas de detalles del proyecto  <br/> |
|35000 - 35999  <br/> 40000 - 40499  <br/> |[Tabla 30: Flujo de trabajo](#pj15_ErrorCodes_Workflow) <br/> |
|40500 - 40999  <br/> 42000 - 42999  <br/> |[Tabla 14: Miscelánea](#pj15_ErrorCodes_Miscellaneous) (**ExchangeSync**; use interno)  <br/> Escala de tiempo de Project Web App  <br/> |
|43000 - 43500  <br/> |[Tabla 29: Delegación de usuarios](#pj15_ErrorCodes_UserDelegation) <br/> |
|50000 - 51999  <br/> |[Tabla 14: Miscelánea](#pj15_ErrorCodes_Miscellaneous) (errores de la base de datos)  <br/> |

<a name="pj15_ErrorCodes_General"></a>

## <a name="table-3-general-error-codes"></a>Tabla 3: Códigos de error generales

|Código de error general|Descripción|
|:-----|:-----|
|NoError = 0; Success = 0  <br/> |No ha habido errores ni acciones realizadas correctamente.  <br/> |
|GeneralRequestInvalidParameter = 6  <br/> |Uno de los nodos o de los parámetros de la solicitud no es válido o no es válido en el contexto de la solicitud.  <br/> |
|GeneralInvalidValue = 11  <br/> |El valor de la solicitud no es válido. Por ejemplo, cuando se especifica 0 para un GUID.  <br/> |
|GeneralStartDateGTorEQFinishDate = 26  <br/> |El intervalo de fechas especificado no es válido.  <br/> |
|GeneralQueueOperationInProcess = 29  <br/> |Error genérico para una operación que sigue en procesamiento en la cola.  <br/> |
|GeneralUnhandledException = 42  <br/> |Se ha producido una excepción no controlada.  <br/> |
|GeneralDuplicateGUIDSpecified = 66  <br/> |Hay un GUID duplicado en la solicitud.  <br/> |
|GeneralDateNotValid = 69  <br/> |Las fechas deben estar incluidas en el intervalo de 1/1/1984 a 12/12/2049.  <br/> |
|GeneralCostInvalid = 70  <br/> |Un parámetro de costo no es válido.  <br/> |
|GeneralWorkInvalid = 71  <br/> |Un parámetro de trabajo no es válido.  <br/> |
|GeneralDurationInvalid = 72  <br/> |Un parámetro de duración no es válido.  <br/> |
|GeneralUnitsInvalid = 73  <br/> |La unidad especificada no es válida.  <br/> |
|GeneralOnlyInsertsAllowed = 74  <br/> |Solo se permiten las inserciones.  <br/> |
|GeneralOnlyUpdatesAllowed = 75  <br/> |Solo se permiten las actualizaciones.  <br/> |
|GeneralSessionInvalid = 76  <br/> |El parámetro de sesión no es válido.  <br/> |
|GeneralDependencyUidInvalid = 78  <br/> |El GUID de dependencia no es válido.  <br/> |
|GeneralNumberInvalid = 79  <br/> |Un número no es válido.  <br/> |
|GeneralInvalidDataStore = 80  <br/> |No existe la base de datos especificada. Use una base de datos en [DataStoreEnum](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.DataStoreEnum.aspx).  <br/> |
|GeneralDurationOrWorkFormatInvalid = 513  <br/> |La duración o el formato de trabajo no son válidos.  <br/> |
|GeneralRateFormatInvalid = 518  <br/> |El formato de tasa no es válido.  <br/> |
|GeneralQueueException = 9131  <br/> |Excepción: Hay un error general en los Servicios en cola.  <br/> |
|GeneralItemDoesNotExist = 10000  <br/> |Un elemento especificado no existe.  <br/> |
|GeneralLCIDInvalid = 10001  <br/> |El identificador de configuración regional (Id. de idioma) no es válido.  <br/> |
|GeneralRowDoesNotExist = 10002  <br/> |No existe la fila especificada en una tabla **DataTable**.  <br/> |
|GeneralInvalidColumnValue = 20000  <br/> |El valor de una columna en una tabla **DataTable** no es válido.  <br/> |
|GeneralInvalidDataRowState = 20001  <br/> |Un estado de **DataRow** no es válido.  <br/> |
|GeneralDuplicatedNames = 20004  <br/> |Hay un nombre duplicado. Los nombres deben ser únicos.  <br/> |
|GeneralReadOnlyColumn = 20005  <br/> |La columna es de solo lectura.  <br/> |
|GeneralReadOnlyRow = 20006  <br/> |La fila es de solo lectura.  <br/> |
|GeneralNotNullColumn = 20007  <br/> |La columna no puede ser nula.  <br/> |
|GeneralObjectAlreadyExists = 20008  <br/> |El objeto ya existe.  <br/> |
|GeneralInvalidObject = 20009  <br/> |El objeto no es válido.  <br/> |
|GeneralSecurityAccessDenied = 20010  <br/> |Se ha denegado el acceso a causa de los permisos de seguridad.  <br/> |
|GeneralInvalidOperation = 20011  <br/> |La operación no es válida.  <br/> |
|GeneralInvalidCharacters = 20012  <br/> |Algunos caracteres no son válidos. Además del carácter de tabulación, los siguientes caracteres no son válidos para un nombre de proyecto: `\ / " : ; < > | , . ' ? * #` <br/> |
|GeneralNameTooLong = 20013  <br/> |El nombre es demasiado largo.  <br/> |
|GeneralNameCannotBeBlank = 20014  <br/> |El nombre no puede estar en blanco. No use una cadena nula ni lo deje en blanco.  <br/> |
|GeneralInvalidOperationOnReadOnlyValue = 20016  <br/> |La operación intentada en un valor de solo lectura no es válida.  <br/> |
|GeneralInvalidDateOverlap = 20018  <br/> |La solicitud contiene fechas solapadas.  <br/> |
|GeneralParameterCannotBeNull = 20020  <br/> |El parámetro no puede ser nulo.  <br/> |
|GeneralDescTooLong = 20021  <br/> |La descripción es demasiado larga.  <br/> |
|GeneralCategoryPermissionDenied = 20022  <br/> |El permiso de categoría ha sido denegado.  <br/> |
|GeneralNotLicensed = 20024  <br/> |El usuario no tiene licencia para Project Server.  <br/> |
|GeneralGlobalPermissionDenied = 20023  <br/> |El permiso global ha sido denegado.  <br/> |
|GeneralActionCanceledByEventHandler = 22000  <br/> |El controlador de eventos canceló la acción.  <br/> |
|GeneralActionCanceledBecauseServerEventServiceNotFound = 22001  <br/> |No se encontró el Servicio de eventos de Project Server.  <br/> |
|GeneralActionCanceledBecauseServerEventServiceProblem = 22002  <br/> |Se ha producido un problema en el Servicio de eventos de Project Server.  <br/> |
|GeneralQueueJobFailed = 26000  <br/> |Error en el trabajo en cola.  <br/> |
|GeneralQueueInvalidJobUID = 26001  <br/> |El GUID de trabajo en cola no es válido.  <br/> |
|GeneralQueueInvalidTrackingUID = 26002  <br/> |El GUID de seguimiento de la cola no es válido.  <br/> |
|GeneralQueueInvalidJobInfoUID = 26003  <br/> |El GUID de información del trabajo en cola no es válido.  <br/> |
|GeneralQueueInvalidCorrelationUID = 26004  <br/> |El GUID de correlación de la cola no es válido.  <br/> |
|GeneralQueueCorrelationBlocked = 26005  <br/> |La correlación de la cola está bloqueada.  <br/> |
|GeneralQueueInvalidMessageType = 26006  <br/> |El tipo de mensaje en cola no es válido.  <br/> |
|GeneralQueueInvalidJobState = 26007  <br/> |El estado del trabajo en cola no es válido.  <br/> |
|GeneralQueueInvalidGroupState = 26008  <br/> |El estado de grupo en la cola no es válido.  <br/> |
|GeneralQueueInvalidGroupPriority = 26009  <br/> |La prioridad del grupo en la cola no es válida.  <br/> |
|GeneralQueueInvalidCorrelationPriority = 26010  <br/> |La prioridad de correlación en la cola no es válida.  <br/> |
|GeneralQueueInvalidQueueID = 26011  <br/> |El número de identificación de la cola no es válido.  <br/> |
|GeneralQueueInvalidAdminAction = 26012  <br/> |La acción **Admin** no es válida para la cola.  <br/> |
|GeneralQueueInvalidStatType = 26013  <br/> |El tipo de estado de cola no es válido.  <br/> |
|GeneralQueueInvalidBlockPolicy = 26014  <br/> |La directiva de bloqueo de la cola no es válida.  <br/> |
|GeneralQueueCannotRetryJob = 26015  <br/> |La cola no puede reintentar el trabajo.  <br/> |
|GeneralQueueInvalidSetting = 26016  <br/> |Una de las opciones de configuración de la cola no es válida.  <br/> |
|GeneralQueueInvalidRendezvousUID = 26017  <br/> |El GUID de encuentro en cola no es válido.  <br/> |
|GeneralDalErrorGettingConnectionStrings = 26018  <br/> |Error al obtener las cadenas de conexión para el nivel de acceso a datos (DAL).  <br/> |
|GeneralDalErrorConnectingToDatabase = 26019  <br/> |Error en el DAL al conectar con la base de datos.  <br/> |
|GeneralDalInvalidArgumentCountCreatingFilter = 26020  <br/> |El número de argumentos para crear un filtro no es válido.  <br/> |
|GeneralDataTableCannotBeNull = 26024  <br/> |Una tabla **DataTable** no puede tener un valor **null**.  <br/> |
|GeneralDatasetConstraints = 26025  <br/> |Error en las restricciones de **DataSet**.  <br/> |
|GeneralInvalidDataSetStructure = 26027  <br/> |La estructura de **DataSet** no es válida.  <br/> |
|GeneralDalNoRowsUpdated = 26028  <br/> |No se ha actualizado ninguna fila en el nivel de acceso a datos (DAL).  <br/> |
|GeneralDataTableCannotBeEmpty = 26029  <br/> |La tabla **DataTable** no puede estar vacía.  <br/> |
|GeneralWSSContentDBNotWritable = 26030  <br/> |No se puede escribir en la base de datos de contenido de SharePoint. Puede que la base de datos de contenido sea de solo lectura o que se haya bloqueado en el nivel de colección de sitios.  <br/> |
|GeneralSPValidateFormDigestError = 26031  <br/> |Error al validar la síntesis de formulario en una devolución de llamada de Project Web App, normalmente por haber excedido el tiempo de espera.  <br/> |
|GeneralDelegationActiveForCurrentUser = 26032  <br/> |El usuario actual tiene una delegación activa. Este error lo provocan métodos web en el servicio **WinProj** para Project Profesional.<br/> |

<a name="pj15_ErrorCodes_ActiveCache"></a>

## <a name="table-4-active-cache"></a>Tabla 4. Caché activa

|Código de error de la caché activa|Descripción|
|:-----|:-----|
|ActiveCacheInvalidDataFormat = 12000  <br/> |El formato de los datos no es válido.  <br/> |
|ActiveCacheUnsupportedDataFormatVersion = 12001  <br/> |La versión del formato de datos no es compatible.  <br/> |
|ActiveCacheInvalidQueuedMessageType = 12003  <br/> |El tipo de mensaje en cola no es válido.  <br/> |
|ActiveCacheNullQueuedMessage = 12004  <br/> |El mensaje en cola es nulo.  <br/> |
|ActiveCacheQueuedMessageExecutionError = 12005  <br/> |Se ha producido un error de ejecución para el mensaje en cola.  <br/> |
|ActiveCacheInvalidDataSize = 12006  <br/> |El tamaño de los datos no es válido.  <br/> |
|ActiveCacheQueueJobAlreadyStarted = 12007  <br/> |El trabajo en cola ya se ha iniciado.  <br/> |
|ActiveCacheInvalidQueuedMessageFormat = 12008  <br/> |El formato del mensaje en cola no es válido.  <br/> |
|ActiveCacheUnsupportedQueuedMessageVersion = 12009  <br/> |La versión del mensaje en cola no es válida.  <br/> |
|ActiveCacheUnsupportedQueueDataType = 12011  <br/> |El tipo de datos en cola no es compatible.  <br/> |
|ActiveCacheInvalidVersionStampForSave = 12012  <br/> |La marca de versión de la operación de guardado no es válida.  <br/> |
|ActiveCacheProjectTypeMismatch = 12013  <br/> |El tipo de proyecto no coincide con el tipo esperado.  <br/> |
|ActiveCacheDataValidationFailed = 12014  <br/> |Error al validar los datos.  <br/> |
|ActiveCacheUnsupportedProjectProfessionalVersion = 12015  <br/> |La versión de Project Professional no es compatible.  <br/> |
|ActiveCacheGeneralSQLException = 12016  <br/> |Hay un error general de SQL.  <br/> |

<a name="pj15_ErrorCodes_ActiveDirectory"></a>

## <a name="table-5-active-directory-synchronization"></a>Tabla 5. Sincronización de Active Directory

|Código de error de la sincronización de Active Directory|Descripción|
|:-----|:-----|
|AdSyncUpdateTimerJobFailed = 27002  <br/> |Error en el trabajo del temporizador de actualización para la sincronización con los servicios de directorio de Active Directory.  <br/> |
|AdSyncDeleteTimerJobFailed = 27003  <br/> |Error en el trabajo del temporizador de eliminación para la sincronización con Active Directory.  <br/> |
|AdSyncAdConnectFail = 27006  <br/> |No se puede conectar con Active Directory.  <br/> |
|AdMaximumGroupsCountExceeded = 27007  <br/> |Se ha excedido el número máximo de grupos.  <br/> |
|SRAInvalidVersion = 27300  <br/> |Versión de SRA no válida.  <br/> |
|SRADelayedUpgradeFailed = 27301  <br/> |Error en la acción de actualización asíncrona de SRA.  <br/> |
|(27000 - 27999)  <br/> |Otros errores de sincronización de Active Directory no se enumeran en Project Server.  <br/> |

<a name="pj15_ErrorCodes_Admin"></a>

## <a name="table-6-admin-web-service"></a>Tabla 6. Servicio web de administración

|Códigos de error del servicio web de administración|Descripción|
|:-----|:-----|
|AdminViewNameAlreadyExists = 16600  <br/> |El nombre de la vista ya existe. Los nombres deben ser únicos.  <br/> |
|AdminViewInvalidDividerPosition = 16601  <br/> |La posición del divisor no es válida.  <br/> |
|AdminViewDataWasTampered = 16602  <br/> |Los datos han sido modificados.  <br/> |
|AdminViewMaxDisplayedFieldsNumberExceeded = 16603  <br/> |La visualización excede el número máximo de campos.  <br/> |
|AdminViewCannotDeleteDefaultView = 16604  <br/> |No se puede eliminar la vista predeterminada.  <br/> |
|AdminViewCannotCopyDefaultView = 16605  <br/> |No se puede copiar la vista predeterminada.  <br/> |
|AdminLocalCustomFieldInvalid = 19011  <br/> |El campo personalizado local no es válido.  <br/> |
|AdminEnterpriseCustomFieldInvalid = 19012  <br/> |El campo personalizado de empresa no es válido.  <br/> |
|AdminNTAccountNotFound = 19032  <br/> |No se ha encontrado la cuenta de Windows (NTLM).  <br/> |
|AdminUnableToMerge = 20003  <br/> |No se pueden combinar los datos.  <br/> |
|AdminDeleteArchivedProjectsFailed = 25004  <br/> |Error en la operación de eliminación de proyectos archivados.  <br/> |
|AdminUpdateArchiveScheduleFailed = 25006  <br/> |No se pudo actualizar la programación de archivo.  <br/> |
|AdminArchiveScheduleFailed = 28018  <br/> |Error en la programación de archivo.  <br/> |
|AdminReadArchivedProjectsListFailed = 28019  <br/> |No se pudo leer la lista de proyectos archivados.  <br/> |
|AdminReadArchiveScheduleFailed = 28020  <br/> |No se pudo leer la programación de archivo.  <br/> |
|AdminUserAccountNameNull = 28021  <br/> |El nombre de la cuenta de usuario es nulo.  <br/> |
|AdminIsWindowsUserNull = 28022  <br/> |La cuenta de usuario de Windows (NTLM) parece nula.  <br/> |
|AdminInvalidTimePeriodState = 28023  <br/> |El estado de timeperiod no es válido.  <br/> |
|AdminGlobalUpdateFailed = 28024  <br/> |Error en la actualización de la información global de la empresa durante la llamada a **SetServerCurrency**.  <br/> |
|AdminGlobalCheckedOut = 28025  <br/> |La plantilla de la información global de la empresa ya está desprotegida durante la llamada a **SetServerCurrency**.  <br/> |
|AdminInvalidDatabaseTimeout = 28026  <br/> |Se ha excedido el tiempo de espera porque una base de datos no es válida.  <br/> |
|AdminInvalidDatabaseTimeoutType = 28027  <br/> |Se ha excedido el tiempo de espera porque un tipo de base de datos no es válido.  <br/> |
|AdminInvalidEntityType = 28028  <br/> |El tipo de entidad no es válido. Vea [EntityCollection](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.aspx).  <br/> |
|AdminInvalidCompatibilityModeChange = 28029  <br/> |El cambio al modo de compatibilidad no es válido.  <br/> |
|AdminInvalidCompatibilityMode = 28030  <br/> |El modo de compatibilidad no es válido.  <br/> |
|AdminInvalidProjectProfessionalVersions = 28031  <br/> |El conjunto de versiones de Project Professional no es válido.  <br/> |
|AdminInvalidProjectProfessionalVersion = 28032  <br/> |La versión de Project Professional no es válida.  <br/> |
|AdminTooManyProjectProfessionalVersions = 28033  <br/> |Se han especificado demasiadas versiones de Project Professional.  <br/> |
|AdminDuplicateProjectProfessionalMajorVersions = 28034  <br/> |Hay duplicados en las versiones principales de Project Professional. Solo puede especificar una versión para cada versión principal a partir de Project Professional 2007.  <br/> |
|AdminInvalidServerFlags = 28035  <br/> |Al menos una marca de la configuración de Project Server no es válida.  <br/> |
|AdminNullProjectProfessionalVersions = 28036  <br/> |Una o varias versiones de Project Profesional son nulas.  <br/> |

<a name="pj15_ErrorCodes_Archive"></a>

## <a name="table-7-archive-web-service"></a>Tabla 7. Servicio web de archivo

|Código de error del servicio web de archivo (copia de seguridad y restauración)|Descripción|
|:-----|:-----|
|ArchiveProjectFailure = 25000  <br/> |Error en la operación de archivo del proyecto.  <br/> |
|ArchiveProjectsFailed = 25001  <br/> |No se puede guardar ninguno de los proyectos en la base de datos de archivo.  <br/> |
|ArchiveProjectFailed = 25002  <br/> |No se puede guardar el archivo del proyecto.  <br/> |
|RestoreProjectFailed = 25003  <br/> |No se puede restaurar el proyecto.  <br/> |
|ArchiveResourcesFailed = 25007  <br/> |No se puede guardar el archivo de recursos.  <br/> |
|ArchiveCustomFieldsFailed = 25008  <br/> |No se puede guardar el archivo de campos personalizados.  <br/> |
|RestoreCustomFieldsFailed = 25009  <br/> |No se pueden restaurar los campos personalizados.  <br/> |
|ArchiveSystemSettingsFailed = 25010  <br/> |No se puede guardar el archivo de configuración del sistema.  <br/> |
|RestoreSystemSettingsFailed = 25011  <br/> |No se puede restaurar la configuración del sistema.  <br/> |
|ArchiveCategoriesFailed = 25012  <br/> |No se puede guardar el archivo de categorías de seguridad.  <br/> |
|RestoreCategoriesFailed = 25013  <br/> |No se pueden restaurar las categorías de seguridad.  <br/> |
|ArchiveViewsFailed = 25014  <br/> |No se puede guardar el archivo de vistas.  <br/> |
|RestoreViewsFailed = 25015  <br/> |No se pueden restaurar las vistas.  <br/> |
|ArchiveGlobalProjectFailed = 25016  <br/> |No se puede guardar el archivo global de empresa.  <br/> |
|RestoreGlobalProjectFailed = 25017  <br/> |No se puede restaurar la plantilla global de empresa.  <br/> |
|ArchiveInvalidRetentionPolicyValue = 25018  <br/> |El valor de la directiva de retención del archivo no es válido.  <br/> |
|ArchiveCustomFieldsFailure = 25019  <br/> |No se puede leer el archivo de campos personalizados.  <br/> |
|ArchiveGlobalProjectFailure = 25020  <br/> |No se puede leer el archivo global de empresa.  <br/> |
|ArchiveResourcesFailure = 25021  <br/> |No se puede leer el archivo de recursos.  <br/> |
|ArchiveSystemSettingsFailure = 25022  <br/> |No se puede leer el archivo de configuración del sistema.  <br/> |
|ArchiveViewsFailure = 25023  <br/> |No se puede leer el archivo de vistas.  <br/> |
|ArchiveCategoriesFailure = 25024  <br/> |No se puede leer el archivo de categorías de seguridad.  <br/> |
|ResourcePlanPublishFailure = 25025  <br/> |No se puede publicar el plan de recursos.  <br/> |
|RestoreCategoriesFailure = 25026  <br/> |No se pueden restaurar las categorías de seguridad desde el archivo.  <br/> |
|RestoreCustomFieldsFailure = 25027  <br/> |No se pueden restaurar los campos personalizados desde el archivo.  <br/> |
|RestoreGlobalProjectFailure = 25028  <br/> |No se puede restaurar la plantilla global de empresa desde el archivo.  <br/> |
|RestoreProjectFailure = 25029  <br/> |No se puede restaurar el proyecto desde el archivo.  <br/> |
|RestoreResourcesFailure = 25030  <br/> |No se pueden restaurar los recursos desde el archivo.  <br/> |
|RestoreSystemSettingsFailure = 25031  <br/> |No se puede restaurar la configuración del sistema desde el archivo.  <br/> |
|RestoreViewsFailure = 25032  <br/> |No se pueden restaurar las vistas desde el archivo.  <br/> |
|ArchiveReadProjectArchiveRetentionSettingFailed = 25033  <br/> |No se pudo leer la configuración de retención del archivo de proyectos.  <br/> |
|RestoreResourcesFailed = 29021  <br/> |No se pueden restaurar los recursos.  <br/> |

<a name="pj15_ErrorCodes_Assignments"></a>

## <a name="table-8-assignment"></a>Tabla 8. Asignación

|Código de error de la asignación|Descripción|
|:-----|:-----|
|AssignmentNotFound = 120  <br/> |No se encontró la asignación.  <br/> |
|AssignmentWrongTrackingMethod = 122  <br/> |El método de seguimiento de la asignación es incorrecto.  <br/> |
|AssignmentWorkTypeInvalid = 127  <br/> |El tipo de trabajo de asignación no es válido.  <br/> |
|AssignmentRateTableInvalid = 130  <br/> |La tabla de tasa para la asignación no es válida.  <br/> |
|AssignmentAlreadyExists = 131  <br/> |La asignación ya existe.  <br/> |
|AssignmentDuplicateSpecified = 132  <br/> |Hay una asignación duplicada.  <br/> |
|AssignmentUidInvalid = 133  <br/> |El GUID de la asignación no es válido.  <br/> |
|AssignmentDelayInvalid = 134  <br/> |El retraso de la asignación no es válido.  <br/> |
|AssignmentCannotEditSummaryTask = 135  <br/> |No se puede editar la tarea de resumen de las asignaciones.  <br/> |
|AssignmentInvalid = 136  <br/> |La asignación no es válida.  <br/> |
|AssignmentFieldsInvalidForBudget = 137  <br/> |Los campos de la asignación no son válidos para el presupuesto.  <br/> |
|AssignmentAlreadyAssignedToResource = 138  <br/> |El recurso ya tenía la asignación.  <br/> |
|AssignmentInvalidOwner = 139  <br/> |El propietario de la asignación no es válido.  <br/> |

<a name="pj15_ErrorCodes_Calendar"></a>

## <a name="table-9-calendar"></a>Tabla 9. Calendario

|Código de error del calendario|Descripción|
|:-----|:-----|
|CalendarUidInvalid = 77  <br/> |El GUID del calendario no es válido.  <br/> |
|CalendarOnlyOneShiftIsNull = 13000  <br/> |Solo un turno es nulo.  <br/> |
|CalendarRecurrenceDaysShouldBeNull = 13001  <br/> |Los días de periodicidad deben ser nulos.  <br/> |
|CalendarRecurrenceMonthDayShouldBeNull = 13002  <br/> |El mes y el día de periodicidad deben ser nulos.  <br/> |
|CalendarRecurrenceMonthShouldBeNull = 13003  <br/> |El mes de periodicidad debe ser nulo.  <br/> |
|CalendarRecurrenceMonthShouldNotBeNull = 13004  <br/> |El mes de periodicidad no debe ser nulo.  <br/> |
|CalendarRecurrencePositionShouldBeNull = 13005  <br/> |La posición de periodicidad debe ser nula.  <br/> |
|CalendarRecurrencePositionShouldNotBeNull = 13006  <br/> |La posición de periodicidad no debe ser nula.  <br/> |
|CalendarRecurrenceDaysShouldNotBeNull = 13007  <br/> |Los días de periodicidad no deben ser nulos.  <br/> |
|CalendarInvalidRecurrenceFrequency = 13008  <br/> |La frecuencia de periodicidad no es válida.  <br/> |
|CalendarInvalidRecurrenceType = 13009  <br/> |El tipo de periodicidad no es válido.  <br/> |
|CalendarInvalidRecurrenceDays = 13010  <br/> |Los días de periodicidad no son válidos.  <br/> |
|CalendarInvalidCombinationOfMonthDayAndPosition = 13011  <br/> |La combinación de mes, día y posición no es válida.  <br/> |
|CalendarInvalidRecurrencePosition = 13012  <br/> |La posición de periodicidad no es válida.  <br/> |
|CalendarCannotModifyExceptionsForCalendarBeingDeleted = 13013  <br/> |Las excepciones de calendario no se pueden modificar cuando se está eliminando un calendario.  <br/> |
|CalendarExceptionConflict = 13014  <br/> |Hay un conflicto en las excepciones del calendario.  <br/> |
|CalendarBadDateValue = 13015  <br/> |La fecha no es válida.  <br/> |
|CalendarNotFound = 13021  <br/> |No se encontró el calendario.  <br/> |
|CalendarAlreadyExists = 13022  <br/> |El calendario ya existe.  <br/> |
|CalendarNameShouldNotBeNull = 13023  <br/> |El nombre del calendario es nulo.  <br/> |
|CalendarInternalError = 13025  <br/> |Hay un error interno en la operación de calendario.  <br/> |
|CalendarNameTooLong = 13027  <br/> |El nombre del calendario es demasiado largo.  <br/> |
|CalendarInvalidCalendarName = 13028  <br/> |El nombre del calendario no es válido.  <br/> |
|CalendarStandardCalendarNotFound = 13031  <br/> |No se encontró el calendario estándar.  <br/> |
|CalendarInvalidShifts = 13032  <br/> |Los turnos no son válidos.  <br/> |
|CalendarCannotDeleteCalendarUsedByProject = 13033  <br/> |No se puede eliminar un calendario que se está usando en un proyecto.  <br/> |
|CalCalendarUniqueIdToDuplicateShouldBeNull = 13035  <br/> |El GUID debe ser nulo para duplicar un calendario.  <br/> |
|CalendarInvalidBaseCalendarUniqueId = 13037  <br/> |El GUID del calendario base no es válido.  <br/> |
|CalendarInvalidUniqueIdToDuplicate = 13038  <br/> |El GUID no es válido para duplicar un calendario.  <br/> |
|CalendarUnusedCalendarException = 13039  <br/> |La excepción de calendario no tiene un calendario correspondiente. Ocurre cuando se usa el método **UpdateResources** si hay una entrada en la tabla **ResourceDataSet.CalendarExceptions**, pero no hay ningún **BaseCalendarUniqueId** para ese recurso en la tabla **Resources**.<br/> |
|CalendarCannotDeleteStandardCalendar = 13040  <br/> |El calendario estándar no se puede eliminar.  <br/> |
|CalendarCannotRenameStandardCalendar = 13041  <br/> |No se puede cambiar el nombre del calendario estándar.  <br/> |
|CalendarCannotDeleteCalendarUsedByEnterpriseResource = 13042  <br/> |Un recurso de empresa está usando el calendario, por lo que no se puede eliminar.  <br/> |
|CalendarFilterInvalid = 13043  <br/> |El filtro no es válido para un calendario.  <br/> |

<a name="pj15_ErrorCodes_CBS"></a>

## <a name="table-10-cubeadmin-and-cube-build-service"></a>Tabla 10. CubeAdmin y Cube Build Service

|Código de error de CubeAdmin y Cube Build Service (CBS)|Descripción|
|:-----|:-----|
|CBSGeneralFailure = 17001  <br/> |Error en Cube Build Service (CBS). Se trata de un código de error general que puede ser resultado de muchas causas diferentes.  <br/> |
|CBSDsoNotInstalled = 17002  <br/> |CBS necesita tener instalado el componente Decision Support Objects (DSO) para Analysis Services.  <br/> |
|CBSASConnectionFailure = 17003  <br/> |CBS no se ha podido conectar al servidor de Analysis Services.  <br/> |
|CBSOlapProcessingFailure = 17004  <br/> |Error al procesar el cubo OLAP.  <br/> |
|CBSMetadataProcessingFailure = 17005  <br/> |Error al procesar los metadatos del cubo.  <br/> |
|CBSASServerLockTimeOut = 17006  <br/> |Se ha excedido el tiempo de espera del bloqueo del servidor de Analysis Services.  <br/> |
|CBSOlapDatabaseSetupFailure = 17007  <br/> |Error en la configuración de la base de datos de cubos OLAP.  <br/> |
|CBSASEntityLimitation = 17008  <br/> |Se ha excedido el número de entidades que puede usar Analysis Services.  <br/> |
|CBSRequestInvalidArguments = 17009  <br/> |Al menos un argumento de la solicitud CBS no es válido.  <br/> |
|CBSQueueingRequestFailed = 17010  <br/> |CBS no pudo enviar el trabajo a la cola.  <br/> |
|CBSUpdateCubeCalculatedMeasureDefintionError = 17011  <br/> |Hay un error en un miembro calculado del cubo.  <br/> |
|CBSAttemptToOverwrite = 17013  <br/> |No se pueden sobrescribir los datos del cubo.  <br/> |
|CBSCustomFieldCannotBeAddedAsDimension = 17014  <br/> |El campo personalizado no puede ser una dimensión del cubo.  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimension = 17015  <br/> |No se pudo agregar el campo personalizado como una dimensión del cubo.  <br/> |
|CBSCustomFieldCannotBeAddedAsMeasure = 17016  <br/> |El campo personalizado no puede ser una medida del cubo.  <br/> |
|CBSCustomFieldFailedToBeAddedAsMeasure = 17017  <br/> |No se pudo agregar el campo personalizado como una medida del cubo.  <br/> |
|CBSDsoTranslatorNotFound = 17018  <br/> |No se ha encontrado el traductor de Decision Support Objects.  <br/> |
|CBSUpdateOlapDBOperationFailure = 17019  <br/> |No se pudo actualizar la base de datos OLAP.  <br/> |
|CBSOlapDBInvalidArguments = 17020  <br/> |Al menos un argumento de la base de datos OLAP no es válido.  <br/> |
|CBSOlapDatabaseReadSettingListFailed = 17021  <br/> |No se pudo leer la lista de configuraciones de la base de datos OLAP.  <br/> |
|CBSOlapDatabaseReadSettingFailed = 17022  <br/> |No se pudo leer la configuración de la base de datos OLAP.  <br/> |
|CBSDeleteOlapDatabaseSetting = 17023  <br/> |Error al eliminar la configuración de la base de datos OLAP.  <br/> |
|CBSSetDefaultOlapDatabase = 17024  <br/> |Error al establecer la base de datos OLAP predeterminada.  <br/> |
|CBSSetOlapDatabaseEnabled = 17025  <br/> |Error al habilitar la base de datos OLAP.  <br/> |
|CBSGetDefaultOlapDatabase = 17026  <br/> |Error al obtener la base de datos OLAP predeterminada.  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimensionOrMeasure = 17027  <br/> |No se puede agregar el campo personalizado como una dimensión o una media.  <br/> |
|CBSOlapDatabaseAssocFieldsSettings = 17028  <br/> |Error en la configuración de campos asociados de la base de datos OLAP.  <br/> |
|CBSUpdateOlapDBOperationDuplicateOrFailure = 17029  <br/> |Error o duplicado de la operación de actualización de la base de datos OLAP.  <br/> |
|CBSErrorReadingDefaultDatabase = 17030  <br/> |Error al leer la base de datos OLAP predeterminada.  <br/> |
|CBSCreateOlapDBOperationFailure = 17031  <br/> |No se pudo crear la operación de base de datos OLAP.  <br/> |
|CBSSetCubeFieldsSettingsFromListForGroupMeasureFailed = 17032  <br/> |No se pudo establecer la lista de configuraciones de medidas de grupo de los campos del cubo.  <br/> |
|CBSErrorReadingCubeDepartments = 17033  <br/> |Error al leer departamentos en el cubo OLAP.  <br/> |
|CBSErrorMaxOlapDatabaseCountReached = 17034  <br/> |Se ha alcanzado el número máximo de bases de datos OLAP.  <br/> |
|CBSErrorReadingCubeFieldsSettings = 17035  <br/> |Error al leer la configuración de los campos del cubo.  <br/> |

<a name="pj15_ErrorCodes_CICO"></a>

## <a name="table-11-check-in-and-check-out"></a>Tabla 11. Protección y desprotección

|Código de error de protección o desprotección|Descripción|
|:-----|:-----|
|CICOCheckedOutToOtherUser = 10100  <br/> |Desprotegido para otro usuario.  <br/> |
|CICOAlreadyCheckedOutToYou = 10101  <br/> |Ya se ha desprotegido para usted.  <br/> |
|CICONotCheckedOut = 10102  <br/> |No está desprotegido.  <br/> |
|CICOCheckedOutInOtherSession = 10103  <br/> |Desprotegido en otra sesión.  <br/> |
|CICOInvalidSessionGuid = 10104  <br/> |El GUID de sesión no es válido.  <br/> |
|CICOAlreadyCheckedOutInSameSession = 10105  <br/> |Ya se ha desprotegido en la misma sesión.  <br/> |
|CICOCannotCheckOutVisibilityModeProjectWithMppInDocLib = 10106  <br/> |No se puede desproteger un proyecto en modo de visibilidad con un archivo MPP en la biblioteca de documentos.  <br/> |

<a name="pj15_ErrorCodes_CustomFields"></a>

## <a name="table-12-custom-field"></a>Tabla 12. Campo personalizado

|Código de error del campo personalizado|Descripción|
|:-----|:-----|
|CustomFieldInvalidPropertyType = 11500  <br/> |El tipo de propiedad no es válido.  <br/> |
|CustomFieldInvalidScope = 11503  <br/> |El ámbito del campo personalizado no es válido.  <br/> |
|CustomFieldScopesMustBeIdentical = 11504  <br/> |Los ámbitos deben ser idénticos.  <br/> |
|CustomFieldInvalidEntityUID = 11505  <br/> |El GUID de entidad del campo personalizado no es válido.  <br/> |
|CustomFieldHasInvalidPropertiesForNonLookupTableCF = 11506  <br/> |Las propiedades no son válidas para un campo personalizado que no tiene tabla de búsqueda.  <br/> |
|CustomFieldNonExistentWeightsTableUID = 11507  <br/> |El GUID de tabla de pesos no existe.  <br/> |
|CustomFieldInvalidName = 11508  <br/> |El nombre del campo personalizado no es válido.  <br/> |
|CustomFieldInvalidDefault = 11510  <br/> |El valor predeterminado del campo personalizado no es válido.  <br/> |
|CustomFieldInvalidLookupTableUID = 11511  <br/> |El GUID de tabla de búsqueda no es válido.  <br/> |
|CustomFieldTypeDoesNotMatchLookupTableMask = 11512  <br/> |El tipo de campo personalizado no coincide con la máscara de tabla de búsqueda.  <br/> |
|CustomFieldCannotHaveNonLeafNodeDefault = 11513  <br/> |El valor predeterminado del campo personalizado debe ser un nodo hoja.  <br/> |
|CustomFieldMatchingOnlyAvailableForResources = 11514  <br/> |El campo personalizado coincidente solo está disponible para los recursos.  <br/> |
|CustomFieldUIDCannotMatchLookupTableUID = 11516  <br/> |El GUID no coincide con ningún GUID de tabla de búsqueda.  <br/> |
|CustomFieldUIDAlreadyExists = 11517  <br/> |El GUID de campo personalizado ya existe.  <br/> |
|CustomFieldIDAlreadyExists = 11518  <br/> |El número de identificación del campo personalizado ya existe.  <br/> |
|CustomFieldNameAlreadyExists = 11519  <br/> |El nombre del campo personalizado ya existe.  <br/> |
|CustomFieldInvalidEntity = 11520  <br/> |La entidad no es válida para el campo personalizado.  <br/> |
|CustomFieldMaskDoesNotMatchEntityType = 11521  <br/> |La máscara de código no coincide con el tipo de entidad.  <br/> |
|CustomFieldLowerOrderBitsOutOfRange = 11522  <br/> |Los bits de orden inferior están fuera del intervalo.  <br/> |
|CustomFieldInvalidMaxValues = 11523  <br/> |Al menos uno de los valores máximos no es válido.  <br/> |
|CustomFieldCannotModifyCertainValuesOnceDefined = 11524  <br/> |Algunos valores no se pueden modificar después de haberlos definido.  <br/> |
|CustomFieldNonExistentPID = 11526  <br/> |El número de identificación de la propiedad del campo personalizado no existe.  <br/> |
|CustomFieldCannotChangeBuiltInFields = 11527  <br/> |No se pueden cambiar los campos integrados de Project Server, como Tipo de costo, Estado y RBS.  <br/> |
|CustomFieldSecondaryUidCannotEqualUid = 11528  <br/> |El GUID secundario no puede ser igual al GUID primario.  <br/> |
|CustomFieldCannotHaveSecondaryUIDorIDForThisEntityType = 11529  <br/> |El campo personalizado no puede tener un GUID secundario ni un GUID para este tipo de entidad.  <br/> |
|CustomFieldNameMatchesIntrinsicField = 11530  <br/> |El nombre del campo personalizado coincide con un campo intrínseco.  <br/> |
|CustomFieldInvalidAggregationType = 11531  <br/> |El tipo de agregación no es válido.  <br/> |
|CustomFieldProjectFormulaFieldsMustUseFormulaAggregation = 11532  <br/> |Los campos de fórmula del proyecto deben usar la agregación de fórmula.  <br/> |
|CustomFieldMustSpecifyEitherIDorUID = 11700  <br/> |Debe especificar el número de identificación o GUID del campo personalizado.  <br/> |
|CustomFieldInvalidID = 11701  <br/> |El número de identificación del campo personalizado no es válido.  <br/> |
|CustomFieldInvalidUID = 11702  <br/> |El GUID de campo personalizado no es válido.  <br/> |
|CustomFieldInvalidType = 11703  <br/> |El tipo de campo personalizado no es válido.  <br/> |
|CustomFieldInvalidTypeColumnFilledIn = 11704  <br/> |El valor de la columna de tipo de campo personalizado no es válido. Vea un ejemplo en [Ejemplo de código de error de WCF](#pj15_ErrorCodes_WCFExample).  <br/> |
|CustomFieldCodeValueDoesNotMatchLookupTable = 11706  <br/> |El valor del código no coincide con la tabla de búsqueda.  <br/> |
|CustomFieldCodeValueIsNotLeafNode = 11707  <br/> |El valor del código no es un nodo hoja de la tabla de búsqueda.  <br/> |
|CustomFieldRowAlreadyExists = 11708  <br/> |La fila de campo personalizado ya existe.  <br/> |
|CustomFieldRowDoesNotMatchCorrespondingDefinitionInDB = 11710  <br/> |La fila de campo personalizado no coincide con la definición de base de datos.  <br/> |
|CustomFieldCodeValueAlreadyUsed = 11711  <br/> |El valor de código ya está en uso.  <br/> |
|CustomFieldMaxValuesExceeded = 11712  <br/> |Se han excedido los valores máximos de los campos predeterminados.  <br/> |
|CustomFieldRequiredValueNotProvided = 11713  <br/> |No se proporciona un valor de campo personalizado obligatorio. Vea un ejemplo en [Ejemplo de código de error de WCF](#pj15_ErrorCodes_WCFExample).  <br/> |
|CustomFieldCannotChangeLookupTable = 11715  <br/> |No se puede cambiar la tabla de búsqueda de campo personalizado.  <br/> |
|CustomFieldFilterInvalid = 11716  <br/> |El filtro de campo personalizado no es válido.  <br/> |
|CustomFieldRolldownInvalidOnFormulaFields = 11717  <br/> |No se puede efectuar la aplicación en un campo personalizado de fórmula.  <br/> |
|CustomFieldFormulaFieldCannotBeRequired = 11718  <br/> |El campo de fórmula no puede ser obligatorio.  <br/> |
|CustomFieldFormulaFieldCannotBeWorkflowControlled = 11719  <br/> |El campo de fórmula no se puede controlar mediante un flujo de trabajo.  <br/> |
|CustomFieldCannotSetValueOnFormulaFields = 11720  <br/> |No se puede definir el valor en los campos de fórmula.  <br/> |
|CustomFieldNewPerRequestLimitExcedeed = 11721  <br/> |Se ha excedido el límite de solicitudes de nuevos campos personalizados. El límite es [NEW_CF_PER_REQUEST_LIMIT](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.CustomField.NEW_CF_PER_REQUEST_LIMIT.aspx) en una solicitud.  <br/> |
|CustomFieldNameIsReservedName = 11722  <br/> |Un nombre de campo personalizado no puede ser un nombre reservado.  <br/> |
|CustomFieldNameInvalidForOlapMeasure = 11723  <br/> |El nombre del campo personalizado no es válido para una medida de cubo OLAP.  <br/> |
|CustomFieldNameInvalidForOlapDimension = 11724  <br/> |El nombre del campo personalizado no es válido para una dimensión de cubo OLAP.  <br/> |
|CustomFieldSettingsInvalidForOlapMeasure = 11725  <br/> |La configuración de campo personalizado no es válida para una medida de cubo OLAP.  <br/> |
|CustomFieldSettingsInvalidForOlapDimension = 11726  <br/> |La configuración de campo personalizado no es válida para una dimensión de cubo OLAP.  <br/> |
|CustomFieldCannotAddRelativeImportanceField = 11727  <br/> |No se puede agregar un campo de importancia relativa.  <br/> |
|CustomFieldCannotAddProjectImpactField = 11728  <br/> |No se puede agregar un campo de impacto del proyecto.  <br/> |
|CustomFieldInvalidDepartmentUid = 11731  <br/> |El GUID de departamento en el campo personalizado no es válido.  <br/> |
|CustomFieldCannotModifyDepartmentUidOnBuiltinFields = 11732  <br/> |El GUID de departamento no se puede modificar en los campos personalizados integrados.  <br/> |
|CustomFieldCannotHaveBothLookupTableAndMultilineText = 11733  <br/> |Un campo personalizado no puede incluir una tabla de búsqueda y texto de varias líneas al mismo tiempo.  <br/> |
|CustomFieldCannotHaveBothFormulaAndMultilineText = 11734  <br/> |Un campo personalizado no puede incluir una fórmula y texto de varias líneas al mismo tiempo.  <br/> |
|CustomFieldDescriptionExceedsLimit = 11735  <br/> |La descripción del campo personalizado es demasiado larga. La longitud máxima de la propiedad **MD_PROP_DESCRIPTION** es 1000 caracteres.<br/> |
|CustomFieldOnlyTextFieldsCanHaveMultilineText = 11736  <br/> |Solo los campos personalizados de texto pueden contener texto de varias líneas.  <br/> |
|CustomFieldOnlyProjectFieldsCanHaveMultilineText = 11737  <br/> |Solo los campos personalizados de proyecto pueden contener texto de varias líneas.  <br/> |
|CustomFieldCannotChangeWorkflowControlledBehaviorForNonProjectCustomFields = 11738  <br/> |Un campo personalizado no puede modificar el comportamiento de los campos personalizados ajenos al proyecto controlados por un flujo de trabajo.  <br/> |
|CustomFieldIsWorkflowControlledAndCannotBeChanged = 11739  <br/> |El campo personalizado se controla mediante un flujo de trabajo y no se puede modificar.  <br/> |
|CustomFieldCannotHaveRequiredFlagWhenWorkflowControlledFlagIsSet = 11740  <br/> |El campo personalizado no puede ser obligatorio cuando se controla mediante un flujo de trabajo.  <br/> |
|CustomFieldFormulaCreatesCircularReference = 11742  <br/> |La fórmula del campo personalizado crea una referencia circular.  <br/> |
|CustomFieldFormulaContainsInvalidFieldReference = 11743  <br/> |La fórmula del campo personalizado contiene una referencia de campo que no es válida.  <br/> |
|CustomFieldFormulaContainsErrors = 11744  <br/> |La fórmula del campo personalizado contiene uno o más errores.  <br/> |
|CustomFieldLocalCustomFieldNotDefined = 11745  <br/> |No se ha definido el campo personalizado local.  <br/> |
|CustomFieldGraphicalIndicatorContainsErrors = 11746  <br/> |El indicador gráfico del campo personalizado contiene errores.  <br/> |
|CustomFieldGraphicalIndicatorContainsInvalidFieldReference = 11747  <br/> |El indicador gráfico del campo personalizado contiene una referencia de campo que no es válida.  <br/> |
|CustomFieldGraphicalIndicatorTypeMismatch = 11748  <br/> |El tipo no coincide con el tipo del indicador gráfico del campo personalizado.  <br/> |
|CustomFieldFormulaFieldCannotReferenceWorkflowControlledField = 11749  <br/> |Un campo de la fórmula no puede hacer referencia a un campo controlado por un flujo de trabajo.  <br/> |
|CustomFieldWorkflowCustomFieldBeingReferencedByFormula = 11750  <br/> |Una fórmula está tratando de hacer referencia a un campo personalizado de flujo de trabajo.  <br/> |

<a name="pj15_ErrorCodes_LookupTables"></a>

## <a name="table-13-lookup-table"></a>Tabla 13. Tabla de búsqueda

|Código de error de la tabla de búsqueda|Descripción|
|:-----|:-----|
|LookupTableMaskNotDefined = 11000  <br/> |No se ha definido la máscara de código de tabla de búsqueda.  <br/> |
|LookupTableMaskHasTooManyValues = 11001  <br/> |La máscara de código de tabla de búsqueda tiene demasiados valores.  <br/> |
|LookupTableMaskHasGaps = 11002  <br/> |La máscara de código de tabla de búsqueda tiene huecos.  <br/> |
|LookupTableMaskSequenceTypeLimitedToOneLevelDeep = 11003  <br/> |El tipo de secuencia de la máscara de código está limitado a un nivel.  <br/> |
|LookupTableMaskSequenceTypeInvalid = 11004  <br/> |El tipo de secuencia de máscara de código no es válido.  <br/> |
|LookupTableMaskSequenceRequiresAnyLength = 11005  <br/> |La secuencia de máscara de código necesita una longitud de _Any_.  <br/> |
|LookupTableMaskSeparatorTooLong = 11006  <br/> |El separador de máscara de código tiene demasiados caracteres.  <br/> |
|LookupTableMaskLevelMustBeBlankAcrossLCIDs = 11007  <br/> |El nivel de máscara de código debe estar en blanco en todos los identificadores de configuración regional (Id. de idioma).  <br/> |
|LookupTableMaskSeparatorInvalid = 11008  <br/> |Un carácter de separador de máscara de código no es válido.  <br/> |
|LookupTableMaskBlankSeparatorInvalidAfterAnyLengthSequence = 11009  <br/> |Un carácter separador en blanco no es válido después de una longitud de secuencia de _Any_.  <br/> |
|LookupTableMaskSequenceLengthInvalid = 11010  <br/> |La longitud de la secuencia de máscara de código no es válida.  <br/> |
|LookupTableMaskLevelMustBeOneOrMore = 11011  <br/> |La máscara de código debe ser de nivel 1 o superior.  <br/> |
|LookupTableItemDoesNotFitMask = 11050  <br/> |El elemento de la tabla de búsqueda no encaja con la definición de la máscara de código.  <br/> |
|LookupTableItemContainsSeparator = 11051  <br/> |El elemento de la tabla de búsqueda contiene un carácter de separación.  <br/> |
|LookupTableItemFullValueTooLong = 11052  <br/> |El valor completo del elemento de la tabla de búsqueda es demasiado largo.  <br/> |
|LookupTableDuplicateSiblingsDisallowed = 11053  <br/> |En la tabla de búsqueda no se permite el uso de elementos del mismo nivel duplicados.  <br/> |
|LookupTableSortOrderIndexInvalid = 11054  <br/> |El índice de criterios de ordenación de la tabla de búsqueda no es válido.  <br/> |
|LookupTableSortOrderIndexDuplicate = 11055  <br/> |Índice de criterios de ordenación de la tabla de búsqueda duplicado.  <br/> |
|LookupTableSortOrderTypeInvalid = 11056  <br/> |El tipo de criterio de ordenación de la tabla de búsqueda no es válido.  <br/> |
|LookupTableSortOrderMustComeAfterParentSortOrder = 11057  <br/> |El criterio de ordenación debe situarse después del criterio de ordenación primario.  <br/> |
|LookupTableSortOrderMustComeBeforeParentNextSiblingSortOrder = 11058  <br/> |El criterio de ordenación debe situarse antes del primario del siguiente criterio de ordenación del mismo nivel.  <br/> |
|LookupTableInvalidCookieLength = 11060  <br/> |La longitud de cookies para una tabla de búsqueda no es válida.  <br/> |
|LookupTableMustHaveValuesForPrimaryLCIDorJustOneValue = 11061  <br/> |La tabla de búsqueda debe tener valores para el identificador de configuración regional (Id. idioma) primario, o solo un valor. Al crear una tabla de búsqueda en varios idiomas, por ejemplo, se debe agregar solo un valor de máscara para cada nivel o agregar primero el valor del LCID primario.  <br/> |
|LookupTableLCIDNotSupportedInLookupTableLanguages = 11062  <br/> |El identificador de configuración regional (Id. idioma) no se ha incluido en los idiomas de la tabla de búsqueda.  <br/> |
|LookupTableInvalidDescriptionLength = 11063  <br/> |La longitud de la descripción de un elemento de la tabla de búsqueda no es válida.  <br/> |
|LookupTableCannotChangeBuiltInTables = 11064  <br/> |No se pueden modificar las tablas de búsqueda integradas.  <br/> |
|LookupTableCannotChangeTypeOnceCreated = 11065  <br/> |No se puede modificar el tipo de tabla de búsqueda después de crear la tabla de búsqueda.  <br/> |
|LookupTableCannotDeleteLTWithDependantCustomField = 11066  <br/> |No se puede eliminar una tabla de búsqueda que se usa en un campo personalizado.  <br/> |
|LookupTableAllLevelsNotFilled = 11067  <br/> |Se deben rellenar todos los niveles de tabla de búsqueda.  <br/> |
|LookupTableDuplicateName = 11068  <br/> |Los nombres de tabla de búsqueda deben ser únicos.  <br/> |
|LookupTableInvalidName = 11069  <br/> |El nombre de tabla de búsqueda no es válido.  <br/> |
|LookupTableDuplicateSiblingPhoneticsDisallowed = 11071  <br/> |No se puede tener elementos fonéticos del mismo nivel duplicados en una tabla de búsqueda.  <br/> |
|LookupTableItemInvalidLookupTable = 11073  <br/> |Un elemento de la tabla de búsqueda no es válido.  <br/> |
|LookupTableInvalidPhoneticsLength = 11074  <br/> |La longitud del campo de fonética no es válida.  <br/> |
|LookupTableAlreadyExists = 11076  <br/> |La tabla de búsqueda ya existe.  <br/> |
|LookupTableInvalidUID = 11078  <br/> |El GUID de tabla de búsqueda no es válido.  <br/> |
|LookupTableFilterInvalid = 11079  <br/> |El filtro de la tabla de búsqueda no es válido.  <br/> |
|LookupTableLanguageParameterInvalidWithXmlFilter = 11080  <br/> |Un parámetro de idioma no es válido con un parámetro _xmlFilter_ de tabla de búsqueda.  <br/> |
|LookupTableInvalidParentStructUid = 11081  <br/> |El GUID de una estructura primaria de tabla de búsqueda no es válido.  <br/> |
|LookupTableItemContainsListSeparator = 11082  <br/> |El elemento de tabla de búsqueda contiene un separador de lista.  <br/> |
   
Los códigos de error de la Tabla 14 incluyen errores de elementos de las páginas de detalles del proyecto (PDP), de sincronización de Exchange, de la escala de tiempo de Project Web App y de bases de datos. Muchos de los códigos de error clasificados en la Tabla 14, en la sección de miscelánea, son de uso interno.
  
> [!NOTE]
> Los códigos de error de auditoría no se usan en Project Server 2013. 

<a name="pj15_ErrorCodes_Miscellaneous"></a>

## <a name="table-14-miscellaneous-error-codes"></a>Tabla 14: Códigos de error misceláneos

|Código de error misceláneo|Descripción|
|:-----|:-----|
|AuditingUpdateFailure = 31000  <br/> |No se usa.  <br/> |
|AuditingCannotDeleteFeature = 31001  <br/> |No se usa.  <br/> |
|AuditingCannotAddFeature = 31002  <br/> |No se usa.  <br/> |
|AuditingFeatureIsNoLongerAudited = 31003  <br/> |No se usa.  <br/> |
|AuditingItemIsNotYetAvailable = 31004  <br/> |No se usa.  <br/> |
|AuditingInvalidFeatureUid = 31005  <br/> |No se usa.  <br/> |
|AuditingInvalidStoreForSelectedFeature = 31006  <br/> |No se usa.  <br/> |
|AuditingInvalidStore = 31007  <br/> |No se usa.  <br/> |
|AuditingVersionNameTooLong = 31008  <br/> |No se usa.  <br/> |
|AuditingBeginVersionFailure = 31009  <br/> |No se usa.  <br/> |
|AuditingEndVersionFailure = 31010  <br/> |No se usa.  <br/> |
|ProjectDetailPagesStrategicImpactRatingRequired = 32000  <br/> |Se requiere una clasificación del impacto estratégico para la página de detalles del proyecto.  <br/> |
|ProjectDetailPagesMissingPDPLinks = 32001  <br/> |Faltan vínculos a las páginas de detalles del proyecto.  <br/> |
|ProjectDetailPagesUnavailableWorker = 32002  <br/> |Error al cargar la obtención de detalles del proyecto. No hay procesos de trabajo disponibles.  <br/> |
|ProjectDetailPagesFailedToLoadProjectInWorker = 32003  <br/> |No se ha podido cargar el proceso de trabajo.  <br/> |
|AppPermissionInvalidAppPermissionId = 32300  <br/> |Se ha producido un problema con el Id. de permiso de la aplicación.  <br/> |
|InvariantValidationPSIFailed = 40000  <br/> |Error devuelto por los métodos de **PWA** si alguno de los métodos privados devuelve **ValidationMethodFailed**. Para uso interno.<br/> |
|ValidationMethodFailed = 40001  <br/> |Error devuelto por los métodos privados de **PWA** cuando detectan incoherencias en la base de datos. Para uso interno.<br/> |
|GeneralExchangeSyncError = 40500  <br/> |Error general en la sincronización de Microsoft Exchange. Uso interno.  <br/> |
|ExchangeSyncRootFolderCreationFailed = 40501  <br/> |No se pudo crear la carpeta raíz en la sincronización de Microsoft Exchange.  <br/> |
|ExchangeSyncTaskFolderCreationFailed = 40502  <br/> |No se pudo crear la carpeta de tarea.  <br/> |
|ExchangeSyncCouldNotGetRootFolder = 40503  <br/> |No se pudo obtener la carpeta raíz.  <br/> |
|ExchangeSyncCouldNotLoadTaskObject = 40504  <br/> |No se pudo cargar el objeto de tarea.  <br/> |
|ExchangeSyncNewExchangeTaskCreationFailed = 40505  <br/> |Error al crear una tarea nueva en la sincronización de Exchange.  <br/> |
|ExchangeSyncFailedToUpdateCacheForUser = 40506  <br/> |No se pudo actualizar la caché de sincronización de Exchange para el usuario.  <br/> |
|ExchangeSyncFailedToUpdateExchangeTask = 40507  <br/> |No se pudo actualizar la tarea en Microsoft Exchange.  <br/> |
|ExchangeSyncSubscriptionUpdateFailed = 40508  <br/> |No se pudo actualizar la suscripción a la sincronización de Exchange.  <br/> |
|ExchangeSyncEWSUrlFailed = 40509  <br/> |Error en la URL del servicio web de Microsoft Exchange.  <br/> |
|ExchangeSyncExchangeUrlRefreshFailed = 40510  <br/> |No se pudo actualizar la URL de Exchange.  <br/> |
|ExchangeSyncExchangeSubscriptionUpdateForUserFailed = 40511  <br/> |No se pudo actualizar la suscripción de Exchange para el usuario.  <br/> |
|ExchangeSyncGeneralProcessingFailure = 40512  <br/> |Error general de procesamiento en la sincronización de Microsoft Exchange.  <br/> |
|ExchangeSyncDeletionOfTasksInExchangeFailure = 40513  <br/> |No se pudieron eliminar tareas de sincronización de Exchange.  <br/> |
|ExchangeSyncAttemptedSyncOfInvalidConfiguredResource = 40514  <br/> |Se intentó sincronizar un recurso con una configuración que no es válida.  <br/> |
|ExchangeSyncRetrievalOfEWSUrlCausedException = 40515  <br/> |Se produjo una excepción durante la recuperación de un servicio web Exchange.  <br/> |
|TimelineViewDataDoesNotExist = 42000  <br/> |No existen datos para la vista de escala de tiempo en Project Web App.  <br/> |
|DatabaseUndefinedError = 50000  <br/> |No se ha definido la base de datos.  <br/> |
|DatabaseCannotInsertDuplicateKeyError = 50001  <br/> |La base de datos no puede insertar una clave duplicada.  <br/> |

<a name="pj15_ErrorCodes_Notifications"></a>

## <a name="table-15-notification"></a>Tabla 15. Notificación

|Código de error de notificación|Descripción|
|:-----|:-----|
|NotificationReminderUnknown = 16050  <br/> |Notificación de aviso desconocida.  <br/> |
|NotificationReminderParentNotSubscribed = 16051  <br/> |No hay suscripción al elemento principal de la notificación de aviso.  <br/> |
|NotificationReminderParentNotFound = 16052  <br/> |No se ha encontrado el elemento principal de la notificación de aviso.  <br/> |
|NotificationReminderChildStillSubscribed = 16053  <br/> |Sigue habiendo una suscripción al elemento secundario de la notificación de aviso.  <br/> |
|NotificationReminderChildNotFound = 16054  <br/> |No se ha encontrado el elemento secundario de la notificación de aviso.  <br/> |
|NotificationEMailDeliveryFailed = 16080  <br/> |Error en la entrega del mensaje de correo electrónico de notificación.  <br/> |
|NotificationQueueMessageFailed = 16082  <br/> |Error en el mensaje de puesta en cola de la notificación.  <br/> |
|NotificationXSLTTransformationError = 16084  <br/> |Error en la transformación XSLT de la notificación.  <br/> |
   
Todos los códigos de error de la Tabla 16 pertenecen al Optimizador, que es un componente de análisis de la cartera de proyectos.

<a name="pj15_ErrorCodes_Optimizer"></a>

## <a name="table-16-optimizer-project-portfolio-analysis"></a>Tabla 16. Optimizador (análisis de la cartera de proyectos)

|Código de error del Optimizador|Descripción|
|:-----|:-----|
|OptimizerDepInvalidDepType = 29000  <br/> |El valor de **DEPENDENCY_TYPE** del optimizador en [OptimizerDependencyDataSet.OptimizerDependenciesRow](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependenciesRow.aspx) no es válido. Vea [Optimizer.DependencyTypes](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Optimizer.DependencyTypes.aspx).  <br/> |
|OptimizerDepInvalidEntityType = 29001  <br/> |El tipo de entidad no es válido. Vea la propiedad [Entities](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.Entities.aspx).  <br/> |
|OptimizerDepInvalidPosition = 29003  <br/> |El valor de [POSITION](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsRow.POSITION.aspx) no es válido.  <br/> |
|OptimizerDepDuplicateDependentProjects = 29004  <br/> |Hay proyectos duplicados en [OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable.aspx).  <br/> |
|OptimizerDepInvalidDependency = 29005  <br/> |La dependencia del Optimizador no es válida.  <br/> |
|OptimizerDepCircularDependency = 29006  <br/> |Hay una dependencia circular.  <br/> |
|OptimizerCannotDeleteDependency = 29007  <br/> |La dependencia no se puede eliminar.  <br/> |
|OptimizerCannotCreateDependency = 29008  <br/> |La dependencia no se puede crear.  <br/> |
|OptimizerCannotUpdateDependency = 29009  <br/> |La dependencia no se puede actualizar.  <br/> |
|OptimizerCannotCreateMultipleDependencies = 29010  <br/> |No se pueden crear varias dependencias.  <br/> |
|OptimizerCannotUpdateMultipleDependencies = 29011  <br/> |No se pueden actualizar varias dependencias.  <br/> |
|OptimizerEngineMatrixNotFilled = 29100  <br/> |El Optimizador no tiene datos suficientes para el cálculo.  <br/> |
|OptimizerEngineCustomFieldIsNotAConstraint = 29101  <br/> |El campo personalizado no es una restricción para el Optimizador.  <br/> |
|OptimizerCouldNotCalculatePrioritiesFromCustomFields = 29102  <br/> |No se pueden calcular las prioridades desde los campos personalizados especificados.  <br/> |
|OptimizerEngineBinaryInfeasibleSolution = 29103  <br/> |El cálculo del Optimizador tiene como resultado una solución inviable.  <br/> |
|OptimizerEngineBinaryNumericalError = 29104  <br/> |Hay un error numérico en el cálculo del Optimizador.  <br/> |
|OptimizerEngineBinaryTimedOut = 29105  <br/> |Se ha excedido el tiempo de espera del cálculo del Optimizador.  <br/> |
|OptimizerEngineBinaryMaxedIterations = 29106  <br/> |El cálculo del Optimizador ha alcanzado el número máximo de iteraciones.  <br/> |
|OptimizerEngineBinarySubOptimal = 29107  <br/> |Los resultados de los cálculos del Optimizador no son óptimos.  <br/> |
|OptimizerEngineBinaryInternalError = 29108  <br/> |Hay un error interno en el cálculo del Optimizador.  <br/> |
|OptimizerInvalidRange = 29200  <br/> |El intervalo de fechas del optimizador no es válido.  <br/> |
|OptimizerNonNormalizedWeights = 29201  <br/> |Los valores de **WEIGHT** en [AnalysisDataSet.AnalysisPriorityDataDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisPriorityDataDataTable.aspx) no están normalizados.  <br/> |
|OptimizerCannotEditPrioritization = 29300  <br/> |No se puede editar la priorización de impulsores.  <br/> |
|OptimizerCannotDeletePrioritization = 29301  <br/> |No se puede eliminar la priorización de impulsores.  <br/> |
|OptimizerCannotCreatePrioritization = 29302  <br/> |No se puede crear la priorización de impulsores.  <br/> |
|OptimizerCannotUpdatePrioritization = 29303  <br/> |No se puede actualizar la priorización de impulsores.  <br/> |
|OptimizerCannotCalculateDriverPriorities = 29304  <br/> |No se pueden calcular las prioridades de impulsores.  <br/> |
|OptimizerCannotCreateMultiplePrioritizations = 29305  <br/> |No se pueden crear varias priorizaciones de impulsores.  <br/> |
|OptimizerCannotUpdateMultiplePrioritizations = 29306  <br/> |No se pueden actualizar varias priorizaciones de impulsores.  <br/> |
|OptimizerDriverRelationsNotFilled = 29307  <br/> |Los datos de DriverRelationsRow no están completos.  <br/> |
|OptimizerDriversNotFilled = 29308  <br/> |No hay información suficiente en los impulsores de proyectos para una solución.  <br/> |
|OptimizerDriverRelationsInvalidInversedValue = 29309  <br/> |Hay valores inversos en [DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx).  <br/> |
|OptimizerCannotCreatePrioritizationUsingInactiveDrivers = 29310  <br/> |Se ha especificado un valor inactivo en [DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx). Compruebe las propiedades **DRIVER1_UID** y **DRIVER2_UID**.  <br/> |
|OptimizerCannotChangePrioritizationType = 29311  <br/> |No se puede cambiar el tipo de priorización.  <br/> |
|OptimizerCannotSpecifyPriorityValuesForCalculatedPrioritizations = 29312  <br/> |Si se ha calculado una prioridad, no podrá especificar el valor de prioridad.  <br/> |
|OptimizerCannotNormalizePriorityValues = 29313  <br/> |Los valores de prioridad no se pueden normalizar.  <br/> |
|OptimizerTooManyDriversInPrioritization = 29314  <br/> |Hay demasiados impulsores de negocios en la priorización.  <br/> |
|OptimizerInvalidProjectImpactValue = 29400  <br/> |El valor del impacto del proyecto no es válido.  <br/> |
|OptimizerCannotDeleteDriver = 29401  <br/> |El impulsor de proyectos no se puede eliminar.  <br/> |
|OptimizerCannotCreateDriver = 29402  <br/> |El impulsor de proyectos no se puede crear.  <br/> |
|OptimizerCannotUpdateDriver = 29403  <br/> |El impulsor de proyectos no se puede actualizar.  <br/> |
|OptimizerCannotEditDriver = 29404  <br/> |El impulsor de proyectos no se puede editar.  <br/> |
|OptimizerCannotCreateMultipleDrivers = 29405  <br/> |No se pueden crear varios impulsores.  <br/> |
|OptimizerCannotUpdateMultipleDrivers = 29406  <br/> |No se pueden actualizar varios impulsores.  <br/> |
|OptimizerInvalidRelativeImportanceValue = 29407  <br/> |El valor de importancia relativa no es válido.  <br/> |
|OptimizerInvalidDriverUid = 29500  <br/> |El GUID de impulsor no es válido.  <br/> |
|OptimizerInvalidEntityType = 29501  <br/> |El tipo de entidad no es válido para el Optimizador.  <br/> |
|OptimizerInvalidProjectUid = 29502  <br/> |El GUID de proyecto no es válido.  <br/> |
|OptimizerInvalidCustomFieldUid = 29503  <br/> |El GUID de campo personalizado no es válido para el Optimizador.  <br/> |
|OptimizerInvalidHardConstraintUid = 29504  <br/> |El GUID de restricción específica no es válido.  <br/> |
|OptimizerInvalidAnalysisUid = 29505  <br/> |El GUID de análisis no es válido.  <br/> |
|OptimizerDriverFilterInvalid = 29506  <br/> |El filtro de impulsores no es válido.  <br/> |
|OptimizerPrioritizationFilterInvalid = 29507  <br/> |El filtro de priorización no es válido.  <br/> |
|OptimizerCannotLoadOptimizationEngine = 29508  <br/> |El motor de cálculo del Optimizador no se puede cargar.  <br/> |
|OptimizerAnalysisFilterInvalid = 29509  <br/> |El filtro de análisis no es válido.  <br/> |
|OptimizerSolutionFilterInvalid = 29510  <br/> |El filtro de soluciones del Optimizador no es válido.  <br/> |
|OptimizerDependenciesFilterInvalid = 29511  <br/> |El filtro de dependencias del Optimizador no es válido.  <br/> |
|OptimizerInvalidSolutionUid = 29512  <br/> |El GUID de solución del Optimizador no es válido.  <br/> |
|OptimizerInvalidViewUid = 29513  <br/> |El GUID de vista del Optimizador no es válido.  <br/> |
|OptimizerInvalidAnalysisType = 29600  <br/> |El tipo de análisis de la cartera no es válido.  <br/> |
|OptimizerInvalidPrioritizationType = 29601  <br/> |El tipo de priorización del Optimizador no es válido.  <br/> |
|OptimizerCannotDeleteAnalysis = 29602  <br/> |No se puede eliminar el análisis de cartera.  <br/> |
|OptimizerCannotCreateAnalysis = 29603  <br/> |No se puede crear el análisis de cartera.  <br/> |
|OptimizerCannotUpdateAnalysis = 29604  <br/> |No se puede actualizar el análisis de cartera.  <br/> |
|OptimizerInvalidPrioritizationUid = 29607  <br/> |El GUID de priorización no es válido.  <br/> |
|OptimizerCannotCreateMultipleAnalyses = 29608  <br/> |No se pueden crear varios análisis de cartera.  <br/> |
|OptimizerCannotUpdateMultipleAnalyses = 29609  <br/> |No se pueden actualizar varios análisis de cartera.  <br/> |
|OptimizerCannotCalculateProjectPriorities = 29610  <br/> |El Optimizador no puede calcular las prioridades de los proyectos.  <br/> |
|OptimizerCannotDeleteAnalysisProjectImpact = 29611  <br/> |No se puede eliminar el impacto del proyecto en el análisis de cartera.  <br/> |
|OptimizerCannotChangeAnalysisProjects = 29612  <br/> |No se pueden cambiar los proyectos en el análisis de cartera.  <br/> |
|OptimizerCannotChangePriorityData = 29613  <br/> |No se pueden cambiar los datos de prioridad.  <br/> |
|OptimizerCannotEditAnalysis = 29614  <br/> |No se puede editar el análisis de cartera.  <br/> |
|OptimizerInvalidPlannerData = 29615  <br/> |Los datos del Organizador no son válidos para el Optimizador.  <br/> |
|OptimizerCannotChangeImpactData = 29616  <br/> |No se pueden cambiar los datos de impacto de los proyectos.  <br/> |
|OptimizerInvalidProjectsNumber = 29617  <br/> |El número de proyectos no es válido.  <br/> |
|OptimizerCannotAddImpactCFUIDToCFAnalysis = 29618  <br/> |No se puede agregar el GUID de campo personalizado de impacto del proyecto ([PROJECT_IMPACT_CF_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.PROJECT_IMPACT_CF_UID.aspx)) al análisis de la cartera.  <br/> |
|OptimizerInvalidDepartmentUid = 29619  <br/> |La propiedad [DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.DEPARTMENT_UID.aspx) no es válida.  <br/> |
|OptimizerTooManyProjectsInAnalysis = 29620  <br/> |Hay demasiados proyectos en el análisis.  <br/> |
|QueueAnalysisCannotDeleteAnalysis = 29680  <br/> |El método [QueueDeleteAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteAnalyses.aspx) no puede eliminar el análisis.  <br/> |
|QueueAnalysisCannotCreateAnalysis = 29681  <br/> |El método [QueueCreateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateAnalysis.aspx) no puede crear el análisis.  <br/> |
|QueueAnalysisCannotUpdateAnalysis = 29682  <br/> |El método [QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx) no puede actualizar el análisis.  <br/> |
|AnalysisMismatchedJobList = 29690  <br/> |La lista de trabajos de análisis tiene discrepancias.  <br/> |
|OptimizerInvalidForceInLookupTableUid = 29691  <br/> |No se puede forzar la entrada del GUID de tabla de búsqueda.  <br/> |
|OptimizerInvalidForceOutLookupTableUid = 29692  <br/> |No se puede forzar la salida del GUID de tabla de búsqueda.  <br/> |
|OptimizerDuplicateForceLookupTableUids = 29693  <br/> |Hay GUID de tabla de búsqueda forzados duplicados.  <br/> |
|OptimizerInvalidDecisionResult = 29701  <br/> |El resultado de la decisión no es válido.  <br/> |
|OptimizerInvalidForcedStatus = 29702  <br/> |El estado forzado no es válido.  <br/> |
|OptimizerCannotDeleteSolution = 29703  <br/> |El método [QueueDeleteOptimizerSolutions](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteOptimizerSolutions.aspx) no puede eliminar la solución del Optimizador.  <br/> |
|OptimizerCannotCreateSolution = 29704  <br/> |El método [QueueCreateOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateOptimizerSolution.aspx) no puede crear la solución del Optimizador.  <br/> |
|OptimizerCannotUpdateSolution = 29705  <br/> |El método [QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx) no puede actualizar la solución del Optimizador.  <br/> |
|OptimizerCannotCalculateSolutionStrategicAlignment = 29706  <br/> |El Optimizador no puede calcular la solución de la alineación estratégica.  <br/> |
|OptimizerCannotCreateMultipleSolutions = 29707  <br/> |El Optimizador no puede crear varias soluciones.  <br/> |
|OptimizerCannotUpdateMultipleSolutions = 29708  <br/> |El Optimizador no puede actualizar varias soluciones.  <br/> |
|OptimizerCannotAddPrioritizationToCFAnalysis = 29709  <br/> |El Optimizador no puede agregar una priorización a un campo personalizado para el análisis.  <br/> |
|OptimizerTableIsReadOnly = 29710  <br/> |La tabla del Optimizador es de solo lectura.  <br/> |
|OptimizerSolutionCreateMessageFailed = 29711  <br/> |El Optimizador no pudo crear un mensaje "solución creada".  <br/> |
|OptimizerSolutionDeleteMessageFailed = 29712  <br/> |El Optimizador no pudo crear un mensaje "solución eliminada".  <br/> |
|OptimizerCannotCalculateEfficientFrontier = 29714  <br/> |El Optimizador no puede calcular la frontera eficiente del análisis.  <br/> |
|OptimizerCannotUpdateSolutionProperties = 29715  <br/> |No se puede actualizar las propiedades de solución.  <br/> |
|OptimizerInvalidConstraintPosition = 29716  <br/> |La posición de restricción del Optimizador no es válida.  <br/> |
|OptimizerInvalidHardConstraintPosition = 29717  <br/> |La posición de restricción específica del Optimizador no es válida.  <br/> |
|OptimizerInvalidConstraintLimit = 29718  <br/> |El límite de restricción en el Optimizador no es válido.  <br/> |
|OptimizerInvalidConstraintValue = 29719  <br/> |El valor de restricción no es válido.  <br/> |
|OptimizerInvalidSolutionProjectsSet = 29720  <br/> |El conjunto de proyectos de la solución no es válido.  <br/> |
|OptimizerCannotCommitSolution = 29721  <br/> |El método [CommitOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.CommitOptimizerSolution.aspx) no puede confirmar la solución.  <br/> |
|OptimizerInvalidInputData = 29723  <br/> |Los datos de entrada del Optimizador no son válidos.  <br/> |
|OptimizerInvalidConstraintSet = 29724  <br/> |El conjunto de restricciones del Optimizador no es válido.  <br/> |
|OptimizerCannotUpdateAnalysisMetrics = 29725  <br/> |No se pueden actualizar las métricas del análisis.  <br/> |
|OptimizerSolutionMismatchedJobList = 29726  <br/> |La lista de trabajos de la solución tiene discrepancias.  <br/> |
|OptimizerInvalidForceLookupTableValue = 29727  <br/> |El valor de la tabla de búsqueda forzada no es válido.  <br/> |
|OptimizerCannotCreateSolutionWhileAnalysisUpdateIsPending = 29728  <br/> |No se puede crear una solución de Optimizador mientras hay una actualización del análisis pendiente.  <br/> |
|OptimizerProjectSelectorAtLeastOne = 29800  <br/> |Debe haber al menos un proyecto seleccionado para el Optimizador.  <br/> |
   
Los códigos de error de la Tabla 17 pertenecen a Planner, que es un componente de análisis de la cartera de proyectos.

<a name="pj15_ErrorCodes_Planner"></a>

## <a name="table-17-planner-project-portfolio-analysis"></a>Tabla 17. Planner (análisis de la cartera de proyectos)

|Código de error de Planner|Descripción|
|:-----|:-----|
|PlannerSolutionMessageDeleteFailed = 28000  <br/> |Error de cola: error en el mensaje para eliminar la solución del Organizador.  <br/> |
|PlannerSolutionMessageCreateFailed = 28001  <br/> |Error de cola: error en el mensaje para crear la solución del Organizador.  <br/> |
|PlannerInvalidRBSValueUid = 28002  <br/> |El GUID de un valor de la estructura de descomposición del recurso no es válido en los datos del Organizador.  <br/> |
|PlannerInvalidCustomFieldUid = 28003  <br/> |El GUID de un campo personalizado no es válido.  <br/> |
|PlannerHorizonInvalid = 28004  <br/> |El horizonte temporal del Organizador no es válido. El horizonte temporal es el período especificado para el planeamiento de capacidad.  <br/> |
|PlannerHorizonTooBig = 28005  <br/> |El horizonte temporal es demasiado lejano.  <br/> |
|PlannerInvalidBookingType = 28006  <br/> |El tipo de reserva de recursos no es válido.  <br/> |
|PlannerInvalidTimeScale = 28007  <br/> |La escala temporal no es válida.  <br/> |
|PlannerInvalidProjectSNET = 28008  <br/> |La fecha "No comenzar antes del" del proyecto no es válida.  <br/> |
|PlannerInvalidProjectFNLT = 28009  <br/> |La fecha "No finalizar después del" del proyecto no es válida.  <br/> |
|PlannerInvalidAnalysisStartDate = 28010  <br/> |La propiedad [START_DATE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectRequirementsByRoleRow.START_DATE.aspx) para el proyecto no es válida.  <br/> |
|PlannerInvalidAnalysisDuration = 28011  <br/> |La propiedad [DURATION](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectsRow.DURATION.aspx) no es válida para el análisis de la cartera.  <br/> |
|PlannerInvalidHorizonStartDate = 28012  <br/> |La fecha de inicio del horizonte temporal no es válida.  <br/> |
|PlannerInvalidHorizonEndDate = 28013  <br/> |La fecha de finalización del horizonte no es válida.  <br/> |
|PlannerInvalidHorizonTimeScale = 28014  <br/> |La escala temporal del horizonte temporal no es válida.  <br/> |
|PlannerInvalidAnalysisType = 28015  <br/> |El tipo de análisis de la cartera no es válido.  <br/> |
|PlannerHorizonStartDateDoesNotMatchTimeScale = 28016  <br/> |La fecha de inicio del horizonte temporal no coincide con la escala temporal.  <br/> |
|PlannerHorizonEndDateDoesNotMatchTimeScale = 28017  <br/> |La fecha de finalización del horizonte temporal no coincide con la escala temporal.  <br/> |
|PlannerAnalysisNoCapacityData = 28037  <br/> |No hay datos sobre la capacidad de recursos del análisis de la cartera.  <br/> |
|PlannerInvalidSolutionUid = 28100  <br/> |El GUID de solución de análisis no es válido.  <br/> |
|PlannerInvalidOptimizerSolutionUid = 28101  <br/> |El GUID de solución del Optimizador no es válido.  <br/> |
|PlannerInvalidLookupTableValueUid = 28102  <br/> |El GUID de valor de tabla de búsqueda no es válido.  <br/> |
|PlannerInvalidEfficientFrontierUid = 28103  <br/> |La propiedad [FRONTIER_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionEfficientFrontierRow.FRONTIER_UID.aspx) no es válida.  <br/> |
|PlannerInvalidProjectUid = 28104  <br/> |El GUID de proyecto no es válido.  <br/> |
|PlannerInvalidAllocationThreshold = 28105  <br/> |El umbral de asignación no es válido.  <br/> |
|PlannerInvalidHiringType = 28109  <br/> |La propiedad [HIRING_TYPE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.HIRING_TYPE.aspx) no es válida. Vea [Planner.PlannerHiringType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.PlannerHiringType.aspx).  <br/> |
|PlannerInvalidConstraintType = 28110  <br/> |La propiedad [CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_TYPE.aspx) no es válida. Vea [Planner.ConstraintType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.ConstraintType.aspx).  <br/> |
|PlannerInvalidConstraintValue = 28111  <br/> |La propiedad [CONSTRAINT_VALUE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_VALUE.aspx) no es válida.  <br/> |
|PlannerInvalidRateTable = 28112  <br/> |La propiedad [RATE_TABLE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.RATE_TABLE.aspx) no es válida.  <br/> |
|PlannerInvalidSolutionForConstraint = 28113  <br/> |La solución del Organizador no es válida para la restricción. Se ha forzado la entrada de demasiados proyectos durante el primer pase del Organizador.  <br/> |
|PlannerInvalidSolutionForDependencies = 28114  <br/> |La solución del Organizador no es válida porque hay demasiados proyectos para tener en cuenta las dependencias o los conflictos de negocio. Este error se produce en el segundo pase.  <br/> |
|PlannerInvalidSolutionForScheduling = 28115  <br/> |La solución del Organizador no es válida para la programación porque hay dependencias circulares.  <br/> |
|PlannerInvalidAnalysisUid = 28116  <br/> |La propiedad [ANALYSIS_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.ANALYSIS_UID.aspx) no es válida.  <br/> |
|PlannerInvalidProjectStartDate = 28200  <br/> |La fecha de inicio del proyecto no es válida.  <br/> |
|PlannerInvalidProjectEndDate = 28201  <br/> |La fecha de finalización del proyecto no es válida.  <br/> |
|PlannerInvalidProjectDuration = 28202  <br/> |La duración del proyecto no es válida.  <br/> |
|PlannerInvalidProjectFNLTDate = 28203  <br/> |La fecha "No finalizar después del" del proyecto no es válida.  <br/> |
|PlannerInvalidProjectSNETDate = 28204  <br/> |La fecha "No comenzar antes del" del proyecto no es válida.  <br/> |
|PlannerCannotCreateSolution = 28900  <br/> |El Organizador no puede crear una solución.  <br/> |
|PlannerCannotUpdateSolution = 28901  <br/> |El Organizador no puede actualizar la solución.  <br/> |
|PlannerCannotDeleteSolution = 28902  <br/> |El Organizador no puede eliminar la solución.  <br/> |
|PlannerCannotCreateMultipleSolutions = 28903  <br/> |El Organizador no puede crear varias soluciones.  <br/> |
|PlannerCannotUpdateMultipleSolutions = 28904  <br/> |El Organizador no puede actualizar varias soluciones.  <br/> |
|PlannerTableIsReadOnly = 28907  <br/> |La tabla **DataTable** es de solo lectura.  <br/> |
|PlannerCannotCommitSolution = 28908  <br/> |El Organizador no puede confirmar la solución en la base de datos.  <br/> |
|PlannerFieldIsReadOnly = 28909  <br/> |El campo es de solo lectura.  <br/> |
|PlannerProjectNotInParentSolution = 28910  <br/> |El proyecto no está en la solución principal.  <br/> |
|PlannerProjectNotSelectedInParentSolution = 28911  <br/> |El proyecto no está seleccionado en la solución principal.  <br/> |
|PlannerProjectNotInParentAnalysis = 28912  <br/> |El proyecto no está en el análisis de la cartera principal.  <br/> |
|PlannerProjectBeyondHorizon = 28913  <br/> |El proyecto se prolonga más allá del horizonte temporal.  <br/> |
|PlannerResourceAllocationInternalError = 28915  <br/> |Hay un error interno en la asignación de recursos.  <br/> |
|PlannerResourceAllocationInfeasibleSolution = 28916  <br/> |La asignación de recursos es una solución inviable.  <br/> |
|PlannerProjectEndDateViolatesDependency = 28917  <br/> |La fecha de finalización del proyecto incumple una dependencia.  <br/> |
|PlannerInvalidProjectsSet = 28919  <br/> |El conjunto de proyectos no es válido.  <br/> |
|PlannerInvalidInputData = 28920  <br/> |El Organizador tiene datos de entrada que no son válidos.  <br/> |
|PlannerDecimalOverflowError = 28921  <br/> |Hay un error de desbordamiento por decimales en el Organizador.  <br/> |
|PlannerSolutionMismatchedJobList = 28922  <br/> |La solución tiene una la lista de trabajos con discrepancias.  <br/> |
|PlannerInvalidForceLookupTableValue = 28923  <br/> |El valor forzado de una tabla de búsqueda no es válido.  <br/> |
|PlannerNoHiredResource = 28924  <br/> |No se ha contratado a ningún recurso para la propuesta.  <br/> |

<a name="pj15_ErrorCodes_Projects"></a>

## <a name="table-18-project"></a>Tabla 18. Proyecto

|Código de error del proyecto|Descripción|
|:-----|:-----|
|ProjectGlobalNotFound = 100  <br/> |No se encuentra la plantilla de información global de la empresa.  <br/> |
|ProjectGlobalCannotBeDeleted = 101  <br/> |No se puede eliminar la plantilla de información global de la empresa.  <br/> |
|ProjectNotFound = 1000  <br/> |No se encontró el proyecto.  <br/> |
|ProjectAlreadyExists = 1001  <br/> |El proyecto ya existe.  <br/> |
|ProjectCheckedoutToOtherUser = 1002  <br/> |El proyecto está desprotegido para otro usuario.  <br/> |
|ProjectTypeInvalidForCreate = 1003  <br/> |El tipo de proyecto de la operación de creación no es válido.  <br/> |
|ProjectParametersInvalid = 1004  <br/> |Al menos un parámetro del proyecto no es válido.  <br/> |
|ProjectNotCheckedoutToUser = 1006  <br/> |El proyecto no está desprotegido para el usuario.  <br/> |
|ProjectCheckedout = 1007  <br/> |Proyecto desprotegido.  <br/> |
|ProjectTypeInvalid = 1008  <br/> |El tipo de proyecto no es válido.  <br/> |
|ProjectIDInvalid = 1009  <br/> |El número de identificación del proyecto no es válido.  <br/> |
|ProjectNameTooLong = 1014  <br/> |El nombre del proyecto es demasiado largo.  <br/> |
|ProjectManagerNameTooLong = 1015  <br/> |El nombre del gestor del proyecto es demasiado largo.  <br/> |
|ProjectNameInvalid = 1016  <br/> |El nombre del proyecto no es válido.  <br/> |
|ProjectStartDateMissing = 1025  <br/> |Falta la fecha de inicio del proyecto.  <br/> |
|ProjectNameMissing = 1026  <br/> |Falta el nombre del proyecto.  <br/> |
|ProjectVersionMissing = 1027  <br/> |Falta la versión del proyecto.  <br/> |
|ProjectDoesNotExist = 1028  <br/> |El proyecto no existe.  <br/> |
|ProjectMultipleProjectsInvalid = 1029  <br/> |Varios proyectos no son válidos.  <br/> |
|ProjectHasWriteLock = 1030  <br/> |El proyecto está bloqueado para escritura en la base de datos.  <br/> |
|ProjectHasPendingWriteLock = 1031  <br/> |El proyecto tiene un bloqueo para escritura pendiente.  <br/> |
|ProjectHasNoReadLock = 1032  <br/> |El proyecto no está bloqueado para lectura.  <br/> |
|ProjectHasReadLock = 1033  <br/> |El proyecto está bloqueado para lectura.  <br/> |
|ProjectNameAlreadyExists = 1034  <br/> |El nombre del proyecto ya existe.  <br/> |
|ProjectOptCriticalSlackLimitInvalid = 1035  <br/> |El límite de demora crítico opcional no es válido.  <br/> |
|ProjectOptCurrencyPositionInvalid = 1036  <br/> |La posición de moneda opcional no es válida.  <br/> |
|ProjectOptCurrencyDigitsInvalid = 1037  <br/> |Los dígitos de moneda opcional no son válidos.  <br/> |
|ProjectOptCurrencySymbolTooLong = 1038  <br/> |El símbolo de moneda opcional es demasiado largo.  <br/> |
|ProjectCannotDelete = 1039  <br/> |No se puede eliminar el proyecto. Solo se pueden eliminar los proyectos del servidor normales o basados en una plantilla.  <br/> |
|ProjectCannotAdd = 1040  <br/> |No se puede usar el método **AddToProject** en el proyecto del servidor.  <br/> |
|ProjectOptCurrencySymbolInvalid = 1041  <br/> |El símbolo de moneda opcional no es válido.  <br/> |
|ProjectHasNoWriteLock = 1042  <br/> |El proyecto no está bloqueado para escritura.  <br/> |
|ProjectFilterInvalid = 1043  <br/> |El filtro del proyecto no es válido.  <br/> |
|ProjectTooLarge = 1044  <br/> |La propuesta de proyecto es demasiado grande.  <br/> |
|ProjectOptCurrencyCodeNot3Chars = 1045  <br/> |El código de moneda opcional no tiene tres caracteres.  <br/> |
|ProjectOptCurrencyCodeInvalid = 1046  <br/> |El código de moneda no es válido en las opciones de proyecto.  <br/> |
|ProjectActualsAreProtected = 1047  <br/> |Los datos reales del proyecto están protegidos.  <br/> |
|ProjectTemplateNotFound = 1048  <br/> |No se ha encontrado la plantilla del proyecto.  <br/> |
|ProjectCurrencyCodeInvalid = 1049  <br/> |El código de moneda no es válido.  <br/> |
|ProjectCannotEditCostResource = 1050  <br/> |No se puede editar el recurso de costo.  <br/> |
|ProjectIsNotPublished = 1051  <br/> |No se ha publicado el proyecto.  <br/> |
|ProjectExceededLWPTaskLimit = 1052  <br/> |Se ha excedido el límite de tareas para una propuesta de proyecto (un proyecto ligero).  <br/> |
|ProjectOptFinishDateInvalid = 1053  <br/> |La fecha de finalización especificada en las opciones del proyecto no es válida.  <br/> |
|ProjectExceededItemsLimit = 1054  <br/> |Se ha excedido el límite de elementos para procesar. La aplicación de servicio de Project Server no puede utilizar **ProjectDataSet** para agregar o actualizar más de 1000 elementos en total en todas las tablas. Para procesar más de 1000 elementos, use varias llamadas, por ejemplo, a **QueueUpdateProject**.<br/> |
|ProjectColumnNotReadOnly = 1055  <br/> |La columna no es de solo lectura.  <br/> |
|ProjectInvalidOwner = 1056  <br/> |El propietario del proyecto no es válido.  <br/> |
|ProjectCantEditPctWrkCompForNonWrkRscs = 1057  <br/> |No se puede editar **PctWorkComplete** para una tarea sin asignaciones de procesamiento.  <br/> |
|ProjectCannotEditMaterialResource = 1058  <br/> |No se puede editar el recurso material.  <br/> |
|ProjectCannotEditFieldWhenTaskHasNoWorkAssignment = 1059  <br/> |No se puede editar el campo porque la tarea no tiene asignaciones de trabajo.  <br/> |
|ProjectSubProjectNotFound = 1070  <br/> |. No se han encontrado subproyectos.  <br/> |
|ProjectResourceNotFound = 1100  <br/> |No se ha encontrado el recurso.  <br/> |
|ProjectResourceAlreadyExists = 1101  <br/> |El recurso ya existe.  <br/> |
|ProjectCannotReplaceResourceWithSelf = 1106  <br/> |No se puede reemplazar el recurso por el mismo objeto.  <br/> |
|ProjectCannotChangeLockedTrackingMethod = 1107  <br/> |No se puede realizar el cambio porque el método de seguimiento está bloqueado.  <br/> |
|ProjectInvalidColumnForCompatibilityMode = 1108  <br/> |La columna del modo de compatibilidad no es válida.  <br/> |
|ProjectUpdateInvalidUpdateSequenceNumber = 1151  <br/> |El número de secuencia de la actualización del proyecto no es válido.  <br/> |
|ProjectUpdateDuplicateUpdateSequenceNumber = 1152  <br/> |Número de secuencia duplicado en la actualización del proyecto.  <br/> |
|ProjectUpdateNullUpdateSequenceNumber = 1153  <br/> |Número de secuencia nulo en la actualización del proyecto.  <br/> |
|ProjectUpdateNullUpdateColumnNames = 1154  <br/> |Nombres de columna nulos en la actualización del proyecto.  <br/> |
|ProjectUpdateInvalidProjectUID = 1155  <br/> |El GUID de proyecto no es válido en la actualización del proyecto.  <br/> |
|ProjectUpdateInvalidColumnForUpdate = 1156  <br/> |La columna no es válida para la actualización del proyecto.  <br/> |
|ProjectUpdateCannotEditColumn = 1157  <br/> |No se puede editar la columna en la actualización del proyecto.  <br/> |
|ProjectUpdateNoChangesToValidateAndSchedule = 1158  <br/> |La actualización del proyecto no contiene cambios que se puedan validar y programar.  <br/> |
|LinkNotFound = 1159  <br/> |No se ha encontrado el vínculo.  <br/> |
|ProjectUpdateInvalidColumnValue = 1160  <br/> |El valor de columna no es válido en la actualización del proyecto.  <br/> |
|ProjectCannotDeleteItem = 1161  <br/> |No se puede eliminar el elemento de proyecto.  <br/> |
|ProjectUpdateCannotComputeOptIndex = 1162  <br/> |No se puede calcular el índice de optimización de la actualización del proyecto.  <br/> |
|ProjectCannotUpdateDueToVisibilityMode = 1163  <br/> |No se puede actualizar porque el proyecto está en modo de visibilidad.  <br/> |
|ProjectNodeConsistencyException = 9132  <br/> |Excepción: el nodo no es coherente.  <br/> |
|ProjectSchedulingEngineException = 9133  <br/> |Excepción en el motor de programación.  <br/> |
|ProjectFormulaCalculationException = 9134  <br/> |Excepción en el cálculo de fórmula.  <br/> |
|ProjectUpdateDatabaseException = 9135  <br/> |Excepción en la actualización de base de datos.  <br/> |
|ProjectDeleteException = 9136  <br/> |Excepción al eliminar el proyecto.  <br/> |
|ProjectOperationException = 9137  <br/> |Excepción en la operación del proyecto.  <br/> |
|ProjectCannotComunicateWithPCS = 9138  <br/> |No se pudo comunicar con el proceso de trabajo PCS.  <br/> |
|ProjectPCSSessionInvalid = 9139  <br/> |No se pudo abrir el proyecto en una sesión de motor.  <br/> |
|ProjectPublishFailure = 23000  <br/> |Error en la cola mientras se publicaba el proyecto.  <br/> |
|ProjectCurrencyConflict = 23001  <br/> |Hay un conflicto en la moneda especificada.  <br/> |
|ProjectPublishFailed = 23002  <br/> |Error en la publicación del proyecto mientras se ponía en cola.  <br/> |
|ProjectReversePublishFailed = 23003  <br/> |Error en la operación de publicación del proyecto cuando se estaba poniendo en cola.  <br/> |
|ProjectReversePublishFailure = 23004  <br/> |Error en la publicación invertida del proyecto durante el procesamiento de la cola.  <br/> |
|ProjectArchiveRetentionDeleteFailure = 23005  <br/> |Error al eliminar el proyecto a causa de la retención de archivo.  <br/> |
|ProjectDeleteFailure = 23006  <br/> |Error al eliminar el proyecto.  <br/> |
|ProjectPublishEnqueueFailure = 23007  <br/> |Error al publicar el proyecto mientras se ponía en cola.  <br/> |
|ProjectCheckinFailure = 23008  <br/> |Error al proteger el proyecto durante el procesamiento de la cola.  <br/> |
|ProjectCheckinFailed = 23009  <br/> |Error al proteger el proyecto mientras se ponía en cola.  <br/> |
|ProjectCheckoutFailed = 23010  <br/> |El usuario no tiene permisos para desproteger el proyecto.  <br/> |
|ProjectPublishSummaryEnqueueFailure = 23011  <br/> |Error de publicación del resumen cuando se ponía en cola.  <br/> |
|ProjectPublishSummaryFailed = 23012  <br/> |Error de publicación del resumen.  <br/> |
|ProjectUpdateScheduledProjectFailure = 26026  <br/> |Error de actualización de la programación del proyecto durante el procesamiento de la cola.  <br/> |
|ProjectSyncProjectEnterpriseEntitiesFailure = 26033  <br/> |Error al sincronizar las entidades de empresa del proyecto durante el procesamiento de la cola.  <br/> |
|GeneralDalDatabaseIsReadOnly = 26034  <br/> |Error al cargar la obtención de detalles del proyecto. La base de datos es de solo lectura.  <br/> |
|GeneralDatabaseCommunicationError = 26035  <br/> |Puede haber varias causas diferentes, como problemas de red o de autenticación.  <br/> |

<a name="pj15_ErrorCodes_RDS"></a>

## <a name="table-19-reporting-data-service-rds"></a>Tabla 19. Servicio de datos de informes (RDS)

|Código de error del RDS|Descripción|
|:-----|:-----|
|ReportingAttributeCubeSettingsChangedMessageFailed = 24000  <br/> |Error en el mensaje de modificación de RDS para un atributo de configuración de cubo.  <br/> |
|ReportingBaseCalendarChangeMessageFailed = 24001  <br/> |Error en el mensaje de modificación de RDS para un calendario base.  <br/> |
|ReportingCustomFieldMetadataChangeMessageFailed = 24002  <br/> |Error en el mensaje de modificación de RDS para los metadatos de un campo personalizado.  <br/> |
|ReportingEntityUserViewChangedMessageFailed = 24003  <br/> |Error en el mensaje de modificación de RDS para una vista de usuario de entidad.  <br/> |
|ReportingFiscalPeriodChangeMessageFailed = 24004  <br/> |Error en el mensaje de modificación de RDS para un período fiscal.  <br/> |
|ReportingLookupTableChangeMessageFailed = 24005  <br/> |Error en el mensaje de modificación de RDS para una tabla de búsqueda.  <br/> |
|ReportingProjectChangeMessageFailed = 24006  <br/> |Error en el mensaje de modificación de RDS para un proyecto.  <br/> |
|ReportingResourceCapacityUpdateMessageFailed = 24007  <br/> |Error en el mensaje de modificación de RDS para capacidad de recursos.  <br/> |
|ReportingResourceChangeMessageFailed = 24008  <br/> |Error en el mensaje de modificación de RDS para un recurso.  <br/> |
|ReportingTimesheetAdjustMessageFailed = 24009  <br/> |Error en el mensaje de ajuste de RDS para un parte de horas.  <br/> |
|ReportingTimesheetClassCreateMessageFailed = 24010  <br/> |Error en el mensaje de creación de RDS para una clase de parte de horas.  <br/> |
|ReportingTimesheetDeleteMessageFailed = 24011  <br/> |Error en el mensaje de eliminación de RDS para un parte de horas.  <br/> |
|ReportingTimesheetPeriodDeleteMessageFailed = 24012  <br/> |Error en el mensaje de eliminación de RDS para un período de parte de horas.  <br/> |
|ReportingTimesheetPeriodMessageFailed = 24013  <br/> |Error en el mensaje de RDS para un período de parte de horas.  <br/> |
|ReportingTimesheetSaveMessageFailed = 24014  <br/> |Error en el mensaje de guardado de RDS para un parte de horas.  <br/> |
|ReportingTimesheetStatusChangeMessageFailed = 24015  <br/> |Error en el mensaje de modificación de RDS para el estado de un parte de horas.  <br/> |
|ReportingWSSSyncMessageFailed = 24016  <br/> |Error en el mensaje de RDS para la sincronización de SharePoint.  <br/> |
|ReportingGetSPWebFailed = 24017  <br/> |RDS no pudo obtener el valor web de SharePoint.  <br/> |
|ReportingWssSyncListFailed = 24018  <br/> |RDS no pudo sincronizarse con la lista de SharePoint.  <br/> |
|ReportingWssTransferLinksFailed = 24019  <br/> |RDS no pudo transferir los vínculos de SharePoint.  <br/> |
|ReportingQueueMessageSubmitFailed = 24020  <br/> |RDS no pudo enviar un mensaje a la cola.  <br/> |
|ReportingWssSyncHRefFailed = 24021  <br/> |RDS no pudo sincronizarse con el valor HRef de SharePoint.  <br/> |
|ReportingSyncGlobalDataMessageFailed = 24022  <br/> |Error en el mensaje de RDS para sincronizarse con los datos globales de empresa.  <br/> |
|ReportingRDBRefreshMessageFailed = 24023  <br/> |Error en el mensaje de RDS para actualizar RDB.  <br/> |
|ReportingAttributeCubeDepartmentsChangedMessageFailed = 24024  <br/> |El mensaje de RDS no pudo modificar el atributo de departamento del cubo OLAP.  <br/> |
|ReportingTimesheetProjectAggregationMessageFailed = 24025  <br/> |El mensaje de RDS no pudo agregar proyectos a las tablas de partes de horas de RDB.  <br/> |
|ReportingRdbBulkDataSyncMessageFailed = 24026  <br/> |Error en el mensaje de RDS para la sincronización de datos masiva en RDB.  <br/> |
|ReportingWorkflowMetadataSyncMessageFailed = 24027  <br/> |El mensaje de RDS no pudo sincronizar los metadatos del flujo de trabajo.  <br/> |
|ReportingProjectWorkflowInformationSyncMessageFailed = 24028  <br/> |El mensaje de RDS no pudo sincronizar la información del flujo de trabajo del proyecto.  <br/> |
|ReportingEptSyncMessageFailed = 24029  <br/> |El mensaje de RDS no pudo sincronizar la plantilla del proyecto empresarial.  <br/> |
|ReportingSummaryProjectPublishMessageFailed = 24030  <br/> |El mensaje de RDS no pudo publicar el proyecto de resumen.  <br/> |
|ReportingSolutionCommitedDecisionChangedMessageFailed = 24031  <br/> |El mensaje de RDS no pudo cambiar la decisión confirmada para la solución.  <br/> |
|ReportingDelayedUpgradeFailed = 24032  <br/> |Error en la actualización retrasada del RDB.  <br/> |

<a name="pj15_ErrorCodes_Resources"></a>

## <a name="table-20-resource"></a>Tabla 20. Recurso

|Código de error del recurso|Descripción|
|:-----|:-----|
|ResourceNotFound = 2000  <br/> |No se ha encontrado el recurso.  <br/> |
|ResourceAlreadyExists = 2001  <br/> |El recurso ya existe.  <br/> |
|ResourceCheckedoutToOtherUser = 2002  <br/> |El recurso se ha desprotegido para otro usuario.  <br/> |
|ResourceUIDInvalid = 2011  <br/> |El GUID de recurso no es válido.  <br/> |
|ResourceNameInvalid = 2016  <br/> |El nombre del recurso no es válido.  <br/> |
|ResourceNameTooLong = 2017  <br/> |El nombre del recurso es demasiado largo.  <br/> |
|ResourceInitialsTooLong = 2018  <br/> |Las iniciales del recurso son demasiado largas.  <br/> |
|ResourceCheckedout = 2025  <br/> |El recurso está desprotegido.  <br/> |
|ResourceNTAccountInvalid = 2026  <br/> |La cuenta de Windows (NTLM) del recurso no es válida.  <br/> |
|ResourceNameAlreadyInUse = 2027  <br/> |El nombre del recurso ya está en uso. Los nombres deben ser únicos.  <br/> |
|ResourceNTAccountAlreadyInUse = 2028  <br/> |La cuenta NTLM del recurso ya está en uso.  <br/> |
|ResourceAdGuidAlreadyInUse = 2029  <br/> |El GUID de recurso ya está en uso.  <br/> |
|ResourceHasActuals = 2031  <br/> |El recurso tiene datos reales.  <br/> |
|ResourceNTAccountTooLong = 2035  <br/> |La cuenta NTLM es demasiado larga.  <br/> |
|ResourceEMailAddressTooLong = 2036  <br/> |La dirección de correo electrónico del recurso es demasiado larga.  <br/> |
|ResourceCodeTooLong = 2037  <br/> |El código del recurso es demasiado largo.  <br/> |
|ResourceGroupTooLong = 2038  <br/> |El grupo del recurso es demasiado largo.  <br/> |
|ResourceWorkGroupInvalid = 2039  <br/> |El grupo de trabajo del recurso no es válido.  <br/> |
|ResourceTypeInvalid = 2040  <br/> |El tipo del recurso no es válido.  <br/> |
|ResourceNonWorkResourceWithEMailInvalid = 2044  <br/> |Un recurso que no sea de trabajo no puede tener una dirección de correo electrónico.  <br/> |
|rsResourceNameHasTrailingOrLeadingWhitespace = 2046  <br/> |El nombre del recurso empieza o termina con un espacio en blanco.  <br/> |
|ResourceCannotDeleteCallingUserAccount = 2047  <br/> |El usuario no puede eliminar su propia cuenta.  <br/> |
|ResourceInitialsInvalid = 2048  <br/> |Las iniciales del recurso no son válidas.  <br/> |
|ResourceAccrueAtInvalid = 2049  <br/> |El valor de acumulación no es válido.  <br/> |
|ResourceNonMaterialResourceCannotHaveMaterialLabel = 2050  <br/> |Un recurso no material no puede tener una etiqueta de material.  <br/> |
|ResourceMaterialResourceCannotHaveCertainFields = 2051  <br/> |Un recurso material no puede tener determinados campos.  <br/> |
|ResourceAvailFromAvailToOverlap = 2052  <br/> |Solapamiento de las fechas de disponible desde y disponible hasta.  <br/> |
|ResourceInvalidEmailLanguage = 2053  <br/> |El idioma del correo electrónico no es válido.  <br/> |
|ResourceBookingTypeInvalid = 2055  <br/> |El tipo de reserva no es válido.  <br/> |
|ResourceCannotReplaceMaterialResourceWithNonMaterialResource = 2056  <br/> |No se puede reemplazar el recurso material por un recurso no material.  <br/> |
|ResourceCannotUpdateEnterpriseResource = 2057  <br/> |No se puede actualizar el recurso de empresa.  <br/> |
|rsResourceCannotAddLocalWithSameNameAsEnterprise = 2058  <br/> |No se puede agregar un recurso local que tiene el mismo nombre que un recurso de empresa.  <br/> |
|ResourceCannotSetRateOnCostResource = 2059  <br/> |No se puede establecer una tasa en recurso de costo.  <br/> |
|ResourceCannotSetRateOnMaterialResource = 2060  <br/> |No se puede establecer una tasa en un recurso material.  <br/> |
|ResourceCannotSetCanLevelOnNonWorkResource = 2061  <br/> |No se puede establecer el nivel en un recurso que no sea de trabajo.  <br/> |
|ResourceCannotDeleteThisUser = 2062  <br/> |No se puede eliminar este usuario.  <br/> |
|ResourceCannotDeactivateSelf = 2063  <br/> |Un recurso no se puede desactivar a sí mismo.  <br/> |
|ResourceAvailabilityDateRangesOverlap = 2064  <br/> |Los intervalos de fechas de disponibilidad del recurso se solapan.  <br/> |
|ResourceAvailabilityOutsideTheHireAndTerminationDateRange = 2065  <br/> |La fecha de disponibilidad del recurso está fuera del intervalo de fechas de contratación y de terminación.  <br/> |
|ResourceFilterInvalid = 2066  <br/> |El filtro de un recurso no es válido.  <br/> |
|ResourceSegmentWithThisEffectiveDateDoesNotExist = 2067  <br/> |No se puede eliminar una tasa de recurso que no se ha guardado.  <br/> |
|ResourceSegmentWithThisEffectiveDateAlready = 2068  <br/> |Ya existe un segmento con esta fecha efectiva.  <br/> |
|ResourceUserHasItemCheckedOutToItStill = 2069  <br/> |El usuario todavía tiene un elemento desprotegido.  <br/> |
|ResourceInvalidHireDate = 2070  <br/> |La fecha de contratación no es válida.  <br/> |
|ResourceInvalidTerminationDate = 2071  <br/> |La fecha de terminación no es válida.  <br/> |
|ResourceCannotChangeExistingResourceType = 2072  <br/> |No se puede cambiar un tipo de recurso.  <br/> |
|ResourceCannotSetTimesheetManagerOnSpecifiedResource = 2073  <br/> |No se puede establecer el administrador del parte de horas en este recurso en concreto.  <br/> |
|ResourceInvalidTimesheetManager = 2074  <br/> |El administrador del parte de horas no es válido.  <br/> |
|ResourceInvalidAssignmentOwner = 2075  <br/> |El propietario de la asignación no es válido.  <br/> |
|ResourceCannotCreateCostResource = 2076  <br/> |No se puede crear un recurso de costo.  <br/> |
|ResourceInvalidRbsValue = 2077  <br/> |El valor de RBS no es válido.  <br/> |
|ResourceCannotSetAssignmentOwnerOnSpecifiedResource = 2078  <br/> |No se puede establecer el propietario de la asignación en el recurso especificado.  <br/> |
|ResourceFieldsInvalidForBudget = 2079  <br/> |Al menos uno de los campos del presupuesto no es válido.  <br/> |
|ResourceHyperlinkInvalid = 2080  <br/> |El hipervínculo del recurso no es válido.  <br/> |
|ResourceAuthorizationValidOnlyOnWorkResources = 2081  <br/> |La autorización es válida solo en los recursos de trabajo.  <br/> |
|ResourceIsProjectOwner = 2082  <br/> |No se puede eliminar el recurso porque es el propietario del proyecto.  <br/> |
|ResourceIsTimesheetManager = 2083  <br/> |No se puede eliminar el recurso porque es el administrador del parte de horas.  <br/> |
|ResourceIsDefaultAssignmentOwner = 2084  <br/> |No se puede eliminar el recurso porque es el propietario de la asignación predeterminado.  <br/> |
|ResourceIsAssignmentOwner = 2085  <br/> |No se puede eliminar el recurso porque es el propietario de la asignación.  <br/> |
|ResourceIsUsedInResourcePlan = 2086  <br/> |No se puede eliminar el recurso porque se usa en el plan de recursos.  <br/> |
|ResourceCannotDeleteEnterpriseResource = 2087  <br/> |No se puede eliminar el recurso de empresa por motivos desconocidos.  <br/> |
|ResourceSetResourceAuthorizationFailed = 2088  <br/> |No se pudo establecer la autorización del recurso.  <br/> |
|ResourceTooManyResourcesSpecifiedToDelete = 2089  <br/> |No se puede eliminar el número de recursos especificado.  <br/> |
|ResourceTooManyResourcesReturned = 2090  <br/> |El método no puede gestionar este número de recursos.  <br/> |
|ResourceCannotDeleteWorkflowProxyUser = 2091  <br/> |El usuario proxy del flujo de trabajo no se puede eliminar.  <br/> |
|ResourceInvalidEmailWithExchangeSync = 2092  <br/> |El correo electrónico no es válido para la sincronización con Microsoft Exchange Server.  <br/> |
|ResourceInvalidResourceTypeWithExchangeSync = 2093  <br/> |El tipo de recurso no es válido para la sincronización con Exchange Server.  <br/> |
|ResourceInvalidPrincipalNameWithExchangeSync = 2094  <br/> |El nombre principal del recurso no es válido para la sincronización con Exchange Server.  <br/> |
|ResourceInvalidAuthenticationTypeWithExchangeSync = 2095  <br/> |El tipo de autenticación del recurso no es válido para la sincronización con Exchange Server.  <br/> |
|ResourceExchangeSyncFlagAndPrincipalNameMismatch = 2096  <br/> |La marca de sincronización de Exchange Server no coincide con el nombre principal del recurso.  <br/> |
|ResourceUnsupportedUserUpdateInSharePointSecurityMode = 2097  <br/> |El modo de seguridad de SharePoint no admite la creación de usuarios.  <br/> |

<a name="pj15_ErrorCodes_ResourcePlans"></a>

## <a name="table-21-resource-plan"></a>Tabla 21. Planeamiento de recursos

|Código de error del planeamiento de recursos|Descripción|
|:-----|:-----|
|ResourcePlanProjectPublishIncomplete = 30000  <br/> |No se completó la publicación del proyecto para el plan de recursos.  <br/> |
|ResourcePlanInvalidResourceType = 30001  <br/> |El tipo de recurso del plan de recursos no es válido.  <br/> |
|ResourcePlanInactiveResourcesDisallowed = 30002  <br/> |No se permite el uso de recursos inactivos en un plan de recursos.  <br/> |
|ResourcePlanFilterInvalid = 30003  <br/> |El filtro de planes de recursos no es válido.  <br/> |
|ResourcePlanSaveFailure = 30004  <br/> |No se pudo guardar el plan de recursos.  <br/> |
|ResourcePlanCheckinFailure = 30005  <br/> |No se pudo proteger el plan de recursos.  <br/> |
|ResourcePlanDeleteFailure = 30006  <br/> |No se pudo eliminar el plan de recursos.  <br/> |
|ResourcePlanInvalidUtilizationType = 30007  <br/> |El tipo de utilización del plan de recursos no es válido.  <br/> |
|ResourcePlanInvalidTimescale = 30008  <br/> |La escala de tiempo del plan de recursos no es válida.  <br/> |
|ResourcePlanMismatchedJobList = 30009  <br/> |La lista de trabajos del plan de recursos tiene discrepancias.  <br/> |
|ResourcePlanAlreadyExists = 30010  <br/> |El plan de recursos ya existe.  <br/> |
|ResourcePlanInvalidProjectUID = 30011  <br/> |El GUID de proyecto del plan de recursos no es válido.  <br/> |
|ResourcePlanResourceAlreadyExists = 30012  <br/> |El recurso ya existe en el planeamiento de recursos.  <br/> |
   
Los códigos de error de la Tabla 22 son para los métodos **Rules** del servicio web de **PWA**. Son de uso interno. 

<a name="pj15_ErrorCodes_Rules"></a>

## <a name="table-22-rules"></a>Tabla 22. Reglas

|Código de error de las reglas|Descripción|
|:-----|:-----|
|RulesNameTooLong = 21001  <br/> |El nombre de la regla de aprobación es demasiado largo. Solo para uso interno en Project Web App.  <br/> |
|RulesDescriptionTooLong = 21002  <br/> |La descripción de la regla es demasiado larga. Solo para uso interno en Project Web App.  <br/> |
|RulesInvalidRuleType = 21003  <br/> |El tipo de regla no es válido. Solo para uso interno en Project Web App.  <br/> |
|RulesInvalidConditionType = 21004  <br/> |El tipo de condición de una regla no es válido. Solo para uso interno en Project Web App.  <br/> |
|RulesInvalidOperatorType = 21005  <br/> |El tipo de operador de una regla no es válido. Solo para uso interno en Project Web App.  <br/> |
|RulesInvalidListItemType = 21007  <br/> |El tipo de elemento de lista de una regla no es válido. Solo para uso interno en Project Web App.  <br/> |
|RulesNameInvalidCharacters = 21008  <br/> |Al menos uno de los caracteres del nombre de la regla no es válido. Solo para uso interno en Project Web App.  <br/> |
|RulesDescriptionInvalidCharacters = 21009  <br/> |Al menos uno de los caracteres de la descripción de la regla no es válido. Solo para uso interno en Project Web App.  <br/> |
|RulesInvalidValueType = 21010  <br/> |El tipo de valor de la regla no es válido. Solo para uso interno en Project Web App.  <br/> |

<a name="pj15_ErrorCodes_Security"></a>

## <a name="table-23-security"></a>Tabla 23. Seguridad

|Código de error de seguridad|Descripción|
|:-----|:-----|
|SecurityGroupCouldNotBeCreated = 19001  <br/> |No se puede crear un grupo de seguridad.  <br/> |
|SecurityFieldAccessIDInvalid = 19003  <br/> |El número de identificación del código de acceso al campo de seguridad no es válido.  <br/> |
|SecurityCannotUpdateFacForNonExistentCategory = 19004  <br/> |La categoría de seguridad no existe. No se puede actualizar el código de acceso al campo.  <br/> |
|SecurityDuplicateCategoryUid = 19005  <br/> |GUID de categoría de seguridad duplicado.  <br/> |
|SecurityDuplicateGroupUid = 19006  <br/> |GUID de grupo de seguridad duplicado.  <br/> |
|SecurityDuplicateTemplateUid = 19007  <br/> |GUID de plantilla de seguridad duplicado.  <br/> |
|SecurityInvalidTemplateUidRef = 19008  <br/> |El GUID de la plantilla de seguridad no es válido.  <br/> |
|SecurityInvalidGlobalPermission = 19009  <br/> |El permiso de seguridad global no es válido.  <br/> |
|SecurityInvalidCategoryPermission = 19010  <br/> |El permiso de categoría de seguridad no es válido.  <br/> |
|SecurityUpdatedGroupNotFound = 19013  <br/> |No se ha encontrado el grupo de seguridad actualizado.  <br/> |
|SecurityUpdatedCategoryNotFound = 19014  <br/> |No se ha encontrado la categoría de seguridad actualizada.  <br/> |
|SecurityUpdatedTemplateNotFound = 19015  <br/> |No se ha encontrado la plantilla de seguridad actualizada.  <br/> |
|SecurityGroupMemberNotFound = 19016  <br/> |No se ha encontrado el miembro del grupo de seguridad.  <br/> |
|SecurityUserNotFound = 19018  <br/> |No se ha encontrado el usuario de Project Server.  <br/> |
|SecurityNoCategoryRelationForPermission = 19019  <br/> |No se ha encontrado la relación de la categoría de seguridad del permiso.  <br/> |
|SecurityCannotDeleteDefaultGroup = 19020  <br/> |No se puede eliminar el grupo de seguridad predeterminado.  <br/> |
|SecurityCannotDeleteDefaultCategory = 19021  <br/> |No se puede eliminar la categoría de seguridad predeterminada.  <br/> |
|SecurityCategoryCouldNotBeCreated = 19022  <br/> |No se puede crear la categoría de seguridad.  <br/> |
|SecurityNoCategoryForPermission = 19023  <br/> |No se ha encontrado la categoría de seguridad del permiso.  <br/> |
|SecurityNoCategoryForObject = 19024  <br/> |No se ha encontrado la categoría de seguridad del objeto.  <br/> |
|SecurityNoCategoryForRule = 19025  <br/> |No se ha encontrado la categoría de seguridad de la regla.  <br/> |
|SecurityNoGroupForPermission = 19026  <br/> |No se ha encontrado el grupo de seguridad del permiso.  <br/> |
|SecurityCannotSetPermissionForFieldGroup = 19027  <br/> |No se puede establecer el permiso para el campo de grupo de seguridad.  <br/> |
|SecurityInvalidFieldGroup = 19028  <br/> |El campo de grupo de seguridad no es válido.  <br/> |
|SecurityCannotSetOrgPermission = 19029  <br/> |No se puede establecer el permiso de organización de seguridad.  <br/> |
|SecurityInvalidOrgPermission = 19030  <br/> |El permiso de organización de seguridad no es válido.  <br/> |
|SecurityInvalidSecurityRule = 19031  <br/> |La regla de seguridad no es válida.  <br/> |
|SecurityTemplateNotFound = 19034  <br/> |No se ha encontrado la plantilla de seguridad.  <br/> |
|SecurityInvalidObjectType = 19035  <br/> |El tipo de objeto de seguridad no es válido.  <br/> |
|SecurityDuplicateUid = 19036  <br/> |GUID de objeto de seguridad duplicado.  <br/> |
|SecurityObjectNotFound = 19037  <br/> |No se ha encontrado el objeto de seguridad.  <br/> |
|SecurityInvalidCategoryUidRef = 19080  <br/> |El GUID de categoría de seguridad no es válido.  <br/> |
|SecurityInvalidProjectUidRef = 19081  <br/> |El GUID de proyecto del objeto de seguridad no es válido.  <br/> |
|SecurityInvalidGroupUidRef = 19082  <br/> |El GUID de grupo de seguridad no es válido.  <br/> |
|SecurityInvalidUserUidRef = 19083  <br/> |El GUID de usuario del objeto de seguridad no es válido.  <br/> |
|SecurityInvalidCategoryPermissionUidRef = 19084  <br/> |El GUID de permiso de la categoría de seguridad no es válido.  <br/> |
|SecurityInvalidGlobalPermissionUidRef = 19085  <br/> |El GUID de permiso global de seguridad no es válido.  <br/> |
|SecurityInvalidResourceUidRef = 19086  <br/> |El GUID de recurso del objeto de seguridad no es válido.  <br/> |
|SecurityDeleteNotSupportedBySetMethod = 19087  <br/> |El método no puede eliminar el objeto de seguridad.  <br/> |
|SecurityInvalidProjectCategoryPermissionUidRef = 19088  <br/> |El GUID de permiso de categoría de proyecto no es válido.  <br/> |
|SecurityCannotModifyCoreProjectCategoryDataInUpdate = 19089  <br/> |El método de actualización de seguridad no puede modificar los datos de categoría de proyecto principales.  <br/> |
|SecurityProjectCategoryEntitiesDoNotAllowInPlaceChanges = 19090  <br/> |Las entidades de categoría de seguridad no pueden modificarse en una actualización.  <br/> |
|SecurityCategoryCannotAddRelationForDeletedCategory = 19091  <br/> |No se puede agregar una relación de una categoría de seguridad eliminada.  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedCategory = 19092  <br/> |No se puede agregar un permiso de una categoría de seguridad eliminada.  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedRelation = 19093  <br/> |No se puede agregar un permiso de una relación de categoría de seguridad eliminada.  <br/> |
|SecurityCategoryCannotDeleteRelationForNewlyAddedCategory = 19094  <br/> |No se puede eliminar la relación de una categoría de seguridad recién agregada.  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedCategory = 19095  <br/> |No se puede eliminar el permiso de una categoría de seguridad recién agregada.  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedRelation = 19096  <br/> |No se puede eliminar el permiso de una relación recién agregada en una categoría de seguridad.  <br/> |
|SecurityCategoryCannotHaveDuplicateUserOrGroupUidsForRelation = 19097  <br/> |No se puede tener un usuario o un UID de grupo duplicado de una relación de categoría de seguridad.  <br/> |
|SecurityCategoryPermissionMustHaveMatchingRelation = 19098  <br/> |Un permiso de categoría debe tener asociada la relación de categoría de seguridad correspondiente.  <br/> |
|SecurityCategoryProjectAlreadyHasSecurityProjectCategory = 19099  <br/> |La lista de categorías seleccionados ya contiene una categoría de seguridad del proyecto.  <br/> |

<a name="pj15_ErrorCodes_Events"></a>

## <a name="table-24-project-server-event"></a>Table 24. Evento de Project Server

|Código de error del evento de Project Server|Descripción|
|:-----|:-----|
|ServerEventInvalidEventId = 19033  <br/> |El número de identificación de evento de Project Server no es válido.  <br/> |
|ServerEventServiceNotFound = 22003  <br/> |No se encontró el Servicio de eventos de Project Server. Este error no se usa en el código de Project Server, sino que remite a un evento del Servicio de registro unificado (ULS) sin formato.  <br/> |
|ServerEventRemoteCouldNotReachProxy = 22005  <br/> |El Project Web App remoto no puede acceder al proxy del Administrador de eventos de Project Server. Este error no se usa en el código de Project Server, pero está asignado a un evento sin procesar del ULS.  <br/> |
|ServerEventManagerCouldNotReachRemote = 22006  <br/> |El Administrador de eventos de Project Server no ha podido acceder al Project Web App remoto. Este error no se usa en el código de Project Server, pero está asignado a un evento sin procesar del ULS.  <br/> |
|ServerEventHandlerNotSigned = 22007  <br/> |El controlador de eventos de Project Server no está firmado.  <br/> |
|ServerEventHandlerMalformedAssemblyName = 22008  <br/> |El nombre de ensamblado del controlador de eventos de Project Server no es válido.  <br/> |
|ServerEventHandlerOrderInvalid = 22009  <br/> |El orden del controlador de eventos de Project Server no es válido.  <br/> |
|ServerEventHandlerDuplicateEntry = 22010  <br/> |Entrada duplicada del controlador de eventos de Project Server.  <br/> |
|ServerEventHandlerNotFound = 22011  <br/> |No se ha encontrado el controlador de eventos de Project Server.  <br/> |
|ServerEventHandlerDuplicateName = 22012  <br/> |Nombre duplicado del controlador de eventos de Project Server.  <br/> |
|ServerEventHandlerNullAssemblyNameAndEndpointUrl = 22013  <br/> |Valide que hay una dirección URL de extremo o un nombre de ensamblado.  <br/> |

<a name="pj15_ErrorCodes_Statusing"></a>

## <a name="table-25-statusing-web-service"></a>Tabla 25. Servicio web del estado 

|Código de error del servicio web del estado|Descripción|
|:-----|:-----|
|StatusingInvalidEntity = 3102  <br/> |La entidad de **Statusing** no es válida.  <br/> |
|StatusingGetDataForTaskFailed = 3103  <br/> |No se pudo obtener datos del estado de las tareas.  <br/> |
|StatusingGetTaskOrAssnCntrFailed = 3104  <br/> |No se pudo obtener la tarea o el centro de asignación del estado.  <br/> |
|StatusingInvalidPIDForProjCntr = 3105  <br/> |El número de identificación de la propiedad **Statusing** para el Centro de proyectos no es válido.  <br/> |
|StatusingDeleteAssnFailed = 3106  <br/> |No se pudo eliminar la asignación en el proceso de **Statusing**.  <br/> |
|StatusingAssnSaveFailed = 3107  <br/> |No se pudo guardar la asignación en el proceso de **Statusing**.  <br/> |
|StatusingTaskSaveFailed = 3108  <br/> |No se pudo guardar la tarea en el proceso de **Statusing**.  <br/> |
|StatusingInvalidPID = 3109  <br/> |El número de identificación de la propiedad **Statusing** no es válido.  <br/> |
|StatusingSetDataValueInvalid = 3111  <br/> |El valor de los datos de **Statusing** no es válido.  <br/> |
|StatusingSetDataFailed = 3112  <br/> |No se pudo establecer el valor de los datos de **Statusing**.  <br/> |
|StatusingInvalidDelegationStart = 3113  <br/> |La hora de inicio de una asignación en el método **DelegateAssignments** no es válida.  <br/> |
|StatusingApprovalUpdateFailed = 3114  <br/> |No se pudo actualizar la aprobación del estado.  <br/> |
|StatusingInvalidApprovalType = 3115  <br/> |El tipo de aprobación del estado no es válido.  <br/> |
|StatusingInternalError = 3116  <br/> |Error de procesamiento interno en un método de **Statusing**.  <br/> |
|StatusingInvalidUpdateData = 3117  <br/> |Los datos de actualización de un método de **Statusing** no son válidos.  <br/> |
|StatusingProjectUpdateFailed = 3118  <br/> |Error en la actualización de **Statusing** del proyecto.  <br/> |
|StatusingInvalidPreviewData = 3119  <br/> |Los datos de previsualización de **Statusing** no son válidos.  <br/> |
|StatusingInvalidTransaction = 3120  <br/> |La transacción de **Statusing** no es válida.  <br/> |
|StatusingTooManyResults = 3121  <br/> |Demasiados resultados. Se podrían devolver más de 5000 filas al leer los datos de estado de la fase temporal.  <br/> |
|StatusingInvalidInterval = 3122  <br/> |El intervalo de un método de **Statusing** no es válido. El intervalo debe estar en minutos y debe ser mayor que cero.<br/> |
|StatusingApplyUpdatesFailed = 3123  <br/> |No se pudieron aplicar las actualizaciones de **Statusing** mientras se ponía en cola la solicitud.  <br/> |
|StatusingApplyUpdatesFailure = 3124  <br/> |No se pudieron aplicar las actualizaciones de **Statusing** durante el procesamiento de la cola.  <br/> |
|StatusingInvalidWorkData = 3125  <br/> |Los datos de trabajo de **Statusing** no son válidos.  <br/> |
|StatusingMissingNameAttribute = 3126  <br/> |Falta el atributo de nombre para **Statusing**.  <br/> |
|StatusingInvalidNameAttribute = 3127  <br/> |El atributo de nombre de **Statusing** no es válido.  <br/> |
|StatusingInvalidData = 3128  <br/> |Los datos de **Statusing** no son válidos.  <br/> |
|StatusingInvalidChangelist = 3130  <br/> |Los datos XML no son válidos en el parámetro _changexml_ del método **UpdateStatus**.  <br/> |
|StatusingInsufficientAssignmentRights = 3131  <br/> |**SetAssignmentWorkData** no puede actualizar una asignación porque el usuario no tiene permisos.  <br/> |
|StatusingInvalidChangeNumber = 3132  <br/> |El número de cambio de **Statusing** no es válido.  <br/> |
|StatusingPidNotEditable = 3133  <br/> |El número de identificación de la propiedad **Statusing** no se puede editar.  <br/> |
|StatusingCannotSetTimephasedDataInManualTasks = 3134  <br/> |No se pueden establecer datos con fases temporales en las tareas manuales para **Statusing**.  <br/> |
|StatusingCannotChangeTaskMode = 3135  <br/> |No se puede cambiar el modo de tarea para **Statusing**.  <br/> |
   
Los códigos de error de la Tabla 26 son para los métodos **StatusReports** del servicio web de **PWA**. Son de uso interno en Project Web App. 

<a name="pj15_ErrorCodes_StatusReports"></a>

## <a name="table-26-statusreports"></a>Tabla 26. Informes de estado 

|Código de error del informe de estado|Descripción|
|:-----|:-----|
|StatusReportsUnknownError = 12100  <br/> |Error desconocido en **StatusReports**.  <br/> |
|StatusReportsPeriodUnmatched = 12101  <br/> |No se puede indicar el período del informe de estado correspondiente.  <br/> |
|StatusReportsPeriodUnavailable = 12102  <br/> |El período del informe de estado no se encuentra disponible.  <br/> |
|StatusReportsInvalidFormInput = 12103  <br/> |Los datos del formulario del informe de estado no son válidos.  <br/> |

<a name="pj15_ErrorCodes_Tasks"></a>

## <a name="table-27-task"></a>Tabla 27. Tarea 

|Código de error de la tarea|Descripción|
|:-----|:-----|
|TaskIDInvalid = 7001  <br/> |El GUID de tarea no es válido.  <br/> |
|TaskNameTooLong = 7003  <br/> |El nombre de la tarea es demasiado largo.  <br/> |
|TaskTypeInvalid = 7005  <br/> |El tipo de tarea no es válido.  <br/> |
|TaskPriorityInvalid = 7006  <br/> |La prioridad de la tarea no es válida.  <br/> |
|TaskConstraintTypeInvalid = 7007  <br/> |El tipo de restricción de la tarea no es válido.  <br/> |
|TaskNameInvalid = 7008  <br/> |El nombre de la tarea no es válido.  <br/> |
|TaskConstraintTypeRequiresConstraint = 7010  <br/> |La tarea necesita un tipo de restricción.  <br/> |
|TaskConstraintTypeCannotHaveConstraintDate = 7011  <br/> |No se puede tener una fecha de restricción para el tipo de restricción.  <br/> |
|TaskSummaryTaskCannotBeMilestone = 7013  <br/> |La tarea de resumen no puede ser un hito.  <br/> |
|TaskFixedCostAccrualInvalid = 7014  <br/> |La acumulación de costos fijos de una tarea no es válida.  <br/> |
|TaskPercentCompleteInvalid = 7015  <br/> |El valor del porcentaje completado de tarea no es válido.  <br/> |
|TaskWorkPercentCompleteInvalid = 7016  <br/> |El valor del porcentaje completado de trabajo de tarea no es válido.  <br/> |
|TaskPhysicalPercentCompleteInvalid = 7017  <br/> |El valor del porcentaje completado físico de tarea no es válido.  <br/> |
|TaskLinkTypeInvalid = 7018  <br/> |El tipo de vínculo de tarea no es válido.  <br/> |
|TaskAlreadyExists = 7019  <br/> |La tarea ya existe.  <br/> |
|TaskLinkAlreadyExists = 7020  <br/> |El vínculo de tarea ya existe.  <br/> |
|TaskNotFound = 7021  <br/> |No se ha encontrado la tarea.  <br/> |
|TaskLinkNotFound = 7022  <br/> |No se ha encontrado el vínculo de tarea.  <br/> |
|TaskLinkLagInvalid = 7023  <br/> |El tiempo de retardo de un vínculo de tarea no es válido.  <br/> |
|TaskUnableToInsert = 7025  <br/> |No se puede insertar una tarea.  <br/> |
|TaskAddPositionInvalid = 7026  <br/> |La posición para agregar una tarea no es válida.  <br/> |
|TaskOutlineLevelInvalid = 7027  <br/> |El nivel de esquema de tarea no es válido.  <br/> |
|TaskDurationFormatInvalid = 7028  <br/> |El formato de duración de tarea no es válido.  <br/> |
|TaskCannotAddWhereSpecified = 7029  <br/> |No se puede agregar la tarea en la posición especificada.  <br/> |
|TaskEarnedValueMethodInvalid = 7030  <br/> |El método para el valor acumulado de la tarea no es válido.  <br/> |
|TaskCannotModifyProjectSummary = 7031  <br/> |No se puede modificar la tarea de resumen del proyecto.  <br/> |
|TaskCannotDeleteProjectSummary = 7032  <br/> |No se puede eliminar la tarea de resumen del proyecto.  <br/> |
|TaskCannotSetActualCost = 7033  <br/> |No se puede establecer el costo real de la tarea.  <br/> |
|TaskLevelingDelayInvalid = 7034  <br/> |El retraso por redistribución de una tarea no es válido.  <br/> |
|TaskCannotEditSummary = 7035  <br/> |No se puede editar la tarea de resumen.  <br/> |
|TaskCannotCreateSubTasksUnderTasksWithAssignments = 7036  <br/> |No se pueden crear subtareas para una tarea que tiene asignaciones.  <br/> |
|TaskCannotDeleteSubProject = 7037  <br/> |No se puede eliminar un subproyecto de la tarea.  <br/> |
|TaskCannotEditExternal = 7038  <br/> |No se puede editar la tarea externa.  <br/> |
|TaskCannotDeleteExternal = 7039  <br/> |No se puede eliminar una tarea externa.  <br/> |
|TaskLinkCannotDeleteExternal = 7040  <br/> |No se puede eliminar un vínculo a una tarea externa.  <br/> |
|TaskCannotModifyNullTask = 7041  <br/> |No se puede modificar una tarea nula.  <br/> |
|TaskCannotModifyLeafTaskWithNoAssignment = 7042  <br/> |No se puede modificar una tarea hoja que no tiene ninguna asignación.  <br/> |
|TaskCannotModifyExternalTask = 7043  <br/> |No se puede modificar una tarea externa.  <br/> |
|TaskStatusManagerInvalid = 7044  <br/> |El administrador del estado de la tarea no es válido.  <br/> |
|TaskLinkCyclicDependency = 7045  <br/> |El vínculo de tarea tiene una dependencia cíclica.  <br/> |
|TaskCannotCreateOrModifySubTasksUnderTasksWithAssignments = 7046  <br/> |No se pueden crear ni modificar subtareas en una tarea de resumen que tiene asignaciones.  <br/> |
|TaskLinkCannotEditExternal = 7047  <br/> |No se puede editar el vínculo a una tarea externa.  <br/> |

<a name="pj15_ErrorCodes_Timesheets"></a>

## <a name="table-28-timesheet"></a>Tabla 28. Parte de horas 

|Código de error del parte de horas|Descripción|
|:-----|:-----|
|TimesheetMaxHourPerDayExceeded = 3201  <br/> |Se ha excedido el número máximo de horas por día para el parte de horas.  <br/> |
|TimesheetHoursPerTSLimitExceeded = 3202  <br/> |Se ha excedido el límite de número de horas en un parte de horas.  <br/> |
|TimesheetUnverifiedTSLineNotAllowed = 3203  <br/> |En este caso no se permite una línea de parte de horas sin verificar.  <br/> |
|TimesheetIncorrectMode = 3204  <br/> |El modo de parte de horas no es válido.  <br/> |
|TimesheetInvalidApprover = 3205  <br/> |El aprobador del parte de horas no es válido.  <br/> |
|TimesheetFutureReportingNotAllowed = 3206  <br/> |No se permiten los informes de elementos futuros para el parte de horas.  <br/> |
|TimesheetIncorrectPeriod = 3208  <br/> |El período del parte de horas no es válido.  <br/> |
|TimesheetPeriodClosed = 3209  <br/> |Período de parte de horas cerrado.  <br/> |
|TimesheetPendingLines = 3210  <br/> |Hay líneas pendientes en el parte de horas.  <br/> |
|TimesheetInvalidDateRange = 3211  <br/> |El intervalo de fechas del parte de horas no es válido.  <br/> |
|TimesheetLineClassDisabled = 3212  <br/> |La clase de la línea del parte de horas está deshabilitada.  <br/> |
|TimesheetLineHasNonExistentItem = 3213  <br/> |La línea del parte de horas incluye un elemento que no existe.  <br/> |
|TimesheetLineInvalidStatus = 3214  <br/> |El estado de la línea del parte de horas no es válido.  <br/> |

<a name="pj15_ErrorCodes_UserDelegation"></a>

## <a name="table-29-user-delegation"></a>Tabla 29. Delegación de usuarios 

|Código de error de la delegación de usuarios|Descripción|
|:-----|:-----|
|UserDelegationExpired = 43000  <br/> |La delegación de usuario ha expirado.  <br/> |
|UserDelegationCannotSelfDelegate = 43001  <br/> |Un usuario no se puede designar a sí mismo como delegado.  <br/> |
|UserDelegationInvalidDelegate = 43002  <br/> |El delegado de usuario no es válido.  <br/> |
|UserDelegationInvalidUser = 43003  <br/> |El usuario no es válido para la delegación.  <br/> |
|UserDelegationInvalidDates = 43004  <br/> |Las fechas de delegación de usuario no son válidas.  <br/> |
|UserDelegationCannotDoubleDelegate = 43005  <br/> |No se pueden crear dos delegados.  <br/> |
|UserDelegationDelegateCannotLogon = 43006  <br/> |El delegado de usuario no puede iniciar sesión en Project Server.  <br/> |
|UserDelegationDelegateIsInactive = 43007  <br/> |El delegado de usuario está inactivo.  <br/> |
|UserDelegationInvalidFilter = 43008  <br/> |El filtro de delegado de usuario no es válido.  <br/> |
|UserDelegationUserCannotLogon = 43010  <br/> |El usuario no puede iniciar sesión en Project Server.  <br/> |
|UserDelegationUserIsInactive = 43011  <br/> |El delegado de usuario está inactivo.  <br/> |

<a name="pj15_ErrorCodes_Workflow"></a>

## <a name="table-30-workflow"></a>Tabla 30. Flujo de trabajo 

|Código de error del flujo de trabajo|Descripción|
|:-----|:-----|
|WorkflowPhasesCannotCreatePhase = 35000  <br/> |No se puede crear la fase de flujo de trabajo.  <br/> |
|WorkflowPhasesCannotUpdatePhase = 35001  <br/> |No se puede actualizar la fase de flujo de trabajo.  <br/> |
|WorkflowPhasesCannotDeletePhase = 35002  <br/> |No se puede eliminar la fase de flujo de trabajo.  <br/> |
|WorkflowPhaseNameIsRequired = 35003  <br/> |El flujo de trabajo [PHASE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_NAME.aspx) es obligatorio.  <br/> |
|WorkflowStagesCannotCreateStage = 35004  <br/> |No se puede crear la etapa de flujo de trabajo.  <br/> |
|WorkflowStagesCannotUpdateStage = 35005  <br/> |No se puede actualizar la etapa de flujo de trabajo.  <br/> |
|WorkflowStagesCannotDeleteStage = 35006  <br/> |No se puede eliminar la etapa de flujo de trabajo.  <br/> |
|WorkflowStagesProjectsInStage = 35007  <br/> |Hay proyectos en la etapa de flujo de trabajo.  <br/> |
|WorkflowCannotAccessPDPLibrary = 35008  <br/> |No se puede tener acceso a la biblioteca de página de detalles del proyecto.  <br/> |
|WorkflowInvalidPDPUid = 35009  <br/> |El GUID de página de detalles del proyecto no es válido.  <br/> |
|WorkflowInvalidCustomFieldUid = 35010  <br/> |El GUID de campo personalizado no es válido.  <br/> |
|WorkflowCustomFieldNotWorkflowControlled = 35011  <br/> |El campo personalizado no está controlado por un flujo de trabajo.  <br/> |
|WorkflowCustomFieldCannotBeRequiredAndReadOnly = 35012  <br/> |El campo personalizado del flujo de trabajo no puede ser obligatorio y de solo lectura simultáneamente.  <br/> |
|WorkflowInvalidWorkflowPhaseUid = 35013  <br/> |El flujo de trabajo [PHASE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_UID.aspx) no es válido.  <br/> |
|WorkflowInsertWorkflowPhaseNotAllowed = 35014  <br/> |No se puede insertar una fase de flujo de trabajo.  <br/> |
|WorkflowInvalidWorkflowStageUid = 35015  <br/> |El flujo de trabajo [STAGE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_UID.aspx) no es válido.  <br/> |
|WorkflowPhaseHasStages = 35016  <br/> |La fase de flujo de trabajo tiene etapas.  <br/> |
|WorkflowStageNameIsRequired = 35020  <br/> |El flujo de trabajo [STAGE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_NAME.aspx) es obligatorio.  <br/> |
|WorkflowStageAtLeastOnePDPIsRequired = 35021  <br/> |Es obligatorio que haya al menos una página de detalles del proyecto para la etapa del flujo de trabajo.  <br/> |
|WorkflowCannotStartWorkflow = 35100  <br/> |No se puede iniciar el flujo de trabajo.  <br/> |
|WorkflowStatusCannotUpdateStatus = 35101  <br/> |No se puede actualizar el estado del flujo de trabajo.  <br/> |
|WorkflowOnlyProjectsHaveWorkflow = 35102  <br/> |Solo los proyectos pueden tener un flujo de trabajo.  <br/> |
|WorkflowNoWorkflowsDefined = 35103  <br/> |No se ha definido ningún flujo de trabajo.  <br/> |
|WorkflowInvalidStageForProject = 35104  <br/> |La etapa del flujo de trabajo para el proyecto no es válida.  <br/> |
|WorkflowNoWorkflowForProject = 35105  <br/> |El proyecto no tiene un flujo de trabajo.  <br/> |
|WorkflowCheckinRequiredAndProjectNotCheckedin = 35106  <br/> |El proyecto debe estar protegido para que funcione el flujo de trabajo.  <br/> |
|WorkflowWaitingForRequiredData = 35107  <br/> |El flujo de trabajo está esperando los datos obligatorios.  <br/> |
|WorkflowFlagCustomFieldsCannotBeRequired = 35108  <br/> |Un campo personalizado de marca no puede ser obligatorio en un flujo de trabajo.  <br/> |
|WorkflowCannotChangeWorkflow = 35109  <br/> |No se puede modificar el flujo de trabajo.  <br/> |
|WorkflowWorkflowStatusPDPNotAllowed = 35110  <br/> |No se permite el uso de la página de detalles del proyecto para el estado de flujo de trabajo.  <br/> |
|WorkflowInvalidWorkflowStatusPDPUid = 35111  <br/> |El GUID de la página de detalles del proyecto del estado de flujo de trabajo no es válido.  <br/> |
|WorkflowInvalidStageStatusValue = 35112  <br/> |El valor de la fase de flujo de trabajo no es válido. Cuando se establece el estado de la fase en el flujo de trabajo, solo se permiten los valores **InProgressRequestSent**, **InProgressRunning** o **InProgressWaiting** en [Workflow.StageStatus](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Workflow.StageStatus.aspx).  <br/> |
|WorkflowCannotCheckinNotify = 35113  <br/> |No se puede notificar al flujo de trabajo que el proyecto está protegido.  <br/> |
|WorkflowCannotCommitNotify = 35114  <br/> |No se puede notificar al flujo de trabajo que el proyecto está confirmado dentro del Organizador o el Optimizador.  <br/> |
|WorkflowExceptionStartingWorkflow = 35115  <br/> |Se ha producido un error al iniciar el flujo de trabajo.  <br/> |
|WorkflowStatusPDPMustBeSupplied = 35116  <br/> |Es obligatorio que haya una página de detalles de proyecto para el estado del flujo de trabajo.  <br/> |
|WorkflowWorkflowProxyAccountNotFound = 35117  <br/> |No se ha encontrado la cuenta proxy del flujo de trabajo.  <br/> |
|WorkflowInvalidCurrentStage = 35118  <br/> |La etapa actual del flujo de trabajo no es válida.  <br/> |
|WorkflowMultipleStagesInProgress = 35119  <br/> |Hay varias etapas en curso en el flujo de trabajo.  <br/> |
|WorkflowActivityInvalidArgument = 35120  <br/> |El mensaje que se recibe si una actividad de flujo de trabajo recibida no es válida.  <br/> |
|WorkflowMTWConfigurationError = 35121  <br/> |Error de configuración de Microsoft Azure Workflow.  <br/> |
|EnterpriseProjectTypeInvalidEnterpriseProjectTypeUid = 35200  <br/> |La propiedad **ENTERPRISE_PROJECT_TYPE_UID** no es válida.  <br/> |
|EnterpriseProjectTypeCannotCreateEnterpriseProjectType = 35201  <br/> |No se puede crear el tipo de proyecto empresarial.  <br/> |
|EnterpriseProjectTypeCannotUpdateEnterpriseProjectType = 35202  <br/> |No se puede actualizar el tipo de proyecto empresarial.  <br/> |
|EnterpriseProjectTypeCannotDeleteEnterpriseProjectType = 35203  <br/> |No se puede eliminar el tipo de proyecto empresarial.  <br/> |
|EnterpriseProjectTypeCannotCreateMultipleEnterpriseProjectTypes = 35204  <br/> |No se pueden crear varios tipos de proyectos empresariales.  <br/> |
|EnterpriseProjectTypeCannotUpdateMultipleEnterpriseProjectTypes = 35205  <br/> |No se pueden actualizar varios tipos de proyectos empresariales.  <br/> |
|EnterpriseProjectTypeInvalidCreatePDPUid = 35206  <br/> |Una plantilla de proyecto empresarial (EPT) requiere una página de detalles del proyecto (PDP) asociada para crear un proyecto con la EPT. Si la EPT es para un flujo de trabajo, este error se produce durante su validación cuando la página de detalles del proyecto (PDP) no es del tipo *Create*. Otros tipos de PDP son: *Normal*, para editar un proyecto, y *Workflow Status*, para mostrar los detalles de un proyecto de flujo de trabajo.  <br/> |
|EnterpriseProjectTypeInvalidProjectPlanTemplateUid = 35207  <br/> |La propiedad [ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID.aspx) no es válida.  <br/> |
|EnterpriseProjectTypeInvalidWorkspaceTemplateName = 35208  <br/> |La propiedad [ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME.aspx) no es válida.  <br/> |
|EnterpriseProjectTypeInvalidWorkflowAssociationUid = 35209  <br/> |La propiedad [WORKFLOW_ASSOCIATION_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.WORKFLOW_ASSOCIATION_UID.aspx) no es válida.  <br/> |
|EnterpriseProjectTypeCannotReadWssSettings = 35210  <br/> |No se puede leer la configuración de SharePoint.  <br/> |
|EnterpriseProjectTypeCannotReadWssLanguagesAndTemplates = 35211  <br/> |No se pueden leer los idiomas y las plantillas de sitio de SharePoint.  <br/> |
|EnterpriseProjectTypeInvalidDepartmentUid = 35212  <br/> |La propiedad [DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.DEPARTMENT_UID.aspx) no es válida.  <br/> |
|EnterpriseProjectTypeInvalidUri = 35213  <br/> |La propiedad [ENTERPRISE_PROJECT_TYPE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.ENTERPRISE_PROJECT_TYPE_UID.aspx) no es válida.  <br/> |
|EnterpriseProjectTypeUriRequiresHttp = 35214  <br/> |El URI de tipo de proyecto empresarial exige el uso del protocolo HTTP.  <br/> |
|EnterpriseProjectTypeCannotDeleteDefault = 35215  <br/> |No se puede eliminar el tipo de proyecto empresarial predeterminado.  <br/> |
|EnterpriseProjectTypeCannotChangeDefault = 35216  <br/> |No se puede modificar el tipo de proyecto empresarial predeterminado.  <br/> |
|EnterpriseProjectTypeHasProjectsCannotDelete = 35217  <br/> |No se puede eliminar un tipo de proyecto empresarial que tiene proyectos.  <br/> |
|EnterpriseProjectTypeCreatePDPIsRequired = 35218  <br/> |Una plantilla de proyecto empresarial (EPT) para un flujo de trabajo requiere una página de detalles del proyecto (PDP) asociada de tipo *Create* para crear un proyecto con la EPT. Este error se produce cuando la PDP no está incluida en la definición de la EPT. Otros tipos de PDP son: *Normal*, para editar un proyecto, y *Workflow Status*, para mostrar los detalles de un proyecto de flujo de trabajo.  <br/> |
|EnterpriseProjectTypeOnlyOneCreatePDPAllowed = 35219  <br/> |La definición de la EPT solo permite una página de detalles del proyecto de tipo *Create*.  <br/> |
|EnterpriseProjectTypeHasWorkflowOnlyCreatePDPAllowed = 35220  <br/> |Una plantilla de proyecto empresarial (EPT) para un flujo de trabajo requiere una página de detalles del proyecto (PDP) asociada de tipo *Create* para crear un proyecto con la EPT. Este error se produce cuando la PDP en la definición de la EPT del flujo de trabajo es de otro tipo. Otros tipos de PDP son: *Normal*, para editar un proyecto, y *Workflow Status*, para mostrar los detalles de un proyecto de flujo de trabajo.  <br/> |
|EnterpriseProjectTypeInvalidData = 35221  <br/> |La clase **WorkflowDataSet** para el tipo de proyecto empresarial contiene datos que no son válidos.  <br/> |
|EnterpriseProjectNoDefaultEnterpriseProjectTypeDefined = 35222  <br/> |No hay ningún tipo de proyecto empresarial predeterminado definido.  <br/> |
|EnterpriseProjectTypeAtLeastOnePDPIsRequired = 35223  <br/> |Es obligatorio que haya al menos una página de detalles del proyecto para el tipo de proyecto empresarial.  <br/> |
|EnterpriseProjectTypeWorkflowStatusPDPNotAllowed = 35224  <br/> |Una página de detalles del proyecto para el estado del flujo de trabajo no está permitida para el tipo de proyecto empresarial.  <br/> |
|EnterpriseProjectTypeCannotChangeWorkflowAssociation = 35225  <br/> |El proyecto ya tiene un tipo de proyecto empresarial (EPT); no puede cambiar la EPT del proyecto.  <br/> |

<a name="pj15_ErrorCodes_WSS"></a>

## <a name="table-31-wssinterop-and-objectlinkprovider-sharepoint-integration"></a>Tabla 31. WssInterop y ObjectLinkProvider (integración de SharePoint)

|Código de error de integración de SharePoint|Descripción|
|:-----|:-----|
|WSSCreateSiteFailure = 16400  <br/> |No se pudo crear un sitio de SharePoint para el área de trabajo de un proyecto.  <br/> |
|WSSCannotCreateWebWithBlankName = 16401  <br/> |No se puede crear un sitio web de SharePoint con un nombre en blanco.  <br/> |
|WSSWebAlreadyExists = 16402  <br/> |El sitio web de SharePoint ya existe.  <br/> |
|WSSInvalidProjectUID = 16403  <br/> |El GUID de proyecto no es válido para el área de trabajo del proyecto de SharePoint.  <br/> |
|WSSProjectAlreadyHasSpWeb = 16404  <br/> |El proyecto ya tiene un sitio de área de trabajo de SharePoint.  <br/> |
|WSSWebDoesNotExist = 16405  <br/> |El sitio web de SharePoint no existe.  <br/> |
|WSSSpWebAlreadyLinkedToProject = 16406  <br/> |El sitio web de SharePoint ya está vinculado a un proyecto.  <br/> |
|WSSWebHierarchyDoesNotExist = 16407  <br/> |La jerarquía web de SharePoint no existe.  <br/> |
|WSSSPWebHasChildren = 16408  <br/> |La web de SharePoint tiene webs secundarias.  <br/> |
|WSSURIInvalidFormat = 16409  <br/> |El formato del URI de la web de SharePoint no es válido.  <br/> |
|WSSSyncReportingDataFailed = 16410  <br/> |No se pudieron sincronizar los datos de informes de SharePoint.  <br/> |
|WSSWorkspaceUrlPathTooLong = 16411  <br/> |La ruta de la URL del área de trabajo del proyecto de SharePoint es demasiado larga.  <br/> |
|WSSWorkspaceNameContainsIllegalChars = 16412  <br/> |Uno o varios caracteres del nombre de un sitio de proyecto de SharePoint no son válidos. Los siguientes caracteres no son válidos en un nombre de proyecto: / " : \< \> | , . ' ? \* #  <br/> |
|WSSInvalidWssServerUid = 16413  <br/> |El GUID de servidor SharePoint no es válido.  <br/> |
|WSSSyncUsersFailed = 16414  <br/> |No se pudieron sincronizar los usuarios de Project Server con SharePoint.  <br/> |
|WSSWrongWebTemplateLCID = 16415  <br/> |El identificador de configuración regional (Id. de idioma) de la plantilla web de SharePoint no es válido.  <br/> |
|WSSWrongWebTemplate = 16416  <br/> |La plantilla web de SharePoint no es válida.  <br/> |
|WSSWebIsNotProjectWorkspace = 16417  <br/> |El sitio web de SharePoint no es un área de trabajo de proyectos.  <br/> |
|WSSWebCannotStartOrEndOnPeriod = 16418  <br/> |El nombre de una web de SharePoint no puede comenzar ni terminar con un punto.  <br/> |
|WSSCannotDeleteSiteCollection = 16419  <br/> |No se puede eliminar la colección de sitios web.  <br/> |
|WSSListUidInvalid = 16420  <br/> |El GUID de lista de SharePoint no es válido.  <br/> |
|WSSSyncDataSetListUidMismatch = 16421  <br/> |El GUID de lista de SharePoint no coincide con el GUID de lista en la sincronización de **DataSet**.  <br/> |
|WSSSyncDataSetMissingProjectSettingsRow = 16422  <br/> |Falta la fila de configuración del proyecto en **DataSet** para la sincronización con SharePoint.  <br/> |
|WSSSyncDataSetTaskMappingsNotAllowed = 16423  <br/> |No se permiten las asignaciones de tareas en **DataSet** para la sincronización con SharePoint.  <br/> |
|WSSSyncDataSetWssListUidEmpty = 16424  <br/> |El GUID de lista de SharePoint está vacío en **DataSet** para la sincronización con SharePoint.  <br/> |
|WSSSyncDataNotFound = 16425  <br/> |Faltan datos en la sincronización con SharePoint.  <br/> |
|WSSSyncCriticalDataValidationError = 16426  <br/> |Se ha producido un error de validación de datos grave en la sincronización con SharePoint.  <br/> |
|WSSSyncSharePointListNotAccessibleError = 16427  <br/> |No se puede tener acceso a la lista de SharePoint.  <br/> |
|WSSSyncInvalidEntityUids = 16428  <br/> |Los GUID de entidad no son válidos para la sincronización con SharePoint.  <br/> |
|WSSSyncInvalidSyncData = 16429  <br/> |La sincronización con SharePoint tiene datos que no son válidos.  <br/> |
|WSSSyncSPSummaryTaskAssignedToResourceError = 16430  <br/> |La sincronización con SharePoint tiene asignada una tarea de resumen a un recurso.  <br/> |
|WSSSyncInsufficientPermissionsToCreateWinUser = 16431  <br/> |Los permisos no son suficientes para crear un usuario de Windows cuando se está sincronizando con SharePoint.  <br/> |
|WSSSyncNoDefaultValueForCustomField = 16432  <br/> |Un campo personalizado no tiene un valor predeterminado en la sincronización con SharePoint.  <br/> |
|WSSOLPCreateLinkFailure = 18000  <br/> |No se pudo crear un vínculo para el proveedor de vínculos de objetos de SharePoint.  <br/> |
|WSSOLPDeleteWebObjectLinkError = 18001  <br/> |Error al eliminar un vínculo de objeto web en el proveedor de vínculos de objetos de SharePoint.  <br/> |
|WSSInvalidPermissionsToWssList = 18002  <br/> |Los permisos no son válidos para la lista de SharePoint.  <br/> |
|WSSWebIsNotUnderDefaultCollection = 18003  <br/> |La web de SharePoint no está en la colección predeterminada.  <br/> |
|WSSWorkspaceUrlIsNotUnderPrimaryCollection = 18004  <br/> |La dirección URL del área de trabajo especificada no está en la colección de sitios asociada a esta instancia de Project Server. Es un requisito del modo de permisos actual.  <br/> |
|WSSWorkspacesMustBeRestrictedToDefaultCollection = 18005  <br/> |Las áreas de trabajo deben restringirse a la colección de sitios predeterminada en el modo de permisos actual.  <br/> |

<a name="pj15_ErrorCodes_ASMXExample"> </a>

## <a name="error-code-example-for-asmx"></a>Ejemplo de códigos de error de ASMX

Para obtener una lista de errores si recibe una excepción cuando llama a un método de PSI, pase el objeto **SoapException** objeto al constructor de clases [Microsoft.Office.Project.Server.Library.PSClientError](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.aspx). Después, puede usar [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx) para almacenar la información de errores en una matriz **PSErrorInfo** y para enumerar los errores, como en el ejemplo siguiente. 
  
> [!NOTE]
> El objeto **PSErrorInfo** no incluye toda la información que puede necesitar. Por ejemplo, si usa **Resource.CheckOutResources** en cuando uno de los recursos ya está desprotegido, **PSErrorInfo** muestra el motivo del error para cada recurso que no se puede desproteger, pero no incluye el nombre del recurso ni el GUID. Para obtener más información sobre una aplicación basada en ASMX, consulte [CheckOutResources](https://msdn.microsoft.com/library/WebSvcResource.Resource.CheckOutResources.aspx). 
  
```cs
using System;
using System.Collections.Generic;
using System.Text;
using System.Web.Services.Protocols;
using System.Windows.Forms;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch (SoapException ex)
{
    string errAttributeName;
    string errAttribute;
    string errMess = "".PadRight(30, '=') + "\r\n" + "Error: " + "\r\n";
    PSLibrary.PSClientError error = new PSLibrary.PSClientError(ex);
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\n" + ex.Message.ToString() + "\r\n";
        errMess += "".PadRight(30, '=') + "\r\nPSCLientError Output:\r\n \r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName +
                       ": " + errAttribute;
        }
        errMess += "\r\n".PadRight(30, '=');
    }
    MessageBox.Show(errMess, "Error", MessageBoxButtons.OK,
        MessageBoxIcon.Error);
}
```

<a name="pj15_ErrorCodes_WCFExample"> </a>

## <a name="error-code-example-for-wcf"></a>Ejemplo de códigos de error de WCF

Para obtener una lista de errores si recibe una excepción **System.ServiceModel.FaultException** cuando llama a un método de PSI en una aplicación basada en WCF, puede extraer un objeto **PSClientError** desde el objeto ** FaultException**. Después, puede usar [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx) para almacenar la información de errores en una matriz **PSErrorInfo** y para enumerar los errores, como en el ejemplo anterior de ASMX. 
  
```cs
using System;
using System.Text;
using System.ServiceModel;
using System.Xml;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch(FaultException fault)
{
    // Use the WCF FaultException, because the ASMX SoapException does not 
    // exist in a WCF-based application.
    WriteFaultOutput(fault);
}
// Get a PSClientError object from the WCF FaultException object, and
// then display the exception details and each error in the PSClientError stack.
private static void WriteFaultOutput(FaultException fault)
{
    string errAttributeName;
    string errAttribute;
    string errOut;
    string errMess = "".PadRight(30, '=') + "\r\n"
        + "Error details: " + "\r\n";
    PSLibrary.PSClientError error = GetPSClientError(fault, out errOut);
    errMess += errOut;
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\r\n".PadRight(30, '=') + "\r\nPSClientError output:\r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName
                + ": " + errAttribute;
        }
    }
    Console.ForegroundColor = ConsoleColor.Red;
    Console.WriteLine(errMess);
    Console.ResetColor();
}
/// <summary>
/// Extract a PSClientError object from the ServiceModel.FaultException,
/// for use in output of the GetPSClientError stack of errors.
/// </summary>
/// <param name="e"></param>
/// <param name="errOut">Shows that FaultException has more information 
/// about the errors than PSClientError has. FaultException can also contain 
/// other types of errors, such as failure to connect to the server.</param>
/// <returns>PSClientError object, for enumerating errors.</returns>
public static PSLibrary.PSClientError GetPSClientError(FaultException e, 
                                                        out string errOut)
{
    const string PREFIX = "GetPSClientError() returns null: ";
    errOut = string.Empty;
    PSLibrary.PSClientError psClientError = null;
    if (e == null)
    {
        errOut = PREFIX + "Null parameter (FaultException e) passed in.";
        psClientError = null;
    }
    else
    {
        // Get a ServiceModel.MessageFault object.
        var messageFault = e.CreateMessageFault();
        if (messageFault.HasDetail)
        {
            using (var xmlReader = messageFault.GetReaderAtDetailContents())
            {
                var xml = new XmlDocument();
                xml.Load(xmlReader);
                var serverExecutionFault = xml["ServerExecutionFault"];
                if (serverExecutionFault != null)
                {
                    var exceptionDetails = serverExecutionFault["ExceptionDetails"];
                    if (exceptionDetails != null)
                    {
                        try
                        {
                            errOut = exceptionDetails.InnerXml + "\r\n";
                            psClientError = 
                                new PSLibrary.PSClientError(exceptionDetails.InnerXml);
                        }
                        catch (InvalidOperationException ex)
                        {
                            errOut = PREFIX + "Unable to convert fault exception info ";
                            errOut += "a valid Project Server error message. Message: \n\t";
                            errOut += ex.Message;
                            psClientError = null;
                        }
                    }
                    else
                    {
                        errOut = PREFIX + "The FaultException e is a ServerExecutionFault, "
                            + "but does not have ExceptionDetails.";
                    }
                }
                else
                {
                    errOut = PREFIX + "The FaultException e is not a ServerExecutionFault.";
                }
            }
        }
        else // No detail in the MessageFault.
        {
            errOut = PREFIX + "The FaultException e does not have any detail.";
        }
    }
    errOut += "\r\n" + e.ToString() + "\r\n";
    return psClientError;
}

```

<br/>

Además de los datos del objeto **PSClientError**, el objeto **FaultException** puede incluir otros tipos de errores, como un error en la conexión a Project Server. El parámetro _errOut_ del método **GetPSClientError** en el ejemplo anterior muestra información adicional. Por ejemplo, el ejemplo de código **CreateProject4Department** en el método [QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) incluye comentarios que muestran cómo crear errores al establecer las propiedades de la tabla ** ProjectCustomFields**. Cuando se ejecuta la aplicación, el parámetro _errOut_ incluye el elemento **errinfo** y otros datos (que aquí se formatea a partir del resultado de la consola). 
  
```XML
==============================
Error details:
<errinfo xmlns="">
  <dataset name="ProjectDataSet">
    <table name="ProjectCustomFields">
      <row CUSTOM_FIELD_UID="976d3bd9-95ff-40a2-a938-960c410b0341">
        <error id="11704" name="CustomFieldInvalidTypeColumnFilledIn" 
               uid="aa8a2fab-9262-422f-b022-ca1cb12bc75f"></error>
        <error id="11713" name="CustomFieldRequiredValueNotProvided" 
               uid="dc2e2156-86e9-4aac-bede-d07dc44dfedc"></error>
      </row>
    </table>
  </dataset>
</errinfo>
System.ServiceModel.FaultException`1[SvcProject.ServerExecutionFault]: 
ProjectServerError(s) LastError=CustomFieldRequiredValueNotProvided Instructions: 
Pass this into PSClientError constructor to access all error information 
(Fault Detail is equal to SvcProject.ServerExecutionFault).
============================
PSClientError output:
CustomFieldInvalidTypeColumnFilledIn
============================
PSClientError output:
CustomFieldRequiredValueNotProvided
```

<a name="pj15_ErrorCodes_AR"> </a>

## <a name="see-also"></a>Vea también

- [Artículos con conceptos e instrucciones de Project](project-conceptual-and-how-to-articles.md)
- [SQL Server Profiler](https://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx)
- [Project Server 2010: What to Expect when you get the Unexpected](https://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx) (Project Server 2010: Qué esperar cuando ocurre lo inesperado)
- [Visor de ULS](https://www.codeproject.com/Articles/458052/ULS-Log-Viewer)
    

