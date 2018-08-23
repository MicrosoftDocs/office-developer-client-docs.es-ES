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
ms.openlocfilehash: 01296995adbca2640c8da42b4d06c1c749be3266
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582416"
---
# <a name="implementing-the-flushqueues-method"></a>Implementar el método FlushQueues

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La cola MAPI usa el método [IXPLogon::FlushQueues](ixplogon-flushqueues.md) para descargar y cargar todos los mensajes pendientes a y desde un proveedor de transporte. Normalmente, la cola MAPI vaciar las colas para todos los proveedores de transporte que han iniciado sesión en la sesión, empezando por el primer proveedor de transporte como se establece en la sección orden de transporte del perfil de usuario. Las colas de baja casi siempre es el resultado de una solicitud directa por el usuario, por lo que el envío y recepción de mensajes mientras se vaciado de colas son sincrónica a la cola MAPI. Debido a que estas llamadas son sincrónicas, el proveedor de transporte debe procesarlos lo más rápido posible. 
  
Los proveedores de transporte deben controlar la llamada **FlushQueues** tal como se describe en la siguiente secuencia de pasos para habilitar el procesamiento del mensaje adecuado y para habilitar los recursos externos, como los módems para ser utilizado por otros proveedores de transporte como parte de la cola MAPI Operación **FlushQueues** . 
  
|**Paso**|**Componente**|**Implementación**|
|:-----|:-----|:-----|
|1.  <br/> |Cola MAPI  <br/> |Llama al método **FlushQueues** para el proveedor de transporte primera que aparecen en el orden de transporte de perfil de usuario, pasando las marcas solicitadas en el parámetro _ulFlags indicado_ . **FlushQueues** se llama una vez con todos los indicadores establecidos para la operación de descarga y carga completa.  <br/> |
|2.  <br/> |Proveedor de transporte  <br/> |Necesita hacer un número de cosas antes de volver de la llamada **FlushQueues** . Si enviado anteriormente se aplazan los mensajes, se debe llamar al método [SpoolerNotify](imapisupport-spoolernotify.md) con el conjunto de marca NOTIFY_SENT_DEFERRED. Tenga en cuenta que es posible que la cola MAPI cancelar un mensaje que se ha aplazado antes el proveedor de transporte tiene una oportunidad para terminar de procesar el mensaje.  <br/> Si el proveedor de transporte usa un recurso externo, como un módem, se debe establecer la conexión con el recurso externo.  <br/> El STATUS_OUTBOUND_FLUSH de bit en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la fila de estado del proveedor de transporte debe establecerse mediante el método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) .  <br/> El proveedor de transporte, a continuación, debe devolver S_OK para la llamada de **FlushQueues** .  <br/> |
|3.  <br/> |Cola MAPI  <br/> |Comprueba la fila de estado del proveedor de transporte para el bit STATUS_OUTBOUND_FLUSH y llama a [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) para el primer mensaje de la cola.  <br/> |
|4.  <br/> |Proveedor de transporte  <br/> |Controla el mensaje y devuelve a partir de la llamada **SubmitMessage** .  <br/> |
|5.  <br/> |Cola MAPI  <br/> |Si el proveedor de transporte devuelve S_OK de **SubmitMessage**, la cola MAPI llama a [IXPLogon::EndMessage](ixplogon-endmessage.md) para el mensaje tal como lo hace con el envío de mensaje normal.  <br/> Si el proveedor de transporte devuelve un valor distinto de S_OK de **SubmitMessage**, la cola MAPI controla el valor correctamente antes de llamar a **EndMessage**o antes de volver a llamar a **SubmitMessage** .  <br/> |
|6.  <br/> |Proveedor de transporte  <br/> |Devuelve desde **EndMessage** con su estado en el parámetro _lpulFlags_ de procesamiento de mensajes.  <br/> |
|7.  <br/> |Proveedor de cola de impresión y transporte MAPI  <br/> |La **SubmitMessage**- **EndMessage** bucle continúa hasta que se han descargado todos los mensajes en la cola.  <br/> |
|8.  <br/> |Cola MAPI  <br/> |Notifica al proveedor de transporte que ha finalizado la descarga de mensajes por llamar al método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) del proveedor de transporte con el conjunto de marca NOTIFY_END_OUTBOUND_FLUSH.  <br/> |
|9.  <br/> |Proveedor de transporte  <br/> |Libera todos los recursos externos utilizados en el envío de los mensajes salientes para que puedan utilizar otros proveedores de transporte a que vacíen sus colas.  <br/> El STATUS_INBOUND_FLUSH de bit en la propiedad **PR_STATUS_CODE** de la fila de estado del proveedor de transporte debe establecerse mediante **ModifyStatusRow**.  <br/> |
|10.  <br/> |Cola MAPI  <br/> |Comprueba la fila de estado del proveedor de transporte para el bit STATUS_INBOUND_FLUSH y llama a [IXPLogon::StartMessage](ixplogon-startmessage.md) si se establece.  <br/> |
|11.  <br/> |Proveedor de transporte  <br/> |Procesa el mensaje y devuelve de **desea iniciar**. Si el proveedor de transporte tiene otros mensajes para cargar, debe llamar a **SpoolerNotify** con el conjunto de marca NOTIFY_NEWMAIL.  <br/> Si no tiene ningún mensaje para cargar el proveedor de transporte, debe llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el mensaje de la cola MAPI se pasan en **desea iniciar** y devolver.  <br/> |
|12.  <br/> |Cola MAPI  <br/> |Continúa hasta que se llama a **SaveChanges** en un mensaje de llamada **desea iniciar** . Después de que el proveedor de transporte ha finalizado la carga, la cola MAPI llama a **TransportNotify** con el conjunto de marca NOTIFY_END_INBOUND_FLUSH.  <br/> |
|13.  <br/> |Proveedor de transporte  <br/> |Borra la STATUS_INBOUND_FLUSH de bit en la propiedad **PR_STATUS_CODE** de su fila de estado utilizando **ModifyStatusRow** y las versiones de todos los recursos externos para que estén disponibles para usan por otros proveedores de transporte.  <br/> |
|14.  <br/> |Cola MAPI  <br/> |Llama a **FlushQueues** para el siguiente proveedor de transporte que aparecen en el orden de transporte del perfil de usuario.  <br/> |
   
