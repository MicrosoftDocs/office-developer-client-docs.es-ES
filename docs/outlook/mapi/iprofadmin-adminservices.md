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
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422085"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en los servicios de mensajes de un perfil.
  
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
  
> [entrada] Puntero al nombre del perfil que se va a modificar. El  _parámetro lpszProfileName_ no debe ser NULL. 
    
 _lpszPassword_
  
> [entrada] Siempre NULL. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana primaria para los cuadros de diálogo o ventanas que muestra este método.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla la recuperación del objeto de administración del servicio de mensajes. Se pueden establecer las siguientes marcas:
    
MAPI_DIALOG 
  
> Habilita la visualización de una interfaz de usuario. 
    
MAPI_UNICODE 
  
> El nombre del perfil está en formato Unicode. Si no MAPI_UNICODE marca, el nombre está en formato ANSI.
    
 _lppServiceAdmin_
  
> [salida] Puntero a un puntero a un objeto de administración del servicio de mensajes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto de administración del servicio de mensajes se devolvió correctamente.
    
MAPI_E_LOGON_FAILED 
  
> El perfil especificado no existe o la contraseña fue incorrecta y no se pudo mostrar un cuadro de diálogo al usuario para solicitar la contraseña correcta porque MAPI_DIALOG no se estableció en  _ulFlags_.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón** Cancelar de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El **método IProfAdmin::AdminServices** proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en la configuración de los servicios de mensajes en un perfil. 
  
 El  _parámetro lpszPassword_ debe ser NULL o un puntero a una cadena de longitud cero. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Aunque puede recuperar un puntero [IMsgServiceAdmin](imsgserviceadminiunknown.md) llamando a este método o [IMAPISession::AdminServices,](imapisession-adminservices.md)llame a **IProfAdmin::AdminServices** si tiene estrictamente un cliente de configuración y no ofrece características de mensajería. **IProfAdmin::AdminServices** no crea un objeto de sesión y no carga ningún proveedor de servicios, lo que mejora el rendimiento. 
  
No puede usar **IProfAdmin::AdminServices** para crear un perfil. Por lo tanto, debe especificar un perfil válido existente  _en lpszProfileName_. Si el perfil especificado no existe, **IProfAdmin::AdminServices** devuelve MAPI_E_LOGON_FAILED. 
  
El nombre del perfil puede tener hasta 64 caracteres de longitud y puede incluir los siguientes caracteres:
  
- Todos los caracteres alfanuméricos, incluidos los caracteres de énfrica y el carácter de subrayado. 
    
- Espacios incrustados, pero no espacios iniciales o finales.
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI usa el **método IProfAdmin::AdminServices** para abrir un objeto de administración de servicio de mensajes para el perfil seleccionado para agregar servicios.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

