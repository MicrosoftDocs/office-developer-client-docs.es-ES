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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317118"
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

## <a name="parameters"></a>Parameters

 _lpszProfileName_
  
> a Un puntero al nombre del nuevo perfil.
    
 _lpszPassword_
  
> a Puntero a la contraseña del nuevo perfil. 
    
 _ulUIParam_
  
> a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que muestra este método.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se crea el perfil. Se pueden establecer los siguientes indicadores:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI debe rellenar el nuevo perfil con los servicios de mensajes que se incluyen en la sección [default Services] del archivo MAPISVC. inf.
    
MAPI_DIALOG 
  
> Se pueden mostrar las hojas de propiedades de configuración de cada uno de los proveedores en los servicios de mensajes que se van a agregar. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha creado el nuevo perfil.
    
MAPI_E_NO_ACCESS 
  
> El nuevo perfil especificado ya existe.
    
## <a name="remarks"></a>Comentarios

El método **IProfAdmin:: CreateProfile** crea un nuevo perfil. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Puede llamar a **CreateProfile** en el momento de la instalación de la aplicación o en cualquier momento durante una sesión. Cuando se llama a este método en el momento de la instalación, muchas de las opciones de configuración proceden del archivo de configuración MAPISVC. inf. Cuando se llama a este método durante una sesión activa, la configuración proviene del usuario al que se le solicita a través de una serie de hojas de propiedades. 
  
Si la marca MAPI_DEFAULT_SERVICES se establece en el parámetro _ulFlags_ , **CreateProfile** llama a la función de punto de entrada del servicio de mensajes para cada servicio de mensajes en la sección [default Services] del archivo MAPISVC. inf. Cada función de punto de entrada del servicio de mensajes se llama con el parámetro _ulContext_ establecido en MSG_SERVICE_CREATE. 
  
Si se establecen las dos marcas MAPI_DIALOG y MAPI_DEFAULT_SERVICES, los valores de los parámetros _ulUIParam_ y _ulFlags_ también se pasan a la función de punto de entrada del servicio de mensajes. Solo se llama a las funciones de punto de entrada del servicio de mensajes después de que se haya agregado al perfil toda la información disponible del archivo MAPISVC. inf. 
  
El nombre del nuevo perfil y su contraseña pueden tener hasta 64 caracteres de longitud y pueden incluir los siguientes caracteres:
  
- Todos los caracteres alfanuméricos, incluidos los caracteres de énfasis y el carácter de subrayado.
    
- Espacios insertados, pero no espacios iniciales ni finales.
    
El parámetro _lpszPassword_ debe ser null o un puntero a una cadena de longitud cero. 
  
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

