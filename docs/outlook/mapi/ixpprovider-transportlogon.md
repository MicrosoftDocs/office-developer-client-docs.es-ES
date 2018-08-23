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
ms.openlocfilehash: 96e81442125ae49e0c2856a1cf3a97a16d3453cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583340"
---
# <a name="ixpprovidertransportlogon"></a>IXPProvider::TransportLogon

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece una sesión en el que una aplicación cliente inicia sesión en un proveedor de transporte. 
  
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

## <a name="parameters"></a>Parámetros

_lpMAPISup_: [entrada] puntero al objeto de soporte técnico del proveedor de transporte para las funciones de devolución de llamada dentro de MAPI para esta sesión. Este objeto sigue siendo válida hasta que el proveedor de transporte lo libera.
    
_ulUIParam_: [entrada] identificador de la ventana principal de los cuadros de diálogo o windows muestra este método. El parámetro _ulUIParam_ puede ser distintos de null, por ejemplo, cuando se marca el LOGON_SETUP se establece en el parámetro _lpulFlags_ . 
    
_lpszProfileName_: [entrada] puntero al nombre de perfil del usuario. El parámetro _lpszProfileName_ se usa principalmente cuando un cuadro de diálogo debe presentarse. 
    
_lpulFlags_: [en, out] máscara de bits de indicadores que controla cómo se establece la sesión de inicio de sesión. Las siguientes marcas se pueden establecer en los datos proporcionados por la cola MAPI:
    
  - LOGON_NO_CONNECT: La cuenta de usuario está iniciando sesión con este proveedor de transporte para fines distintos de transmisión y recepción de mensajes. El proveedor de transporte no debe intentar establecer las conexiones con otros sistemas de mensajería.
        
  - LOGON_NO_DIALOG: Ningún cuadro de diálogo debe mostrarse incluso si las credenciales del usuario actualmente guardada no son válidas o suficientes para el inicio de sesión.
        
  - LOGON_NO_INBOUND: El proveedor de transporte no tiene que inicializar para la recepción de mensajes y no debe aceptar los mensajes entrantes. La cola MAPI puede utilizar el método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) más adelante para señalar el proveedor de transporte para habilitar el procesamiento de mensajes entrantes. 
        
  - LOGON_NO_OUTBOUND: El proveedor de transporte no se tiene que inicializar para el envío de mensajes, como la cola MAPI no proporciona. Si una aplicación cliente requiere una conexión a un proveedor remoto durante la composición de un mensaje para que pueden realizar llamadas al método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) , el proveedor de transporte debe realizar la conexión. La cola MAPI puede utilizar **TransportNotify** para indicar el proveedor de transporte cuando puedan comenzar las operaciones realizadas. 
      
  - MAPI_UNICODE.: La cadena pasada para el nombre del perfil que se encuentra en formato Unicode. Si la MAPI\_no está establecido el indicador UNICODE, la cadena está en formato ANSI.
      
    Pueden establecer los siguientes indicadores en la salida por el proveedor de transporte:
      
  - LOGON_SP_IDLE: Solicitudes que la cola MAPI llama con frecuencia (método [IXPLogon::Idle](ixplogon-idle.md) ) del proveedor de transporte para el procesamiento de tiempo de inactividad. 
      
  - LOGON_SP_POLL: Las solicitudes que con frecuencia la cola MAPI llamar al método [IXPLogon::Poll](ixplogon-poll.md) en el objeto devuelto de inicio de sesión para comprobar para nuevos mensajes. Si no se establece este marcador, la cola MAPI sólo se comprueba para nuevos mensajes cuando el proveedor de transporte que usa el método [SpoolerNotify](imapisupport-spoolernotify.md) para notificar a la cola de impresión que no hay mensajes nuevos para procesar. Un proveedor de transporte eficazmente se convierte en solo envío estableciendo esta marca no y no se informa a la cola MAPI de recepción de mensaje. 
      
  - LOGON_SP_RESOLVE: Las solicitudes de la cola MAPI resolverse en total direcciones de todas las direcciones de mensaje para los destinatarios no admitidas por este proveedor de transporte. Por lo tanto, que el proveedor de transporte puede construir una ruta de acceso de respuesta para todos los destinatarios.
      
  - MAPI_UNICODE.: Las cadenas devueltas en la estructura [MAPIERROR](mapierror.md) , si hay alguna, se encuentran en formato Unicode. Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI. 
    
_lppMAPIError_: [salida] puntero a un puntero a la estructura **MAPIERROR** devuelta, si hay alguna, que contiene información de versión, el componente y el contexto para el error. El parámetro _lppMAPIError_ se puede establecer en NULL si no hay ninguna estructura **MAPIERROR** para devolver. 
    
_lppXPLogon_: [salida] puntero al puntero para el objeto de inicio de sesión del proveedor de transporte devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK: La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_FAILONEPROVIDER: Este proveedor no puede iniciar sesión, pero este error debe deshabilitar el servicio. 
    
MAPI_E_UNCONFIGURED: El perfil no contiene información suficiente para el inicio de sesión para completarse. MAPI llama a la función de punto de entrada de servicio de mensajes del proveedor.
    
MAPI_E_UNKNOWN_CPID: El proveedor no admite la página de códigos del cliente.
    
MAPI_E_UNKNOWN_LCID: El proveedor no admite la información de configuración regional del cliente.
    
MAPI_E_USER_CANCEL: El usuario ha cancelado la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método de **IXPProvider::TransportLogon** para establecer una sesión de inicio de sesión de un usuario. 
  
