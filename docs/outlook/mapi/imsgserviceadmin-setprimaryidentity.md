---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 38d55f45280b0b037dc9b5cbbd0dc8809ed04e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817746"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**Hace referencia a**: Outlook 
  
Designa un servicio de mensajes para ser el proveedor de la identidad principal para el perfil.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Parámetros

 _lpUID_
  
> [entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes proporcionar la identidad principal, o NULL, que indica que **SetPrimaryIdentity** debe borrar la identidad actual. 
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El servicio de mensajes se ha asignado correctamente el proveedor de la identidad principal.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** intentó designar un servicio de mensajes que tiene la marca SERVICE_NO_PRIMARY_IDENTITY establecer en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin::SetPrimaryIdentity** establece un servicio de mensajes como el proveedor de la identidad principal para el perfil. La identidad principal normalmente es el usuario que ha iniciado sesión en el servicio de mensajes. Se representan mediante tres propiedades: 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Cada proveedor de servicios en el servicio de mensajes designados establece estas tres propiedades en el nombre para mostrar, el identificador de entrada y la clave de búsqueda del usuario de mensajería que proporciona la identidad principal. Los clientes pueden recuperar el identificador de entrada de la identidad principal al llamar al método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) . 
  
La propiedad **PR_RESOURCE_FLAGS** se establece a STATUS_PRIMARY_IDENTITY para cada proveedor que es un miembro del servicio de mensajes que proporciona la identidad principal y a SERVICE_PRIMARY_IDENTITY para el servicio de mensajes. Cuando un proveedor de servicios no puede facilitar la identidad principal para su servicio de mensajes, establece **PR_RESOURCE_FLAGS** a STATUS_NO_PRIMARY_IDENTITY. **SetPrimaryIdentity** establece la propiedad **PR_RESOURCE_FLAGS** de cada servicio de mensajes que no proporciona la identidad principal a SERVICE_NO_PRIMARY_IDENTITY. 
  
Cada proveedor de servicios de mensaje MAPI tiene información sobre puede establecer una identidad para cada uno de sus usuarios cuando un cliente inicia sesión en el servicio. Sin embargo, debido a que MAPI admite conexiones a varios proveedores de servicio para cada sesión MAPI, no hay ninguna definición firme de identidad de un usuario determinado para la sesión MAPI como un todo; depende de la identidad del usuario en el servicio que está implicado. Los clientes pueden llamar a **SetPrimaryIdentity** para designar una de las muchas identidades establecidas para un usuario por servicios de mensajes como la identidad principal para ese usuario. 
  
## <a name="see-also"></a>Vea también



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

