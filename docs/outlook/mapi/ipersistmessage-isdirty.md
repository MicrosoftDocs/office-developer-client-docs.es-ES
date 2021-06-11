---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407574"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Comprueba en el formulario los cambios realizados desde el último guardado.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Parámetros

Ninguno
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario tiene cambios realizados desde la última vez que se guardó.
    
S_FALSE 
  
> El formulario no tiene cambios realizados desde la última vez que se guardó.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al **método IPersistMessage::IsDirty** para determinar si el mensaje tiene datos no guardados. 
  
## <a name="see-also"></a>Vea también



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

