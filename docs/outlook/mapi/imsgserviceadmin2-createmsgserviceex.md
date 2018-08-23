---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f700389315ca7bd184a9d6defb0b44eaec99a38e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574779"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega un servicio de mensajes para el perfil actual y devuelve que acaba de agregar UID de servicio.
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a>Parámetros

 _lpszService_
  
> [entrada] Un puntero al nombre del servicio de mensajes para agregar. Este nombre de servicio de mensajes debe aparecer en la sección **[Services]** del archivo MapiSvc.inf. 
    
 _lpszDisplayName_
  
> [entrada] Un puntero para el nombre para mostrar del servicio de mensajes para agregar. El parámetro _lpszDisplayName_ se omite si el servicio de mensajes ha establecido la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el archivo MapiSvc.inf.
    
 _ulUIParam_
  
> [entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se instala el servicio de mensajes. Se pueden establecer los siguientes indicadores:
    
MAPI_UNICODE.
  
> El lpszService y los parámetros de lpszDisplayName deben convertirse a LPWSTR e interpreta como cadenas Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Al agregar un nuevo servicio de mensajes para el perfil, el subsistema MAPI, en función de diversos criterios y circunstancias a menudo determina que esta acción requiere un reinicio de Outlook. Si no se incluye la marca SERVICE_NO_RESTART_WARNING y se permite la interfaz de usuario - según los indicadores SERVICE_UI_ALWAYS y SERVICE_UI_ALLOWED - y al menos un proceso ha iniciado sesión en el perfil actual, esta función muestra el mensaje "debe reiniciar Outlook para estos cambios surtan efecto." Incluido el indicador de SERVICE_NO_RESTART_WARNING suprime la visualización de ese mensaje de advertencia.
    
SERVICE_UI_ALLOWED
  
> La configuración del servicio de mensajes que se permite la interfaz de usuario si es necesario.
    
SERVICE_UI_ALWAYS
  
> El servicio de mensajes muestra su hoja de propiedades de configuración.
    
 _lpuidService_
  
> [out] El puntero para el UID del servicio de mensajes agregado.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND
  
> El nombre del servicio de mensajes no está en la sección **[Services]** de MapiSvc.inf. 
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin2::CreateMsgServiceEx** agrega un servicio de mensajes para el perfil actual. **CreateMsgServiceEx** llama a la función de punto de entrada del servicio de mensajes para realizar las tareas de configuración específica de cada servicio. Si se establece la marca SERVICE_UI_ALLOWED en el parámetro _ulFlags_ , el servicio de mensajes que se va a instalar puede mostrar una hoja de propiedades que permite al usuario configurar su configuración. 
  
El archivo MapiSvc.inf contiene la lista de proveedores que componen un servicio de mensajes y las propiedades para cada uno. **CreateMsgServiceEx** primero se crea una nueva sección de perfil para el servicio de mensajes y, a continuación, copia toda la información de ese servicio desde el archivo MapiSvc.inf en el perfil, crear nuevas secciones para cada proveedor. 
  
Después de que toda la información se ha copiado desde MapiSvc.inf, se denomina función de punto de entrada del servicio de mensajes, **MSGSERVICEENTRY**, con el valor MSG_SERVICE_CREATE establecido en el parámetro _ulContext_ . Si se establece la marca SERVICE_UI_ALLOWED en el **CreateMsgServiceEx** parámetro del método _ulFlags_ , también se pasan los valores de los parámetros _ulUIParam_ y _ulFlags_ cuando se llama a la función de punto de entrada del servicio de mensajes. Proveedores de servicios deben mostrar sus hojas de propiedades de configuración, por lo que los usuarios pueden configurar el servicio de mensajes. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si el argumento de _lpuidService_ **CreateMsgServiceEx** no es nulo, se devuelve la propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la que se ha agregado al perfil de servicio de mensajes en el **GUID** al que señala. 
  
Pasar el valor de la propiedad **PR_SERVICE_UID** en el parámetro _lpuidService_ al método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar el servicio. 
  
> [!CAUTION]
> La implementación de Microsoft Outlook 2010 del subsistema MAPI no admite MAPI_UNICODE y se producirá un error si se usa. 
  
> [!IMPORTANT]
> La interfaz de IMsgServiceAdmin2 es expuesta por el mismo objeto que implementa la interfaz IMsgServiceAdmin y ha estado disponible mediante la implementación de Outlook del subsistema MAPI desde Outlook 2003. Su IID se define como sigue: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING no pueden definirse en el archivo de encabezado que se pueden descargar tiene actualmente, en cuyo caso se puede agregar a su código con el siguiente valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Recursos adicionales



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

