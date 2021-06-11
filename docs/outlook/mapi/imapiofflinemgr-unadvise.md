---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404858"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela las devoluciones de llamada de un objeto sin conexión.
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Marcas para cancelar la devolución de llamada. Solo se admite MAPIOFFLINE_UNADVISE_DEFAULT valor.
    
 _ulAdviseToken_
  
> [in] Un token de aviso que identifica el registro de devolución de llamada que se va a cancelar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada se ha realizado correctamente. Esta llamada debe devolver S_OK.
    
## <a name="remarks"></a>Comentarios

Quita el registro de la devolución de llamada asociada con  *ulAdviseToken*  devuelto de una llamada anterior a **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Hace que **el objeto IMAPIOfflineMgr** libere su referencia en el objeto **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** asociado con  *ulAdviseToken*  . 
  
## <a name="see-also"></a>Vea también



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Constantes MAPI](mapi-constants.md)

