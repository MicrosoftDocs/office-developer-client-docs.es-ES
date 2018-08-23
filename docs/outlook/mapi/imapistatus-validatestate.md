---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5ab459239bdcdcad30c4b6c82d5a3f8641bd4aca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567807"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Confirma la información de estado externo disponible para el recurso MAPI o el proveedor de servicios. Este método se admite en todos los objetos de estado. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

_ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.
    
_ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la validación. Se pueden establecer los siguientes indicadores:
    
ABORT_XP_HEADER_OPERATION
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en el cuadro de diálogo correspondiente. El objeto de estado tiene dos opciones: 
    
   - Continuar trabajando en la operación.
    
   - Detener la operación y devolver MAPI_E_USER_CANCELED.
    
CONFIG_CHANGED 
  
> Una o varias de las propiedades de configuración del objeto de estado ha cambiado. Los clientes pueden establecer esta marca para permitir que la cola MAPI para dinámicamente corregir errores del proveedor de transporte crítico. 
    
FORCE_XP_CONNECT 
  
> Debe realizar una conexión en el objeto de estado. Cuando este indicador se utiliza con el indicador REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la conexión se produce sin almacenamiento en caché.
    
FORCE_XP_DISCONNECT 
  
> Debe realizar una operación de desconexión en el objeto de estado. Cuando este indicador se utiliza con el indicador REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, se produce la desconexión sin almacenamiento en caché.
    
PROCESS_XP_HEADER_CACHE 
  
> Se deben procesar las entradas de la tabla de la memoria caché de encabezado, que deben descargarse todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DOWNLOAD y se deben eliminar todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DELETE. Los mensajes que tienen MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE establecer se va a mover.
    
REFRESH_XP_HEADER_CACHE 
  
> Para un proveedor remoto de transporte, que debe descargarse una nueva lista de encabezados de mensaje y se deben borrar todos los marcadores que marca el estado del mensaje.
    
SUPPRESS_UI 
  
> Impide que el objeto de estado muestre una interfaz de usuario como parte de la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La validación fue correcta.
    
MAPI_E_BUSY 
  
> Otra operación está en curso; se debe permitir para llevar a cabo o se debe detener, antes de inicia esta operación.
    
MAPI_E_NO_SUPPORT 
  
> El objeto de estado no es compatible con el método de validación, como se indica por la ausencia de la marca STATUS_VALIDATE_STATE en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación de validación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. Este valor se devuelve sólo por los proveedores de transporte remoto. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPIStatus::ValidateState** comprueba el estado de un recurso que esté asociado a un objeto de estado. **ValidateState** es el único método en la interfaz de [IMAPIStatus](imapistatusimapiprop.md) que es necesario para todos los objetos de estado. El comportamiento exacto de este método depende de la implementación. En la siguiente tabla se describe la implementación de cada uno de los distintos tipos de objetos de estado. 
  
|**Objeto de estado**|ValidateState ** implementación **|
|:-----|:-----|
|Subsistema MAPI  <br/> |Valida el estado de todos los recursos que poseen los proveedores de servicios activo actualmente y el subsistema de sí mismo.  <br/> |
|Cola MAPI  <br/> |Realiza un inicio de sesión de todos los proveedores de transporte, independientemente de si ya han iniciado sesión.  <br/> |
|Libreta de direcciones MAPI  <br/> |Comprobaciones de las entradas en la sección de perfil.  <br/> |
|Proveedor de servicios  <br/> |Implementación depende del tipo de proveedor y los indicadores establecidos en el parámetro _ulFlags indicado_ .  <br/> |
   
## <a name="notes-to-implementers"></a>Notas para los implementadores

Las aplicaciones cliente remoto llaman al método **ValidateState** para iniciar el proceso remoto para varias acciones. Este método existe principalmente para establecer los bits de estado para comunicarse con la cola MAPI, en lugar de hacerlo realmente realizar cualquier trabajo. Normalmente, el proveedor de transporte establece marcas en su fila de estado que se indican a la cola MAPI qué acciones deben iniciarse para completar la solicitud del cliente. 

