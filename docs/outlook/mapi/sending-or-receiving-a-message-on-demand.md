---
title: Enviar o recibir un mensaje a petición
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 15b9c8c5a56b6f37464d2469bd1d7b3e24596502
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436373"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Enviar o recibir un mensaje a petición
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes suelen confiar en el subsistema MAPI (la cola MAPI y los proveedores de servicios) para controlar el tiempo de transmisión y recepción de mensajes. Sin embargo, puede modificar este tiempo mediante el objeto de estado de la cola MAPI o un proveedor de transporte.
  
El [método IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) quita todos los mensajes de una o más colas entrantes o salientes del proveedor de transporte. En los siguientes procedimientos se describen dos técnicas para enviar o recibir mensajes a petición. El primer procedimiento usa el objeto de estado de la cola MAPI para vaciar las colas de todos los proveedores de transporte del perfil; el segundo procedimiento vacía la cola de un único proveedor de transporte. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Para vaciar todas las colas entrantes o salientes en una sola operación
  
1. Llame [a IMAPISession::GetStatusTable para](imapisession-getstatustable.md) obtener acceso a la tabla de estado. 
    
2. Llame al método [IMAPITable::SetColumns](imapitable-setcolumns.md) de la tabla de estado para limitar la columna establecida en **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
    
3. Cree una restricción de propiedad mediante una [estructura SPropertyRestriction](spropertyrestriction.md) para que coincida **PR_RESOURCE_TYPE** con MAPI_SPOOLER. 
    
4. Llame [a HrQueryAllRows](hrqueryallrows.md), pasando por la estructura **SPropertyRestriction,** para recuperar la fila que representa el estado de la cola MAPI. 
    
5. Pase la **PR_ENTRYID** a [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir el objeto de estado de la cola MAPI. 
    
6. Llame al método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) de la cola MAPI, pasando la marca FLUSH_NO_UI para suprimir la interfaz de usuario y la marca FLUSH_DOWNLOAD o FLUSH_UPLOAD para vaciar las colas salientes o entrantes. 
    
7. Libere el objeto status y la tabla de estado, así como la estructura [SRowSet](srowset.md) que se asigna a la tabla. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Para vaciar las colas entrantes o salientes individualmente por el proveedor de transporte
  
1. Llame [a IMAPISession::GetStatusTable para](imapisession-getstatustable.md) obtener acceso a la tabla de estado. 
    
2. Llame al método [IMAPITable::SetColumns](imapitable-setcolumns.md) de la tabla de estado para limitar la columna establecida en **PR_ENTRYID** y **PR_RESOURCE_TYPE**.
    
3. Cree una restricción de propiedad mediante una [estructura SPropertyRestriction](spropertyrestriction.md) para que coincida **PR_RESOURCE_TYPE** con MAPI_TRANSPORT_PROVIDER. 
    
4. Llame [a HrQueryAllRows](hrqueryallrows.md), pasando por la estructura **SPropertyRestriction,** para recuperar las filas proporcionadas por los proveedores de transporte. 
    
5. Para cada fila devuelta desde **HrQueryAllRows**:
    
    1. Pase la **PR_ENTRYID** a [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir el objeto de estado del proveedor de transporte. 
        
    2. Compruebe que el objeto de estado de transporte admite el método **FlushQueues** comprobando que su propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) tiene el STATUS_FLUSH_QUEUES marca. 
        
    3. Si se admite, llame [a IMAPIStatus::FlushQueues](imapistatus-flushqueues.md). Si no se admite, llame al método **IMAPIStatus::FlushQueues** de la cola MAPI, pasando el identificador de entrada del transporte en el _parámetro lpTargetTransport._ Vea el procedimiento anterior para obtener instrucciones sobre cómo obtener acceso al objeto de estado de la cola MAPI. Establezca la FLUSH_DOWNLOAD para vaciar las colas salientes o la marca FLUSH_UPLOAD para vaciar las colas entrantes. 
        
    4. Libere el objeto status y la tabla de estado, así como la estructura [SRowSet](srowset.md) que se asigna a la tabla. 
    
La cola MAPI respeta la marca FLUSH_NO_UI como lo hacen la mayoría de los proveedores de transporte LAN. Sin embargo, no todos los proveedores de transporte respetan esta marca, especialmente los que usan un módem explícitamente y el Servicio de acceso remoto (RAS). RAS no se diseñó para permitir a los clientes suprimir la interfaz de usuario. Es posible configurar un cliente para que pueda conectarse sin necesidad de la interacción de un usuario, pero es difícil y requiere un conocimiento profundo de los servicios de mensajes del cliente.
  

