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
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434980"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En desuso: se recomienda [el uso de IMsgServiceAdmin2::CreateMsgServiceEx.](imsgserviceadmin2-createmsgserviceex.md) Agrega un servicio de mensajes al perfil actual. 
  
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
  
> [entrada] Puntero al nombre del servicio de mensajes que se agregará. Este nombre del servicio de mensajes debe aparecer en la **sección [Servicios]** del archivo MapiSvc.inf. 
    
 _lpszDisplayName_
  
> [entrada] Puntero al nombre para mostrar del servicio de mensajes que se agregará. El  _parámetro lpszDisplayName_ se omite si el servicio de mensajes ha establecido la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el archivo MapiSvc.inf.
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de cualquier cuadro de diálogo o ventana que muestra este método.
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se instala el servicio de mensajes. Se pueden establecer las siguientes marcas:
    
MAPI_UNICODE
  
> Los parámetros lpszService y lpszDisplayName deben convertirse en LPWSTR e interpretarse como cadenas Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Al agregar un nuevo servicio de mensajes al perfil, el subsistema MAPI, en función de diversas circunstancias y criterios, suele determinar que esta acción requiere un reinicio de Outlook. Si no se incluye la marca SERVICE_NO_RESTART_WARNING y se permite la interfaz de usuario (basada en las marcas SERVICE_UI_ALWAYS y SERVICE_UI_ALLOWED) y al menos un proceso ha iniciado sesión en el perfil actual, esta función muestra el mensaje "Debe reiniciar Outlook para que estos cambios entren en vigor". La inclusión SERVICE_NO_RESTART_WARNING marca suprime la presentación de ese mensaje de advertencia.
    
SERVICE_UI_ALLOWED
  
> La interfaz de usuario de configuración del servicio de mensajes se permite si es necesario.
    
SERVICE_UI_ALWAYS 
  
> El servicio de mensajes muestra su hoja de propiedades de configuración.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND 
  
> El nombre del servicio de mensajes no está en la **sección [Servicios]** de MapiSvc.inf. 
    
## <a name="remarks"></a>Comentarios

El **método IMsgServiceAdmin::CreateMsgService** agrega un servicio de mensajes al perfil actual. **CreateMsgService llama** a la función de punto de entrada del servicio de mensajes para realizar cualquier tarea de configuración específica del servicio. Si la SERVICE_UI_ALLOWED se establece en el parámetro  _ulFlags,_ el servicio de mensajes que se está instalando puede mostrar una hoja de propiedades para permitir al usuario configurar sus opciones. 
  
El archivo MapiSvc.inf contiene la lista de proveedores que forma un servicio de mensajes y las propiedades de cada uno. **CreateMsgService** primero crea una nueva sección de perfil para el servicio de mensajes y, a continuación, copia toda la información de ese servicio desde el archivo MapiSvc.inf en el perfil, creando nuevas secciones para cada proveedor. 
  
Después de copiar toda la información de MapiSvc.inf, se llama a la función de punto de entrada del servicio de mensajes con el valor MSG_SERVICE_CREATE establecido en el _parámetro ulContext._ Si la marca SERVICE_UI_ALLOWED se establece en el parámetro _ulFlags_ del método **CreateMsgService,** los valores de los parámetros _ulUIParam_ y _ulFlags_ también se pasan cuando se llama a la función de punto de entrada del servicio de mensajes. Los proveedores de servicios deben mostrar sus hojas de propiedades de configuración para que los usuarios puedan configurar el servicio de mensajes. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **CreateMsgService** no devuelve la estructura [MAPIUID](mapiuid.md) para el servicio de mensajes que se agregó al perfil. 
  
Para recuperar **mapiuid** para el servicio de mensajes creado, use el siguiente procedimiento: 
  
1. Llame al [método IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obtener la tabla de administración del servicio de mensajes. 
    
2. Busque la fila que representa el servicio de mensajes colocando una restricción en la tabla que coincida con la propiedad **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) con el nombre del servicio de mensajes. 
    
3. Recupere la propiedad **PR_SERVICE_UID** del servicio ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)). 
    
4. Pase el valor de **la PR_SERVICE_UID** en el parámetro  _lpUid_ al método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar el servicio. 
    
> [!CAUTION]
> La implementación de Microsoft Outlook 2010 del subsistema MAPI no admite MAPI_UNICODE y producirá un error si se usa. 
  
> [!IMPORTANT]
> Es posible SERVICE_NO_RESTART_WARNING que el archivo de encabezado  _ulFlags_ no esté definido en el archivo de encabezado descargable que tenga actualmente, en cuyo caso puede agregarlo al código con el siguiente valor: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI usa el **método IMsgServiceAdmin::CreateMsgService** para agregar un servicio a un perfil.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

