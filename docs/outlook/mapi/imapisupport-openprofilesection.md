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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326449"
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
  
> a Puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil que se va a abrir. Al pasar NULL para el parámetro _lpUid_ , se abre la sección de perfil del autor de la llamada. 
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se abre la sección de perfil. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProfileSection** se devuelva correctamente, posiblemente antes de que el autor de la llamada pueda obtener acceso total a la sección del perfil. Si no se puede tener acceso a la sección de perfil, realizar una llamada de objeto subsiguiente puede dar como resultado un error. 
    
MAPI_MODIFY 
  
> Solicita el permiso de lectura y escritura. De forma predeterminada, los objetos se abren como de solo lectura y los llamadores no deben trabajar en el supuesto de que se ha concedido el permiso de lectura y escritura. 
    
 _lppProfileObj_
  
> contempla Un puntero a un puntero a la sección de perfil abierta.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La sección de perfil se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se intentó modificar una sección de Perfil de solo lectura o tener acceso a un objeto para el que el autor de la llamada no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> No hay ninguna sección de perfil asociada con el identificador de entrada pasado en _lpEntryID_.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Se usaron marcas reservadas o no admitidas y, por lo tanto, la operación no se completó.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport:: OpenProfileSection** se implementa para todos los objetos de compatibilidad. Los proveedores de servicios y los servicios de mensajes llaman a **OpenProfileSection** para abrir una sección de perfil y recuperar un puntero a su implementación de interfaz de **IProfSect** . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **OpenProfileSection** abre secciones de perfil como de solo lectura, a menos que establezca la marca MAPI_MODIFY en el parámetro _ulFlags_ y el permiso sea suficiente. La configuración de esta marca no garantiza el permiso de lectura y escritura; los permisos que se conceden dependen del nivel de acceso y del objeto. 
  
Si **OpenProfileSection** intenta abrir una sección de un perfil que no existe como de sólo lectura, devuelve MAPI_E_NOT_FOUND. Si **OpenProfileSection** intenta abrir una sección de perfil que no existe como de lectura y escritura, crea la sección de perfil y devuelve el puntero **IProfSect** . 
  
## <a name="see-also"></a>Vea también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

