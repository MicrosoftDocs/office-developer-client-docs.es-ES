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
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317363"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Designa un servicio de mensajes para que sea el proveedor de la identidad principal del perfil.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> a Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes para proporcionar la identidad principal, o null, que indica que **SetPrimaryIdentity** debe borrar la identidad actual. 
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El servicio de mensajes se asignó correctamente al proveedor de la identidad principal.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** intentó designar un servicio de mensajes que tiene la marca SERVICE_NO_PRIMARY_IDENTITY establecida en su propiedad **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin:: SetPrimaryIdentity** establece un servicio de mensajes como el proveedor de la identidad principal del perfil. La identidad principal suele ser el usuario que ha iniciado sesión en el servicio de mensajes. Se representa mediante tres propiedades: 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Todos los proveedores de servicios del servicio de mensajes designados establecen estas tres propiedades en el nombre para mostrar, el identificador de entrada y la clave de búsqueda del usuario de mensajería que proporciona la identidad principal. Los clientes pueden recuperar el identificador de entrada de la identidad principal llamando al método [IMAPISession:: QueryIdentity](imapisession-queryidentity.md) . 
  
La propiedad **PR_RESOURCE_FLAGS** se establece en STATUS_PRIMARY_IDENTITY para todos los proveedores que son miembros del servicio de mensajes que proporciona la identidad principal y para SERVICE_PRIMARY_IDENTITY para el servicio de mensajes. Cuando un proveedor de servicios no puede proporcionar la identidad principal para su servicio de mensajes, establece **PR_RESOURCE_FLAGS** en STATUS_NO_PRIMARY_IDENTITY. **SetPrimaryIdentity** establece la propiedad **PR_RESOURCE_FLAGS** de cada servicio de mensajes que no proporciona la identidad principal a SERVICE_NO_PRIMARY_IDENTITY. 
  
Cada proveedor de servicios de mensajes con el que MAPI tiene información puede establecer una identidad para cada uno de los usuarios cuando un cliente inicia sesión en el servicio. Sin embargo, debido a que MAPI admite conexiones a varios proveedores de servicios para cada sesión de MAPI, no hay ninguna definición de la identidad de un usuario en particular para la sesión MAPI en su conjunto; la identidad de un usuario depende del servicio implicado. Los clientes pueden llamar a **SetPrimaryIdentity** para designar una de las muchas identidades que los servicios de mensajes establecen para un usuario como identidad principal para ese usuario. 
  
## <a name="see-also"></a>Vea también



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

