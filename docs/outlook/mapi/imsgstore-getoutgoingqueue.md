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
  
Proporciona acceso a la tabla cola de salida, una tabla que contiene información sobre todos los mensajes de la cola de salida del almacén de mensajes. Se llama a este m�todo s�lo por la cola MAPI.
  
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
  
> contempla Un puntero a un puntero a la tabla de colas de salida.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de cola de salida se ha devuelto correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore:: GetOutgoingQueue** proporciona al administrador de trabajos en cola MAPI acceso a la tabla que muestra la cola de mensajes salientes del almacén de mensajes. Normalmente, los mensajes se colocan en la tabla de colas de salida después de llamar al método [IMessage:: SubmitMessage](imessage-submitmessage.md) . Sin embargo, como el orden de envío afecta al orden de preprocesamiento y envío al proveedor de transporte, algunos mensajes que se marcaron para enviar podrían no aparecer inmediatamente en la tabla de colas de salida. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Para obtener una lista de las propiedades que deben incluirse como columnas en la tabla cola de salida, consulte [tablas de colas de salida](outgoing-queue-tables.md). 
  
Debido a que la cola MAPI está diseñada para aceptar mensajes de un almacén de mensajes en orden ascendente de tiempo de envío, permita que la cola MAPI ordene la tabla cola de salida para que se ajuste a este orden o que se establezca como criterio de ordenación predeterminado.
  
Debe admitir notificaciones para la tabla de colas de mensajes salientes, lo que garantiza que la cola MAPI recibirá una notificación cuando cambie el contenido de la cola. 
  
## <a name="see-also"></a>Ver también



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

