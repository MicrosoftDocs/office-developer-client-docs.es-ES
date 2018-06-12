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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: b52dcd87c8714ad59db560a5ae4a8300f9cc83ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817385"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**Se aplica a**: Outlook 
  
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
    
## <a name="remarks"></a>Notas

Quita el registro de la devolución de llamada que se ha asociado con *ulAdviseToken* devuelto desde una llamada anterior a **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Hace que el objeto **IMAPIOfflineMgr** liberar su referencia en el objeto **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** asociado con *ulAdviseToken* . 
  
## <a name="see-also"></a>Ver también



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Constantes MAPI](mapi-constants.md)

