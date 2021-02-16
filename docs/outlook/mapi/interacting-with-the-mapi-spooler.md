---
title: Interactuar con la cola MAPI
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
# <a name="interacting-with-the-mapi-spooler"></a>Interactuar con la cola MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La cola MAPI usa los métodos de la interfaz [IXPLogon : IUnknown](ixplogoniunknown.md) al llamar al proveedor de transporte. Debería ser posible que la mayoría de los tipos de proveedores de transporte implementen la mayoría de estos métodos para que vuelvan rápidamente. Esto es deseable porque si un método tarda mucho tiempo en devolverse, debe dividirse con llamadas de nuevo a la cola MAPI para liberar la CPU para otras tareas. 
  
La cola MAPI hace su trabajo y realiza sus llamadas a proveedores de transporte cuando las aplicaciones en primer plano están inactivas. Después de mostrar opcionalmente cuadros de diálogo cuando el proveedor de transporte inicia sesión por primera vez (regido por marcas pasadas de MAPI al proveedor de transporte), los proveedores de transporte funcionan en segundo plano a menos que el cliente lo llame para vaciar las colas de envío y recepción. Vaciar colas es la única vez que un proveedor de transporte no necesita liberar la CPU y, a continuación, solo si se informa al usuario de que hay una acción potencialmente larga en curso. La cola MAPI normalmente solicita que un proveedor de transporte vacíe sus colas en respuesta a una acción del usuario, por lo que el proveedor de transporte normalmente no necesita hacer nada para asegurarse de que el usuario está informado.
  
Un proveedor de transporte puede decidir independientemente vaciar una cola y usar los bits STATUS_INBOUND_FLUSH y STATUS_OUTBOUND_FLUSH en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de su fila de estado para informar a la cola MAPI de que desea atención para que pueda realizar el trabajo. La fila de estado se actualiza mediante el [método IMAPISupport::ModifyStatusRow.](imapisupport-modifystatusrow.md) En este caso, el proveedor de transporte probablemente debería mostrar un indicador de progreso u otra interfaz para informar al usuario de que se está haciendo una acción larga. 
  
Dado que la actividad de red a menudo tarda más de 0,2 segundos, los proveedores de transporte deben, siempre que sea posible, usar solicitudes de red asincrónicas. Esto les permite iniciar una solicitud, liberar la CPU llamando de nuevo a la cola MAPI y, cuando la cola MAPI de nuevo les da control, para comprobar si su solicitud de red se ha completado. Si aún no se ha completado, de nuevo liberan la CPU llamando de nuevo a la cola MAPI con el método [IMAPISupport::SpoolerYield.](imapisupport-spooleryield.md) 
  
Durante el procesamiento de mensajes, entre [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) e [IXPLogon::EndMessage](ixplogon-endmessage.md) y durante [IXPLogon::StartMessage,](ixplogon-startmessage.md)el proveedor de transporte suele hacer muchas llamadas en objetos expuestos a él por la cola MAPI. Como parte de su control de estos objetos, la cola MAPI ayuda al proveedor de transporte a comportarse correctamente como un proceso en segundo plano, cediendo por sí mismo cuando corresponda. Un proveedor de transporte que requiera procesamiento de tiempo crítico puede declarar una sección crítica para la cola MAPI mediante el método de objeto de compatibilidad [IMAPISupport::SpoolerNotify.](imapisupport-spoolernotify.md) En este caso, la CPU solo se libera en llamadas **SpoolerYield** explícitas por el proveedor de transporte hasta que el proveedor de transporte finaliza el procesamiento de sección crítica con otra llamada a **SpoolerNotify**.
  
> [!NOTE]
> Esto no es lo mismo que una sección crítica de Win32. Esto solo debe hacerse cuando el proveedor de transporte necesita un control en tiempo real de recursos externos, como la lectura de datos entrantes desde una línea de fax. Dado que esto aumenta la prioridad del proceso de cola MAPI y puede hacer que la estación de trabajo deje de responder durante la operación, es una buena idea notificar al usuario que hay una acción potencialmente larga en curso y proporcionar un indicador de progreso si es posible. 
  