En este modelo de interacción de cliente y transporte de cola de impresión, las acciones solicitadas por el cliente son asincrónicas, en que **ValidateState** devuelve antes de que las acciones requeridas se completa. Sin embargo, las acciones que implican necesariamente el sistema de mensajería subyacente o que implican una interfaz específica de transporte, pueden ser sincrónicas. La aplicación cliente pasa una máscara de bits de los siguientes indicadores para especificar las acciones que debe realizar el proveedor de transporte remoto. 
  
ABORT_XP_HEADER_OPERATION 
  
> Si es posible, el proveedor de transporte remoto debe cancelar las operaciones que implican descargar encabezados. Para ello, el proveedor de transporte debe establecer los siguientes valores de propiedad en la fila de estado del objeto de inicio de sesión:
    
   - Desactive los bits STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) para indicar a la cola MAPI para detener el proceso de vaciado entrante para este proveedor de transporte.
    
   - Establecer el bit en la propiedad **PR_STATUS_CODE** de STATUS_OFFLINE. 
    
   - Establezca la propiedad **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) en TRUE.
    
   - Establezca la propiedad **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) en una cadena que indica el estado del proveedor de transporte para el usuario.
    
   - Devuelve S_OK. Sin embargo, si no se puede cancelar la operación en curso, **ValidateState** debe devolver MAPI_E_BUSY. 
    
FORCE_XP_CONNECT 
  
> Un proveedor de transporte remoto nunca debe establecer una conexión a un recurso compartido (por ejemplo, un módem o un puerto COM) fuera del contexto de la interacción de transporte de la cola de impresión MAPI implica en el método [IXPLogon::FlushQueues](ixplogon-flushqueues.md) . Si se llama a **ValidateState** con este indicador, el proveedor de transporte debe hacer lo siguiente: 
    
   - Establecer un indicador de estado interno para indicar que se debe establecer la conexión remota cuando se llama al método **IXPLogon::FlushQueues** . 
    
   - Establecer los valores correctos en la tabla de estado para hacer que la cola MAPI iniciar la cola de proceso de vaciado.
    
   - Cuando se haya completado el vaciado de colas, el recurso compartido de la versión.
    
   - Desactive el STATUS_OFFLINE de bit en la propiedad **PR_STATUS_CODE** . 
    
   - Devuelve S_OK.
    
FORCE_XP_DISCONNECT 
  
> El proveedor de transporte remoto debe liberar su conexión con los recursos del sistema de mensajería. Después de hacer esto, se debe establecer el bit STATUS_OFFLINE en la propiedad **PR_STATUS_CODE** y devolver S_OK. 
    
PROCESS_XP_HEADER_CACHE 
  
> El proveedor de transporte remoto debe procesar los mensajes remotos y cargar todos los mensajes que se han aplazado. Para ello, el proveedor de transporte debe establecer los siguientes valores de propiedad en la fila de estado del objeto de inicio de sesión:
    
   - Establezca la propiedad **PR_STATUS_STRING** en una cadena que indica el estado del proveedor de transporte para el usuario. 
    
   - Establecer los bits STATUS_OUTBOUND_ENABLED y STATUS_OUTBOUND_ACTIVE en la propiedad **PR_STATUS_CODE** . 
    
   - Establezca la propiedad **PR_REMOTE_VALIDATE_OK** en la fila de estado del proveedor de transporte en FALSE. 
    
   - Si hay otra operación en curso (por ejemplo, descargar encabezados) cuando se llama a **ValidateState** , **ValidateState** debe devolver MAPI_E_BUSY. 
    
   - Ejecutar el código para procesar la marca REFRESH_XP_HEADER_CACHE, también, para satisfacer los requisitos del cliente de Microsoft Exchange.
    
REFRESH_XP_HEADER_CACHE 
  
