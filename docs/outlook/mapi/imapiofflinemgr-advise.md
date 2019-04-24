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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321430"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra un cliente para recibir las devoluciones de llamada en un objeto sin conexión.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
>  a Marcas que modifican el comportamiento. Solo se admite el valor MAPIOFFLINE_ADVISE_DEFAULT. 
    
 _pAdviseInfo_
  
> a Información sobre el tipo de devolución de llamada, Cuándo recibir una devolución de llamada, una interfaz de devolución de llamada para la persona que llama y otros detalles. También contiene un token de cliente que Outlook usa para enviar devoluciones de llamada de notificación posteriores al llamador del cliente.
    
 _pulAdviseToken_
  
> contempla Un token de aviso devuelto al llamador del cliente para cancelar posteriormente la devolución de llamada para el objeto.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada se realizó correctamente.
    
E_INVALIDARG
  
> Se ha especificado un parámetro no válido.
    
E_NOINTERFACE
  
> La interfaz de devolución de llamada especificada en *pAdviseInfo* no es válida. 
    
## <a name="remarks"></a>Comentarios

Al abrir un objeto sin conexión mediante **[HrOpenOfflineObj](hropenofflineobj.md)**, un cliente obtiene un objeto sin conexión que admite **IMAPIOfflineMgr**. El cliente puede comprobar los tipos de devoluciones de llamada admitidas por el objeto mediante **[IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)**. El cliente puede determinar el tipo y otros detalles sobre la devolución de llamada que desea y, a continuación, llamar a **IMAPIOfflineMgr:: Advise** para registrarse para recibir las devoluciones de llamada sobre el objeto. 
  
## <a name="see-also"></a>Vea también



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

