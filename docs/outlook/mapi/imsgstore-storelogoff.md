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
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424339"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Habilita el cierre de sesión orden del almacén de mensajes.
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in, out] Máscara de bits de marcas que controla el cierre de sesión desde el almacén de mensajes. En la entrada, todas las marcas establecidas para este parámetro son mutuamente excluyentes; Un autor de la llamada debe especificar solo una marca por llamada. Las siguientes marcas son válidas en la entrada:
    
LOGOFF_ABORT 
  
> Cualquier actividad del proveedor de transporte para este almacén de mensajes debe detenerse antes de cerrar sesión. El control se devuelve al autor de la llamada después de detener la actividad. Si se está llevando a cabo alguna actividad del proveedor de transporte, el cierre de sesión no se produce y no se produce ningún cambio en el comportamiento de la cola MAPI o los proveedores de transporte. Si la actividad del proveedor de transporte está inactiva, la cola MAPI libera el almacén. 
    
LOGOFF_NO_WAIT 
  
> El almacén de mensajes no debe esperar los mensajes de los proveedores de transporte antes de cerrarse. Se envían los mensajes salientes que están listos para enviarse. Si este almacén contiene la Bandeja de entrada predeterminada, se reciben los mensajes en proceso y, a continuación, se deshabilita la recepción adicional. Cuando se completa toda la actividad, la cola MAPI libera el almacén y el control se devuelve inmediatamente al autor de la llamada. 
    
LOGOFF_ORDERLY 
  
> El almacén de mensajes no debe esperar la información de los proveedores de transporte antes de cerrar. Los mensajes que se están procesando actualmente se completan, pero no se procesan mensajes nuevos. Cuando se completa toda la actividad, la cola MAPI libera el almacén y el control se devuelve inmediatamente al proveedor de la tienda. 
    
LOGOFF_PURGE 
  
> El cierre de sesión debe funcionar igual que si se establece la marca LOGOFF_NO_WAIT, pero se debe llamar al método [IXPLogon::FlushQueues](ixplogon-flushqueues.md) o [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) para los proveedores de transporte adecuados. La LOGOFF_PURGE devuelve el control al autor de la llamada después de finalizar. 
    
LOGOFF_QUIET 
  
> Si se está llevando a cabo alguna actividad del proveedor de transporte, no debe producirse el cierre de sesión.
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> Los mensajes entrantes están llegando actualmente.
    
LOGOFF_OUTBOUND 
  
> Los mensajes salientes están en proceso de envío.
    
LOGOFF_OUTBOUND_QUEUE 
  
> Los mensajes salientes están pendientes (es decir, están en la Bandeja de salida).
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El cierre de sesión se completó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::StoreLogoff** ejerce control sobre la interacción del almacén de mensajes y los proveedores de transporte durante el proceso de cierre de sesión. La **llamada a StoreLogoff** solo es válida para los almacenes de mensajes que solo usa el autor de la llamada. Por ejemplo, cuando dos clientes usan el mismo almacén de mensajes y uno de ellos llama a **StoreLogoff,** el almacén de mensajes se libera inmediatamente y el control se devuelve al cliente que realiza la llamada.
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Guarde las marcas que se pasan a **StoreLogoff** y pásalos cuando llame al método [IMAPISupport::StoreLogoffTransports.](imapisupport-storelogofftransports.md) No llame a **StoreLogoffTransports hasta** que el recuento de referencias del almacén de mensajes caiga a cero. Varias llamadas a **StoreLogoffTransports** simplemente sobrescriben las marcas guardadas. 
  
Si no se ha realizado ninguna llamada a **StoreLogoff** antes de que el recuento de referencias del almacén de mensajes alcance cero, establezca la marca LOGOFF_ABORT en el parámetro  _ulFlags_ que pase a **StoreLogoffTransports**.
  
## <a name="see-also"></a>Vea también



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

