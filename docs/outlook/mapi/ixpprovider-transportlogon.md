---
title: IXPProviderTransportLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.TransportLogon
api_type:
- COM
ms.assetid: 534929f2-36a2-463d-8c4c-d86060cde127
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 53b2733dbf38d680027dc00ecf5513f384e46660
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417311"
---
# <a name="ixpprovidertransportlogon"></a>IXPProvider::TransportLogon

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece una sesión en la que una aplicación cliente inicia sesión en un proveedor de transporte. 
  
```cpp
HRESULT TransportLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG FAR * lpulFlags,
  LPMAPIERROR FAR * lppMAPIError,
  LPXPLOGON FAR * lppXPLogon
);
```

## <a name="parameters"></a>Parameters

_lpMAPISup_: [in] Puntero al objeto de soporte del proveedor de transporte para funciones de devolución de llamada dentro de MAPI para esta sesión. Este objeto permanece válido hasta que el proveedor de transporte lo libere.
    
_ulUIParam_: [in] Controlar en la ventana principal de los cuadros de diálogo o ventanas que muestra este método. El _parámetro ulUIParam_ puede ser distinto de null, por ejemplo, cuando la marca LOGON_SETUP se establece en el parámetro _lpulFlags._ 
    
_lpszProfileName_: [in] Puntero al nombre del perfil del usuario. El  _parámetro lpszProfileName_ se usa principalmente cuando se debe presentar un cuadro de diálogo. 
    
_lpulFlags_: [in, out] Máscara de bits de marcas que controla cómo se establece la sesión de inicio de sesión. La cola MAPI puede establecer las siguientes marcas en la entrada:
    
  - LOGON_NO_CONNECT: la cuenta de usuario inicia sesión en este proveedor de transporte para fines distintos de la transmisión y recepción de mensajes. El proveedor de transporte no debe intentar realizar conexiones a otros sistemas de mensajería.
        
  - LOGON_NO_DIALOG: no se debe mostrar ningún cuadro de diálogo incluso si las credenciales de usuario guardadas actualmente no son válidas o insuficientes para el inicio de sesión.
        
  - LOGON_NO_INBOUND: el proveedor de transporte no tiene que inicializarse para recibir mensajes y no debe aceptar mensajes entrantes. La cola MAPI puede usar el método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) más adelante para indicar al proveedor de transporte que habilite el procesamiento de mensajes entrantes. 
        
  - LOGON_NO_OUTBOUND: el proveedor de transporte no tiene que inicializarse para enviar mensajes, ya que la cola MAPI no proporciona ninguna. Si una aplicación cliente requiere una conexión con un proveedor remoto durante la composición de un mensaje para que pueda realizar llamadas al método [IXPLogon::AddressTypes,](ixplogon-addresstypes.md) el proveedor de transporte debe realizar la conexión. La cola MAPI puede usar **TransportNotify** para indicar al proveedor de transporte cuándo pueden comenzar las operaciones salientes. 
      
  - MAPI_UNICODE: la cadena pasada para el nombre del perfil está en formato Unicode. Si no se establece \_ la marca UNICODE MAPI, la cadena tiene el formato ANSI.
      
    El proveedor de transporte puede establecer las siguientes marcas en la salida:
      
  - LOGON_SP_IDLE: solicita que la cola MAPI llame con frecuencia al método [IXPLogon::Idle](ixplogon-idle.md) del proveedor de transporte para procesar el tiempo de inactividad. 
      
  - LOGON_SP_POLL: solicita que la cola MAPI llame con frecuencia al método [IXPLogon::P oll](ixplogon-poll.md) en el objeto de inicio de sesión devuelto para buscar mensajes nuevos. Si no se establece esta marca, la cola MAPI solo comprueba si hay mensajes nuevos cuando el proveedor de transporte usa el método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) para notificar al colador que hay nuevos mensajes que procesar. Un proveedor de transporte se convierte efectivamente en solo envío al no establecer esta marca y no notificar a la cola MAPI de la recepción de mensajes. 
      
  - LOGON_SP_RESOLVE: solicitudes que la cola MAPI resuelve en direcciones completa todas las direcciones de mensaje para destinatarios no admitidos por este proveedor de transporte. Por lo tanto, el proveedor de transporte puede crear una ruta de respuesta para todos los destinatarios.
      
  - MAPI_UNICODE: las cadenas devueltas en la estructura [MAPIERROR,](mapierror.md) si las hay, están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI. 
    
_lppMAPIError_: [out] Puntero a un puntero a la estructura **MAPIERROR** devuelta, si la hubiera, que contiene información de versión, componente y contexto del error. El  _parámetro lppMAPIError_ se puede establecer en NULL si no hay ninguna **estructura MAPIERROR** que devolver. 
    
_lppXPLogon_: [out] Puntero al puntero al objeto de inicio de sesión del proveedor de transporte devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK: la llamada se ha hecho correctamente y ha devuelto el valor o los valores esperados.
    
MAPI_E_FAILONEPROVIDER: este proveedor no puede iniciar sesión, pero este error no debe deshabilitar el servicio. 
    
MAPI_E_UNCONFIGURED: el perfil no contiene suficiente información para que se complete el inicio de sesión. MAPI llama a la función de punto de entrada del servicio de mensajes del proveedor.
    
MAPI_E_UNKNOWN_CPID: el proveedor no puede admitir la página de códigos del cliente.
    
MAPI_E_UNKNOWN_LCID: el proveedor no puede admitir la información de configuración regional del cliente.
    
