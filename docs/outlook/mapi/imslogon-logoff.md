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
ms.openlocfilehash: 5d9a57cee371675493ba71b2df52b83941d34fc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817816"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**Hace referencia a**: Outlook 
  
Proveedor de almacén de registros de un mensaje. 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpulFlags_
  
> [entrada] Reservado; debe ser un puntero a cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de almacén de mensajes implementan el método **IMSLogon::Logoff** para forzar apagar un proveedor de almacén de mensajes. Se denomina **IMSLogon::Logoff** en las situaciones siguientes: 
  
- Mientras MAPI está cerrando un cliente después de una llamada al método [IMAPISession::Logoff](imapisession-logoff.md) . 
    
- Mientras MAPI está cerrando un proveedor de almacén de mensajes. En este caso, se denomina **IMSLogon::Logoff** como parte de MAPI al procesar el método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) del objeto de soporte técnico que el proveedor de almacenamiento de mensaje crea mientras está procesando un [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) o **IUnknown:: Versión** llamada al método en un objeto de almacén de mensajes. 
    
## <a name="see-also"></a>Vea también



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

