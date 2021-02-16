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
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416401"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicia el proceso de cierre de sesión.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proceso de cierre de sesión se inició correctamente.
    
## <a name="remarks"></a>Comentarios

El proceso de cierre de sesión suele iniciarse cuando un cliente llama al método [IMAPISession::Logoff](imapisession-logoff.md) para finalizar una sesión. MAPI llama al método **IABLogon::Logoff** de cada proveedor de libreta de direcciones para iniciar el proceso de cierre de sesión. 
  
El **método IABLogon::Logoff** hace lo siguiente: 
  
- Libera todos los objetos abiertos, como los subobjetos o el objeto de estado.
    
- Libera el objeto de compatibilidad del proveedor.
    
Para obtener más información acerca del proceso de cierre de sesión de los proveedores de libretas de direcciones, vea [Apagar un proveedor de servicios.](shutting-down-a-service-provider.md)
  
## <a name="see-also"></a>Consulte también



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