MAPI_E_USER_CANCEL: el usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPProvider::TransportLogon** para establecer una sesión de inicio de sesión para un usuario. 
  
La mayoría de los proveedores de transporte usan el método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) proporcionado con el objeto de soporte al que apunta el parámetro  _lpMAPISup_ para guardar y recuperar información de identidad de usuario, direcciones de servidor y credenciales. Mediante **OpenProfileSection,** un proveedor de transporte puede guardar información arbitraria y asociarla con un inicio de sesión a un recurso determinado. Por ejemplo, un proveedor puede usar **OpenProfileSection** para guardar el nombre de cuenta y la contraseña asociados con una sesión determinada y cualquier nombre de servidor u otra información necesaria que sea necesaria para tener acceso a los recursos de esa sesión. MAPI oculta la información asociada a un recurso desde el acceso externo. La sección de perfil disponible a través de  _lpMAPISup_ se administra mediante la cola MAPI para que los datos relacionados con este contexto de usuario estén separados de los datos de otros contextos. 
  
El proveedor de transporte debe llamar al método **IUnknown::AddRef** en el objeto de soporte técnico y mantener una copia del puntero a este objeto como parte del objeto de inicio de sesión del proveedor. 
  
El nombre para mostrar del perfil  _en lpszProfileName_ se proporciona para que el proveedor de transporte pueda usarlo en mensajes de error o cuadros de diálogo de inicio de sesión. Si el proveedor conserva este nombre, debe copiarse en el almacenamiento asignado por el proveedor. 
  
Los proveedores de transporte estrechamente combinados con otros proveedores de servicios pueden tener que realizar un trabajo adicional durante el inicio de sesión para establecer las buenas credenciales necesarias para las operaciones entre proveedores complementarios.
  
Normalmente, los proveedores de transporte se abren cuando el usuario inicia sesión por primera vez en un perfil. Dado que el primer inicio de sesión en un perfil por lo general se produce antes de iniciar sesión en cualquier almacén de mensajes, la cola MAPI normalmente llama a **TransportLogon** con las marcas LOGON_NO_INBOUND y LOGON_NO_OUTBOUND establecidas en  _lpulFlags_. Más adelante, cuando los almacenes de mensajes adecuados están disponibles en la sesión de perfil, la cola MAPI llama a **TransportNotify** para iniciar operaciones entrantes y salientes para el proveedor de transporte. 
  
Pasar la LOGON_NO_CONNECT en  _lpulFlags_ indica el funcionamiento sin conexión del proveedor de transporte. Esta marca indica que no se deben realizar conexiones externas; si el proveedor de transporte no puede establecer una sesión sin una conexión externa, debe devolver un valor de error para el inicio de sesión. 
  
Un proveedor de transporte debe establecer la marca LOGON_SP_IDLE en  _lpulFlags_ en el momento de la inicialización si está diseñado para usar el tiempo que el sistema de otro modo pasa inactivo. Este tiempo suele usarse para controlar las operaciones automáticas, como la descarga automática de mensajes, la descarga de mensajes con tiempo o el envío de mensajes con tiempo. Si se establece esta marca, la cola MAPI llama a **Idle** cuando se produce el tiempo de inactividad del sistema para iniciar dichas operaciones. La cola MAPI no llama a **Idle** a intervalos establecidos; en su lugar, se llama solo durante el tiempo de inactividad real. Por lo tanto, los proveedores no deben trabajar en ninguna suposición sobre la frecuencia con la que se llamará a sus **métodos** Idle. Los proveedores que admiten operaciones de tiempo de inactividad deben proporcionar una interfaz de usuario de configuración para ella en su hoja de propiedades de proveedor. 
  
Si el inicio de sesión del proveedor de transporte se realiza correctamente, el proveedor debe devolver en el parámetro  _lppXPLogon_ un puntero a un objeto de inicio de sesión. La cola MAPI usará este objeto para obtener acceso adicional al proveedor. Si **TransportLogon** muestra un cuadro de diálogo de inicio  de sesión y el usuario cancela el inicio de sesión normalmente haciendo clic en el botón Cancelar del cuadro de diálogo, el proveedor debe devolver MAPI_E_USER_CANCEL. 
  
Para la mayoría de los valores de error devueltos de **TransportLogon**, MAPI deshabilita los servicios de mensajes a los que pertenece el proveedor. MAPI no llamará a ningún proveedor que pertenezca a ese servicio durante el resto de la sesión MAPI. En cambio, cuando **TransportLogon** devuelve el valor de error MAPI_E_FAILONEPROVIDER desde su inicio de sesión, MAPI no deshabilita el servicio de mensajes al que pertenece el proveedor. **TransportLogon** debe devolver MAPI_E_FAILONEPROVIDER si encuentra un error que no garantiza deshabilitar el servicio durante el resto de la sesión. 
  
Si un proveedor devuelve MAPI_E_UNCONFIGURED desde su inicio de sesión, MAPI llamará a la función de entrada del servicio de mensajes del proveedor y, a continuación, reintentará el inicio de sesión. MAPI pasa MSG_SERVICE_CONFIGURE como contexto, para dar al servicio la oportunidad de configurarse a sí mismo. Si el cliente ha elegido permitir una interfaz de usuario en el inicio de sesión, el servicio puede presentar su hoja de propiedades de configuración para que el usuario pueda escribir información de configuración. 
  
Si el proveedor encuentra que toda la información necesaria no está en el perfil, debe devolver MAPI_E_UNCONFIGURED para que MAPI llame a la función de punto de entrada del servicio de mensajes del proveedor. 
  
## <a name="see-also"></a>Vea también

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

