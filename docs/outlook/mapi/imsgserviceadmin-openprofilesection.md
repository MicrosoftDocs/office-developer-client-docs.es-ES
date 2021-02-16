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
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437115"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
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
  
> Puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil. 
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la sección de perfil. Si se pasa NULL, se devuelve un puntero a su interfaz estándar en el parámetro _lppProfSect._ La interfaz estándar para una sección de perfil **es IProfSect**.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla el acceso a la sección de perfil. Se pueden establecer las siguientes marcas:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que OpenProfileSection** vuelva correctamente, posiblemente antes de que la sección de perfil esté totalmente disponible para el cliente que realiza la llamada. Si la sección de perfil no está disponible, realizar una llamada posterior a ella puede generar un error. 
    
MAPI_MODIFY 
  
> Solicita permiso de lectura y escritura. De forma predeterminada, las secciones de perfil se abren con permiso de solo lectura y los clientes no deben trabajar en la suposición de que se ha concedido permiso de lectura y escritura. 
    
MAPI_FORCE_ACCESS
  
> Permite el acceso a todas las secciones de perfil, incluso a las que pertenecen a proveedores de servicios individuales.
    
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

El **método IMsgServiceAdmin::OpenProfileSection** abre una sección de perfil, un objeto que admite la [interfaz IProfSect.](iprofsectimapiprop.md) Las secciones de perfil se usan para leer y escribir información en el perfil de sesión. 
  
 **OpenProfileSection** no se puede usar para abrir secciones de perfil propiedad de proveedores de servicios individuales a menos MAPI_FORCE_ACCESS se use. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Varios clientes pueden abrir una sección de perfil con permiso de solo lectura, pero solo un cliente puede abrir una sección de perfil con permiso de lectura y escritura. Si otro cliente tiene abierta una sección de perfil que intenta abrir llamando a **OpenProfileSection** con la marca MAPI_MODIFY establecida, se producirá un error en la llamada, lo que MAPI_E_NO_ACCESS. 
  
Se produce un error en una operación de apertura de solo lectura si la sección está abierta para escritura. 
  
Puede crear una sección de perfil llamando a **OpenProfileSection** con la marca MAPI_MODIFY y una estructura [MAPIUID](mapiuid.md) inexistente en el _parámetro lpUID._ Asegúrese de especificar MAPI_MODIFY. Si establece  _lpUID_ para que apunte a un **MAPIUID** que no existe y **OpenProfileSection** está establecido para usar el modo de acceso predeterminado de solo lectura, la llamada producirá un error con MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI usa el **método IMsgServiceAdmin::OpenProfileSection** para abrir una sección de perfil.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

