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
ms.openlocfilehash: fe722e8723fdc3868cbbc3188f03e13ef3f466f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575339"
---
# <a name="imsgstoregetoutgoingqueue"></a>IMsgStore::GetOutgoingQueue

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de cola saliente, una tabla que contiene información acerca de todos los mensajes en cola de salida del almacén de mensajes. Se llama a este m�todo s�lo por la cola MAPI.
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lppTable_
  
> [out] Un puntero a un puntero a la tabla de cola saliente.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> En la tabla cola saliente se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore::GetOutgoingQueue** proporciona a la cola MAPI con acceso a la tabla que muestra la cola del almacén de mensajes de los mensajes salientes. Normalmente, los mensajes se colocan en la tabla cola saliente después de que se llama a su método [IMessage::SubmitMessage](imessage-submitmessage.md) . Sin embargo, debido a que el orden de envío afecta al orden de preprocesamiento y envío para el proveedor de transporte, algunos mensajes que se han marcado para el envío es posible que no aparezca en la tabla cola saliente inmediatamente. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Para obtener una lista de las propiedades que se debe incluir como columnas en la tabla cola saliente, vea [Las tablas de cola saliente](outgoing-queue-tables.md). 
  
Debido a que la cola MAPI está diseñada para aceptar los mensajes de un almacén de mensajes en orden ascendente de tiempo de envío, permitir que la cola MAPI ordenar la tabla de cola saliente para que coincida con este orden o establecer como el criterio de ordenación predeterminado.
  
Debe admitir las notificaciones para la tabla de cola de mensajes salientes, asegurarse de que la cola MAPI recibe una notificación cuando cambia el contenido de la cola. 
  
## <a name="see-also"></a>Recursos adicionales



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

