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
ms.openlocfilehash: ebde06d0d22320ecb5edb633cf8d04aaeec2a841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433986"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Notifica al visor de formularios que el mensaje actual se ha enviado a la cola MAPI.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Parámetros

Ninguno
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha publicado correctamente.
    
## <a name="remarks"></a>Comentarios

Un objeto form llama al método **IMAPIViewAdviseSink::OnSubmitted** después de que una llamada a [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) haya devuelto correctamente. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Después **de llamar a OnSubmitted,** puede continuar con la suposición de que el mensaje se ha actualizado. Actualiza las ventanas para reflejar los cambios que se han producido. 
  
Para obtener más información acerca de las notificaciones de formulario, vea [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Vea también



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

