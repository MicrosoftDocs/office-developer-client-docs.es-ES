---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2ec78331fd013777f001d39bd7e978a67abb5342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351201"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Notifica al visor de formularios que se ha guardado el mensaje actual en un formulario.
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>Parámetros

Ninguno
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Un objeto Form llama al método **IMAPIViewAdviseSink:: onSave** después de que se haya guardado correctamente el mensaje actual en un formulario. Esto permite a los visores actualizar sus ventanas para reflejar los cambios realizados en el mensaje. 
  
Para obtener más información acerca de las notificaciones de formulario, vea [enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Vea también



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

