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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427881"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define un prototipo de una función de punto de entrada de servicio de mensajes para admitir la configuración del servicio de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Función definida implementada por:  <br/> |Servicios de mensajes  <br/> |
|Función definida llamada por:  <br/> |MAPI  <br/> |
   
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

## <a name="parameters"></a>Parameters

 _hInstance_
  
> [in] Identificador de la instancia del proveedor de serviciosDLL. El identificador se usa normalmente para recuperar recursos. 
    
 _lpMalloc_
  
> [in] Puntero a un objeto de asignador de memoria que expone la **interfaz OLE IMalloc.** Es posible que el servicio de mensajes necesite usar este método de asignación al trabajar con determinadas interfaces como **IStream**. 
    
 _lpMAPISup_
  
> [in] Puntero a una [implementación de interfaz IMAPISupport: IUnknown.](imapisupportiunknown.md) 
    
 _ulUIParam_
  
> [in] Valor específico de la implementación que se usa para pasar información de la interfaz de usuario a una función o cero. El  _parámetro ulUIParam_ es el controlador de ventana principal del cuadro de diálogo de configuración y es de tipo HWND (se convierte en un ULONG_PTR). Un valor de cero indica que no hay ninguna ventana primaria. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que indican las opciones de la función de entrada de servicio. Se pueden establecer las siguientes marcas:
    
MAPI_UNICODE 
  
> Las cadenas pasadas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> La interfaz de usuario de configuración del servicio debe mostrar la configuración actual, pero no permitir que el usuario la cambie. 
    
SERVICE_UI_ALLOWED 
  
> Permite mostrar un cuadro de diálogo de configuración si es necesario. Cuando se SERVICE_UI_ALLOWED marca, el cuadro de diálogo solo debe mostrarse si la matriz de valores de la propiedad  _lpProps_ está vacía o no contiene una configuración válida. Si SERVICE_UI_ALLOWED no está establecido, es posible que se muestre un cuadro de diálogo si se SERVICE_UI_ALWAYS marca. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Solicita que el cuadro de diálogo de configuración del proveedor activo se muestre encima de otros cuadros de diálogo. 
    
SERVICE_UI_ALWAYS 
  
> Requiere que el servicio de mensajes muestre un cuadro de diálogo de configuración. Si la marca SERVICE_UI_ALWAYS no está establecida, es posible que se muestre un cuadro de diálogo de configuración si se establece la marca SERVICE_UI_ALLOWED y la información de configuración válida no está disponible en la matriz de valores de la propiedad _lpProps._ Debe SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS para permitir que se muestre una interfaz de usuario. 
    
 _ulContext_
  
> [in] La operación de configuración que MAPI está realizando actualmente. El  _parámetro ulContext_ contendrá uno de los siguientes valores: 
    
MSG_SERVICE_CONFIGURE 
  
> Los cambios en la configuración del servicio deben realizarse en el perfil. Si se SERVICE_UI_ALWAYS marca, el servicio debe mostrar su cuadro de diálogo de configuración. El cuadro de diálogo también debe mostrarse si se establece la marca SERVICE_UI_ALLOWED y el parámetro  _lpProps_ está vacío o no contiene datos de configuración válidos. Si lpProps contiene datos  _válidos,_ no se debe mostrar ningún cuadro de diálogo y el servicio debe usar estos datos para realizar el cambio de configuración. 
    
MSG_SERVICE_CREATE 
  
> El servicio se está agregando a un perfil. Si se establece SERVICE_UI_ALWAYS o SERVICE_UI_ALLOWED marca, el servicio debe mostrar su cuadro de diálogo de configuración. Si no se establece ninguna marca, el servicio debe producir un error. 
    
MSG_SERVICE_DELETE 
  
> El servicio se está quitando de un perfil. Después de recibir este evento, el servicio debe devolver S_OK.
    
MSG_SERVICE_INSTALL 
  
> El servicio se ha instalado en la estación de trabajo del usuario desde una red, un disquete u otro medio externo. Después de recibir este evento, el servicio normalmente devuelve S_OK. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Solicita que el servicio cree una instancia adicional de un proveedor. Si el servicio admite esta operación, debe llamar a [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md). Si el servicio no admite esta operación, puede devolver MAPI_E_NO_SUPPORT. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Solicita que el servicio elimine una instancia de proveedor. Si el servicio admite esta operación, debe llamar a [IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md). Si el servicio no admite esta operación, puede devolver MAPI_E_NO_SUPPORT.
    
