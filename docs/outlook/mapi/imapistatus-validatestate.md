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
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438151"
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

## <a name="parameters"></a>Parameters

_ulUIParam_
  
> [in] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método.
    
_ulFlags_
  
> [in] Máscara de bits de marcas que controla la validación. Se pueden establecer las siguientes marcas:
    
ABORT_XP_HEADER_OPERATION
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** del cuadro de diálogo correspondiente. El objeto status tiene dos opciones: 
    
   - Siga trabajando en la operación.
    
   - Detenga la operación y devuelva MAPI_E_USER_CANCELED.
    
CONFIG_CHANGED 
  
> Se cambiaron una o varias de las propiedades de configuración del objeto de estado. Los clientes pueden establecer esta marca para permitir que la cola MAPI corrija dinámicamente los errores críticos del proveedor de transporte. 
    
FORCE_XP_CONNECT 
  
> El objeto status debe realizar una conexión. Cuando esta marca se usa con la REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la conexión se produce sin almacenamiento en caché.
    
FORCE_XP_DISCONNECT 
  
> El objeto status debe realizar una operación de desconexión. Cuando esta marca se usa con la REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la desconexión se produce sin almacenamiento en caché.
    
PROCESS_XP_HEADER_CACHE 
  
> Se deben procesar las entradas de la tabla de caché de encabezado, descargar todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DOWNLOAD y eliminar todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DELETE. Los mensajes que tienen MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE deben moverse.
    
REFRESH_XP_HEADER_CACHE 
  
> Para un proveedor de transporte remoto, se debe descargar una nueva lista de encabezados de mensaje y se deben borrar todas las marcas que marcan el estado del mensaje.
    
SUPPRESS_UI 
  
> Impide que el objeto de estado muestre una interfaz de usuario como parte de la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La validación se ha realizado correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso; debe poder completarse, o debe detenerse, antes de iniciar esta operación.
    
MAPI_E_NO_SUPPORT 
  
> El objeto status no admite el método de validación, como se indica por la ausencia de la marca STATUS_VALIDATE_STATE en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación de validación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo. Este valor solo lo devuelven los proveedores de transporte remoto. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPIStatus::ValidateState** comprueba el estado de un recurso asociado a un objeto status. **ValidateState** es el único método de la [interfaz IMAPIStatus](imapistatusimapiprop.md) que es necesario para todos los objetos de estado. El comportamiento exacto de este método depende de la implementación. En la tabla siguiente se describe la implementación de cada uno de los distintos tipos de objetos de estado. 
  
|**Status (objeto)**|ValidateState** implementación**|
|:-----|:-----|
|Subsistema MAPI  <br/> |Valida el estado de todos los recursos que poseen los proveedores de servicios activos actualmente y el propio subsistema.  <br/> |
|Cola MAPI  <br/> |Realiza un inicio de sesión de todos los proveedores de transporte, independientemente de si ya han iniciado sesión.  <br/> |
|Libreta de direcciones MAPI  <br/> |Comprueba las entradas de su sección de perfil.  <br/> |
|Proveedor de servicios  <br/> |La implementación depende del tipo de proveedor y las marcas establecidas en el _parámetro ulFlags._  <br/> |
   
## <a name="notes-to-implementers"></a>Notas a los implementadores

Las aplicaciones cliente remotas llaman **al método ValidateState** para iniciar el procesamiento remoto de varias acciones. Este método existe principalmente para establecer bits de estado para comunicarse con la cola MAPI, en lugar de realizar realmente cualquier trabajo. Normalmente, el proveedor de transporte establece marcas en su fila de estado que indican a la cola MAPI qué acciones deben iniciarse para completar la solicitud del cliente. 

