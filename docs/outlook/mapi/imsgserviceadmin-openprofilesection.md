---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8dfa777480af48819e5357fad9b1e7524148a8b7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568815"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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
  
> Un puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil. 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil. Si se pasa NULL da como resultado un puntero a su interfaz estándar que se devuelven en el parámetro _lppProfSect_ . La interfaz estándar para una sección de perfil es **IProfSect**.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el acceso a la sección de perfil. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenProfileSection** devolver correctamente, posiblemente antes el perfil de sección es completamente disponible para el cliente de la llamada. Si la sección de perfil no está disponible, realizar una llamada posterior a él puede provocar un error. 
    
MAPI_MODIFY 
  
> Las solicitudes de permiso de lectura y escritura. De forma predeterminada, las secciones del perfil se abren con permiso de sólo lectura, y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
MAPI_FORCE_ACCESS
  
> Permite el acceso a todas las secciones de perfil, incluso los que pertenecen a los proveedores de servicios individuales.
    
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

El método **IMsgServiceAdmin::OpenProfileSection** abre una sección de perfil, un objeto que admite la interfaz [IProfSect](iprofsectimapiprop.md) . Las secciones de perfil se usan para lectura y escritura de información en el perfil de sesión. 
  
 **OpenProfileSection** no se puede usar para abrir secciones de perfil que son propiedad de los proveedores de servicios individuales, a menos que se usa MAPI_FORCE_ACCESS. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Varios clientes pueden abrir una sección de perfil con permiso de sólo lectura, pero sólo un cliente puede abrir una sección de perfil con permiso de lectura y escritura. Si otro cliente tiene una sección de perfil abierto que intenta abrir llamando a **OpenProfileSection** con el conjunto de marca MAPI_MODIFY, la llamada se producirá un error, devolver MAPI_E_NO_ACCESS. 
  
Se produce un error en una operación de apertura de sólo lectura si la sección está abierta para escribir en él. 
  
Puede crear una sección de perfil mediante una llamada a **OpenProfileSection** con la marca MAPI_MODIFY y una estructura [MAPIUID](mapiuid.md) que no existe en el parámetro _lpUID_ . No olvide que especificar MAPI_MODIFY. Si se establece _lpUID_ para que apunte a una que no existe **MAPIUID** y **OpenProfileSection** está configurado para usar el modo de acceso predeterminada de sólo lectura, se producirá un error en la llamada con MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI utiliza el método **IMsgServiceAdmin::OpenProfileSection** para abrir una sección de perfil.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

