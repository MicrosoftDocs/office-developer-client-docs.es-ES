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
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576207"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Comprueba el formulario para que los cambios realizados desde la última vez que guardó.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Parámetros

Ninguna
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario tiene los cambios realizados desde la última vez que se guardó.
    
S_FALSE 
  
> El formulario no tiene los cambios realizados desde la última vez que se guardó.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IPersistMessage::IsDirty** para determinar si el mensaje se han guardado los datos. 
  
## <a name="see-also"></a>Recursos adicionales



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

