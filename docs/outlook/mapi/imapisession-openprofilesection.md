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
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439922"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso. 
  
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
  
> [entrada] Puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil. 
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil. Pasar NULL hace que  _el parámetro lppProfSect_ devuelva un puntero a la interfaz estándar de la sección de perfil, **IProfSect**.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el acceso a la sección de perfil. Se pueden establecer las siguientes marcas:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que OpenProfileSection** vuelva correctamente, posiblemente antes de que la sección de perfil esté totalmente disponible para el cliente que realiza la llamada. Si la sección de perfil no está disponible, realizar una llamada posterior a ella puede provocar un error. 
    
MAPI_FORCE_ACCESS
  
> Permite el acceso a una sección de perfil que no pertenece al proveedor.
    
MAPI_MODIFY 
  
> Solicita permiso de lectura y escritura. De forma predeterminada, las secciones de perfil se abren con permiso de solo lectura y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
 _lppProfSect_
  
> [salida] Puntero a un puntero a la sección de perfil.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La sección de perfil se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a una sección de perfil para la que el autor de la llamada no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> La sección de perfil solicitada no existe.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISession::OpenProfileSection** abre una sección de perfil u objeto que admite la **interfaz IProfSect.** Las secciones de perfil se usan para leer y escribir información en el perfil de sesión. 
  
No puede usar **OpenProfileSection para** abrir las secciones de perfil que poseen los proveedores de servicios individuales a menos que MAPI_FORCE_ACCESS en el _parámetro ulFlags._ 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Varios clientes pueden abrir una sección de perfil con permiso de solo lectura, pero solo un cliente puede abrir una sección de perfil con permiso de lectura y escritura. Si otro cliente tiene abierta una sección de perfil que intenta abrir llamando a **OpenProfileSection** con la marca MAPI_MODIFY establecida, se producirá un error en la llamada, lo que MAPI_E_NO_ACCESS. 
  
Se produce un error en una operación de apertura de solo lectura si la sección está abierta para escritura. 
  
Puede crear una sección de perfil llamando a **OpenProfileSection** con la marca MAPI_MODIFY y una estructura **MAPIUID** inexistente en el _parámetro lpUID._ Asegúrese de especificar MAPI_MODIFY. Si establece  _lpUID_ para que apunte a un **MAPIUID** que no existe y **OpenProfileSection** está establecido para usar el modo de acceso predeterminado de solo lectura, la llamada producirá un error con MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>Consulte también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

