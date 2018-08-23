---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a55fc361120472473bcba70152c153fb7824fb9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566554"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite el cierre de sesión ordenada del almacén de mensajes.
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpulFlags_
  
> [entrada, salida] Una máscara de bits de indicadores que controla el cierre de sesión desde el almacén de mensajes. En la entrada, todos los indicadores que se hayan establecido para este parámetro son mutuamente excluyentes; un autor de la llamada debe especificar sólo una marca por llamada. Las siguientes marcas son válidas en la entrada:
    
LOGOFF_ABORT 
  
> Cualquier actividad de proveedor de transporte para este almacén de mensajes se debe detener antes de cierre de sesión. Control se devuelve al autor de la llamada después de que se ha detenido la actividad. Si está produciendo alguna actividad del proveedor de transporte, no se produce el cierre de sesión y se produce ningún cambio en el comportamiento de los proveedores de cola de impresión o de transporte MAPI. Si la actividad del proveedor de transporte está inactivo, la cola MAPI libera el almacén. 
    
LOGOFF_NO_WAIT 
  
> No debe esperar el almacén de mensajes para mensajes de proveedores de transporte antes de cerrar. Se envían los mensajes salientes que están listos para ser enviados. Si este almacén contiene la Bandeja de entrada predeterminada, se reciben los mensajes en proceso y, a continuación, se deshabilita la recepción de más. Una vez finalizada toda la actividad, la cola MAPI libera el almacén y control se devuelve inmediatamente al autor de la llamada. 
    
LOGOFF_ORDERLY 
  
> El almacén de mensajes no debe esperar para obtener información de los proveedores de transporte antes de cerrar. Los mensajes que se están procesando actualmente están completados, pero no los mensajes nuevos se procesan. Una vez finalizada toda la actividad, la cola MAPI libera el almacén e inmediatamente el control se devuelve al proveedor de almacenamiento. 
    
LOGOFF_PURGE 
  
> El cierre de sesión debe trabajar el mismo como si se establece la marca LOGOFF_NO_WAIT, pero debe llamar al método de la [IXPLogon::FlushQueues](ixplogon-flushqueues.md) o [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) para los proveedores de transporte apropiado. El indicador LOGOFF_PURGE devuelve el control al autor de la llamada después de la finalización. 
    
LOGOFF_QUIET 
  
> Si está produciendo alguna actividad del proveedor de transporte, no debe producirse el cierre de sesión.
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> Actualmente llegan mensajes entrantes.
    
LOGOFF_OUTBOUND 
  
> Los mensajes salientes están en proceso de enviarse.
    
LOGOFF_OUTBOUND_QUEUE 
  
> Los mensajes salientes son pendientes (es decir, se encuentran en la Bandeja de salida).
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cierre de sesión que se realizó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore::StoreLogoff** ejerce control a través de la interacción del mensaje almacenar y los proveedores de transporte durante el proceso de cierre de sesión. Al llamar a **StoreLogoff** sólo es válido para los almacenes de mensajes que se usan solo por el autor de la llamada. Por ejemplo, cuando dos clientes están utilizando el mismo almacén de mensajes y uno de ellos llama a **StoreLogoff**, inmediatamente se libera el almacén de mensajes y el control se devuelve al cliente que llama.
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Guarde los indicadores que se pasan al **StoreLogoff** y páselos al llamar al método [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) . No llame a **StoreLogoffTransports** hasta que el recuento de referencia del almacén de mensajes cae a cero. Varias llamadas a **StoreLogoffTransports** simplemente sobrescribirán los indicadores de guardado. 
  
Si no se ha realizado ninguna llamada a **StoreLogoff** antes de que el mensaje recuento de referencia de la tienda llega a cero, establecer el indicador LOGOFF_ABORT en el parámetro _ulFlags_ que se pasa a **StoreLogoffTransports**.
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

