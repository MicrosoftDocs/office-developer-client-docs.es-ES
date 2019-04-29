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
ms.openlocfilehash: fb26c7f366ce6a262362001773e825c60d0e4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421973"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Solicita que el proveedor de transporte entregue inmediatamente todos los mensajes entrantes o salientes pendientes.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de la ventana primaria de los cuadros de diálogo o ventanas que muestra este método.
    
 _cbTargetTransport_
  
> [entrada] Reservado; debe ser cero.
    
 _lpTargetTransport_
  
> a Reserve debe ser NULL.
    
 _ulFlags_
  
> a Una máscara de máscara de marcadores que controla cómo se realiza el vaciado de la cola de mensajes. Se pueden establecer los siguientes indicadores:
    
FLUSH_DOWNLOAD 
  
> Las colas de mensajes entrantes deben vaciarse.
    
FLUSH_FORCE 
  
> El proveedor de transporte debe procesar esta solicitud, si es posible, incluso si se trata de tiempo largo. 
    
FLUSH_NO_UI 
  
> El proveedor de transporte no debe mostrar una interfaz de usuario.
    
FLUSH_UPLOAD 
  
> Se deben vaciar las colas de mensajes salientes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama al método **IXPLogon:: FlushQueues** para informar al proveedor de transporte que la cola MAPI va a empezar a procesar mensajes. El proveedor de transporte debería llamar al método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) para establecer un bit adecuado para su estado en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de su fila de estado. Después de actualizar la fila de estado, el proveedor de transporte debe devolver S_OK para la llamada **FlushQueues** . A continuación, la cola MAPI comienza a enviar mensajes, con la operación sincrónica a la cola MAPI. 
  
Para admitir su implementación del método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) , la cola MAPI llama a **IXPLogon:: FlushQueues** para todos los objetos de inicio de sesión de los proveedores de transporte activos que se ejecutan en una sesión de perfil. Cuando se llama a un método **FlushQueues** de un proveedor de transporte como resultado de una llamada de aplicación cliente a **IMAPIStatus:: FlushQueues**, el procesamiento de mensajes se produce de forma asincrónica en el cliente.
  
## <a name="see-also"></a>Ver también



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

