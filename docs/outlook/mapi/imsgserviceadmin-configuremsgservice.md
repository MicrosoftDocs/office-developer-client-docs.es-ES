---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f58d0f5cd7dfe74d3859d4f06a41aad6c3a55ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817713"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**Hace referencia a**: Outlook 
  
Vuelve a configurar un servicio de mensajes.
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Parámetros

 _lpUID_
  
> [entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes configurar. 
    
 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de la hoja de propiedades de configuración.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la presentación de la hoja de propiedades. Se pueden establecer los siguientes indicadores:
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.
    
MSG_SERVICE_UI_READ_ONLY 
  
> El servicio de mensajes debe mostrar su hoja de propiedades de configuración, pero no permitir que el usuario que la cambie. La mayoría de los servicios de mensaje pase por alto esta marca.
    
SERVICE_UI_ALLOWED 
  
> El servicio de mensajes debe mostrar su hoja de propiedades de configuración sólo si el servicio no está configurado completamente.
    
SERVICE_UI_ALWAYS 
  
> El servicio de mensajes siempre debe mostrar su hoja de propiedades de configuración. Si no se establece SERVICE_UI_ALWAYS, una hoja de propiedades de configuración aún puede mostrarse si se establece SERVICE_UI_ALLOWED y no está disponible desde la matriz de valores de propiedad en el parámetro _lpProps_ información de configuración válido. SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS se debe establecer para que una hoja de propiedades que se mostrará. 
    
 _cValues_
  
> [entrada] El recuento de valores de propiedad en la estructura [SPropValue](spropvalue.md) apunta a _lpProps_. 
    
 _lpProps_
  
> [entrada] Un puntero a una matriz de valores de propiedad que se describen las propiedades que se muestra en la hoja de propiedades. El parámetro _lpProps_ no debe ser NULL si el servicio de mensajes debe configurarse sin necesidad de una interfaz de usuario. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El servicio de mensajes se ha configurado correctamente.
    
MAPI_E_EXTENDED_ERROR 
  
> Un error específico a un servicio de mensaje. Para obtener la estructura [MAPIERROR](mapierror.md) que describe el error, la aplicación cliente debe llamar al método de [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) . 
    
MAPI_E_NOT_FOUND 
  
> El **MAPIUID** que señala _lpUID_ no coincide con el de un servicio de mensaje existente. 
    
MAPI_E_NOT_INITIALIZED 
  
> El servicio de mensajes no tiene una entrada de función de punto.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en la hoja de propiedades. 
    
## <a name="remarks"></a>Comentarios

El método **IMsgServiceAdmin::ConfigureMsgService** permite un servicio de mensajes que desea configurar, con o sin una hoja de propiedades de configuración. 
  
Para permitir la configuración sin una presentación de hoja de propiedades, servicios de mensajes normalmente preparan un archivo de encabezado que incluya las constantes de todas las propiedades opcionales y obligatorios y sus valores.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar la estructura **MAPIUID** para el servicio de mensajes configurar, recuperar la columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes en la tabla de servicios de mensaje. Para obtener más información, vea el procedimiento descrito en el método [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) . 
  
Puede configurar un servicio de mensajes sin mostrar una hoja de propiedades a un usuario sólo si tienen información avanzada acerca de los valores de propiedad va a establecer. Si va a configurar un servicio de mensajes sin mostrar una hoja de propiedades, pase los valores de propiedad válido en el parámetro _lpProps_ y no se establece los indicadores MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS. 
  
Si recibe todo o parte de la información de configuración del usuario por medio de una hoja de propiedades, establezca SERVICE_UI_ALLOWED en _ulFlags_. Si utiliza información de la propiedad existente sólo para establecer la configuración predeterminada y el usuario tiene permiso Cambiar la configuración, establezca SERVICE_UI_ALWAYS en _ulFlags_.
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI usa el método **IMsgServiceAdmin::ConfigureMsgService** para configurar un servicio que se ha agregado a un perfil.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