En este modelo de interacción client-transport-spooler, las acciones solicitadas por el cliente son asincrónicas, ya que **ValidateState** devuelve antes de que se completen las acciones solicitadas. Sin embargo, las acciones que no implican necesariamente el sistema de mensajería subyacente, o que implican una interfaz específica del transporte, pueden ser sincrónicas. La aplicación cliente pasa una máscara de bits de las siguientes marcas para especificar qué acciones debe realizar el proveedor de transporte remoto. 
  
ABORT_XP_HEADER_OPERATION 
  
> Si es posible, el proveedor de transporte remoto debe cancelar las operaciones que impliquen la descarga de encabezados. Para ello, el proveedor de transporte debe establecer los siguientes valores de propiedad en la fila de estado del objeto de inicio de sesión:
    
   - Desactive los bits STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) para que la cola MAPI detenga el proceso de vaciado entrante para este proveedor de transporte.
    
   - Establezca el STATUS_OFFLINE en la **PR_STATUS_CODE** propiedad. 
    
   - Establezca la **propiedad PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) en TRUE.
    
   - Establezca la **propiedad PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) en una cadena que indique el estado del proveedor de transporte al usuario.
    
   - Devuelve S_OK. Sin embargo, si la operación en curso no se puede cancelar, **ValidateState** debe devolver MAPI_E_BUSY. 
    
FORCE_XP_CONNECT 
  
> Un proveedor de transporte remoto nunca debe establecer una conexión a un recurso compartido (por ejemplo, un módem o un puerto COM) fuera del contexto de la interacción de transporte de cola MAPI implicada en el método [IXPLogon::FlushQueues.](ixplogon-flushqueues.md) Si se llama a **ValidateState** con esta marca, el proveedor de transporte debe hacer lo siguiente: 
    
   - Establezca una marca de estado interno para indicar que la conexión remota debe establecerse cuando se llama al método **IXPLogon::FlushQueues.** 
    
   - Establezca los valores correctos en la tabla de estado para que la cola MAPI inicie el proceso de vaciado de cola.
    
   - Cuando se complete el vaciado de colas, libere el recurso compartido.
    
   - Desactive el STATUS_OFFLINE en la **PR_STATUS_CODE** propiedad. 
    
   - Devuelve S_OK.
    
FORCE_XP_DISCONNECT 
  
> El proveedor de transporte remoto debe liberar su conexión a los recursos del sistema de mensajería. Después de hacerlo, debe establecer el STATUS_OFFLINE en la **propiedad PR_STATUS_CODE** y devolver S_OK. 
    
PROCESS_XP_HEADER_CACHE 
  
> El proveedor de transporte remoto debe procesar mensajes remotos y cargar los mensajes que se hayan aplazado. Para ello, el proveedor de transporte debe establecer los siguientes valores de propiedad en la fila de estado del objeto de inicio de sesión:
    
   - Establezca la **PR_STATUS_STRING** propiedad en una cadena que indique el estado del proveedor de transporte al usuario. 
    
   - Establezca los STATUS_OUTBOUND_ENABLED y STATUS_OUTBOUND_ACTIVE bits en la **PR_STATUS_CODE** propiedad. 
    
   - Establezca la **propiedad PR_REMOTE_VALIDATE_OK** en la fila de estado del proveedor de transporte en FALSE. 
    
   - Si hay otra operación en curso (como los encabezados de descarga) cuando se llama **a ValidateState,** **ValidateState** debe devolver MAPI_E_BUSY. 
    
   - Ejecute el código para procesar la marca REFRESH_XP_HEADER_CACHE, así, para satisfacer los requisitos del cliente Exchange Microsoft.
    
REFRESH_XP_HEADER_CACHE 
  
> El proveedor de transporte remoto debe recuperar los nuevos encabezados de mensaje del sistema de mensajería. Para ello, el proveedor de transporte debe hacer lo siguiente:
    
   - Establezca la **PR_STATUS_STRING** propiedad en una cadena que indique el estado del proveedor de transporte al usuario. 
    
   - Establezca los STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE bits en la **PR_STATUS_CODE** propiedad. 
    
   - Desactive el STATUS_OFFLINE en la **PR_STATUS_CODE** propiedad. 
    
   - Establezca el STATUS_ONLINE bit en la **PR_STATUS_CODE** propiedad. 
    
   - Establezca la **propiedad PR_REMOTE_VALIDATE_OK** en la fila de estado del proveedor de transporte en FALSE. 
    
