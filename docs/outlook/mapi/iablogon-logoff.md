---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a20fdd45c39cc2147f8fdc7b1998ff6d1b0797bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586210"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Inicia el proceso de cierre de sesión.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proceso de cierre de sesión iniciado correctamente.
    
## <a name="remarks"></a>Comentarios

Normalmente, se inicia el proceso de cierre de sesión cuando un cliente llama al método [IMAPISession::Logoff](imapisession-logoff.md) para finalizar una sesión. MAPI, a continuación, llama al método **IABLogon::Logoff** de cada proveedor de la libreta de direcciones para iniciar el proceso de cierre de sesión. 
  
El método **IABLogon::Logoff** hace lo siguiente: 
  
- Libera todos los objetos abiertos, como los objetos secundarios o el objeto de estado.
    
- Libera el objeto de Ayuda del proveedor.
    
Para obtener más información acerca del proceso de cierre de sesión de los proveedores de la libreta de direcciones, vea [Cerrando hacia abajo un proveedor de servicios](shutting-down-a-service-provider.md).
  
## <a name="see-also"></a>Vea también



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

