---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8ccb732dd587b2e5107290b2db7c48e85d0145d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434154"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de cola saliente, una tabla que tiene información sobre todos los mensajes de la cola saliente del almacén de mensajes. Se llama a este m�todo s�lo por la cola MAPI.
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lppTable_
  
> [salida] Puntero a un puntero a la tabla de cola saliente.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de cola saliente se ha devuelto correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::GetOutgoingQueue** proporciona a la cola MAPI acceso a la tabla que muestra la cola de mensajes salientes del almacén de mensajes. Normalmente, los mensajes se colocan en la tabla de cola saliente después de llamar al método [IMessage::SubmitMessage.](imessage-submitmessage.md) Sin embargo, dado que el orden de envío afecta al orden de preprocesamiento y envío al proveedor de transporte, es posible que algunos mensajes marcados para el envío no aparezcan inmediatamente en la tabla de cola saliente. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Para obtener una lista de las propiedades que deben incluirse como columnas en la tabla de cola saliente, vea [Outgoing Queue Tables](outgoing-queue-tables.md). 
  
Dado que la cola MAPI está diseñada para aceptar mensajes de un almacén de mensajes en orden ascendente de tiempo de envío, permitir que la cola MAPI ordene la tabla de cola saliente para que coincida con este orden o establecerla como el criterio de ordenación predeterminado.
  
Debe admitir notificaciones para la tabla de cola de mensajes salientes, lo que garantiza que se notifique a la cola MAPI cuando cambie el contenido de la cola. 
  
## <a name="see-also"></a>Vea también



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

