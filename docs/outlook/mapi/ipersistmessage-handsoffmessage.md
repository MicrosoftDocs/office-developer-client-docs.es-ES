---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2cd4c86dc45bca85632a3fadc9023c9ad25cfa37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583032"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Hace que el formulario liberar su mensaje actual.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Parámetros

Ninguna
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje fue publicado correctamente.
    
## <a name="remarks"></a>Comentarios

Transición de formularios en dos Estados de HandsOff:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Cuando un formulario está en cualquiera de estos Estados, está en el proceso que se almacena de manera permanente. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Cuando un visor de formulario llama al método de **IPersistMessage::HandsOffMessage** mientras el formulario está en estado [Normal](normal-state.md) o [NoScribble](noscribble-state.md) , de forma recursiva llamada **HandsOffMessage** en cada mensaje insertado en el mensaje actual y la [ IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) método en cada objeto OLE incrustado en el mensaje actual. A continuación, liberar el mensaje actual y todos los mensajes y objetos OLE incrustados. Si el formulario se encontraba en el estado Normal, realizar la transición al estado HandsOffFromNormal. Si el formulario se encontraba en el estado de NoScribble, realizar la transición al estado HandsOffAfterSave. Después de una transición correcta, llamar al método [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del mensaje y devolver S_OK. 
  
Cuando un visor de formulario llama a **HandsOffMessage** mientras el formulario está en cualquiera de los Estados de HandsOff, devolver E_UNEXPECTED. 
  
Para obtener más información acerca de los diferentes Estados de un formulario, vea [Estados de formulario](form-states.md). Para obtener más información acerca de cómo trabajar con el estado HandsOff de objetos de almacenamiento, vea el método [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) . 
  
## <a name="see-also"></a>Vea también



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estados de formulario](form-states.md)

