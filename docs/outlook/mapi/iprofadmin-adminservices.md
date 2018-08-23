---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a9e596ff8561d5aabc71ffe3540efaeef8f5b83d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593987"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en los servicios de mensaje en un perfil.
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Parámetros

 _lpszProfileName_
  
> [entrada] Un puntero al nombre del perfil que desea modificar. El parámetro _lpszProfileName_ no debe ser NULL. 
    
 _lpszPassword_
  
> [entrada] Siempre es NULL. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la recuperación del objeto de administración de servicio de mensaje. Se pueden establecer los siguientes indicadores:
    
MAPI_DIALOG 
  
> Habilita la presentación de una interfaz de usuario. 
    
MAPI_UNICODE. 
  
> El nombre del perfil está en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., el nombre está en formato ANSI.
    
 _lppServiceAdmin_
  
> [out] Un puntero a un puntero a un objeto de administración del servicio de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto de administración del servicio de mensajes se devolvió correctamente.
    
MAPI_E_LOGON_FAILED 
  
> El perfil especificado no existe, o la contraseña es incorrecta y no se pudo mostrar un cuadro de diálogo al usuario para solicitar la contraseña correcta debido a que no se estableció en MAPI_DIALOG en _ulFlags_.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El método **IProfAdmin::AdminServices** proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en los servicios de mensaje en un perfil de configuración. 
  
 El parámetro _lpszPassword_ debe ser NULL o un puntero a una cadena de longitud cero. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Aunque puede recuperar un puntero [IMsgServiceAdmin](imsgserviceadminiunknown.md) mediante una llamada a este método o el [IMAPISession::AdminServices](imapisession-adminservices.md), llamar a **IProfAdmin::AdminServices** si tiene un cliente de configuración de manera estricta y ofrecer no hay características de mensajería. **IProfAdmin::AdminServices** no crea un objeto de sesión y no se carga ningún proveedor de servicios, que mejora el rendimiento. 
  
No se puede usar **IProfAdmin::AdminServices** para crear un perfil. Por lo tanto, debe especificar un perfil existente válido en _lpszProfileName_. Si no existe el perfil especificado, **IProfAdmin::AdminServices** devuelve MAPI_E_LOGON_FAILED. 
  
El nombre del perfil puede tener hasta 64 caracteres de longitud y puede incluir los siguientes caracteres:
  
- Todos los caracteres alfanuméricos, incluidos los caracteres de énfasis y el carácter de subrayado. 
    
- Espacios incrustados, pero no espacios al principio o al final.
    
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI utiliza el método **IProfAdmin::AdminServices** para abrir un objeto de administración del servicio de mensajes para el perfil seleccionado agregar servicios.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

