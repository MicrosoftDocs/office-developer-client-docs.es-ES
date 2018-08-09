---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e0f8dc1beeb669532e3731b38a4f03966403f76c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817896"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**Hace referencia a**: Outlook 
  
Elimina un proveedor de servicios desde el servicio de mensajes.
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>Parámetros

 _lpUID_
  
> [entrada, salida] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único que representa el proveedor que se va a eliminar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proveedor se eliminó correctamente desde el servicio de mensajes.
    
MAPI_E_NOT_FOUND 
  
> No se reconoció la **MAPIUID** indicada por el parámetro _lpUID_ . 
    
## <a name="remarks"></a>Comentarios

El método **IProviderAdmin::DeleteProvider** elimina un proveedor de servicios desde el servicio de mensajes. **DeleteProvider** determina el proveedor de servicios para eliminar de forma que coincidan con la estructura **MAPIUID** que señala _lpUID_ con el conjunto de identificadores registrados por los proveedores de servicio de active. 
  
La mayoría de los servicios de mensaje no permiten que los proveedores se elimina mientras el perfil está en uso. Si el proveedor que se va a eliminar está en uso, **DeleteProvider** se marca para su eliminación en lugar de quitarlo inmediatamente y devuelve S_OK. Cuando ya no se usa el proveedor, se elimina. 
  
 **DeleteProvider** llama a la función de punto de entrada del servicio de mensajes antes de que se ha quitado el proveedor del servicio. El parámetro _ulContext_ se establece en MSG_SERVICE_PROVIDER_DELETE. La función de punto de entrada de servicio de mensaje lleva a cabo las siguientes tareas: 
  
- Elimina el proveedor de servicios.
    
- Elimina la sección de perfil de un proveedor de servicios.
    
La función de punto de entrada de servicio de mensajes no se llama de nuevo después de que se ha eliminado el proveedor.
  
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