> El proveedor de transporte remoto debe recuperar los encabezados de mensaje nuevo desde el sistema de mensajería. Para ello, el proveedor de transporte debe hacer lo siguiente:
    
   - Establezca la propiedad **PR_STATUS_STRING** en una cadena que indica el estado del proveedor de transporte para el usuario. 
    
   - Establecer los bits STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE en la propiedad **PR_STATUS_CODE** . 
    
   - Desactive el STATUS_OFFLINE de bit en la propiedad **PR_STATUS_CODE** . 
    
   - Establecer el bit en la propiedad **PR_STATUS_CODE** de STATUS_ONLINE. 
    
   - Establezca la propiedad **PR_REMOTE_VALIDATE_OK** en la fila de estado del proveedor de transporte en FALSE. 
    
SHOW_XP_SESSION_UI 
  
> Si su proveedor de transporte tiene cualquier partes de la interfaz de usuario para procesar los encabezados del mensaje (por ejemplo, un cuadro de diálogo que confirma la descarga de mensajes), se debe mostrar ese cuadro de diálogo. De lo contrario, **ValidateState** puede devolver MAPI_E_NO_SUPPORT. 
    
Si se pasan los indicadores distintos de estos, **ValidateState** debe devolver MAPI_E_UNKNOWN_FLAGS. 
  
El método **IMAPIStatus::ValidateState** a menudo será la llamada del cliente para el proveedor de transporte. Durante el procesamiento de **ValidateState**, el proveedor de transporte no debe realizar todas las acciones que asignan recursos escaso del sistema, como un módem o el puerto COM. Esto es debido a que la cola MAPI en ocasiones, necesite vaciar las colas en más de un proveedor de transporte. Sin embargo, el cliente puede llamar a método **ValidateState** del cualquier proveedor transporte en cualquier momento. Si su proveedor de transporte intenta asignar un recurso escaso durante el procesamiento de **ValidateState**, puede producir un error debido a conflictos con otro proveedor de transporte que se ha indicado la cola MAPI a que vacíen sus colas. Si permite que todas las asignaciones de recurso escaso se producen bajo la dirección de la cola MAPI, puede evitar estos conflictos. El proveedor de transporte debe admitir la propiedad **PR_REMOTE_VALIDATE_OK** para que pueden detectar las aplicaciones cliente cuando el proveedor de transporte está ocupado o tener que esperar la cola MAPI iniciar una acción. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Debido a que este método puede causar que otras llamadas potencialmente prolongados efectuarán, **ValidateState** puede devolver MAPI_E_BUSY para informarle de que este método está esperando la finalización de otra operación. Debe esperar hasta que se complete la operación pendiente antes de intentar otra tarea. 
  
Tener el máximo control sobre las llamadas a objetos de estado de proveedor de transporte. Puede pasar uno o más indicadores a **ValidateState** que afectan a las operaciones del proveedor de transporte. Por ejemplo, el indicador ABORT_XP_HEADER_OPERATION indica que el usuario canceló la validación. Los proveedores de transporte pueden optar por anular, devolver MAPI_E_USER_CANCELED, o pueden continuar. 
  
Puede establecer la marca CONFIG_CHANGED en una llamada para el objeto de estado de un proveedor de servicios o la cola MAPI para indicar que se ha cambiado una opción de configuración. Puede usar CONFIG_CHANGED para dinámicamente volver a configurar un proveedor de transporte. Cuando se establece CONFIG_CHANGED en una llamada al objeto de estado de un proveedor de servicios, el proveedor responde con una llamada a [SpoolerNotify](imapisupport-spoolernotify.md) a la cola MAPI del cambio de la alerta. Cuando se establece CONFIG_CHANGED en una llamada al objeto de estado de la cola MAPI, la cola de impresión llama a [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para cada proveedor de transporte activa. **AddressTypes** informa a la cola MAPI de tipos de direcciones compatibles de un transporte. Algunos proveedores de servicios también mostrar un indicador de progreso si la validación se espera a tardar mucho tiempo. Mostrar un indicador de progreso es útil, pero no se requiere. 
  
Cuando se establece la marca SUPPRESS_UI, se pueden mostrar ninguna de las hojas de propiedades de configuración o cuadros de diálogo de progreso. 
  
## <a name="see-also"></a>Recursos adicionales

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [Propiedad canónica PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)
- [Propiedad canónica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
- [Propiedad canónica PidTagStatusCode](pidtagstatuscode-canonical-property.md)
- [Propiedad canónica PidTagStatusString](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

