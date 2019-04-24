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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356479"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Enviar o recibir un mensaje a petición
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes suelen basarse en el subsistema MAPI (la cola MAPI y los proveedores de servicios) para controlar el momento de la transmisión y la recepción de mensajes. Sin embargo, puede modificar este intervalo usando el objeto de estado de la cola MAPI o de un proveedor de transporte.
  
El método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) quita todos los mensajes de una o varias colas de entrada o de salida del proveedor de transporte. Los siguientes procedimientos describen dos técnicas para enviar o recibir mensajes a petición. El primer procedimiento utiliza el objeto status del administrador de trabajos de MAPI para vaciar las colas de cada proveedor de transporte en el perfil; el segundo procedimiento vacía la cola de un proveedor de transporte único. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Para vaciar todas las colas entrantes o salientes en una sola operación
  
1. Llame a [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado. 
    
2. Llame al método [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la tabla de estado para limitar la columna **** establecida como valor máximo ([PidTagEntryId](pidtagentryid-canonical-property.md)) y **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
    
3. Cree una restricción de propiedad con una estructura [SPropertyRestriction](spropertyrestriction.md) para que sea igual a **PR_RESOURCE_TYPE** con MAPI_SPOOLER. 
    
4. Llame a [HrQueryAllRows](hrqueryallrows.md), pasando la estructura **SPropertyRestriction** , para recuperar la fila que representa el estado de la cola de impresión MAPI. 
    
5. Pase la **** columna que se va a [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir el objeto de estado del administrador de trabajos en cola MAPI. 
    
6. Llame al método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) del administrador de colas de MAPI, pasando la marca FLUSH_NO_UI para suprimir la interfaz de usuario y la marca FLUSH_DOWNLOAD o FLUSH_UPLOAD para vaciar las colas de salida o de entrada. 
    
7. Libere el objeto status y la tabla de estado, así como la estructura [SRowSet](srowset.md) que se asigna a la tabla. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Para vaciar las colas entrantes o salientes individualmente por el proveedor de transporte
  
1. Llame a [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) para obtener acceso a la tabla de estado. 
    
2. Llame al método [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la tabla de estado para limitar la columna **** establecida en valor y **PR_RESOURCE_TYPE**.
    
3. Cree una restricción de propiedad con una estructura [SPropertyRestriction](spropertyrestriction.md) para que sea igual a **PR_RESOURCE_TYPE** con MAPI_TRANSPORT_PROVIDER. 
    
4. Llame a [HrQueryAllRows](hrqueryallrows.md), pasando la estructura **SPropertyRestriction** , para recuperar las filas suministradas por los proveedores de transporte. 
    
5. Para cada fila devuelta desde **HrQueryAllRows**:
    
    1. Pase la **** columna que se va a [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir el objeto de estado del proveedor de transporte. 
        
    2. Compruebe que el objeto de estado de transporte admita el método **FlushQueues** comprobando que su propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) tiene establecida la marca STATUS_FLUSH_QUEUES. 
        
    3. Si se admite, llame a [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md). Si no se admite, llame al método **IMAPIStatus:: FlushQueues** del administrador de la cola de MAPI, pasando el identificador de entrada del transporte en el parámetro _lpTargetTransport_ . Consulte el procedimiento anterior para obtener instrucciones sobre cómo tener acceso al objeto de estado del administrador de trabajos en cola MAPI. Establezca la marca FLUSH_DOWNLOAD para vaciar las colas de salida o la marca FLUSH_UPLOAD para vaciar las colas entrantes. 
        
    4. Libere el objeto status y la tabla de estado, así como la estructura [SRowSet](srowset.md) que se asigna a la tabla. 
    
La cola MAPI respeta la marca FLUSH_NO_UI como la mayoría de los proveedores de transporte de LAN. Sin embargo, no todos los proveedores de transporte admiten esta marca, en especial los que usan un módem de forma explícita y el servicio de acceso remoto (RAS). RAS no se diseñó para permitir a los clientes suprimir la interfaz de usuario. Es posible configurar un cliente para que se pueda conectar sin que se requiera la interacción de un usuario, pero es difícil y requiere un conocimiento profundo de los servicios de mensajes del cliente.
  

