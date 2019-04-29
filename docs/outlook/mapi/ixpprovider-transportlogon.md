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

_lpMAPISup_: [entrada] puntero al objeto de compatibilidad del proveedor de transporte para funciones de devolución de llamada en MAPI para esta sesión. Este objeto sigue siendo válido hasta que el proveedor de transporte lo libera.
    
_ulUIParam_: [in] identificador de la ventana principal de los cuadros de diálogo o ventanas que este método muestra. El parámetro _ulUIParam_ puede no ser null, por ejemplo, cuando se establece la marca LOGON_SETUP en el parámetro _lpulFlags_ . 
    
_lpszProfileName_: [in] puntero al nombre del perfil del usuario. El parámetro _lpszProfileName_ se usa principalmente cuando se debe presentar un cuadro de diálogo. 
    
_lpulFlags_: [in, out] máscara de la máscara de los marcadores que controla cómo se establece la sesión de inicio de sesión. La cola MAPI puede establecer los siguientes indicadores en la entrada:
    
  - LOGON_NO_CONNECT: la cuenta de usuario está iniciando sesión en este proveedor de transporte para fines distintos de la transmisión y recepción de mensajes. El proveedor de transporte no debe intentar realizar ninguna conexión con otros sistemas de mensajería.
        
  - LOGON_NO_DIALOG: no se debe mostrar ningún cuadro de diálogo aunque las credenciales de usuario guardadas actualmente no sean válidas o insuficientes para el inicio de sesión.
        
  - LOGON_NO_INBOUND: el proveedor de transporte no tiene que inicializarse para la recepción de mensajes y no debe aceptar mensajes entrantes. La cola MAPI puede usar el método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) más adelante para indicar al proveedor de transporte que habilite el procesamiento de mensajes entrantes. 
        
  - LOGON_NO_OUTBOUND: el proveedor de transporte no tiene que inicializar para enviar mensajes, ya que la cola MAPI no proporciona ningún. Si una aplicación cliente requiere una conexión a un proveedor remoto durante la composición de un mensaje para que pueda realizar llamadas al método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) , el proveedor de transporte debe realizar la conexión. La cola MAPI puede usar **TransportNotify** para indicar al proveedor de transporte Cuándo pueden comenzar las operaciones salientes. 
      
  - MAPI_UNICODE: la cadena pasada para el nombre de perfil está en formato Unicode. Si no se\_establece la marca MAPI Unicode, la cadena está en formato ANSI.
      
    Los siguientes indicadores pueden establecerse en el resultado del proveedor de transporte:
      
  - LOGON_SP_IDLE: solicita que la cola MAPI llame con frecuencia al método [IXPLogon:: idle](ixplogon-idle.md) del proveedor de transporte para el procesamiento en tiempo de inactividad. 
      
  - LOGON_SP_POLL: solicita que la cola MAPI llame con frecuencia al método [IXPLogon::P Oll](ixplogon-poll.md) del objeto de inicio de sesión devuelto para comprobar si hay mensajes nuevos. Si no se establece esta marca, la cola MAPI solo comprueba los mensajes nuevos cuando el proveedor de transporte usa el método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) para notificar al administrador de trabajos de impresión que hay mensajes nuevos que procesar. Un proveedor de transporte se convierte efectivamente en solo envío si no se establece esta marca y no se notifica a la cola MAPI de la confirmación de mensajes. 
      
  - LOGON_SP_RESOLVE: solicita que la cola MAPI se resuelva como completa todas las direcciones de mensajes de los destinatarios que no son compatibles con este proveedor de transporte. Por lo tanto, el proveedor de transporte puede construir una ruta de respuesta para todos los destinatarios.
      
  - MAPI_UNICODE: las cadenas devueltas en la estructura [MAPIERROR](mapierror.md) , si las hay, están en formato Unicode. Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI. 
    
_lppMAPIError_: [out] puntero a un puntero a la estructura **MAPIERROR** devuelta, si la hay, que contiene información de la versión, el componente y el contexto del error. El parámetro _lppMAPIError_ puede establecerse en NULL si no hay ninguna estructura **MAPIERROR** para devolver. 
    
_lppXPLogon_: [out] puntero al puntero al objeto de inicio de sesión del proveedor de transporte devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK: la llamada se ha realizado correctamente y ha devuelto el valor o valores esperados.
    
MAPI_E_FAILONEPROVIDER: este proveedor no puede iniciar sesión, pero este error no debe deshabilitar el servicio. 
    
MAPI_E_UNCONFIGURED: el perfil no contiene suficiente información para que se complete el inicio de sesión. MAPI llama a la función de punto de entrada del servicio de mensajes del proveedor.
    
MAPI_E_UNKNOWN_CPID: el proveedor no admite la página de códigos del cliente.
    
MAPI_E_UNKNOWN_LCID: el proveedor no admite la información de la configuración regional del cliente.
    
MAPI_E_USER_CANCEL: el usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPProvider:: TransportLogon** para establecer una sesión de inicio de sesión para un usuario. 
  
