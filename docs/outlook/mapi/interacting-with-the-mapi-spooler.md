---
title: Interactuar con el administrador de trabajos en cola MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c8032172ef19fbb01af68058b2e0255e269183a8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587897"
---
# <a name="interacting-with-the-mapi-spooler"></a>Interactuar con el administrador de trabajos en cola MAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Los métodos en el [IXPLogon: IUnknown](ixplogoniunknown.md) interfaz usadas por la cola MAPI al llamar al proveedor de transporte. Debe ser posible para la mayoría de los tipos de proveedores de transporte para implementar la mayoría de estos métodos para que devuelvan rápidamente. Esto es deseable porque si un método toma mucho tiempo en devolver, a continuación, se debe ser dividido con las llamadas a la cola de MAPI para liberar la CPU para otras tareas. 
  
La cola MAPI realiza su trabajo y realiza sus llamadas a los proveedores de transporte cuando las aplicaciones de primer plano inactivo. Después, opcionalmente, mostrar cuadros de diálogo cuando el proveedor de transporte en primer lugar se registra (regirá marcas pasadas de MAPI para el proveedor de transporte), los proveedores de transporte operan en segundo plano a menos que llame por el cliente para vaciar enviar y recibir las colas. Las colas de baja es la única vez que un proveedor de transporte no necesita liberar la CPU y, a continuación, sólo si se informa al usuario que está en curso una acción potencialmente larga. Normalmente, la cola MAPI solicita que un proveedor de transporte vacíen sus colas en respuesta a una acción del usuario, por lo que el proveedor de transporte normalmente no es necesario hacer nada para asegurarse de que se informa al usuario.
  
Un proveedor de transporte de forma independiente puede optar por vaciar una cola y utilizar los bits STATUS_INBOUND_FLUSH y STATUS_OUTBOUND_FLUSH en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la fila de estado para informar a la cola MAPI que desea atención, por lo que TI puede realizar el trabajo. La fila de estado se actualiza mediante el método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . En este caso, el proveedor de transporte probablemente debe mostrar un indicador de progreso o de otra interfaz para informar al usuario que se está produciendo una acción de tipo long. 
  
Desde la actividad de red a menudo tarda más de 0,2 segundos, los proveedores de transporte deben, siempre que sea posible, use solicitudes de red asincrónicas. Esto les permite iniciar una solicitud, la versión de la CPU por devolución de llamada a la cola MAPI, y cuando la cola MAPI nuevo, se les concede control, para comprobar si se ha completado su solicitud de red. Si no se ha completado, vuelva a liberar la CPU mediante la devolución de llamada a la cola MAPI con el método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) . 
  
Durante el procesamiento de mensajes, entre [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) y [IXPLogon::EndMessage](ixplogon-endmessage.md) y durante la [IXPLogon::StartMessage](ixplogon-startmessage.md), el proveedor de transporte normalmente realiza llamadas muchas en objetos podrán verlas la cola de MAPI. Como parte de su control de estos objetos, la cola MAPI ayuda a que el proveedor de transporte se comportan de forma adecuada como un proceso en segundo plano produciendo en su propio cuando sea apropiado. Un proveedor de transporte que requieren procesamiento urgente puede declarar una sección crítica a la cola MAPI utilizando el método del objeto [SpoolerNotify](imapisupport-spoolernotify.md) soporte técnico. En este caso, la CPU se libera únicamente en llamadas explícitas de **SpoolerYield** por el proveedor de transporte hasta que el proveedor de transporte termina con otra llamada a **SpoolerNotify**de procesamiento de sección crítica.
  
> [!NOTE]
> No es el mismo que una sección crítica de Win32. Sólo debe realizarse cuando el proveedor de transporte necesita control en tiempo real de recursos externos, como la lectura de datos entrantes desde una línea de fax. Dado que esto aumenta la prioridad del proceso de cola de impresión de MAPI y puede provocar la estación de trabajo que no responde de la duración de la operación, es una buena idea para notificar al usuario que una acción potencialmente larga está en curso y proporcionar un indicador de progreso si es posible. 
  

