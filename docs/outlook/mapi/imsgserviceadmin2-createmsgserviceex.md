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
  
Agrega un servicio de mensajes al perfil actual y devuelve el nuevo UID de servicio agregado.
  
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
  
> a Un puntero al nombre del servicio de mensajes que se va a agregar. Este nombre de servicio de mensaje debe aparecer en la sección **[Services]** del archivo MapiSvc. inf. 
    
 _lpszDisplayName_
  
> a Un puntero al nombre para mostrar del servicio de mensajes que se va a agregar. El parámetro _lpszDisplayName_ se omite si el servicio de mensajes ha establecido la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el archivo MapiSvc. inf.
    
 _ulUIParam_
  
> a Un controlador para la ventana primaria de los cuadros de diálogo o ventanas que este método muestra.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se instala el servicio de mensajes. Se pueden establecer los siguientes indicadores:
    
MAPI_UNICODE
  
> Los parámetros lpszService y lpszDisplayName deben convertirse en LPWSTR e interpretarse como cadenas Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Cuando se agrega un nuevo servicio de mensajes al perfil, el subsistema MAPI, basado en varias circunstancias y criterios, a menudo determina que esta acción requiere el reinicio de Outlook. Si no se incluye la marca SERVICE_NO_RESTART_WARNING y se permite la interfaz de usuario en función de los marcadores SERVICE_UI_ALWAYS y SERVICE_UI_ALLOWED, y al menos un proceso ha iniciado sesión en el perfil actual, esta función muestra el mensaje "debe reiniciar Outlook para Estos cambios se aplicarán. " La inclusión de la marca SERVICE_NO_RESTART_WARNING suprime la visualización de ese mensaje de advertencia.
    
SERVICE_UI_ALLOWED
  
> La interfaz de usuario de configuración del servicio de mensajes se permite si es necesario.
    
SERVICE_UI_ALWAYS
  
> El servicio de mensajes muestra su hoja de propiedades de configuración.
    
 _lpuidService_
  
> contempla El puntero al UID del servicio de mensajes agregado.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND
  
> El nombre del servicio de mensajes no se encuentra en la sección **[Services]** del archivo MapiSvc. inf. 
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin2:: CreateMsgServiceEx** agrega un servicio de mensajes al perfil actual. **CreateMsgServiceEx** llama a la función de punto de entrada del servicio de mensajería para realizar cualquier tarea de configuración específica del servicio. Si la marca SERVICE_UI_ALLOWED se establece en el parámetro _ulFlags_ , el servicio de mensajes que se instala puede mostrar una hoja de propiedades que permite al usuario configurar su configuración. 
  
El archivo MapiSvc. inf contiene la lista de proveedores que componen un servicio de mensajes y las propiedades de cada uno. **CreateMsgServiceEx** primero crea una nueva sección de perfil para el servicio de mensajes y, a continuación, copia toda la información de ese servicio del archivo MapiSvc. inf en el perfil, creando secciones nuevas para cada proveedor. 
  
Una vez que se ha copiado toda la información de MapiSvc. inf, se llama a la función de punto de entrada del servicio de mensajes, **MSGSERVICEENTRY**, con el valor MSG_SERVICE_CREATE establecido en el parámetro _ulContext_ . Si la marca SERVICE_UI_ALLOWED se establece en el parámetro _ulFlags_ del método **CreateMsgServiceEx** , los valores de los parámetros _ulUIParam_ y _ulFlags_ también se pasan cuando se llama a la función de punto de entrada del servicio de mensajería. Los proveedores de servicios deben mostrar sus hojas de propiedades de configuración para que los usuarios puedan configurar el servicio de mensajes. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si el argumento **CreateMsgServiceEx** _LPUIDSERVICE_ no es null, la propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) del servicio de mensajes que se agregó al perfil se devuelve en el **GUID** al que señala. 
  
Pase el valor de la propiedad **PR_SERVICE_UID** en el parámetro _LpuidService_ al método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar el servicio. 
  
> [!CAUTION]
> La implementación de Microsoft Outlook 2010 del subsistema MAPI no es compatible con MAPI_UNICODE y se producirá un error si se usa. 
  
> [!IMPORTANT]
> La interfaz IMsgServiceAdmin2 se expone mediante el mismo objeto que implementa la interfaz IMsgServiceAdmin, y está disponible mediante la implementación de Outlook del subsistema MAPI desde Outlook 2003. Su IID se define de la siguiente manera `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`: > > puede que el _ulFlags_ SERVICE_NO_RESTART_WARNING no esté definido en el archivo de encabezado descargable que tiene actualmente, en cuyo caso puede agregarlo al código con el siguiente valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Ver también



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

