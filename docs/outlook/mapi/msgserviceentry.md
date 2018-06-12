---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9af170f3445757eb96b9fe78c7cbea2c29ef4612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818427"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**Se aplica a**: Outlook 
  
Define un prototipo de una función de punto de entrada del servicio de mensaje admitir la configuración del servicio de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Función definido implementada por:  <br/> |Servicios de mensajes  <br/> |
|Llamado por una función definida:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT MSGSERVICEENTRY(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulContext,
  ULONG cValues,
  LPSPropValue lpProps,
  LPPROVIDERADMIN lpProviderAdmin,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>Sintaxis

 _hInstance_
  
> [entrada] Identificador de la instancia de la providerDLL de servicio. El controlador se suele usar para recuperar recursos. 
    
 _lpMalloc_
  
> [entrada] Puntero a un objeto del asignador de memoria exposición de la interfaz de OLE **IMalloc** . El servicio de mensajes es posible que necesite utilizar este método de asignación cuando se trabaja con ciertas interfaces como **IStream**. 
    
 _lpMAPISup_
  
> [entrada] Puntero a un [IMAPISupport: IUnknown](imapisupportiunknown.md) implementación de la interfaz. 
    
 _ulUIParam_
  
> [entrada] Un valor específico de la implementación utilizado para pasar información de interfaz de usuario a una función o un valor cero. El parámetro _ulUIParam_ es el identificador de ventana primario para el cuadro de diálogo de configuración y es de tipo HWND (conversión a un ULONG_PTR). Un valor de cero indica que no hay ninguna ventana primario. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcadores que indica las opciones para la función de entrada de servicio. Se pueden establecer los siguientes indicadores:
    
MAPI_UNICODE. 
  
> Las cadenas que se pasan en están en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> Interfaz de usuario de configuración del servicio debe mostrar la configuración actual, pero no permitir que el usuario que la cambie. 
    
SERVICE_UI_ALLOWED 
  
> Permite a un cuadro de diálogo de configuración que se mostrará si es necesario. Cuando se establece la marca SERVICE_UI_ALLOWED, se debe mostrar el cuadro de diálogo sólo si la matriz de valores de propiedad _lpProps_ está vacía o no contiene una configuración válida. Si no se establece SERVICE_UI_ALLOWED, aún es posible que mostrará un cuadro de diálogo si se establece la marca SERVICE_UI_ALWAYS. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Solicitudes que se muestre el cuadro de diálogo de configuración para el proveedor activo encima de otros cuadros de diálogo. 
    
SERVICE_UI_ALWAYS 
  
> Requiere el servicio de mensajes para mostrar un cuadro de diálogo de configuración. Si no está establecido el indicador SERVICE_UI_ALWAYS, aún es posible que mostrará un cuadro de diálogo Configuración si se establece la marca SERVICE_UI_ALLOWED y no está disponible desde la matriz de valores de propiedad de _lpProps_ información de configuración válido. SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS se debe establecer para permitir una interfaz de usuario que se mostrará. 
    
 _ulContext_
  
> [entrada] La operación de configuración que MAPI está realizando actualmente. El parámetro _ulContext_ contendrá uno de los siguientes valores: 
    
MSG_SERVICE_CONFIGURE 
  
> Se deben realizar cambios a la configuración del servicio en el perfil. Si se establece la marca SERVICE_UI_ALWAYS, el servicio debe mostrar su cuadro de diálogo de configuración. También se debe mostrar el cuadro de diálogo si se establece la marca SERVICE_UI_ALLOWED y el parámetro _lpProps_ está vacío o no contiene datos de configuración válida. Si _lpProps_ contiene datos válidos, no se debería mostrar ningún cuadro de diálogo y el servicio debe utilizar estos datos para realizar el cambio de configuración. 
    
MSG_SERVICE_CREATE 
  
> El servicio se agrega a un perfil. Si se establece la marca de la SERVICE_UI_ALWAYS o SERVICE_UI_ALLOWED, el servicio debe mostrar su cuadro de diálogo de configuración. Si se establece ninguna marca, debería producirá un error en el servicio. 
    
MSG_SERVICE_DELETE 
  
> El servicio se está quitando de un perfil. Después de recibir este evento, el servicio debe devolver S_OK.
    
MSG_SERVICE_INSTALL 
  
> El servicio se ha instalado en estación de trabajo del usuario de una red, disquete u otro medio externo. Después de recibir este evento, el servicio normalmente devuelve S_OK. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Solicitudes que el servicio de creación de una instancia adicional de un proveedor. Si el servicio admite esta operación, debe llamar a [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md). Si el servicio no es compatible con esta operación, puede devolver MAPI_E_NO_SUPPORT. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Solicitudes que el servicio de eliminación de una instancia del proveedor. Si el servicio admite esta operación, debe llamar a [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md). Si el servicio no es compatible con esta operación, puede devolver MAPI_E_NO_SUPPORT.
    
MSG_SERVICE_UNINSTALL 
  
> El servicio se está eliminando. Después de recibir este evento, el servicio puede realizar las tareas de limpieza que deben llevarse a cabo antes de que el servicio termina y, a continuación, devolver con un valor de éxito. Si el usuario cancela la eliminación, el servicio debe devolver MAPI_E_USER_CANCEL. 
    
 _cValues_
  
> [entrada] Recuento de valores de propiedad en la matriz indicada por el parámetro _lpProps_ . El valor del parámetro _cValues_ es cero si MAPI no está pasando valores de propiedad. 
    
 _lpProps_
  
> [entrada] Puntero a una matriz opcional de [SPropValue](spropvalue.md) de las estructuras que indica los valores de propiedades compatibles con el proveedor que se va a usar la función en la configuración del servicio de mensajes. La función sólo usa este parámetro si el parámetro _ulContext_ se establece en MSG_SERVICE_CONFIGURE. Este parámetro se usa con frecuencia para pasar la ruta de acceso a un archivo para un servicio basado en archivos, como un servicio de libreta de direcciones personales. Si no se pasa el indicador MSG_SERVICE_CONFIGURE en el parámetro _ulFlags_ , el parámetro _lpProps_ debe ser cero. 
    
 _lpProviderAdmin_
  
> [entrada] Puntero a una interfaz [IProviderAdmin:IUnknown](iprovideradminiunknown.md) que puede usar la función para localizar las secciones de perfil para un proveedor específico en el servicio de mensajes actual. 
    
 _lppMapiError_
  
> [out] Puntero a una estructura [MAPIERROR](mapierror.md) . Se asigna la estructura con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) . Todos los miembros son opcionales, aunque la mayoría de las estructuras contendrá una cadena de mensaje de error válido en el miembro _lpszError_ . Si están presentes los miembros _lpszComponent_ o _lpszError_ de la estructura, su memoria finalmente se debe liberar mediante una simple llamada a [MAPIFreeBuffer](mapifreebuffer.md) en la estructura de base. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_UNCONFIGURED 
  
