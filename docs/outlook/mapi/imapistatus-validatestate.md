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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331552"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Confirma la información de estado externo disponible para el recurso MAPI o el proveedor de servicios. Este método se admite en todos los objetos status. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

_ulUIParam_
  
> a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que muestra este método.
    
_ulFlags_
  
> a Máscara de máscara de marcadores que controla la validación. Se pueden establecer los siguientes indicadores:
    
ABORT_XP_HEADER_OPERATION
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en el cuadro de diálogo correspondiente. El objeto status tiene dos opciones: 
    
   - Continúe trabajando en la operación.
    
   - Detenga la operación y devuelva MAPI_E_USER_CANCELED.
    
CONFIG_CHANGED 
  
> Una o varias de las propiedades de configuración del objeto de estado han cambiado. Los clientes pueden establecer esta marca para permitir que la cola MAPI corrija dinámicamente los errores del proveedor de transporte crítico. 
    
FORCE_XP_CONNECT 
  
> El objeto de Estado debe realizar una conexión. Cuando se usa este indicador con la marca REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la conexión se produce sin almacenamiento en la memoria caché.
    
FORCE_XP_DISCONNECT 
  
> El objeto de Estado debe realizar una operación de desconexión. Cuando se usa este indicador con la marca REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la desconexión se produce sin almacenamiento en la memoria caché.
    
PROCESS_XP_HEADER_CACHE 
  
> Las entradas de la tabla de caché de encabezado deben ser procesadas, se deben descargar todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DOWNLOAD y se eliminarán todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DELETE. Se deben mover los mensajes que tienen el conjunto MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE.
    
REFRESH_XP_HEADER_CACHE 
  
> Para un proveedor de transporte remoto, se debe descargar una nueva lista de encabezados de mensaje y se deben borrar todas las marcas que marcan el estado del mensaje.
    
SUPPRESS_UI 
  
> Impide que el objeto status muestre una interfaz de usuario como parte de la operación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La validación se realizó correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso; se debe permitir que se complete o debe detenerse antes de que se inicie esta operación.
    
MAPI_E_NO_SUPPORT 
  
> El objeto status no admite el método de validación, tal como indica la ausencia de la marca STATUS_VALIDATE_STATE en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación de validación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. Este valor solo lo devuelven los proveedores de transporte remoto. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPIStatus:: ValidateState** comprueba el estado de un recurso que está asociado a un objeto status. **ValidateState** es el único método de la interfaz [IMAPIStatus](imapistatusimapiprop.md) que se requiere para todos los objetos status. El comportamiento exacto de este método depende de la implementación. En la tabla siguiente se describe la implementación de cada uno de los distintos tipos de objetos de estado. 
  
|**Status (objeto)**|Implementación de ValidateState * * * *|
|:-----|:-----|
|Subsistema MAPI  <br/> |Valida el estado de todos los recursos que poseen los proveedores de servicios actualmente activos y el propio subsistema.  <br/> |
|Cola MAPI  <br/> |Realiza un inicio de sesión de todos los proveedores de transporte, independientemente de si ya han iniciado sesión.  <br/> |
|Libreta de direcciones MAPI  <br/> |Comprueba las entradas en su sección de perfil.  <br/> |
|Proveedor de servicios  <br/> |La implementación depende del tipo de proveedor y de los marcadores establecidos en el parámetro _ulFlags_ .  <br/> |
   
## <a name="notes-to-implementers"></a>Notas a los implementadores

Las aplicaciones cliente remotas llaman al método **ValidateState** para iniciar el procesamiento remoto para varias acciones. Este método existe principalmente para establecer bits de estado para comunicarse con la cola MAPI, en lugar de hacerlo realmente. Normalmente, el proveedor de transporte establece indicadores en su fila de estado que indican a la cola MAPI las acciones que deben iniciarse para completar la solicitud del cliente. 

