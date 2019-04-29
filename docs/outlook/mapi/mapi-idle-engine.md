---
title: Motor inActivo de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d8d591c02bb621c16a1d1b46272b19573ea79785
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428455"
---
# <a name="mapi-idle-engine"></a>Motor inActivo de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona varias funciones que se conocen colectivamente como el motor inactivo. Estas funciones permiten a los clientes, proveedores de la libreta de direcciones y proveedores de almacenamiento de mensajes realizar diversas tareas durante las horas lentas de la sesión o en respuesta a un tiempo lento. Por ejemplo, los clientes y los proveedores de servicios pueden diferir las operaciones lentas o cerrar archivos que se han mantenido sin usar durante un período prolongado. Por lo general, los proveedores de transporte no usan el motor inactivo porque el método **IXPLogon:: idle** toma su posición. Para obtener más información, vea [IXPLogon:: idle](ixplogon-idle.md).
  
Para usar el motor inactivo, los clientes y los proveedores de servicios crean una función de devolución de llamada que contiene las tareas que deben producirse cuando el subsistema MAPI está inactivo. Cuando MAPI detecta el tiempo de inactividad, invoca esta función de devolución de llamada. La función de devolución de llamada sigue el prototipo **FNIDLE** , que se define de la siguiente manera: 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Para obtener más información, vea [FNIDLE](fnidle.md).
  
Las funciones que componen el motor inactivo son:
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Para registrar una función de devolución de llamada, los clientes y los proveedores de servicios llaman a la función **FtgRegisterIdleRoutine** . Los parámetros de entrada incluyen una prioridad opcional, un bloque de memoria que se pasa a la función de devolución de llamada como entrada, una cantidad de tiempo que se va a usar de forma adecuada y un conjunto de indicadores de opción. 
  
Los clientes y los proveedores de servicios pueden especificar una prioridad en el parámetro _priIdle_ que controla cómo se ejecuta la función inactiva o especifica cero si Priority no es un problema. Como los números negativos representan prioridades más altas que los números positivos o cero, se deben asignar números negativos a las operaciones de compresión y de búsqueda. Las tareas que tienen lugar una vez se deben asignar números positivos. 
  
Para anular el registro de una función de devolución de llamada activa, los clientes y los proveedores de servicios llaman a la función **DeregisterIdleRoutine** . Dado que **DeregisterIdleRoutine** funciona de forma asincrónica, es posible que se invoque la función de devolución de llamada en cualquier momento durante la llamada a Register y, posiblemente, incluso después de que se devuelva **DeregisterIdleRoutine** . 
  
Para modificar algunas o todas las características de una función de devolución de llamada, los clientes y los proveedores de servicios llaman a la función **ChangeIdleRoutine** . **ChangeIdleRoutine** realiza cambios según la forma en que se establece el parámetro de indicadores _ircIdle_ ; **ChangeIdleRoutine** puede cambiar la función, su prioridad, la configuración de hora y el parámetro de entrada. 
  
MAPI define inactivamente el mismo que el sistema operativo, cuando el sistema operativo tiene una definición. En Win32, MAPI crea un subproceso con prioridad de clase inactiva para programar tareas inactivas. Este subproceso realiza un seguimiento de la hora y envía un mensaje al subproceso que va a ejecutar la tarea inactiva cuando llega la hora de su ejecución. Win32 programa subprocesos, no procesos. Si las tareas que tienen una prioridad superior a la prioridad de inactividad se producen en la estación de trabajo, la tarea inactiva no debería estar programada para su ejecución hasta que se completen las tareas. 
  
Todas las tareas inactivas se ejecutan en el subproceso que llamó a **MAPIInitIdle**. MAPI tiene un subproceso independiente para la programación, pero cuando una tarea inactiva se convierte en válida, envía un mensaje de vuelta al subproceso de inicialización y la tarea inactiva se ejecuta allí. Las implicaciones para los distintos tipos de clientes son las siguientes.
  
|**Modelo de subProcesos**|**Implicación**|
|:-----|:-----|
|Un solo subproceso  <br/> |Sin problemas. Las funciones inActivas se ejecutan en el subproceso principal del cliente y se serializan a través del bucle de mensajes.  <br/> |
|Subprocesamiento libre  <br/> |Las funciones inActivas deben ser seguras para subprocesos, pero su cliente ya tiene la infraestructura necesaria. Es posible que el cliente no necesite el motor inactivo de MAPI.  <br/> |
|De subprocesamiento controlado  <br/> |La función inActiva tiene que ejecutarse en el mismo subproceso que la registró si desea usar MAPI, OLE o cualquier otra interfaz COM. La forma más sencilla es registrar una función inactiva con MAPI que envíe un mensaje al hilo correcto y envíe la función inactiva "real" directamente desde el bucle de mensajes de ese subproceso.  <br/> |
   

