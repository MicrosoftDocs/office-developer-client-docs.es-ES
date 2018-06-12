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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: e748427b39418a80cae88e98b4aa7eef6df24393
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817874"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**Se aplica a**: Outlook 
  
Comprueba el formulario para que los cambios realizados desde la última vez que guardó.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Parámetros

None
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario tiene los cambios realizados desde la última vez que se guardó.
    
S_FALSE 
  
> El formulario no tiene los cambios realizados desde la última vez que se guardó.
    
## <a name="remarks"></a>Notas

Visores de formulario llamar al método **IPersistMessage::IsDirty** para determinar si el mensaje se han guardado los datos. 
  
## <a name="see-also"></a>Ver también



[IPersistMessage: IUnknown](ipersistmessageiunknown.md)

