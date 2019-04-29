---
title: Interacción con la cola MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: da94347dcb47e5fdbd4a6c1d404b795f4f7938ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432152"
---
# <a name="interacting-with-the-mapi-spooler"></a>Interacción con la cola MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La cola MAPI usa los métodos de la interfaz [IXPLogon: IUnknown](ixplogoniunknown.md) al llamar al proveedor de transporte. Para la mayoría de los tipos de proveedores de transporte, es necesario que implementen la mayoría de estos métodos para que vuelvan rápidamente. Esto es conveniente porque, si un método tarda mucho tiempo en volver, se debe dividir con las llamadas de vuelta a la cola MAPI para liberar la CPU de otras tareas. 
  
La cola MAPI realiza su trabajo y realiza sus llamadas a los proveedores de transporte cuando las aplicaciones de primer plano están inactivas. Después de mostrar de forma opcional los cuadros de diálogo cuando el proveedor de transporte inicia sesión por primera vez (regido por marcas pasadas de MAPI al proveedor de transporte), los proveedores de transporte operan en segundo plano a menos que el cliente lo llame para vaciar las colas de envío y recepción. Vaciar colas es la única vez que un proveedor de transporte no necesita liberar la CPU y, a continuación, solo si se informa al usuario de que una acción potencialmente prolongada está en curso. La cola MAPI suele solicitar que un proveedor de transporte vacíe sus colas en respuesta a una acción del usuario, por lo que el proveedor de transporte no suele tener que hacer nada para asegurarse de que se informa al usuario.
  
Un proveedor de transporte puede decidir por separado vaciar una cola y usar los bits STATUS_INBOUND_FLUSH y STATUS_OUTBOUND_FLUSH en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de su fila de estado para informar a la cola MAPI que desea atención para que pueda llevarse a cabo el trabajo. La fila de estado se actualiza con el método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) . En este caso, el proveedor de transporte probablemente debería mostrar un indicador de progreso u otra interfaz para informar al usuario de que se está produciendo una acción de larga duración. 
  
Dado que la actividad de red suele tardar más de 0,2 segundos, los proveedores de transporte deben, siempre que sea posible, usar solicitudes de red asincrónicas. Esto les permite iniciar una solicitud, liberar la CPU al volver a llamar a la cola de espera de MAPI y, cuando vuelva a proporcionar el administrador de cola MAPI, para comprobar si se ha completado la solicitud de red. Si aún no se ha completado, vuelven a liberar la CPU mediante la devolución de llamada a la cola MAPI con el método [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) . 
  
Durante el procesamiento de mensajes, entre [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) y [IXPLogon:: EndMessage](ixplogon-endmessage.md) y durante la [IXPLogon:: StartMessage](ixplogon-startmessage.md), el proveedor de transporte suele realizar muchas llamadas en objetos expuestos por la cola MAPI. Como parte de su control de estos objetos, la cola MAPI ayuda al proveedor de transporte a que se comporte de manera adecuada como un proceso en segundo plano al proporcionar por sí solo cuando sea necesario. Un proveedor de transporte que requiera un procesamiento de tiempo crítico puede declarar una sección crítica a la cola MAPI mediante el método de objeto de compatibilidad [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) . En este caso, la CPU solo se publica en llamadas **SpoolerYield** realizadas por el proveedor de transporte hasta que el proveedor de transporte finalice el procesamiento de secciones críticas con otra llamada a **SpoolerNotify**.
  
> [!NOTE]
> No es lo mismo que una sección crítica de Win32. Esto solo debe realizarse cuando el proveedor de transporte necesite control en tiempo real de recursos externos, como la lectura de datos entrantes de una línea de fax. Puesto que esto eleva la prioridad del proceso de cola MAPI y puede provocar que la estación de trabajo deje de responder durante la operación, es aconsejable notificar al usuario que se está llevando a cabo una acción potencialmente larga y proporcionar un indicador de progreso si es posible. 
  

