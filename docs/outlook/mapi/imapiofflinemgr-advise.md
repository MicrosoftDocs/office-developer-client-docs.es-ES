---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426922"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra un cliente para recibir devoluciones de llamada en un objeto sin conexión.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
>  [in] Marcas que modifican el comportamiento. Solo se admite MAPIOFFLINE_ADVISE_DEFAULT valor. 
    
 _pAdviseInfo_
  
> [in] Información sobre el tipo de devolución de llamada, cuándo recibir una devolución de llamada, una interfaz de devolución de llamada para el autor de la llamada y otros detalles. También contiene un token de cliente que Outlook para enviar devoluciones de llamada de notificación posteriores al autor de la llamada del cliente.
    
 _pulAdviseToken_
  
> [salida] Un token de aviso devuelto al autor de la llamada del cliente para cancelar posteriormente la devolución de llamada del objeto.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada se ha realizado correctamente.
    
E_INVALIDARG
  
> Se ha especificado un parámetro no válido.
    
E_NOINTERFACE
  
> La interfaz de devolución de llamada especificada en  *pAdviseInfo*  no es válida. 
    
## <a name="remarks"></a>Comentarios

Al abrir un objeto sin conexión mediante **[HrOpenOfflineObj](hropenofflineobj.md)**, un cliente obtiene un objeto sin conexión que admite **IMAPIOfflineMgr**. El cliente puede comprobar los tipos de devoluciones de llamada compatibles con el objeto mediante **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. El cliente puede determinar el tipo y otros detalles sobre la devolución de llamada que desea y, a continuación, llamar a **IMAPIOfflineMgr::Advise** para registrarse para recibir dichas devoluciones de llamada sobre el objeto. 
  
## <a name="see-also"></a>Vea también



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

