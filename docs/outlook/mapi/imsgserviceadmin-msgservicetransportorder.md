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
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420097"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el orden en que se llama a los proveedores de transporte para entregar un mensaje.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Parameters

 _cUID_
  
> [in] Recuento de identificadores únicos en el _parámetro lpUIDList._ 
    
 _lpUIDList_
  
> [in] Puntero a una matriz de identificadores únicos que representan proveedores de transporte. La matriz contiene un identificador para cada proveedor de transporte configurado en el perfil actual.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El orden de transporte se estableció correctamente.
    
MAPI_E_BUSY 
  
> El valor del  _parámetro cUID_ difiere del número de proveedores de transporte en realidad en el perfil. 
    
MAPI_E_NOT_FOUND 
  
> Una o varias de las estructuras [MAPIUID](mapiuid.md) pasadas en el parámetro  _lpUIDList_ no hacen referencia a un proveedor de transporte actualmente en el perfil. 
    
## <a name="remarks"></a>Comentarios

El **método IMsgServiceAdmin::MsgServiceTransportOrder** establece el orden de entrega de los proveedores de transporte en un perfil. El parámetro _lpUIDList_ debe contener una lista ordenada de identificadores de entrada del proveedor de transporte obtenidos **de** la propiedad PR_PROVIDER_UID ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) de la tabla devuelta desde el método [IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md) Una aplicación cliente debe pasar la lista completa  _en lpUIDList_.
  
 **SetTransportOrder** invalida las preferencias del proveedor de transporte, como la marca STATUS_XP_PREFER_LAST establecida en **la propiedad PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)). 
  
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

