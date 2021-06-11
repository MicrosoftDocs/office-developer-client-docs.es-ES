---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348877"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cierra la sesión de un proveedor de almacén de mensajes. 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in] Reservado; debe ser un puntero a cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de almacén de mensajes implementan el método **IMSLogon::Logoff** para cerrar por la fuerza un proveedor de almacén de mensajes. **Se llama a IMSLogon::Logoff** en las siguientes situaciones: 
  
- Mientras MAPI cierra sesión en un cliente después de una llamada al método [IMAPISession::Logoff.](imapisession-logoff.md) 
    
- Mientras MAPI está iniciando sesión en un proveedor de almacén de mensajes. En este caso, se llama a **IMSLogon::Logoff** como parte del procesamiento MAPI del método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) del objeto de soporte técnico que el proveedor del almacén de mensajes crea mientras procesa una llamada al método [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) o **IUnknown::Release** en un objeto de almacén de mensajes. 
    
## <a name="see-also"></a>Vea también



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

