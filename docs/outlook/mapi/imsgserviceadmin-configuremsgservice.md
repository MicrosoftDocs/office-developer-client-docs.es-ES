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
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422190"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Reconfigura un servicio de mensajes.
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes que se debe configurar. 
    
 _ulUIParam_
  
> [in] Identificador de la ventana principal de la hoja de propiedades de configuración.
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla la presentación de la hoja de propiedades. Se pueden establecer las siguientes marcas:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.
    
MSG_SERVICE_UI_READ_ONLY 
  
> El servicio de mensajes debe mostrar su hoja de propiedades de configuración, pero no permitir que el usuario la cambie. La mayoría de los servicios de mensajes omiten esta marca.
    
SERVICE_UI_ALLOWED 
  
> El servicio de mensajes debe mostrar su hoja de propiedades de configuración solo si el servicio no está completamente configurado.
    
SERVICE_UI_ALWAYS 
  
> El servicio de mensajes siempre debe mostrar su hoja de propiedades de configuración. Si SERVICE_UI_ALWAYS no está establecido, se puede mostrar una hoja de propiedades de configuración si SERVICE_UI_ALLOWED está establecido y la información de configuración válida no está disponible en la matriz de valores de propiedad en el parámetro _lpProps._ Debe SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS para que se muestre una hoja de propiedades. 
    
 _cValues_
  
> [in] Recuento de valores de propiedad en la [estructura SPropValue](spropvalue.md) apuntada  _por lpProps_. 
    
 _lpProps_
  
> [in] Puntero a una matriz de valores de propiedad que describen las propiedades que se muestran en la hoja de propiedades. El  _parámetro lpProps_ no debe ser NULL si el servicio de mensajes debe configurarse sin una interfaz de usuario. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El servicio de mensajes se configuró correctamente.
    
MAPI_E_EXTENDED_ERROR 
  
> Error específico de un servicio de mensajes. Para obtener la [estructura MAPIERROR](mapierror.md) que describe el error, la aplicación cliente debe llamar al método [IMsgServiceAdmin::GetLastError.](imsgserviceadmin-getlasterror.md) 
    
MAPI_E_NOT_FOUND 
  
> El **MAPIUID señalado** por  _lpUID_ no coincide con el de un servicio de mensajes existente. 
    
MAPI_E_NOT_INITIALIZED 
  
> El servicio de mensajes no tiene una función de punto de entrada.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de la hoja de propiedades. 
    
## <a name="remarks"></a>Comentarios

El **método IMsgServiceAdmin::ConfigureMsgService** permite configurar un servicio de mensajes, con o sin una hoja de propiedades de configuración. 
  
Para permitir la configuración sin mostrar una hoja de propiedades, los servicios de mensajes suelen preparar un archivo de encabezado que incluya constantes para todas las propiedades obligatorias y opcionales y sus valores.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Para recuperar la estructura **MAPIUID** para que el servicio de mensajes configure, recupere la columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes de la tabla de servicio de mensajes. Para obtener más información, vea el procedimiento descrito en el [método IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md) 
  
Puede configurar un servicio de mensajes sin mostrar una hoja de propiedades a un usuario solo si tiene información previa sobre los valores de propiedad que se establecerán. Si va a configurar un servicio de mensajes sin mostrar una hoja de propiedades, pase valores de propiedad válidos en el parámetro  _lpProps_ y no establezca las marcas MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS. 
  
Si recibe toda o parte de la información de configuración del usuario a través de una hoja de propiedades, establezca SERVICE_UI_ALLOWED en  _ulFlags_. Si usa información de propiedad existente solo para establecer la configuración predeterminada y el usuario puede cambiar la configuración, establezca SERVICE_UI_ALWAYS en  _ulFlags_.
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI usa el **método IMsgServiceAdmin::ConfigureMsgService** para configurar un servicio que se ha agregado a un perfil.  <br/> |
   
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

