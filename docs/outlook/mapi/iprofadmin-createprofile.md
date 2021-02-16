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
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404403"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
> [entrada] Puntero al nombre del nuevo perfil.
    
 _lpszPassword_
  
> [entrada] Puntero a la contraseña del nuevo perfil. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se crea el perfil. Se pueden establecer las siguientes marcas:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI debe rellenar el nuevo perfil con los servicios de mensaje que se incluyen en la sección [Servicios predeterminados] del archivo Mapisvc.inf.
    
MAPI_DIALOG 
  
> Se pueden mostrar las hojas de propiedades de configuración de cada uno de los proveedores de los servicios de mensajes que se van a agregar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se creó el nuevo perfil.
    
MAPI_E_NO_ACCESS 
  
> El nuevo perfil especificado ya existe.
    
## <a name="remarks"></a>Comentarios

El **método IProfAdmin::CreateProfile** crea un nuevo perfil. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede llamar a **CreateProfile en el** momento de la instalación de la aplicación o en cualquier momento durante una sesión. Cuando se llama a este método en el momento de la instalación, muchas de las opciones de configuración provienen del archivo de configuración Mapisvc.inf. Cuando se llama a este método durante una sesión activa, la configuración procede del usuario al que se le solicita a través de una serie de hojas de propiedades. 
  
Si la marca MAPI_DEFAULT_SERVICES se establece en el parámetro  _ulFlags,_ **CreateProfile** llama a la función de punto de entrada del servicio de mensajes para cada servicio de mensajes en la sección [Servicios predeterminados] del archivo Mapisvc.inf. Se llama a cada función de punto de entrada del servicio de mensajes con el  _parámetro ulContext_ establecido en MSG_SERVICE_CREATE. 
  
Si se establecen las marcas MAPI_DIALOG y MAPI_DEFAULT_SERVICES, los valores de los parámetros  _ulUIParam_ y  _ulFlags_ también se pasan a la función de punto de entrada del servicio de mensajes. Solo se llama a las funciones de punto de entrada del servicio de mensajes después de que toda la información disponible del archivo Mapisvc.inf se haya agregado al perfil. 
  
El nombre del nuevo perfil y su contraseña pueden tener hasta 64 caracteres de longitud y pueden incluir los siguientes caracteres:
  
- Todos los caracteres alfanuméricos, incluidos los caracteres de énfrica y el carácter de subrayado.
    
- Espacios incrustados, pero no espacios iniciales o finales.
    
El  _parámetro lpszPassword_ debe ser NULL o un puntero a una cadena de longitud cero. 
  
## <a name="see-also"></a>Consulte también



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

