---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5b96a45bab4cd00d23604d0b0b25f3e772277395
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817749"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**Hace referencia a**: Outlook 
  
Establece el orden en que transporte se denominan proveedores para entregar un mensaje.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Parámetros

 _cUID_
  
> [entrada] El recuento de identificadores únicos en el parámetro _lpUIDList_ . 
    
 _lpUIDList_
  
> [entrada] Un puntero a una matriz de identificadores únicos que representan los proveedores de transporte. La matriz contiene un identificador para cada proveedor de transporte configurado en el perfil actual.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se estableció correctamente en el orden de transporte.
    
MAPI_E_BUSY 
  
> El valor en el parámetro _cUID_ difiere del número de proveedores de transporte realmente en el perfil. 
    
MAPI_E_NOT_FOUND 
  
> Una o varias de las estructuras [MAPIUID](mapiuid.md) que se pasa en el parámetro _lpUIDList_ no hacen referencia a un proveedor de transporte que están actualmente en el perfil. 
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin::MsgServiceTransportOrder** establece el orden de entrega de los proveedores de transporte en un perfil. El parámetro _lpUIDList_ debe contener una lista ordenada de los identificadores de entrada de proveedor de transporte obtenido de la propiedad **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) de la tabla devuelta desde el [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) (método). Una aplicación de cliente debe pasar la lista completa de _lpUIDList_.
  
 **SetTransportOrder** invalidaciones de transporte preferencias de proveedor como la marca STATUS_XP_PREFER_LAST establecida en la propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)). 
  
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

