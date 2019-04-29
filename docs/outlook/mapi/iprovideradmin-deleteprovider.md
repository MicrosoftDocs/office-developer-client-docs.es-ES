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
ms.openlocfilehash: 28dbbb98c9810bb688b9ecdd730ef6c4ada5f60b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404865"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Elimina un proveedor de servicios del servicio de mensajes.
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in, out] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único que representa al proveedor que se va a eliminar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El proveedor se eliminó correctamente del servicio de mensajes.
    
MAPI_E_NOT_FOUND 
  
> No se reconoció el **MAPIUID** al que señala el parámetro _lpUID_ . 
    
## <a name="remarks"></a>Comentarios

El método **IProviderAdmin::D eleteprovider** elimina un proveedor de servicios del servicio de mensajes. **DeleteProvider** determina el proveedor de servicios que se va a eliminar al hacer coincidir la estructura **MAPIUID** a la que apunta _lpUID_ con el conjunto de identificadores registrados por los proveedores de servicios activos. 
  
La mayoría de los servicios de mensajes no permiten que se eliminen los proveedores mientras el perfil está en uso. Si el proveedor que se va a eliminar está en uso, **DeleteProvider** lo marca para su eliminación en lugar de quitarlo inmediatamente y Devuelve S_OK. Cuando el proveedor ya no se usa, se elimina. 
  
 **DeleteProvider** llama a la función de punto de entrada del servicio de mensajería antes de que se quite el proveedor del servicio. El parámetro _ulContext_ está establecido en MSG_SERVICE_PROVIDER_DELETE. La función de punto de entrada del servicio de mensajes realiza las siguientes tareas: 
  
- Elimina el proveedor de servicios.
    
- Elimina la sección de perfil del proveedor de servicios.
    
No se llama de nuevo a la función de punto de entrada del servicio de mensajes después de que se haya eliminado el proveedor.
  
## <a name="see-also"></a>Ver también



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

