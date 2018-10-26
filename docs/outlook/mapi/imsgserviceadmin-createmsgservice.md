---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7c649680d1d04e210ac4d90779e9a4e57aaab25a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579868"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Obsoleto: Se recomienda el uso de [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) . Agrega un servicio de mensajes para el perfil actual. 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
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
    
MAPI_UNICODE
  
> El lpszService y los parámetros de lpszDisplayName deben convertirse a LPWSTR e interpreta como cadenas Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Al agregar un nuevo servicio de mensajes para el perfil, el subsistema MAPI, en función de diversos criterios y circunstancias a menudo determina que esta acción requiere un reinicio de Outlook. Si no se incluye la marca SERVICE_NO_RESTART_WARNING y se permite la interfaz de usuario - según los indicadores SERVICE_UI_ALWAYS y SERVICE_UI_ALLOWED - y al menos un proceso ha iniciado sesión en el perfil actual, esta función muestra el mensaje "debe reiniciar Outlook para estos cambios surtan efecto." Incluido el indicador de SERVICE_NO_RESTART_WARNING suprime la visualización de ese mensaje de advertencia.
    
SERVICE_UI_ALLOWED
  
> La configuración del servicio de mensajes que se permite la interfaz de usuario si es necesario.
    
SERVICE_UI_ALWAYS 
  
> El servicio de mensajes muestra su hoja de propiedades de configuración.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND 
  
> El nombre del servicio de mensajes no está en la sección **[Services]** de MapiSvc.inf. 
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin::** agrega un servicio de mensajes para el perfil actual. **CreateMsgService** llama a la función de punto de entrada del servicio de mensajes para realizar las tareas de configuración específica de cada servicio. Si se establece la marca SERVICE_UI_ALLOWED en el parámetro _ulFlags_ , el servicio de mensajes que se va a instalar puede mostrar una hoja de propiedades para permitir que el usuario realizar la configuración. 
  
El archivo MapiSvc.inf contiene la lista de proveedores que componen un servicio de mensajes y las propiedades para cada uno. **CreateMsgService** primero se crea una nueva sección de perfil para el servicio de mensajes y, a continuación, copia toda la información de ese servicio desde el archivo MapiSvc.inf en el perfil, crear nuevas secciones para cada proveedor. 
  
Después de que toda la información se ha copiado desde MapiSvc.inf, se denomina función de punto de entrada del servicio de mensajes con el valor MSG_SERVICE_CREATE establecido en el parámetro _ulContext_ . Si se establece la marca SERVICE_UI_ALLOWED en el **CreateMsgService** parámetro del método _ulFlags_ , también se pasan los valores de los parámetros _ulUIParam_ y _ulFlags_ cuando se llama a la función de punto de entrada del servicio de mensajes. Proveedores de servicios deben mostrar sus hojas de propiedades de configuración, por lo que los usuarios pueden configurar el servicio de mensajes. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **CreateMsgService** no devuelve la estructura [MAPIUID](mapiuid.md) para el servicio de mensajes que se ha agregado al perfil. 
  
Para recuperar la **MAPIUID** para el servicio de mensaje de creación, utilice el procedimiento siguiente: 
  
1. Llame al método [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obtener la tabla de administración del servicio de mensajes. 
    
2. Busque la fila que representa el servicio de mensajes mediante la colocación de una restricción en la tabla que coincida con la propiedad **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) con el nombre del servicio de mensajes. 
    
3. Recupere la propiedad del servicio **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)). 
    
4. Pasar el valor de la propiedad **PR_SERVICE_UID** en el parámetro _lpUid_ al método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar el servicio. 
    
> [!CAUTION]
> La implementación de Microsoft Outlook 2010 del subsistema MAPI no admite MAPI_UNICODE y se producirá un error si se usa. 
  
> [!IMPORTANT]
> _UlFlags_ SERVICE_NO_RESTART_WARNING no pueden definirse en el archivo de encabezado que se pueden descargar tiene actualmente, en cuyo caso se puede agregar a su código con el siguiente valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI usa el método **IMsgServiceAdmin::** para agregar un servicio a un perfil.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

