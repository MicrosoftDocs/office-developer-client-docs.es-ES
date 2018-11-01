---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0f917989d9bac403f2bea5b2d6699b7a1caf2008
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573015"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Abre una sección de perfil desde el perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso. 
  
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
  
> [entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para la sección de perfil que se va a abrir. Los clientes no deben pasar NULL para el parámetro _lpUID_ . Proveedores de servicios pueden pasar NULL para recuperar el **MAPIUID** al que llaman desde sus funciones de punto de entrada de servicio de mensaje. 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil. Si se pasa NULL da como resultado en la interfaz de estándar de la sección perfil (**IProfSect**) que se devuelven. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se abre la sección de perfil. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenProfileSection** devolver de correctamente, posiblemente antes de la sección de perfil es completamente disponible para el autor de la llamada. Si la sección de perfil no está disponible, realizar una llamada posterior a él puede provocar un error. 
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren con permiso de sólo lectura y los autores de llamadas no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. Permiso de lectura y escritura a las secciones del proveedor del perfil no se permiten a los clientes.
    
MAPI_FORCE_ACCESS
  
> Permite el acceso a todas las secciones de perfil, incluso los que pertenecen a los proveedores de servicios individuales.
    
 _lppProfSect_
  
> [out] Un puntero a un puntero a la sección de perfil.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La sección de perfil se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se ha intentado modificar una sección de perfil de sólo lectura o tener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> La sección de perfil solicitado no existe.
    
## <a name="remarks"></a>Comentarios

El método **IProviderAdmin::OpenProfileSection** abre una sección de perfil, que permita el autor de la llamada leer información desde y, posiblemente, escribir información en el perfil activo. 
  
Los clientes no pueden abrir las secciones de perfil que pertenecen a los proveedores mediante el método **OpenProfileSection** . 
  
Varios clientes o proveedores de servicios pueden abrir simultáneamente una sección de perfil con permiso de sólo lectura. Sin embargo, cuando una sección de perfil está abierta con permiso de lectura y escritura, no hay otras llamadas pueden estar para abrir la sección, independientemente del tipo de acceso. Si una sección de perfil se abre con permiso de sólo lectura, se producirá un error en una llamada posterior a la solicitud de permiso de lectura y escritura con MAPI_E_NO_ACCESS. Del mismo modo, si una sección está abierta con permiso de lectura y escritura, también producirá una llamada posterior a la solicitud de permiso de sólo lectura. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si solicita **OpenProfileSection** para abrir una sección de perfil que no existe, pasando MAPI_MODIFY _ulFlags_ y se creará un desconocido **MAPIUID** en _lpUID_, la sección de perfil. 
  
Si solicita que **OpenProfileSection** abrir una sección que no existe con permiso de sólo lectura, devuelve MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI utiliza el método **IProviderAdmin::OpenProfileSection** para abrir una sección de perfil desde el perfil actual.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