Si una aplicación las llamadas del cliente [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) en el objeto de estado del proveedor de transporte, el proveedor de transporte debe establecer el bit correspondiente en su fila de estado con **ModifyStatusRow**. La cola MAPI, a continuación, llama a (método **IXPLogon::FlushQueues** ) del proveedor de transporte durante la comodidad de la cola MAPI. Cuando se llama (método **IXPLogon::FlushQueues** ) del proveedor de transporte como resultado de llamada de **IMAPIStatus::FlushQueues** de la aplicación de cliente, la operación se produce de forma asincrónica a la aplicación cliente. En caso contrario, **IXPLogon::FlushQueues** funciona de manera sincrónica con la cola de MAPI. 
  
Por motivos de rendimiento, la cola MAPI sólo llamará a (método **FlushQueues** ) del proveedor de transporte si se establecen los indicadores STATUS_INBOUND_FLUSH y STATUS_OUTBOUND_FLUSH en la fila de estado del proveedor de transporte. Por consiguiente, un proveedor de transporte puede detener la operación **FlushQueues** en cualquier momento desactivando los indicadores STATUS_OUTBOUND_FLUSH y STATUS_INBOUND_FLUSH en su fila de estado. Si la cola MAPI se está cerrando y necesita finalizar la operación de **FlushQueues** , se llama **TransportNotify** con el NOTIFY_END_INBOUND_FLUSH y el NOTIFY_END_OUTBOUND_FLUSH conjunto de indicadores. El proveedor de transporte debe liberar todos los recursos externos y devolver. 
  

