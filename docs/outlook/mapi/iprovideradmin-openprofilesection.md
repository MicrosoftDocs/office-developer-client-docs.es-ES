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
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405663"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Abre una sección de perfil del perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso. 
  
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
  
> [in] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único de la sección de perfil que se va a abrir. Los clientes no deben pasar NULL para el _parámetro lpUID._ Los proveedores de servicios pueden pasar NULL para recuperar **MAPIUID** cuando llaman desde sus funciones de punto de entrada de servicio de mensajes. 
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil. Si se pasa NULL, se devuelve la interfaz estándar de la sección de perfil (**IProfSect).** 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se abre la sección de perfil. Se pueden establecer las siguientes marcas:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que OpenProfileSection** vuelva correctamente, posiblemente antes de que la sección de perfil esté totalmente disponible para el autor de la llamada. Si la sección de perfil no está disponible, realizar una llamada posterior a ella puede generar un error. 
    
MAPI_MODIFY 
  
> Solicitudes de permiso de lectura y escritura. De forma predeterminada, los objetos se abren con permiso de solo lectura y los autores de llamadas no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. Los clientes no tienen permiso de lectura y escritura para las secciones del proveedor del perfil.
    
MAPI_FORCE_ACCESS
  
> Permite el acceso a todas las secciones de perfil, incluso las que pertenecen a proveedores de servicios individuales.
    
 _lppProfSect_
  
> [salida] Puntero a un puntero a la sección de perfil.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La sección de perfil se abrió correctamente.
    
MAPI_E_NO_ACCESS 
  
> Se intentó modificar una sección de perfil de solo lectura o obtener acceso a un objeto para el que el usuario no tiene permisos suficientes.
    
MAPI_E_NOT_FOUND 
  
> La sección de perfil solicitado no existe.
    
## <a name="remarks"></a>Comentarios

El **método IProviderAdmin::OpenProfileSection** abre una sección de perfil, lo que permite al autor de la llamada leer información y, posiblemente, escribir información en el perfil activo. 
  
Los clientes no pueden abrir secciones de perfil que pertenecen a proveedores mediante el **método OpenProfileSection.** 
  
Varios clientes o proveedores de servicios pueden abrir simultáneamente una sección de perfil con permiso de solo lectura. Sin embargo, cuando una sección de perfil está abierta con permiso de lectura y escritura, no se pueden realizar otras llamadas para abrir la sección, independientemente del tipo de acceso. Si una sección de perfil está abierta con permiso de solo lectura, se producirá un error en una llamada posterior para solicitar permiso de lectura y escritura con MAPI_E_NO_ACCESS. Del mismo modo, si una sección está abierta con permiso de lectura y escritura, también se producirá un error en una llamada posterior para solicitar permiso de solo lectura. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si solicita que **OpenProfileSection** abra una sección de perfil inexistente pasando MAPI_MODIFY  _en ulFlags_ y un **MAPIUID** desconocido en  _lpUID,_ se creará la sección de perfil. 
  
Si solicita que **OpenProfileSection** abra una sección inexistente con permiso de solo lectura, devuelve MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI usa el **método IProviderAdmin::OpenProfileSection** para abrir una sección de perfil desde el perfil actual.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

