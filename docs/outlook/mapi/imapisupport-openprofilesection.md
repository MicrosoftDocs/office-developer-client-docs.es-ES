---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2f45028219f0f5f4cc881db3bc512626b3ad2f4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817526"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**Hace referencia a**: Outlook 
  
Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Parámetros

 _lpUid_
  
> [entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil que se va a abrir. Al pasar NULL para el parámetro _lpUid_ abre la sección de perfil del autor de la llamada. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre la sección de perfil. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenProfileSection** devolver correctamente, posiblemente antes el perfil de sección es totalmente accesible para el autor de la llamada. Si la sección de perfil no está accesible, realizar una llamada de objeto subsiguientes se puede producir un error. 
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren como de sólo lectura y los autores de llamadas no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
 _lppProfileObj_
  
> [out] Un puntero a un puntero a la sección de perfil abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La sección de perfil se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado modificar una sección de perfil de sólo lectura o tener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> No hay una sección de perfil asociada con el identificador de entrada que se pasó _lpEntryID_.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Indicadores reservados o no compatibles se usaron y, por lo tanto, no se completó la operación.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::OpenProfileSection** se implementa para todos los objetos de soporte técnico. Proveedores de servicio y servicios de mensajes de llamada **OpenProfileSection** para abrir una sección de perfil y recuperar un puntero a su implementación de la interfaz **IProfSect** . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **OpenProfileSection** abre secciones de perfil como de solo lectura, a menos que se establece la marca MAPI_MODIFY en el parámetro _ulFlags_ y su permiso es suficiente. Establecer esta marca no garantiza el permiso de lectura y escritura; los permisos que se le concede dependen de su nivel de acceso y el objeto. 
  
Si **OpenProfileSection** intenta abrir una sección de perfil que no existe como de sólo lectura, devuelve MAPI_E_NOT_FOUND. Si **OpenProfileSection** intenta abrir una sección de perfil que no existe como lectura y escritura, la sección de perfil se crea y devuelve el puntero **IProfSect** . 
  
## <a name="see-also"></a>Vea también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

