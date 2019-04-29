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

## <a name="parameters"></a>Parameters

 _lpUID_
  
> a Puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil. 
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la sección de perfil. Pasar NULL hace que el parámetro _lppProfSect_ devuelva un puntero a la interfaz estándar de la sección del perfil, **IProfSect**.
    
 _ulFlags_
  
> a Una máscara de máscara de marcas que controla el acceso a la sección de perfil. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProfileSection** se devuelva correctamente, posiblemente antes de que la sección de perfil esté completamente disponible para el cliente que realiza la llamada. Si la sección de perfil no está disponible, realizar una llamada subsiguiente al mismo puede provocar un error. 
    
MAPI_FORCE_ACCESS
  
> Permite el acceso a una sección de perfil que no pertenece al proveedor.
    
MAPI_MODIFY 
  
> Solicita el permiso de lectura y escritura. De forma predeterminada, las secciones de perfil se abren con permiso de solo lectura y los clientes no deben trabajar en el supuesto de que se ha concedido el permiso de lectura y escritura. 
    
 _lppProfSect_
  
> contempla Un puntero a un puntero a la sección de perfil.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La sección de perfil se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se intentó obtener acceso a una sección de perfil para la que el autor de la llamada no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> La sección de perfil solicitada no existe.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: OpenProfileSection** abre una sección o un objeto de perfil que admite la interfaz **IProfSect** . Las secciones de perfil se usan para leer información y escribir información en el perfil de sesión. 
  
No puede usar **OpenProfileSection** para abrir secciones de perfil que sean propias de proveedores de servicios individuales a menos que especifique MAPI_FORCE_ACCESS en el parámetro _ulFlags_ . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Varios clientes pueden abrir una sección de perfil con permiso de solo lectura, pero solo un cliente puede abrir una sección de perfil con permiso de lectura y escritura. Si otro cliente tiene una sección de perfil abierta que intenta abrir llamando a **OpenProfileSection** con el indicador MAPI_MODIFY, se producirá un error en la llamada y se devolverá MAPI_E_NO_ACCESS. 
  
Se producirá un error en una operación de apertura de sólo lectura si la sección está abierta para la escritura. 
  
Puede crear una sección de perfil llamando a **OpenProfileSection** con la marca MAPI_MODIFY y una estructura **MAPIUID** no existente en el parámetro _lpUID_ . Asegúrese de especificar MAPI_MODIFY. Si establece _lpUID_ para que apunte a una **MAPIUID** no existente y **OpenProfileSection** se establece para usar el modo de acceso predeterminado de solo lectura, se producirá un error en la llamada con MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>Ver también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

