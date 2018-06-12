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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817104"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**Se aplica a**: Outlook 
  
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
    
## <a name="remarks"></a>Notas

Normalmente, se inicia el proceso de cierre de sesión cuando un cliente llama al método [IMAPISession::Logoff](imapisession-logoff.md) para finalizar una sesión. MAPI, a continuación, llama al método **IABLogon::Logoff** de cada proveedor de la libreta de direcciones para iniciar el proceso de cierre de sesión. 
  
El método **IABLogon::Logoff** hace lo siguiente: 
  
- Libera todos los objetos abiertos, como los objetos secundarios o el objeto de estado.
    
- Libera el objeto de Ayuda del proveedor.
    
Para obtener más información acerca del proceso de cierre de sesión de los proveedores de la libreta de direcciones, vea [Cerrando hacia abajo un proveedor de servicios](shutting-down-a-service-provider.md).
  
## <a name="see-also"></a>Ver también



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon: IUnknown](iablogoniunknown.md)

