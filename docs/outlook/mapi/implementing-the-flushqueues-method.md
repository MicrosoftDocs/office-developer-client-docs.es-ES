---
title: Implementación del método FlushQueues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1e5c78c71f7fddb04d3517aca0a34efa151ece08
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411781"
---
# <a name="implementing-the-flushqueues-method"></a>Implementación del método FlushQueues

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La cola MAPI usa el método [IXPLogon::FlushQueues](ixplogon-flushqueues.md) para descargar y cargar los mensajes pendientes a y desde un proveedor de transporte. Normalmente, la cola MAPI vaciará las colas de todos los proveedores de transporte que hayan iniciado sesión en la sesión, empezando por el primer proveedor de transporte tal y como se establece en la sección de orden de transporte del perfil del usuario. El vaciado de colas casi siempre es el resultado de una solicitud directa por parte del usuario, por lo que el envío y recepción de mensajes mientras se vacían las colas es sincrónico para la cola MAPI. Dado que estas llamadas son sincrónicas, el proveedor de transporte debe procesarlas lo antes posible. 
  
Los proveedores de transporte deben controlar la llamada **FlushQueues** tal como se describe en la siguiente secuencia de pasos para permitir el procesamiento correcto de mensajes y para permitir que otros proveedores de transporte utilicen recursos externos como módems como parte de la operación **FlushQueues** de la cola MAPI. 
  
|**Paso**|**Componente**|**Implementación**|
|:-----|:-----|:-----|
|1.  <br/> |Cola MAPI  <br/> |Llama al **método FlushQueues** para el primer proveedor de transporte que aparece en el orden de transporte del perfil del usuario y pasa las marcas solicitadas en el _parámetro ulFlags._ **Se llama a FlushQueues** una vez con todas las marcas establecidas para toda la operación de carga y descarga.  <br/> |
|2.  <br/> |Proveedor de transporte  <br/> |Debe realizar varias acciones antes de volver de la **llamada FlushQueues.** Si se aplazan los mensajes enviados anteriormente, se debe llamar al método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) con el NOTIFY_SENT_DEFERRED marca establecida. Tenga en cuenta que es posible que la cola MAPI cancele un mensaje que se ha aplazado antes de que el proveedor de transporte tenga la oportunidad de terminar de procesar el mensaje.  <br/> Si el proveedor de transporte usa un recurso externo como un módem, se debe establecer la conexión con el recurso externo.  <br/> El STATUS_OUTBOUND_FLUSH de la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la fila de estado del proveedor de transporte debe establecerse mediante el método [IMAPISupport::ModifyStatusRow.](imapisupport-modifystatusrow.md)  <br/> A continuación, el proveedor de transporte debe S_OK para la **llamada FlushQueues.**  <br/> |
|3.  <br/> |Cola MAPI  <br/> |Comprueba la fila de estado del proveedor de transporte para el bit STATUS_OUTBOUND_FLUSH y llama a [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) para el primer mensaje de la cola.  <br/> |
|4.  <br/> |Proveedor de transporte  <br/> |Controla el mensaje y devuelve desde la **llamada SubmitMessage.**  <br/> |
|5.  <br/> |Cola MAPI  <br/> |Si el proveedor de transporte devuelve S_OK **de SubmitMessage**, la cola MAPI llama a [IXPLogon::EndMessage](ixplogon-endmessage.md) para el mensaje como lo hace con el envío normal de mensajes.  <br/> Si el proveedor de transporte devuelve un valor distinto de S_OK de **SubmitMessage**, la cola MAPI controla el valor correctamente antes de llamar a **EndMessage** o antes de llamar de nuevo **a SubmitMessage.**  <br/> |
|6.  <br/> |Proveedor de transporte  <br/> |Devuelve de **EndMessage** con su estado de procesamiento de mensajes en el _parámetro lpulFlags._  <br/> |
|7.  <br/> |Cola MAPI y proveedor de transporte  <br/> |El **bucle SubmitMessage** -  **EndMessage** continúa hasta que se han descargado todos los mensajes de la cola.  <br/> |
|8.  <br/> |Cola MAPI  <br/> |Notifica al proveedor de transporte que ha terminado de descargar mensajes llamando al método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) del proveedor de transporte con la marca NOTIFY_END_OUTBOUND_FLUSH establecida.  <br/> |
|9.  <br/> |Proveedor de transporte  <br/> |Libera los recursos externos usados para enviar mensajes salientes, de modo que otros proveedores de transporte puedan usar estos recursos para vaciar las colas.  <br/> El STATUS_INBOUND_FLUSH bit de la **PR_STATUS_CODE** propiedad de la fila de estado del proveedor de transporte debe establecerse **mediante ModifyStatusRow**.  <br/> |
|10.  <br/> |Cola MAPI  <br/> |Comprueba la fila de estado del proveedor de transporte para el STATUS_INBOUND_FLUSH bits y llama a [IXPLogon::StartMessage](ixplogon-startmessage.md) si está establecida.  <br/> |
|11.  <br/> |Proveedor de transporte  <br/> |Procesa el mensaje y devuelve desde **StartMessage**. Si el proveedor de transporte tiene otros mensajes que cargar, debe llamar a **SpoolerNotify** con el NOTIFY_NEWMAIL marca establecida.  <br/> Si el proveedor de transporte no tiene mensajes para cargar, debe llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el mensaje que la cola MAPI pasó en **StartMessage** y devolver.  <br/> |
|12.  <br/> |Cola MAPI  <br/> |Continúa llamando **a StartMessage** hasta que se llama a **SaveChanges** en un mensaje. Una vez que el proveedor de transporte haya terminado de cargarse, la cola MAPI llama a **TransportNotify** con NOTIFY_END_INBOUND_FLUSH marca establecida.  <br/> |
|13.  <br/> |Proveedor de transporte  <br/> |Borra el bit STATUS_INBOUND_FLUSH en la propiedad **PR_STATUS_CODE** de su fila de estado mediante **ModifyStatusRow** y libera todos los recursos externos para que estén disponibles para su uso por otros proveedores de transporte.  <br/> |
|14.  <br/> |Cola MAPI  <br/> |Llama **a FlushQueues** para el siguiente proveedor de transporte que aparece en el orden de transporte del perfil del usuario.  <br/> |
   
