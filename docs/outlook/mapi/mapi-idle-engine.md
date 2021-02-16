---
title: Motor de inactividad MAPI
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
# <a name="mapi-idle-engine"></a>Motor de inactividad MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona varias funciones que se conocen colectivamente como motor inactivo. Estas funciones permiten a los clientes, proveedores de libretas de direcciones y proveedores de almacenamiento de mensajes realizar diversas tareas durante las horas lentas de la sesión o en respuesta a un tiempo lento. Por ejemplo, los clientes y proveedores de servicios pueden aplazar operaciones lentas o cerrar archivos que han estado sin usar durante un período prolongado. Los proveedores de transporte normalmente no usan el motor inactivo porque el **método IXPLogon::Idle** ocupa su lugar. Para obtener más información, [vea IXPLogon::Idle](ixplogon-idle.md).
  
Para usar el motor inactivo, los clientes y los proveedores de servicios crean una función de devolución de llamada que contiene las tareas que deben producirse cuando el subsistema MAPI está inactivo. Cuando MAPI detecta el tiempo de inactividad, invoca esta función de devolución de llamada. La función de devolución de llamada sigue el prototipo **FNIDLE,** definido de la siguiente manera: 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Para obtener más información, vea [FNIDLE](fnidle.md).
  
Las funciones que forma el motor inactivo son:
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Para registrar una función de devolución de llamada, los clientes y proveedores de servicios llaman a la **función FtgRegisterIdleRoutine.** Los parámetros de entrada incluyen una prioridad opcional, un bloque de memoria que se pasa a la función de devolución de llamada como entrada, una cantidad de tiempo que se usará de cualquier manera apropiada y un conjunto de marcas de opción. 
  
Los clientes y proveedores de servicios pueden especificar una prioridad en el  _parámetro priIdle_ que controla cómo se ejecuta la función inactiva o especificar cero si la prioridad no es un problema. Dado que los números negativos representan prioridades más altas que números positivos o cero, se deben asignar números negativos a las operaciones de compresión y búsqueda. A las tareas que se producen una vez se les deben asignar números positivos. 
  
Para anular el registro de una función de devolución de llamada activa, los clientes y proveedores de servicios llaman a **la función DeregisterIdleRoutine.** Dado que **DeregisterIdleRoutine** funciona de forma asincrónica, es posible que la función de devolución de llamada se invoque en cualquier momento durante la llamada de anulación del registro y posiblemente incluso después de que **DeregisterIdleRoutine** haya devuelto. 
  
Para modificar algunas o todas las características de una función de devolución de llamada, los clientes y proveedores de servicios llaman a la **función ChangeIdleRoutine.** **ChangeIdleRoutine** realiza cambios según cómo se establece el  _parámetro flags ircIdle;_ **ChangeIdleRoutine** puede cambiar la función en sí, su prioridad, configuración de hora y parámetro de entrada. 
  
MAPI define la inactividad igual que el sistema operativo, cuando el sistema operativo tiene una definición. En Win32, MAPI crea un subproceso con prioridad de clase inactiva para programar tareas inactivas. Este subproceso realiza un seguimiento de la hora y publica un mensaje en el subproceso que va a ejecutar la tarea inactiva cuando llega el momento de su ejecución. Win32 programa subprocesos, no procesos. Si las tareas que tienen una prioridad superior a la prioridad de inactividad se producen en la estación de trabajo, la tarea inactiva no debe programarse para su ejecución hasta que se hayan completado. 
  
Todas las tareas inactivas se ejecutan en el subproceso que llamó **MAPIInitIdle**. MAPI tiene un subproceso independiente para la programación, pero cuando una tarea inactiva es apta, vuelve a enviar un mensaje al subproceso de inicialización y la tarea inactiva se ejecuta allí. Las implicaciones para los distintos tipos de clientes son las siguientes.
  
|**Modelo de subprocesos**|**Implicación**|
|:-----|:-----|
|Subproceso único  <br/> |No pasa nada. Las funciones inactivas se ejecutan en el subproceso principal del cliente y se serializan a través del bucle de mensajes.  <br/> |
|Subproceso libre  <br/> |Las funciones inactivas deben ser seguras para subprocesos, pero el cliente ya tiene la infraestructura necesaria. Es posible que el cliente no necesite el motor de inactividad MAPI en absoluto.  <br/> |
|Subprocesos de departamentos  <br/> |La función inactiva debe ejecutarse en el mismo subproceso que la registró si desea usar MAPI, OLE o cualquier otra interfaz COM. La forma más sencilla es registrar una función inactiva con MAPI que publica un mensaje en el subproceso correcto y distribuir la función inactiva "real" directamente desde el bucle de mensajes de ese subproceso.  <br/> |
   

