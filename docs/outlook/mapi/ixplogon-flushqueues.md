---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 116e3cfaace9c0965001021575b76ec371667877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818008"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**Hace referencia a**: Outlook 
  
Solicitudes que el proveedor de transporte entrega inmediatamente todos los mensajes entrantes o salientes pendientes.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.
    
 _cbTargetTransport_
  
> [entrada] Reservado; debe ser cero.
    
 _lpTargetTransport_
  
> [entrada] Reservado; debe ser NULL.
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se realiza el vaciado de la cola de mensajes. Se pueden establecer los siguientes indicadores:
    
FLUSH_DOWNLOAD 
  
> Deben vaciar la cola de mensajes entrantes o colas.
    
FLUSH_FORCE 
  
> El proveedor de transporte debe procesar esta solicitud, si es posible, incluso si esto es mucho tiempo. 
    
FLUSH_NO_UI 
  
> El proveedor de transporte no debe mostrar una interfaz de usuario.
    
FLUSH_UPLOAD 
  
> Deben vaciar la cola de mensajes salientes o colas.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método de **IXPLogon::FlushQueues** para indicar que el proveedor de transporte que la cola MAPI está a punto de comenzar el procesamiento de los mensajes. El proveedor de transporte debe llamar al método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para establecer un bit apropiado para su estado en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la fila de estado correspondiente. Después de actualizar su fila de estado, el proveedor de transporte debe devolver S_OK para la llamada de **FlushQueues** . La cola MAPI, a continuación, inicia el envío de mensajes, con la operación que se va a sincrónica a la cola MAPI. 
  
Para admitir su implementación del método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) , la cola MAPI llama a **IXPLogon::FlushQueues** para todos los objetos de inicio de sesión para los proveedores de transporte de activo que se ejecutan en una sesión de perfil. Cuando se llama a método de **FlushQueues** del proveedor de transporte como resultado de una llamada de la aplicación de cliente a **IMAPIStatus::FlushQueues**, el procesamiento del mensaje se produce de forma asincrónica al cliente.
  
## <a name="see-also"></a>Vea también



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

