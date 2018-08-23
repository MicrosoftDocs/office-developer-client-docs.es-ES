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
ms.openlocfilehash: 668e1c57c59bf2356be808e0347e1bd5135478a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563894"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Enviar o recibir un mensaje a petición
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes que normalmente se basan en el subsistema MAPI: la cola MAPI y los proveedores de servicios, para controlar el tiempo de recepción y transmisión de mensajes. Sin embargo, puede modificar este intervalo mediante el objeto de estado de la cola MAPI o un proveedor de transporte.
  
El método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) quita todos los mensajes de las colas entrantes o salientes de uno o más del proveedor del transporte. Los procedimientos siguientes describen dos técnicas para enviar o recibir los mensajes de petición. El primer procedimiento usa el objeto de estado de la cola MAPI para vaciar las colas de cada proveedor de transporte en el perfil; el segundo procedimiento vacía la cola de un proveedor de transporte único. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Para vaciar todas las colas de entrantes o salientes en una sola operación
  
1. Llame a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado. 
    
2. Llamar al método [IMAPITable::SetColumns](imapitable-setcolumns.md) de la tabla de estado para limitar la columna establecida en la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
    
3. Crear una restricción de propiedad con una estructura de [SPropertyRestriction](spropertyrestriction.md) para que coincida con **PR_RESOURCE_TYPE** con MAPI_SPOOLER. 
    
4. Llame a [HrQueryAllRows](hrqueryallrows.md), pasando la estructura **SPropertyRestriction** , para recuperar la fila que representa el estado de la cola de MAPI. 
    
5. Pase la columna de **entrada del objeto** a [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir el objeto de estado de la cola MAPI. 
    
6. Llamar al método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) de la cola MAPI, pasando el indicador FLUSH_NO_UI para suprimir la interfaz de usuario y el indicador de la FLUSH_DOWNLOAD o FLUSH_UPLOAD para vaciar las colas entrantes o salientes. 
    
7. Liberar el objeto de estado y la tabla de estado, así como la estructura de [SRowSet](srowset.md) que se asigna para la tabla. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Para vaciar las colas entrantes o salientes individualmente por proveedor de transporte
  
1. Llame a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado. 
    
2. Llamar al método [IMAPITable::SetColumns](imapitable-setcolumns.md) de la tabla de estado para limitar la columna establecida en la **entrada del objeto** y **PR_RESOURCE_TYPE**.
    
3. Crear una restricción de propiedad con una estructura de [SPropertyRestriction](spropertyrestriction.md) para que coincida con **PR_RESOURCE_TYPE** con MAPI_TRANSPORT_PROVIDER. 
    
4. Llame a [HrQueryAllRows](hrqueryallrows.md), pasando la estructura **SPropertyRestriction** , para recuperar las filas que son proporcionadas por los proveedores de transporte. 
    
5. Para cada fila devuelta desde **HrQueryAllRows**:
    
    1. Pase la columna de **entrada del objeto** a [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir el objeto de estado del proveedor de transporte. 
        
    2. Compruebe que el objeto de estado de transporte es compatible con el método **FlushQueues** mediante la comprobación de que su propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) tiene la STATUS_FLUSH_QUEUES marcador establecido. 
        
    3. Si se admite, llame a [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md). Si no es compatible, llame al método **IMAPIStatus::FlushQueues** de la cola MAPI, pasando el identificador de entrada del transporte en el parámetro _lpTargetTransport_ . Vea el procedimiento anterior para obtener instrucciones sobre cómo acceder al objeto de estado de la cola MAPI. Establecer el indicador FLUSH_DOWNLOAD para vaciar las colas de salida o el indicador FLUSH_UPLOAD para vaciar las colas entrantes. 
        
    4. Liberar el objeto de estado y la tabla de estado, así como la estructura de [SRowSet](srowset.md) que se asigna para la tabla. 
    
La cola MAPI respeta la marca FLUSH_NO_UI como hacen la mayoría de los proveedores de transporte de LAN. Sin embargo, no todos los proveedores de transporte respetan esta marca, especialmente aquellos que usan un módem explícitamente y el servicio de acceso remoto (RAS). RAS no se diseñaron para permitir que los clientes suprimir la interfaz de usuario. Es posible que un cliente para configurarse de modo que se puede conectar sin necesidad de la interacción de un usuario, pero es difícil y requiere un conocimiento profundo del cliente servicios de message.
  

