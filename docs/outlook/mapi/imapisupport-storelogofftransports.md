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
ms.openlocfilehash: b77a58b04e5cdeee7a9e84051a6ed287c1a20115
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578314"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Solicita la versión ordenada de un almacén de mensajes.
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpulFlags_
  
> [entrada, salida] Una máscara de bits de indicadores que controla cómo se produce el cierre de sesión de almacén de mensajes. En la entrada, todos los indicadores para este parámetro son mutuamente excluyentes; por llamada, se puede establecer solo uno de los siguientes indicadores:
    
LOGOFF_ABORT 
  
> Cualquier actividad de proveedor de transporte para este almacén se debe detener antes de cierre de sesión. Control se devuelve al cliente una vez que se ha detenido la actividad y la cola MAPI ha cerrado el almacén de la sesión. Si está produciendo alguna actividad de transporte, no se produce el cierre de sesión y se produce ningún cambio en el comportamiento del proveedor de cola de impresión o de transporte MAPI. Si actualmente no hay ninguna actividad, la cola MAPI libera el almacén. 
    
LOGOFF_NO_WAIT 
  
> La cola MAPI debe liberar el almacén y devolver el control al cliente inmediatamente se envía el correo saliente después de todo que está listo para ser enviado. Si el almacén de mensajes tiene la Bandeja de entrada predeterminada, se recibe ningún mensaje en el proceso y, a continuación, se deshabilita la recepción de más. 
    
LOGOFF_ORDERLY 
  
> La cola MAPI debe liberar el almacén y devolver el control al cliente inmediatamente después de que se complete cualquiera mensajes pendientes de procesamiento. No hay mensajes nuevos se deben procesar. 
    
LOGOFF_PURGE 
  
> Funciona de la misma que la marca LOGOFF_NO_WAIT. El indicador LOGOFF_PURGE devuelve el control al autor de la llamada después de la finalización. 
    
LOGOFF_QUIET 
  
> El cierre de sesión no debe producirse si está produciendo alguna actividad del proveedor de transporte. Se devuelve el tipo de actividad que tiene lugar como una marca en la salida.
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> Puede completar el cierre de sesión. Se han publicado todos los recursos asociados con el almacén y el objeto se ha invalidado. La cola MAPI ha llevado a cabo o llevará a cabo todas las solicitudes. Método de **IUnknown:: Release** del almacén de mensajes sólo se debe llamar en este momento. 
    
LOGOFF_INBOUND 
  
> Un mensaje procede actualmente en el almacén de uno o varios proveedores de transporte. 
    
LOGOFF_OUTBOUND 
  
> Actualmente se que se envía un mensaje desde el almacén por uno o varios proveedores de transporte. 
    
LOGOFF_OUTBOUND_QUEUE 
  
> Actualmente hay mensajes en la cola de salida para el almacén.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El procedimiento de cierre de sesión fue correcto.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::StoreLogoffTransports** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes. Los proveedores de almacén de mensajes llamada **StoreLogoffTransports** para que las aplicaciones cliente de algún control sobre cómo se está cerrando la actividad de proveedor de transporte MAPI identificadores como un almacén de mensajes. 
  
Si otro proceso tiene el almacén que se cerró sesión abrir para el mismo perfil, MAPI omite una llamada a **StoreLogoffTransports** y devuelve la marca LOGOFF_COMPLETE en el parámetro _lpulFlags_ . 
  
El comportamiento del proveedor de almacén de seguir la devolución de **StoreLogoffTransports** debe basarse en el valor de _lpulFlags_, que indica el estado del sistema y transmite las instrucciones del cliente para el comportamiento de cierre de sesión. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

 **StoreLogoffTransports** normalmente se llama desde (método [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) ) del proveedor de almacenamiento. Sin embargo, también se puede llamar desde el método **IUnknown:: Release** del almacén de mensajes. Implementar el método de la **versión** de su almacén de mensajes de modo que puede comprobar si una llamada a **StoreLogoffTransports** se ha producido. Si no se ha producido una llamada, llame a **StoreLogoffTransports** con el conjunto de marca LOGOFF_ABORT. 
  
El parámetro _lpulFlags_ se establece en una marca que indica cómo el cliente requiere que el almacén de mensajes para cerrarse. Determinar la configuración adecuada para _ulFlags_ según la configuración del parámetro correspondiente en la llamada a **StoreLogoff**. Es decir, si un cliente llama al método **StoreLogoff** con _ulFlags_ establecida en LOGOFF_ORDERLY, debe llamar a **StoreLogoffTransports** con _ulFlags_ establecida en LOGOFF_ORDERLY. 
  
Para obtener más información acerca del proceso de cierre de sesión del almacén de mensajes, vea [Cerrando hacia abajo un mensaje Store Provider](shutting-down-a-message-store-provider.md).
  
## <a name="see-also"></a>Recursos adicionales



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

