---
title: Implementar el método FlushQueues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1e5c78c71f7fddb04d3517aca0a34efa151ece08
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310118"
---
# <a name="implementing-the-flushqueues-method"></a>Implementar el método FlushQueues

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La cola MAPI usa el método [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) para descargar y cargar todos los mensajes pendientes a y desde un proveedor de transporte. Normalmente, la cola de espera de MAPI vaciará las colas de todos los proveedores de transporte que hayan iniciado sesión en la sesión, empezando por el primer proveedor de transporte establecido en la sección orden de transporte del perfil del usuario. Vaciar colas es casi siempre el resultado de una solicitud directa del usuario, por lo que el envío y la recepción de mensajes mientras se están vaciando las colas es sincrónico a la cola MAPI. Como estas llamadas son sincrónicas, el proveedor de transporte debería procesarlas tan rápido como sea posible. 
  
Los proveedores de transporte deben administrar la llamada **FlushQueues** como se describe en la siguiente secuencia de pasos para habilitar el procesamiento adecuado de mensajes y habilitar recursos externos, como módems que pueden usar otros proveedores de transporte como parte de la cola MAPI del Operación **FlushQueues** . 
  
|**Paso**|**Componente**|**Implementación**|
|:-----|:-----|:-----|
|1.  <br/> |Cola MAPI  <br/> |Llama al método **FlushQueues** para el primer proveedor de transporte enumerado en el orden de transporte del perfil del usuario, pasando los indicadores solicitados en el parámetro _ulFlags_ . Se llama a **FlushQueues** una vez con todos los indicadores establecidos para toda la operación de carga y descarga.  <br/> |
|2.  <br/> |Proveedor de transporte  <br/> |Tiene que hacer una serie de cosas antes de volver de la llamada **FlushQueues** . Si se aplazan los mensajes enviados anteriormente, se debe llamar al método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) con el conjunto de marcas NOTIFY_SENT_DEFERRED. Tenga en cuenta que la cola MAPI puede cancelar un mensaje aplazado antes de que el proveedor de transporte tenga la oportunidad de finalizar el procesamiento del mensaje.  <br/> Si el proveedor de transporte usa un recurso externo, como un módem, se debe establecer la conexión con el recurso externo.  <br/> El bit STATUS_OUTBOUND_FLUSH de la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la fila de estado del proveedor de transporte debe establecerse mediante el método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) .  <br/> El proveedor de transporte debería devolver S_OK para la llamada **FlushQueues** .  <br/> |
|3.  <br/> |Cola MAPI  <br/> |Comprueba la fila de estado del proveedor de transporte para el bit STATUS_OUTBOUND_FLUSH y llama a [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) para el primer mensaje de la cola.  <br/> |
|4.  <br/> |Proveedor de transporte  <br/> |Administra el mensaje y vuelve de la llamada de **SubmitMessage** .  <br/> |
|5.  <br/> |Cola MAPI  <br/> |Si el proveedor de transporte Devuelve S_OK desde **SubmitMessage**, la cola MAPI llama a [IXPLogon:: EndMessage](ixplogon-endmessage.md) para el mensaje como lo haría con el envío normal de mensajes.  <br/> Si el proveedor de transporte devuelve un valor distinto de S_OK desde **SubmitMessage**, la cola MAPI controla el valor adecuadamente antes de llamar a **EndMessage**o a volver a llamar a **SubmitMessage** .  <br/> |
|6.  <br/> |Proveedor de transporte  <br/> |Devuelve de **EndMessage** con el estado de procesamiento de mensajes en el parámetro _lpulFlags_ .  <br/> |
|7.  <br/> |Cola MAPI y proveedor de transporte  <br/> |El bucle**EndMessage** de **SubmitMessage**- continuará hasta que se hayan descargado todos los mensajes de la cola.  <br/> |
|8.  <br/> |Cola MAPI  <br/> |Notifica al proveedor de transporte que ha terminado de descargar mensajes llamando al método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) del proveedor de transporte con el indicador NOTIFY_END_OUTBOUND_FLUSH establecido.  <br/> |
|9.  <br/> |Proveedor de transporte  <br/> |Libera los recursos externos usados para enviar mensajes salientes para que otros proveedores de transporte puedan usarlos para vaciar sus colas.  <br/> El bit STATUS_INBOUND_FLUSH de la propiedad **PR_STATUS_CODE** de la fila de estado del proveedor de transporte debe establecerse mediante **ModifyStatusRow**.  <br/> |
|10.  <br/> |Cola MAPI  <br/> |Comprueba la fila de estado del proveedor de transporte para el bit STATUS_INBOUND_FLUSH y llama a [IXPLogon:: StartMessage](ixplogon-startmessage.md) si está establecida.  <br/> |
|11.  <br/> |Proveedor de transporte  <br/> |Procesa el mensaje y vuelve de **StartMessage**. Si el proveedor de transporte tiene otros mensajes que cargar, debe llamar a **SpoolerNotify** con el indicador NOTIFY_NEWMAIL establecido.  <br/> Si el proveedor de transporte no tiene mensajes que cargar, debe llamar a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) en el mensaje que la cola MAPI pasa en **StartMessage** y volver.  <br/> |
|12.  <br/> |Cola MAPI  <br/> |Sigue llamando a **StartMessage** hasta que se llama a **SaveChanges** en un mensaje. Una vez finalizada la carga del proveedor de transporte, la cola MAPI llama a **TransportNotify** con el indicador NOTIFY_END_INBOUND_FLUSH establecido.  <br/> |
|apartado.  <br/> |Proveedor de transporte  <br/> |Borra el bit STATUS_INBOUND_FLUSH de la propiedad **PR_STATUS_CODE** de la fila de estado mediante **ModifyStatusRow** y libera todos los recursos externos para que estén disponibles para su uso por otros proveedores de transporte.  <br/> |
|apartado.  <br/> |Cola MAPI  <br/> |Llama a **FlushQueues** para el siguiente proveedor de transporte que aparece en el orden de transporte del perfil del usuario.  <br/> |
   
Si una aplicación de cliente llama a [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) en el objeto de estado de un proveedor de transporte, el proveedor de transporte debe establecer el bit apropiado en su fila de estado con **ModifyStatusRow**. A continuación, la cola MAPI llama al método **IXPLogon:: FlushQueues** del proveedor de transporte en la comodidad del administrador de trabajos de impresión MAPI. Cuando se llama al método **IXPLogon:: FlushQueues** del proveedor de transporte como resultado de la llamada **IMAPIStatus:: FlushQueues** de una aplicación cliente, la operación se produce de forma asincrónica en la aplicación cliente. De lo contrario, **IXPLogon:: FlushQueues** funciona sincrónicamente con la cola MAPI. 
  
Por motivos de rendimiento, la cola de impresión MAPI solo llamará al método **FlushQueues** de un proveedor de transporte si se establecen las marcas STATUS_INBOUND_FLUSH y STATUS_OUTBOUND_FLUSH en la fila de estado del proveedor de transporte. Por lo tanto, un proveedor de transporte puede detener la operación **FlushQueues** en cualquier momento borrando los indicadores STATUS_OUTBOUND_FLUSH y STATUS_INBOUND_FLUSH en su fila de estado. Si la cola MAPI se está cerrando y necesita finalizar la operación **FlushQueues** , llama a **TransportNotify** con los indicadores NOTIFY_END_INBOUND_FLUSH y NOTIFY_END_OUTBOUND_FLUSH establecidos. El proveedor de transporte debe liberar todos los recursos externos y volver. 
  