Si una aplicación cliente llama a [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) en el objeto de estado de un proveedor de transporte, el proveedor de transporte debe establecer el bit adecuado en su fila de estado con **ModifyStatusRow**. A continuación, la cola MAPI llama al método **IXPLogon::FlushQueues** del proveedor de transporte en la comodidad de la cola MAPI. Cuando se llama al método **IXPLogon::FlushQueues** del proveedor de transporte como resultado de una llamada **IMAPIStatus::FlushQueues** de una aplicación cliente, la operación se produce de forma asincrónica en la aplicación cliente. De **lo contrario, IXPLogon::FlushQueues** funciona de forma sincrónica con la cola MAPI. 
  
Por motivos de rendimiento, la cola MAPI solo llamará al método **FlushQueues** de un proveedor de transporte si las marcas STATUS_INBOUND_FLUSH y STATUS_OUTBOUND_FLUSH se establecen en la fila de estado del proveedor de transporte. Por lo tanto, un proveedor de transporte puede detener la operación **FlushQueues** en cualquier momento borrando las marcas STATUS_OUTBOUND_FLUSH y STATUS_INBOUND_FLUSH en su fila de estado. Si la cola MAPI se está apagando y necesita finalizar la operación **FlushQueues,** llama a **TransportNotify** con las marcas NOTIFY_END_INBOUND_FLUSH y NOTIFY_END_OUTBOUND_FLUSH establecidas. El proveedor de transporte debe liberar todos los recursos externos y devolver. 
  

