---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e5f329ef0d3483683d5c94ed38c6631d86e77b93
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817460"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**Hace referencia a**: Outlook 
  
Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Parámetros

 _lpUID_
  
> [entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil. 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil. Pasando NULL hace que el parámetro _lppProfSect_ devolver un puntero a la interfaz estándar de la sección de perfil, **IProfSect**.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el acceso a la sección de perfil. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenProfileSection** devolver correctamente, posiblemente antes el perfil de sección es completamente disponible para el cliente de la llamada. Si la sección de perfil no está disponible, realizar una llamada posterior a él puede provocar un error. 
    
MAPI_FORCE_ACCESS
  
> Permite el acceso a una sección de perfil que no pertenecen al proveedor.
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, las secciones del perfil se abren con permiso de sólo lectura, y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
 _lppProfSect_
  
> [out] Un puntero a un puntero a la sección de perfil.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La sección de perfil se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado tener acceso a una sección de perfil para el que el autor de la llamada no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> La sección de perfil solicitado no existe.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession::OpenProfileSection** abre una sección de perfil o un objeto que admite la interfaz **IProfSect** . Las secciones de perfil se usan para lectura y escritura de información en el perfil de sesión. 
  
No se puede usar **OpenProfileSection** para abrir las secciones del perfil que proveedores de servicio individuales propio a menos que especifique el parámetro _ulFlags_ MAPI_FORCE_ACCESS. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Varios clientes pueden abrir una sección de perfil con permiso de sólo lectura, pero sólo un cliente puede abrir una sección de perfil con permiso de lectura y escritura. Si otro cliente tiene una sección de perfil abierto que intenta abrir llamando a **OpenProfileSection** con el conjunto de marca MAPI_MODIFY, la llamada se producirá un error, devolver MAPI_E_NO_ACCESS. 
  
Se produce un error en una operación de apertura de sólo lectura si la sección está abierta para escribir en él. 
  
Puede crear una sección de perfil mediante una llamada a **OpenProfileSection** con la marca MAPI_MODIFY y una estructura **MAPIUID** que no existe en el parámetro _lpUID_ . Asegúrese de que especificar MAPI_MODIFY. Si se establece _lpUID_ para que apunte a una que no existe **MAPIUID** y **OpenProfileSection** está configurado para usar el modo de acceso predeterminada de sólo lectura, se producirá un error en la llamada con MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>Vea también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