En este modelo de interacción de cola de transporte de cliente, las acciones solicitadas por el cliente son asincrónicas, en la que **ValidateState** devuelve antes de que se completen las acciones solicitadas. Sin embargo, las acciones que no necesariamente implican el sistema de mensajería subyacente o que implican una interfaz específica de transporte pueden ser sincrónicas. La aplicación cliente pasa una máscara de máscara de los siguientes indicadores para especificar las acciones que debe realizar el proveedor de transporte remoto. 
  
ABORT_XP_HEADER_OPERATION 
  
> Si es posible, el proveedor de transporte remoto debe cancelar cualquier operación que implique la descarga de encabezados. Para ello, el proveedor de transporte debe establecer los siguientes valores de propiedad en la fila de estado del objeto de inicio de sesión:
    
   - Borre los bits STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE de la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) para decir a la cola MAPI que detenga el proceso de vaciado entrante para este proveedor de transporte.
    
   - Establezca el bit STATUS_OFFLINE en la propiedad **PR_STATUS_CODE** . 
    
   - Establezca la propiedad **PR_REMOTE_VALIDATE_OK** ([PIDTAGREMOTEVALIDATEOK](pidtagremotevalidateok-canonical-property.md)) en true.
    
   - Establezca la propiedad **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) en una cadena que indique el estado del proveedor de transporte al usuario.
    
   - Devuelve S_OK. Sin embargo, si no se puede cancelar la operación en curso, **ValidateState** debe devolver MAPI_E_BUSY. 
    
FORCE_XP_CONNECT 
  
> Un proveedor de transporte remoto nunca debe establecer una conexión a un recurso compartido (por ejemplo, un módem o un puerto COM) fuera del contexto de la interacción de administrador de trabajos en cola de MAPI que interviene en el método [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) . Si se llama a **ValidateState** con este indicador, el proveedor de transporte debe hacer lo siguiente: 
    
   - Establezca un indicador de estado interno para indicar que se debe establecer la conexión remota cuando se llama al método **IXPLogon:: FlushQueues** . 
    
   - Establezca los valores correctos en la tabla de estado para hacer que la cola MAPI inicie el proceso de vaciado de la cola.
    
   - Una vez finalizada la vaciado de las colas, libere el recurso compartido.
    
   - Borre el bit STATUS_OFFLINE en la propiedad **PR_STATUS_CODE** . 
    
   - Devuelve S_OK.
    
FORCE_XP_DISCONNECT 
  
> El proveedor de transporte remoto debe liberar su conexión a los recursos del sistema de mensajería. Después de hacerlo, debe establecer el bit STATUS_OFFLINE en la propiedad **PR_STATUS_CODE** y devolver S_OK. 
    
PROCESS_XP_HEADER_CACHE 
  
> El proveedor de transporte remoto debe procesar los mensajes remotos y cargar los mensajes que se han aplazado. Para ello, el proveedor de transporte debe establecer los siguientes valores de propiedad en la fila de estado del objeto de inicio de sesión:
    
   - Establezca la propiedad **PR_STATUS_STRING** en una cadena que indique el estado del proveedor de transporte al usuario. 
    
   - Establezca los bits STATUS_OUTBOUND_ENABLED y STATUS_OUTBOUND_ACTIVE en la propiedad **PR_STATUS_CODE** . 
    
   - Establezca la propiedad **PR_REMOTE_VALIDATE_OK** de la fila estado del proveedor de transporte en false. 
    
   - Si hay otra operación en curso (como descargar encabezados) cuando se llama a **ValidateState** , **VALIDATESTATE** debe devolver MAPI_E_BUSY. 
    
   - Ejecute también el código para procesar la marca REFRESH_XP_HEADER_CACHE para satisfacer los requisitos del cliente de Microsoft Exchange.
    
REFRESH_XP_HEADER_CACHE 
  
> El proveedor de transporte remoto debe recuperar los nuevos encabezados de mensajes del sistema de mensajería. Para ello, el proveedor de transporte debe hacer lo siguiente:
    
   - Establezca la propiedad **PR_STATUS_STRING** en una cadena que indique el estado del proveedor de transporte al usuario. 
    
   - Establezca los bits STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE en la propiedad **PR_STATUS_CODE** . 
    
   - Borre el bit STATUS_OFFLINE en la propiedad **PR_STATUS_CODE** . 
    
   - Establezca el bit STATUS_ONLINE en la propiedad **PR_STATUS_CODE** . 
    
   - Establezca la propiedad **PR_REMOTE_VALIDATE_OK** de la fila estado del proveedor de transporte en false. 
    