MSG_SERVICE_UNINSTALL 
  
> Se está quitando el servicio. Después de recibir este evento, el servicio puede realizar las tareas de limpieza que deben realizarse antes de que finalice el servicio y, a continuación, devolver con un valor correcto. Si el usuario cancela la eliminación, el servicio debe devolver MAPI_E_USER_CANCEL. 
    
 _cValues_
  
> [in] Recuento de valores de propiedad en la matriz apuntada por el _parámetro lpProps._ El valor del parámetro  _cValues_ es cero si MAPI no pasa ningún valor de propiedad. 
    
 _lpProps_
  
> [in] Puntero a una matriz opcional de [estructuras SPropValue](spropvalue.md) que indica los valores de las propiedades admitidas por el proveedor que la función usará en la configuración del servicio de mensajes. La función solo usa este parámetro si  _el parámetro ulContext_ está establecido en MSG_SERVICE_CONFIGURE. Este parámetro se usa normalmente para pasar la ruta de acceso a un archivo de un servicio basado en archivos, como un servicio de libreta de direcciones personal. Si el MSG_SERVICE_CONFIGURE no se pasa en el  _parámetro ulFlags,_ el parámetro  _lpProps_ debe ser cero. 
    
 _lpProviderAdmin_
  
> [in] Puntero a una [interfaz IProviderAdmin:IUnknown](iprovideradminiunknown.md) que la función puede usar para buscar secciones de perfil para un proveedor específico en el servicio de mensajes actual. 
    
 _lppMapiError_
  
> [salida] Puntero a una [estructura MAPIERROR.](mapierror.md) La estructura se asigna con la [función MAPIAllocateBuffer.](mapiallocatebuffer.md) Todos los miembros son opcionales, aunque la mayoría de las estructuras contendrán una cadena de mensaje de error válida en el _miembro lpszError._ Si  _los miembros lpszComponent_ o  _lpszError_ de la estructura están presentes, su memoria debe liberarse con una sola llamada a [MAPIFreeBuffer](mapifreebuffer.md) en la estructura base. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_UNCONFIGURED 
  
> El proveedor de servicios no se ha configurado. 
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo. 
    
MAPI_E_NO_SUPPORT 
  
> El proveedor no admite cambios en sus objetos o no admite la notificación de cambios. 
    
MAPI_E_BAD_CHARWIDTH 
  
> La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.
    
## <a name="remarks"></a>Comentarios

Una función definida mediante el prototipo de función **MSGSERVICEENTRY** permite a los servicios de mensajes configurarse a sí mismos o realizar otras acciones específicas del servicio. La función proporciona principalmente un cuadro de diálogo en el que el usuario puede cambiar la configuración específica del servicio de mensajes. También puede admitir la configuración mediante programación mediante la matriz de valores de propiedad pasada en el _parámetro lpProps._ La configuración mediante programación es opcional a menos que el servicio admita el Asistente para perfiles, para el que es necesario. 
  
MAPI llama a este punto de entrada desde la aplicación del Panel de control o en respuesta a una aplicación cliente que llama a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) o [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
MAPI no establece ninguna restricción en el nombre de función que un servicio de mensajes usa para el prototipo **MSGSERVICEENTRY,** pero prefiere el nombre **ServiceEntry**. No hay ninguna restricción en el ordinal para la función y un único DLL de proveedor puede contener más de una función. Sin embargo, solo una de las funciones se puede **denominar ServiceEntry**. 
  
Un servicio de mensajes puede usar [la función BuildDisplayTable](builddisplaytable.md) y el método [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) para simplificar la implementación del cuadro de diálogo de configuración. 
  
Es posible que un usuario cancele una MSG_SERVICE_UNINSTALL operación. En este caso, la función **ServiceEntry** debe comprobar con el usuario que no se debe quitar el servicio y devolver MAPI_E_USER_CANCEL si el servicio permanece instalado. 
  
Una función basada en el **prototipo MSGSERVICEENTRY** devuelve uno de los valores HRESULT enumerados. MAPI reenvía este valor al responder a la llamada de un cliente a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
Los servicios de mensajes que exportan una función de entrada de servicio deben incluir las propiedades **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) y **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) en la sección de servicio de mensajes de MAPISVC.INF. 
  