Mayoría de los proveedores de transporte use el método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) que se proporcionan con el objeto de soporte técnico que apunta el parámetro _lpMAPISup_ para guardar y recuperar información de identidad de usuario, las direcciones del servidor y las credenciales. Mediante el uso de **OpenProfileSection**, un proveedor de transporte puede guardar información arbitraria y asociarlo con un inicio de sesión a un recurso determinado. Por ejemplo, un proveedor puede usar **OpenProfileSection** para guardar el nombre de cuenta y la contraseña asociada a una sesión determinada y los nombres de servidor u otra información necesaria que se requieren acceso a los recursos para esa sesión. MAPI oculta información asociada con un recurso desde fuera de access. La sección de perfil disponible a través de _lpMAPISup_ está administrada por la cola de MAPI para que datos relacionados con el contexto de usuario están separados de datos para otros contextos. 
  
El proveedor de transporte debe llamar al método **IUnknown:: AddRef** en el objeto de soporte técnico y mantener una copia del puntero a este objeto como parte del objeto de proveedor de inicio de sesión. 
  
El nombre para mostrar del perfil en _lpszProfileName_ se proporciona para que el proveedor de transporte puede usar en los mensajes de error o cuadros de diálogo de inicio de sesión. Si el proveedor mantiene este nombre, se debe copiar almacenamiento asignado por el proveedor. 
  
Los proveedores de transporte que estén asociados estrechamente con otros proveedores de servicios que tenga que realizar trabajo adicional en el inicio de sesión para establecer las credenciales de una buena necesarias para las operaciones entre proveedores complementarios.
  
Normalmente, los proveedores de transporte se abren cuando el usuario inicia sesión en primer lugar en un perfil. Debido a que el primer inicio de sesión a un perfil por lo tanto, generalmente viene antes de iniciar sesión en cualquier almacén de mensajes, la cola MAPI llama normalmente **TransportLogon** con el LOGON_NO_INBOUND y el LOGON_NO_OUTBOUND indicadores establecidos en _lpulFlags_. Más adelante, cuando los almacenes de mensaje adecuado están disponibles en la sesión de perfiles, la cola MAPI llama **TransportNotify** para iniciar operaciones entrantes y salientes para el proveedor de transporte. 
  
Se pasa el indicador LOGON_NO_CONNECT en _lpulFlags_ señales operación sin conexión del proveedor de transporte. Esta marca indica que no deben realizarse conexiones externas; Si el proveedor de transporte no puede establecer una sesión sin una conexión externa, debe devolver un valor de error para el inicio de sesión. 
  
Un proveedor de transporte debe establecer la marca LOGON_SP_IDLE en _lpulFlags_ en tiempo de inicialización si está diseñado para usar el tiempo que emplea el sistema en caso contrario, inactivo. Tal vez a menudo se usa para controlar operaciones automáticas, como automática de mensajes descargar el archivo, agotaba el tiempo de descarga de mensaje o superó el tiempo de envío de mensajes. Si se establece este marcador, la cola MAPI llama a **inactivo** cuando se produzca el tiempo de inactividad del sistema iniciar dichas operaciones. La cola MAPI no llame a **inactivo** al establecer los intervalos; en su lugar, se invoca sólo durante un tiempo de inactividad es true. Por lo tanto, los proveedores no deberían funcionar en cualquier suposición sobre ¿con qué frecuencia se llamará a sus métodos **inactivo** . Los proveedores que admiten operaciones de tiempo de inactividad deben proporcionar una interfaz de usuario de configuración en su hoja de propiedades del proveedor. 
  
Si el inicio de sesión del proveedor de transporte se realiza correctamente, el proveedor debe devolver en el parámetro _lppXPLogon_ un puntero a un objeto de inicio de sesión. La cola MAPI usará este objeto para el acceso de proveedor adicionales. Si **TransportLogon** muestra un cuadro de diálogo de inicio de sesión y el usuario cancela el inicio de sesión normalmente haciendo clic en el botón **Cancelar** en el cuadro de diálogo el proveedor debe devolver MAPI_E_USER_CANCEL. 
  
Para la mayoría de los valores de error devuelta por **TransportLogon**, MAPI deshabilita los servicios de mensaje a la que pertenece el proveedor. MAPI no llamará a todos los proveedores que pertenecen a ese servicio para el resto de la sesión MAPI. Por el contrario, cuando **TransportLogon** devuelve el valor de error MAPI_E_FAILONEPROVIDER desde su inicio de sesión, MAPI deshabilitar el servicio de mensajes a la que pertenece el proveedor. **TransportLogon** debe devolver MAPI_E_FAILONEPROVIDER si encuentra un error que no merece la pena la deshabilitación del servicio para el resto de la sesión. 
  
Si un proveedor devuelve MAPI_E_UNCONFIGURED desde su inicio de sesión, MAPI llamar a la función de entrada de servicio de mensajes del proveedor y, a continuación, vuelva a intentar el inicio de sesión. MAPI pasa MSG_SERVICE_CONFIGURE como el contexto, para conceder a una oportunidad para que se configure el servicio. Si el cliente ha elegido permitir una interfaz de usuario en el inicio de sesión, el servicio puede presentar su hoja de propiedades de configuración para que el usuario pueda escribir información de configuración. 
  
Si el proveedor busca todas la información necesaria no está en el perfil, debe devolver MAPI_E_UNCONFIGURED para que MAPI llama a la función de punto de entrada de servicio de mensajes del proveedor. 
  
## <a name="see-also"></a>Recursos adicionales

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