SHOW_XP_SESSION_UI 
  
> Si el proveedor de transporte tiene alguna de las partes de la interfaz de usuario para procesar los encabezados del mensaje (por ejemplo, un cuadro de diálogo que confirma la descarga de mensajes), debe mostrarse el cuadro de diálogo. De lo contrario, **ValidateState** puede devolver MAPI_E_NO_SUPPORT. 
    
Si se pasan otros marcadores que no sean estos, **ValidateState** debe devolver MAPI_E_UNKNOWN_FLAGS. 
  
La llamada del cliente al proveedor de transporte será a menudo el método **IMAPIStatus:: ValidateState** . Durante el procesamiento de **ValidateState**, el proveedor de transporte no debe realizar ninguna acción que asigne pocos recursos del sistema, como un módem o un puerto com. Esto se debe a que, en ocasiones, la cola MAPI tendrá que vaciar colas en más de un proveedor de transporte. Sin embargo, el cliente puede llamar a cualquier método **ValidateState** de un proveedor de transporte en cualquier momento. Si el proveedor de transporte intenta asignar un recurso escaso durante el procesamiento de **ValidateState**, se puede producir un error debido a un conflicto con otro proveedor de transporte que la cola MAPI ha instruido para vaciar sus colas. Si permite que se produzcan todas las asignaciones de recursos escasos bajo la dirección de la cola MAPI, puede evitar estos conflictos. El proveedor de transporte debe ser compatible con la propiedad **PR_REMOTE_VALIDATE_OK** para que las aplicaciones cliente puedan detectar cuándo el proveedor de transporte está ocupado o esperando que la cola MAPI inicie una acción. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Como este método puede hacer que se realicen otras llamadas potencialmente largas, **ValidateState** puede devolver MAPI_E_BUSY para informarle de que este método está esperando a que se complete otra operación. Debe esperar hasta que se complete la operación pendiente antes de intentar otra tarea. 
  
Tiene el máximo control sobre las llamadas a los objetos de estado del proveedor de transporte. Puede pasar una o varias marcas a **ValidateState** que afectan a las operaciones del proveedor de transporte. Por ejemplo, la marca ABORT_XP_HEADER_OPERATION indica que el usuario canceló la validación. Los proveedores de transporte pueden decidir si anular, devolver MAPI_E_USER_CANCELED o puede continuar. 
  
Puede establecer la marca CONFIG_CHANGED en una llamada al objeto status de un proveedor de servicios o a la cola MAPI para indicar que se ha cambiado una opción de configuración. Puede usar CONFIG_CHANGED para volver a configurar dinámicamente un proveedor de transporte. Cuando se establece CONFIG_CHANGED en una llamada a un objeto de estado de un proveedor de servicios, el proveedor responde con una llamada a [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) para alertar al administrador de trabajos en cola MAPI del cambio. Cuando establece CONFIG_CHANGED en una llamada al objeto status del administrador de trabajos en cola MAPI, la cola de impresión llama a [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) para cada proveedor de transporte activo. **AddressTypes** informa a la cola MAPI de los tipos de direcciones admitidos de un transporte. Algunos proveedores de servicios también muestran un indicador de progreso si se espera que la validación tarde mucho tiempo. Es útil mostrar un indicador de progreso, pero no es necesario. 
  
Cuando se establece la marca SUPPRESS_UI, no se puede mostrar ninguna de las hojas de propiedades de configuración ni los cuadros de diálogo de progreso. 
  
## <a name="see-also"></a>Vea también

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [Propiedad canónica PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)
- [Propiedad canónica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
- [Propiedad canónica PidTagStatusCode](pidtagstatuscode-canonical-property.md)
- [Propiedad canónica PidTagStatusString](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

