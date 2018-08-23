---
title: IMAPIViewAdviseSinkOnShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnShutdown
api_type:
- COM
ms.assetid: c9c3aecf-5e4b-407a-8ea1-6211b4c6e0a5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f49ea23ed7fef91bcb360483611af2ee60429934
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592972"
---
# <a name="imapiviewadvisesinkonshutdown"></a>IMAPIViewAdviseSink::OnShutdown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se notifica al Visor de formulario que se está cerrando un formulario.
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a>Parámetros

Ninguna
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha realizado correctamente.
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

