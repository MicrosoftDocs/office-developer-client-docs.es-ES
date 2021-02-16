---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421385"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Solicita la publicación por orden de un almacén de mensajes.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpulFlags_
  
> [entrada, salida] Máscara de bits de marcas que controla cómo se produce el cierre de sesión del almacén de mensajes. En la entrada, todas las marcas de este parámetro son mutuamente excluyentes; solo se puede establecer una de las siguientes marcas por llamada:
    
LOGOFF_ABORT 
  
> Cualquier actividad del proveedor de transporte para este almacén debe detenerse antes de cerrar sesión. El control se devuelve al cliente después de detener la actividad y de que la cola MAPI haya cerrado sesión en el almacén. Si se produce alguna actividad de transporte, no se produce el cierre de sesión y no se produce ningún cambio en la cola MAPI ni en el comportamiento del proveedor de transporte. Si actualmente no hay ninguna actividad, la cola MAPI libera el almacén. 
    
LOGOFF_NO_WAIT 
  
> La cola MAPI debe liberar el almacén y devolver el control al cliente inmediatamente después de que se envíe todo el correo saliente que esté listo para enviarse. Si el almacén de mensajes tiene la Bandeja de entrada predeterminada, se recibe cualquier mensaje dentro del proceso y, a continuación, se deshabilita la recepción adicional. 
    
LOGOFF_ORDERLY 
  
> La cola MAPI debe liberar el almacén y devolver el control al cliente inmediatamente después de que finalice el procesamiento de los mensajes pendientes. No se deben procesar mensajes nuevos. 
    
LOGOFF_PURGE 
  
> Funciona igual que la marca LOGOFF_NO_WAIT de datos. La LOGOFF_PURGE devuelve el control al autor de la llamada después de finalizar. 
    
LOGOFF_QUIET 
  
> El cierre de sesión no debe producirse si se está llevando a cabo alguna actividad del proveedor de transporte. El tipo de actividad que tiene lugar se devuelve como una marca en el resultado.
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> El cierre de sesión puede completarse. Se han liberado todos los recursos asociados con el almacén y se ha invalidado el objeto. La cola MAPI ha realizado o realizará todas las solicitudes. Solo se debe llamar al método **IUnknown::Release** del almacén de mensajes en este momento. 
    
LOGOFF_INBOUND 
  
> Actualmente, hay un mensaje en el almacén procedente de uno o más proveedores de transporte. 
    
LOGOFF_OUTBOUND 
  
> Actualmente, uno o varios proveedores de transporte envían un mensaje desde el almacén. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Actualmente hay mensajes en la cola de salida para el almacén.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El procedimiento de cierre de sesión se ha realizado correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::StoreLogoffTransports** se implementa para objetos de compatibilidad del proveedor de al almacenamiento de mensajes. Los proveedores de almacén de mensajes llaman a **StoreLogoffTransports** para proporcionar a las aplicaciones cliente cierto control sobre cómo MAPI controla la actividad del proveedor de transporte mientras se cierra un almacén de mensajes. 
  
Si otro proceso tiene que haber cerrado la sesión del almacén para el mismo perfil, MAPI omite una llamada a **StoreLogoffTransports** y devuelve la marca LOGOFF_COMPLETE en el parámetro _lpulFlags._ 
  
El comportamiento del proveedor del almacén después de la devolución de **StoreLogoffTransports** debe basarse en el valor de  _lpulFlags_, que indica el estado del sistema y transmite instrucciones de cliente para el comportamiento de cierre de sesión. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 Normalmente se llama a **StoreLogoffTransports** desde el método [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) de un proveedor de almacén. Sin embargo, también se puede llamar desde el método **IUnknown::Release** del almacén de mensajes. Implemente **el método Release** del almacén de mensajes para que pueda comprobar si se ha producido o no una llamada a **StoreLogoffTransports.** Si no se ha producido una llamada, llame **a StoreLogoffTransports** con LOGOFF_ABORT marca establecida. 
  
El  _parámetro lpulFlags_ se establece en una marca que indica cómo el cliente requiere que se cierre el almacén de mensajes. Determine la configuración adecuada para  _ulFlags_ en función de la configuración del parámetro correspondiente en la llamada **a StoreLogoff**. Es decir, si un cliente llamó al método **StoreLogoff** con  _ulFlags_ establecido en LOGOFF_ORDERLY, debe llamar a **StoreLogoffTransports** con  _ulFlags_ establecido en LOGOFF_ORDERLY. 
  
Para obtener más información acerca del proceso de cierre de sesión del almacén de mensajes, vea [Apagar un proveedor de almacenamiento de mensajes.](shutting-down-a-message-store-provider.md)
  
## <a name="see-also"></a>Consulte también



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

