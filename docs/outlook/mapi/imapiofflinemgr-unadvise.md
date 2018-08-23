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
ms.openlocfilehash: 35dfc7af9852609dcfcc3fcb9d65ec2e4afa9632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579525"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela devoluciones de llamada para un objeto sin conexión.
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Marcas para cancelar la devolución de llamada. Se admite el valor MAPIOFFLINE_UNADVISE_DEFAULT.
    
 _ulAdviseToken_
  
> [entrada] Símbolo (token) advise que identifica el registro de devolución de llamada que debe cancelarse. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada tuvo éxito. Esta llamada debe devolver S_OK.
    
## <a name="remarks"></a>Comentarios

Quita el registro de la devolución de llamada que se ha asociado con *ulAdviseToken* devuelto desde una llamada anterior a **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Hace que el objeto **IMAPIOfflineMgr** liberar su referencia en el objeto **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** asociado con *ulAdviseToken* . 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Constantes MAPI](mapi-constants.md)

