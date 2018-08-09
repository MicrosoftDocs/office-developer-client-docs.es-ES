---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a15561a6f3af35c1c7c2285bb6252e6400e0e8df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817882"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**Hace referencia a**: Outlook 
  
Crea un nuevo perfil.
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpszProfileName_
  
> [entrada] Un puntero al nombre del nuevo perfil.
    
 _lpszPassword_
  
> [entrada] Un puntero a la contraseña del nuevo perfil. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se crea el perfil. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI debe rellenar el nuevo perfil con los servicios de mensaje que se incluyen en la sección [Services predeterminada] del archivo Mapisvc.inf.
    
MAPI_DIALOG 
  
> Se pueden mostrar las hojas de propiedades de configuración de cada uno de los proveedores en los servicios de mensaje que se va a agregar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se creó el nuevo perfil.
    
MAPI_E_NO_ACCESS 
  
> El nuevo perfil especificado ya existe.
    
## <a name="remarks"></a>Comentarios

El método **IProfAdmin::CreateProfile** crea un nuevo perfil. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Se puede llamar a **CreateProfile** durante la instalación de la aplicación o en cualquier momento durante una sesión. Cuando se llama a este método en tiempo de instalación, muchas de las opciones de configuración proceden del archivo de configuración Mapisvc.inf. Cuando se llama a este método durante una sesión activa, la configuración procedentes del usuario que se le pide a través de una serie de hojas de propiedades. 
  
Si se establece la marca MAPI_DEFAULT_SERVICES en el parámetro _ulFlags_ , **CreateProfile** llama a la función de punto de entrada de servicio de mensaje para cada servicio de mensajes en la sección [Services Default] en el archivo Mapisvc.inf. Cada función de punto de entrada de servicio de mensajes se denomina con el parámetro _ulContext_ establecido en MSG_SERVICE_CREATE. 
  
Si se establecen las marcas MAPI_DIALOG tanto MAPI_DEFAULT_SERVICES, los valores de los parámetros _ulUIParam_ y _ulFlags_ también se pasan a la función de punto de entrada de servicio de mensaje. Las funciones de punto de entrada de servicio de mensajes se denominan sólo después de toda la información disponible desde el archivo Mapisvc.inf se ha agregado al perfil. 
  
El nombre del nuevo perfil y su contraseña puede tener hasta 64 caracteres de longitud y puede incluir los siguientes caracteres:
  
- Todos los caracteres alfanuméricos, incluidos los caracteres de énfasis y el carácter de subrayado.
    
- Espacios incrustados, pero no espacios al principio o al final.
    
El parámetro _lpszPassword_ debe ser NULL o un puntero a una cadena de longitud cero. 
  
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

