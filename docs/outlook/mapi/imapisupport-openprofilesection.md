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
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411389"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una sección del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Parameters

 _lpUid_
  
> [in] Puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil que se va a abrir. Si se pasa NULL para  _el parámetro lpUid,_ se abre la sección de perfil del autor de la llamada. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre la sección de perfil. Se pueden establecer las siguientes marcas:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que OpenProfileSection** vuelva correctamente, posiblemente antes de que la sección de perfil sea totalmente accesible para el autor de la llamada. Si la sección de perfil no es accesible, realizar una llamada de objeto posterior puede provocar un error. 
    
MAPI_MODIFY 
  
> Solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren como de solo lectura y los autores de llamadas no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
 _lppProfileObj_
  
> [salida] Puntero a un puntero a la sección de perfil abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La sección de perfil se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se intentó modificar una sección de perfil de solo lectura o obtener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> No hay una sección de perfil asociada con el identificador de entrada pasado en  _lpEntryID_.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Se usaron marcas reservadas o no admitidas y, por lo tanto, la operación no se ha completado.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::OpenProfileSection** se implementa para todos los objetos de soporte técnico. Los proveedores de servicios y servicios de mensajes llaman a **OpenProfileSection** para abrir una sección de perfil y recuperar un puntero a su implementación de interfaz **IProfSect.** 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **OpenProfileSection** abre secciones de perfil como de solo lectura, a menos que establezca la marca MAPI_MODIFY en el  _parámetro ulFlags_ y su permiso sea suficiente. Establecer esta marca no garantiza el permiso de lectura y escritura; los permisos que se le concedan dependen del nivel de acceso y del objeto. 
  
Si **OpenProfileSection intenta** abrir una sección de perfil inexistente como de solo lectura, devuelve MAPI_E_NOT_FOUND. Si **OpenProfileSection intenta** abrir una sección de perfil inexistente como lectura y escritura, crea la sección de perfil y devuelve el puntero **IProfSect.** 
  
## <a name="see-also"></a>Vea también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