SHOW_XP_SESSION_UI 
  
> Si el proveedor de transporte tiene algún fragmento de interfaz de usuario para procesar los encabezados de mensaje (como un cuadro de diálogo que confirma la descarga de mensajes), ese cuadro de diálogo debe mostrarse. De lo contrario, **ValidateState** puede devolver MAPI_E_NO_SUPPORT. 
    
Si se pasan marcas que no sean estas, **ValidateState** debe devolver MAPI_E_UNKNOWN_FLAGS. 
  
La llamada del cliente al proveedor de transporte suele ser al método **IMAPIStatus::ValidateState.** Durante el procesamiento de **ValidateState,** el proveedor de transporte no debe realizar ninguna acción que asigne recursos del sistema escasos, como un módem o un puerto COM. Esto se debe a que la cola MAPI a veces tendrá que vaciar colas en más de un proveedor de transporte. Sin embargo, el cliente puede llamar al método **ValidateState** de cualquier proveedor de transporte en cualquier momento. Si el proveedor de transporte intenta asignar un recurso escaso durante el procesamiento de **ValidateState**, puede producirse un error debido a un conflicto con otro proveedor de transporte que la cola MAPI ha ordenado vaciar sus colas. Si permite que todas las asignaciones de recursos escasos se produzcan bajo la dirección de la cola MAPI, puede evitar dichos conflictos. El proveedor de transporte debe admitir la **propiedad PR_REMOTE_VALIDATE_OK** para que las aplicaciones cliente puedan detectar cuándo el proveedor de transporte está ocupado o esperando que la cola MAPI inicie una acción. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Dado que este método puede provocar otras llamadas potencialmente largas, **ValidateState** puede devolver MAPI_E_BUSY para informarle de que este método está esperando la finalización de otra operación. Debe esperar hasta que se complete la operación pendiente antes de intentar otra tarea. 
  
Tiene el mayor control sobre las llamadas a objetos de estado del proveedor de transporte. Puede pasar una o más marcas a **ValidateState** que afecten a las operaciones del proveedor de transporte. Por ejemplo, la marca ABORT_XP_HEADER_OPERATION indica que el usuario canceló la validación. Los proveedores de transporte pueden decidir anular, devolver MAPI_E_USER_CANCELED o pueden continuar. 
  
Puede establecer la marca CONFIG_CHANGED en una llamada al objeto de estado de un proveedor de servicios o a la cola MAPI para indicar que se ha cambiado una opción de configuración. Puede usar CONFIG_CHANGED para volver a configurar dinámicamente un proveedor de transporte. Al establecer CONFIG_CHANGED en una llamada al objeto de estado de un proveedor de servicios, el proveedor responde con una llamada a [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) para alertar al colador MAPI del cambio. Al establecer CONFIG_CHANGED en una llamada al objeto de estado de la cola MAPI, la cola llama a [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para cada proveedor de transporte activo. **AddressTypes** informa a la cola MAPI de los tipos de direcciones compatibles de un transporte. Algunos proveedores de servicios también muestran un indicador de progreso si se espera que la validación lleve mucho tiempo. Mostrar un indicador de progreso es útil, pero no necesario. 
  
Cuando se SUPPRESS_UI marca, no se puede mostrar ninguna de las hojas de propiedades de configuración ni los cuadros de diálogo de progreso. 
  
## <a name="see-also"></a>Vea también

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [Propiedad canónica PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)
- [Propiedad canónica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
- [Propiedad canónica PidTagStatusCode](pidtagstatuscode-canonical-property.md)
- [Propiedad canónica PidTagStatusString](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

