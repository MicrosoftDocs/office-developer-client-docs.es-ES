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
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410185"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Agrega un servicio de mensajes al perfil actual y devuelve ese UID de servicio recién agregado.
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a>Parameters

 _lpszService_
  
> [in] Puntero al nombre del servicio de mensajes que se agregará. Este nombre del servicio de mensajes debe aparecer en la sección **[Servicios]** del archivo MapiSvc.inf. 
    
 _lpszDisplayName_
  
> [in] Puntero al nombre para mostrar del servicio de mensajes que se agregará. El  _parámetro lpszDisplayName_ se omite si el servicio de mensajes ha establecido la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el archivo MapiSvc.inf.
    
 _ulUIParam_
  
> [in] Un identificador de la ventana principal de cualquier cuadro de diálogo o ventana que muestre este método.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se instala el servicio de mensajes. Se pueden establecer las siguientes marcas:
    
MAPI_UNICODE
  
> Los parámetros lpszService y lpszDisplayName deben convertirse en LPWSTR e interpretarse como cadenas Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Al agregar un nuevo servicio de mensajes al perfil, el subsistema MAPI, en función de diversas circunstancias y criterios, suele determinar que esta acción requiere un reinicio de Outlook. Si no se incluye la marca SERVICE_NO_RESTART_WARNING y se permite la interfaz de usuario (en función de las marcas SERVICE_UI_ALWAYS y SERVICE_UI_ALLOWED) y al menos un proceso se inicia sesión en el perfil actual, esta función muestra el mensaje "Debe reiniciar Outlook para que estos cambios entren en vigor". La inclusión SERVICE_NO_RESTART_WARNING marca elimina la presentación de ese mensaje de advertencia.
    
SERVICE_UI_ALLOWED
  
> La interfaz de usuario de configuración del servicio de mensajes se permite si es necesario.
    
SERVICE_UI_ALWAYS
  
> El servicio de mensajes muestra su hoja de propiedades de configuración.
    
 _lpuidService_
  
> [salida] El puntero al UID del servicio de mensajes agregado.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND
  
> El nombre del servicio de mensajes no está en la sección **[Servicios]** de MapiSvc.inf. 
    
## <a name="remarks"></a>Comentarios

El **método IMsgServiceAdmin2::CreateMsgServiceEx** agrega un servicio de mensajes al perfil actual. **CreateMsgServiceEx** llama a la función de punto de entrada del servicio de mensajes para realizar cualquier tarea de configuración específica del servicio. Si la SERVICE_UI_ALLOWED se establece en el parámetro  _ulFlags,_ el servicio de mensajes que se está instalando puede mostrar una hoja de propiedades que permita al usuario configurar sus opciones. 
  
El archivo MapiSvc.inf contiene la lista de proveedores que forma un servicio de mensajes y las propiedades de cada uno. **CreateMsgServiceEx** primero crea una nueva sección de perfil para el servicio de mensajes y, a continuación, copia toda la información de ese servicio desde el archivo MapiSvc.inf en el perfil, creando nuevas secciones para cada proveedor. 
  
Después de copiar toda la información de MapiSvc.inf, se llama a la función de punto de entrada del servicio de mensajes, **MSGSERVICEENTRY,** con el valor MSG_SERVICE_CREATE establecido en el _parámetro ulContext._ Si la marca SERVICE_UI_ALLOWED se establece en el parámetro _ulFlags_ del método **CreateMsgServiceEx,** los valores de los parámetros _ulUIParam_ y _ulFlags_ también se pasan cuando se llama a la función de punto de entrada del servicio de mensajes. Los proveedores de servicios deben mostrar sus hojas de propiedades de configuración para que los usuarios puedan configurar el servicio de mensajes. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si el argumento **CreateMsgServiceEx** _lpuidService_ no es NULL, la propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) del servicio de mensajes que se agregó al perfil se devuelve en el **GUID** al que apunta. 
  
Pase el valor de la **propiedad PR_SERVICE_UID** del parámetro  _lpuidService_ al método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar el servicio. 
  
> [!CAUTION]
> La Microsoft Outlook 2010 del subsistema MAPI no admite MAPI_UNICODE y producirá un error si se usa. 
  
> [!IMPORTANT]
> La interfaz IMsgServiceAdmin2 está expuesta por el mismo objeto que implementa la interfaz IMsgServiceAdmin y ha estado disponible mediante la implementación del subsistema MAPI de Outlook desde Outlook 2003. Su IID se define de la siguiente manera: >> Es posible que el `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);` _SERVICE_NO_RESTART_WARNING ulFlags_ no esté definido en el archivo de encabezado descargable que tenga actualmente, en cuyo caso puede agregarlo al código con el siguiente valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Vea también



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

