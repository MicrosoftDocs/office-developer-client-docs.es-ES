---
title: Motor de inactividad de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9fdc254053c2d35c83866bd8a076279fd383db02
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583039"
---
# <a name="mapi-idle-engine"></a>Motor de inactividad de MAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona varias funciones que se conocen como el motor de inactividad. Estas funciones permiten a los clientes, los proveedores de la libreta de direcciones y los proveedores de almacén de mensajes realizar diversas tareas durante tiempos lentos en la sesión o en respuesta a un tiempo lento. Por ejemplo, clientes y proveedores de servicios pueden aplazar operaciones lentas o cerrar los archivos que han permanecido sin usar durante un período extenso. Normalmente, los proveedores de transporte no usar el motor de inactivo debido a que el método **IXPLogon::Idle** toma su lugar. Para obtener más información, vea [IXPLogon::Idle](ixplogon-idle.md).
  
Para usar el motor de inactividad, clientes y proveedores de servicios de creación una función de devolución de llamada que contiene las tareas que deben producirse cuando el subsistema MAPI está inactivo. Cuando MAPI detecta el tiempo de inactividad, invoca esta función de devolución de llamada. La función de devolución de llamada sigue el prototipo **FNIDLE** , que se definen como sigue: 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Para obtener más información, vea [FNIDLE](fnidle.md).
  
Las funciones que componen el motor de inactividad son:
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Para registrar una función de devolución de llamada, los clientes y proveedores de servicios de llamar a la función **FtgRegisterIdleRoutine** . Los parámetros de entrada incluyen una prioridad opcional, un bloque de memoria que se pasa a la función de devolución de llamada como entrada, una cantidad de tiempo que se usará de forma apropiada, y un conjunto de opción marcas. 
  
Los clientes y proveedores de servicios pueden especificar una prioridad en el parámetro _priIdle_ que controla cómo se ejecuta la función inactivo o especificar cero si la prioridad no es un problema. Debido a que los números negativos representan prioridades mayores que los números positivos o cero, se deben asignar las operaciones de búsqueda y la compresión de los números negativos. Tareas que se producen una vez que se debe asignar a números positivos. 
  
Para anular el registro de una función de devolución de llamada activa, clientes y proveedores de servicios de llamar a la función **DeregisterIdleRoutine** . Debido a que **DeregisterIdleRoutine** funciona de manera asincrónica, es posible para la función de devolución de llamada que va a invocar en cualquier momento durante la llamada Cancelar registro y, posiblemente, incluso después de que se devuelva **DeregisterIdleRoutine** . 
  
Para modificar algunas o todas las características de una función de devolución de llamada, los clientes y proveedores de servicios de llamar a la función **ChangeIdleRoutine** . **ChangeIdleRoutine** hace que cambia en función de cómo se establece el parámetro de indicadores _ircIdle_ ; **ChangeIdleRoutine** puede cambiar la propia función, su prioridad, configuración de hora y parámetro de entrada. 
  
MAPI define inactivo el mismo que el sistema operativo, cuando el sistema operativo tiene una definición. En Win32, MAPI crea un subproceso con prioridad de clase inactiva para programar tareas inactivas. Este subproceso realiza un seguimiento de la hora y envía un mensaje al subproceso de la que va a ejecutar la tarea inactivo cuando llegue la hora para su ejecución. Win32 programa los subprocesos, no se procesa. Si se están produciendo las tareas que tienen una prioridad superior a la prioridad de inactividad en la estación de trabajo, la tarea inactiva debe no obtener programada para su ejecución hasta que han completado las tareas. 
  
Todas las tareas inactivas se ejecutan en el subproceso que llamó a **MAPIInitIdle**. MAPI tiene un subproceso independiente para la programación, pero cuando se convierte en una tarea inactiva elegible, envía un mensaje vuelta al subproceso de inicialización y la tarea inactivo se ejecuta no existe. Las implicaciones de distintos tipos de clientes son los siguientes.
  
|**Modelo de subprocesos**|**Implicación**|
|:-----|:-----|
|Un único subproceso  <br/> |No hay problema. Funciones de inactividad de ejecución en el subproceso principal de su cliente y se puede serializar a través del bucle de mensaje.  <br/> |
|Subprocesamiento libre  <br/> |Funciones de inactividad deben ser seguros para subprocesos, pero el cliente ya tiene la infraestructura necesaria. El cliente no es posible que necesita el motor de inactividad de MAPI en absoluto.  <br/> |
|Subprocesamiento controlado  <br/> |Función inactivo tiene que ejecutarse en el mismo subproceso que lo registró si desea utilizar MAPI, OLE o cualquier otros interfaces COM. Es la manera más sencilla registrar una función de inactividad con MAPI que se envía un mensaje al subproceso de la derecha y la función "real" inactividad directamente desde el bucle de mensajes del subproceso que de distribución.  <br/> |
   

