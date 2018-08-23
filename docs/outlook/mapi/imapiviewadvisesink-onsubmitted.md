---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2aa1aca2816b8f0e148d35d1fcec761f621a2239
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579448"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se notifica al Visor de formulario que se ha enviado el mensaje actual a la cola MAPI.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Parámetros

Ninguna
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha realizado correctamente.
    
## <a name="remarks"></a>Comentarios

Un objeto de formulario llama al método de **IMAPIViewAdviseSink::OnSubmitted** después de que una llamada a [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) devuelva correctamente. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Después de llamar a **OnSubmitted** , puede continuar en la suposición de que se ha actualizado el mensaje. Actualice sus windows para reflejar los cambios que se han producido. 
  
Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

