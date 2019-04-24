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
ms.openlocfilehash: 84f0ca88403980ff9ea1c91821a8a3d7edae74fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309719"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hace que el formulario libere el mensaje actual.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Parámetros

Ninguno
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje se ha lanzado correctamente.
    
## <a name="remarks"></a>Comentarios

La transición de formularios a dos Estados de HandsOff:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Cuando un formulario está en cualquiera de estos Estados, se almacena de forma permanente. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Cuando un visor de formularios llama al método **IPersistMessage:: HandsOffMessage** mientras el formulario está en estado [normal](normal-state.md) o noscribble, llame de forma recursiva a **HandsOffMessage** en cada mensaje incrustado en el mensaje actual y el [](noscribble-state.md) [ IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) método en cada objeto OLE incrustado en el mensaje actual. A continuación, libere el mensaje actual y todos los mensajes incrustados y objetos OLE. Si el formulario estaba en estado normal, pase al estado HandsOffFromNormal. Si el formulario estaba en estado noScribble, pase al estado HandsOffAfterSave. Después de una transición correcta, llame al método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) del mensaje y devuelva S_OK. 
  
Cuando un visor de formularios llama a **HandsOffMessage** mientras el formulario está en cualquiera de los Estados HandsOff, devuelva E_UNEXPECTED. 
  
Para obtener más información acerca de los distintos Estados de un formulario, vea [Form States](form-states.md). Para obtener más información sobre cómo trabajar con el estado HandsOff de los objetos de almacenamiento, vea el método [IPersistStorage:: HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) . 
  
## <a name="see-also"></a>Vea también



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estados de formulario](form-states.md)