La mayoría de los proveedores de transporte usan el método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) que se proporciona con el objeto de soporte al que apunta el parámetro _lpMAPISup_ para guardar y recuperar información de identidad del usuario, direcciones de servidor y credenciales. Mediante el uso de **OpenProfileSection**, un proveedor de transporte puede guardar información arbitraria y asociarla con un inicio de sesión a un recurso determinado. Por ejemplo, un proveedor puede usar **OpenProfileSection** para guardar el nombre y la contraseña de la cuenta asociados con una sesión en particular y los nombres de servidor u otra información necesaria necesaria para obtener acceso a los recursos de esa sesión. MAPI oculta la información asociada a un recurso desde fuera de Access. La sección de perfil que está disponible a través de _lpMAPISup_ se administra mediante la cola MAPI, por lo que los datos relacionados con este contexto de usuario están separados de los datos de otros contextos. 
  
El proveedor de transporte debe llamar al método **IUnknown:: AddRef** en el objeto de soporte y conservar una copia del puntero a este objeto como parte del objeto de inicio de sesión del proveedor. 
  
El nombre para mostrar del perfil en _lpszProfileName_ se proporciona para que el proveedor de transporte pueda usarlo en los cuadros de diálogo de inicio de sesión o mensajes de error. Si el proveedor conserva este nombre, debe copiarse en el almacenamiento asignado por el proveedor. 
  
Los proveedores de transporte que están estrechamente acoplados a otros proveedores de servicios pueden tener que realizar trabajo adicional en el inicio de sesión para establecer las credenciales buenas necesarias para las operaciones entre los proveedores complementarios.
  
Normalmente, los proveedores de transporte se abren cuando el usuario inicia sesión por primera vez en un perfil. Dado que el primer inicio de sesión en un perfil suele ser antes de iniciar sesión en cualquier almacén de mensajes, la cola MAPI suele llamar a **TransportLogon** con los indicadores LOGON_NO_INBOUND y LOGON_NO_OUTBOUND establecidos en _lpulFlags_. Más adelante, cuando los almacenes de mensajes apropiados están disponibles en la sesión de perfil, la cola MAPI llama a **TransportNotify** para iniciar las operaciones entrantes y salientes del proveedor de transporte. 
  
Pasar la marca LOGON_NO_CONNECT en _lpulFlags_ operación sin conexión del proveedor de transporte. Esta marca indica que no debe realizarse ninguna conexión externa; Si el proveedor de transporte no puede establecer una sesión sin una conexión externa, debe devolver un valor de error para el inicio de sesión. 
  
Un proveedor de transporte debe establecer la marca LOGON_SP_IDLE en _lpulFlags_ en el momento de la inicialización si está diseñada para usar tiempo que el sistema pasa inactivo de otro modo. Este tiempo se usa a menudo para controlar operaciones automáticas, como la descarga automática de mensajes, la descarga de mensajes con tiempo o el envío de mensajes transformados. Si se establece esta marca, la cola MAPI llama **inactiva** cuando se produce el tiempo de inactividad del sistema para iniciar dichas operaciones. La cola MAPI no llama a **inactividad** en los intervalos establecidos; en su lugar, solo se llama a este método durante el tiempo de inactividad real. Por lo tanto, los proveedores no deben trabajar en ninguna suposición **** sobre la frecuencia con la que se llamará a sus métodos de inactividad. Los proveedores que admiten operaciones en tiempo de inactividad deben proporcionar una interfaz de usuario de configuración en su hoja de propiedades del proveedor. 
  
Si el inicio de sesión del proveedor de transporte se realiza correctamente, el proveedor debe volver al parámetro _lppXPLogon_ un puntero a un objeto de inicio de sesión. La cola MAPI usará este objeto para obtener acceso adicional al proveedor. Si **TransportLogon** muestra un cuadro de diálogo de inicio de sesión y el usuario cancela el inicio de sesión normalmente al hacer clic en el botón **Cancelar** del cuadro de diálogo, el proveedor debe devolver MAPI_E_USER_CANCEL. 
  
Para la mayoría de los valores de error devueltos por **TransportLogon**, MAPI deshabilita los servicios de mensajes a los que pertenece el proveedor. MAPI no llamará a los proveedores que pertenezcan a ese servicio durante el resto de la sesión MAPI. Por el contrario, cuando **TransportLogon** devuelve el valor de error MAPI_E_FAILONEPROVIDER desde el inicio de sesión, MAPI no deshabilita el servicio de mensajes al que pertenece el proveedor. **TransportLogon** debe devolver MAPI_E_FAILONEPROVIDER si encuentra un error que no garantiza la deshabilitación del servicio para el resto de la sesión. 
  
Si un proveedor devuelve MAPI_E_UNCONFIGURED desde su inicio de sesión, MAPI llamará a la función de entrada del servicio de mensajes del proveedor y, a continuación, volverá a intentar iniciar sesión. MAPI pasa MSG_SERVICE_CONFIGURE como contexto, para dar al servicio una oportunidad de configurarse a sí mismo. Si el cliente ha elegido permitir una interfaz de usuario en el inicio de sesión, el servicio puede presentar su hoja de propiedades de configuración para que el usuario pueda escribir la información de configuración. 
  
Si el proveedor encuentra que toda la información necesaria no está en el perfil, debe devolver MAPI_E_UNCONFIGURED para que MAPI llame a la función de punto de entrada del servicio de mensajes del proveedor. 
  
## <a name="see-also"></a>Ver también

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