> No se ha configurado el proveedor de servicios. 
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
MAPI_E_NO_SUPPORT 
  
> El proveedor no admite los cambios realizados en sus objetos o no admite la notificación de cambios. 
    
MAPI_E_BAD_CHARWIDTH 
  
> Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación sólo es compatible con Unicode.
    
## <a name="remarks"></a>Notas

Una función definida mediante el prototipo de función **MSGSERVICEENTRY** habilita los servicios de mensaje para configurar ellos mismos o para llevar a cabo otras acciones específicas al servicio. La función principalmente proporciona un cuadro de diálogo en el que el usuario puede cambiar valores de configuración específicos para el servicio de mensajes. También puede admitir configuración mediante programación mediante el uso de la matriz de valores de propiedad pasada en el parámetro _lpProps_ . Configuración mediante programación es opcional, a menos que el servicio admite al Asistente para perfiles, para la que se requiere. 
  
MAPI llama a este punto de entrada de la aplicación de Panel de Control o en respuesta a una aplicación cliente de una llamada a [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) o [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
MAPI no coloca ninguna restricción en el nombre de la función que un servicio de mensajes se usa para el prototipo **MSGSERVICEENTRY** pero prefiere el nombre de la **entrada de servicio**. No hay ninguna restricción en el ordinal de la función y un único proveedor DLL puede contener más de una función. Sin embargo, se puede denominar sólo una de las funciones de **entrada de servicio**. 
  
Un servicio de mensaje puede usar la función [BuildDisplayTable](builddisplaytable.md) y el método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para simplificar la implementación de cuadro de diálogo de configuración. 
  
Es posible que un usuario cancelar una operación de MSG_SERVICE_UNINSTALL. En este caso, la función de **entrada de servicio** debe comprobar con el usuario para comprobar que el servicio no debe quitarse y devolver MAPI_E_USER_CANCEL si el servicio permanecerá instalado. 
  
Una función según el prototipo **MSGSERVICEENTRY** devuelve uno de los valores HRESULT enumerados. MAPI reenvía este valor al responder a una llamada del cliente a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
Servicios de mensaje que exportan una función de entrada de servicio deben incluir las propiedades de **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) y **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) en la sección servicio de mensajes de MAPISVC.INF. 
  

