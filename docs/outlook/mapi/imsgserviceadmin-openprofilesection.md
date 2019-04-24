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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317404"
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

## <a name="parameters"></a>Parameters

 _lpUID_
  
> Puntero a la estructura [MAPIUID](mapiuid.md) que identifica la sección de perfil. 
    
 _lpInterface_
  
> a Un puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso a la sección de perfil. Pasar NULL da como resultado un puntero a su interfaz estándar que se está devolviendo en el parámetro _lppProfSect_ . La interfaz estándar para una sección de perfil es **IProfSect**.
    
 _ulFlags_
  
> a Una máscara de máscara de marcas que controla el acceso a la sección de perfil. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProfileSection** se devuelva correctamente, posiblemente antes de que la sección de perfil esté completamente disponible para el cliente que realiza la llamada. Si la sección de perfil no está disponible, realizar una llamada subsiguiente a ella puede generar un error. 
    
MAPI_MODIFY 
  
> Solicita el permiso de lectura y escritura. De forma predeterminada, las secciones de perfil se abren con permiso de solo lectura y los clientes no deben trabajar en el supuesto de que se ha concedido el permiso de lectura y escritura. 
    
MAPI_FORCE_ACCESS
  
> Permite el acceso a todas las secciones de perfil, incluso las que pertenecen a proveedores de servicios individuales.
    
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

El método **IMsgServiceAdmin:: OpenProfileSection** abre una sección de perfil, un objeto que admite la interfaz [IProfSect](iprofsectimapiprop.md) . Las secciones de perfil se usan para leer información y escribir información en el perfil de sesión. 
  
 **OpenProfileSection** no se puede usar para abrir las secciones de perfil que pertenecen a los proveedores de servicios individuales a menos que se use MAPI_FORCE_ACCESS. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Varios clientes pueden abrir una sección de perfil con permiso de solo lectura, pero solo un cliente puede abrir una sección de perfil con permiso de lectura y escritura. Si otro cliente tiene una sección de perfil abierta que intenta abrir llamando a **OpenProfileSection** con el indicador MAPI_MODIFY, se producirá un error en la llamada y se devolverá MAPI_E_NO_ACCESS. 
  
Se producirá un error en una operación de apertura de sólo lectura si la sección está abierta para la escritura. 
  
Puede crear una sección de perfil llamando a **OpenProfileSection** con la marca MAPI_MODIFY y una estructura [MAPIUID](mapiuid.md) no existente en el parámetro _lpUID_ . Asegúrese de especificar MAPI_MODIFY. Si establece _lpUID_ para que apunte a una **MAPIUID** no existente y **OpenProfileSection** se establece para usar el modo de acceso predeterminado de solo lectura, se producirá un error en la llamada con MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI usa el método **IMsgServiceAdmin:: OpenProfileSection** para abrir una sección de perfil.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

