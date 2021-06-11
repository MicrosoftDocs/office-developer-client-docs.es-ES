---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432607"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Fuerza a que todos los mensajes que esperan ser enviados o recibidos se carguen o descarguen inmediatamente. El objeto de estado de cola MAPI y los objetos de estado que los proveedores de transporte implementan admiten este método.
  
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
  
> [in] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método.
    
 _cbTargetTransport_
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpTargetTransport._ El  _parámetro cbTargetTransport_ solo se establece en llamadas al objeto de estado de la cola MAPI. Para las llamadas a un proveedor de transporte, el  _parámetro cbTargetTransport_ se establece en 0. 
    
 _lpTargetTransport_
  
> [in] Puntero al identificador de entrada del proveedor de transporte que va a vaciar sus colas de mensajes. El  _parámetro lpTargetTransport_ solo se establece en llamadas al objeto de estado de la cola MAPI. Para las llamadas a un proveedor de transporte, el  _parámetro lpTargetTransport_ se establece en NULL. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla la operación de vaciado. Se pueden establecer las siguientes marcas:
    
FLUSH_ASYNC_OK 
  
> La operación de vaciado puede producirse de forma asincrónica. Esta marca solo se aplica al objeto de estado de la cola MAPI. 
    
FLUSH_DOWNLOAD 
  
> Las colas de mensajes entrantes deben vaciarse.
    
FLUSH_FORCE 
  
> La operación de vaciado debe producirse independientemente, a pesar de la posibilidad de una disminución del rendimiento. Esta marca debe establecerse cuando se tiene como destino un proveedor de transporte asincrónico.
    
FLUSH_NO_UI 
  
> El objeto status no debe mostrar un indicador de progreso.
    
FLUSH_UPLOAD 
  
> Las colas de mensajes salientes deben vaciarse.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de vaciado se ha realizado correctamente.
    
MAPI_E_BUSY 
  
> Hay otra operación en curso; debe poder completarse, o debe detenerse, antes de que se pueda iniciar esta operación.
    
MAPI_E_NO_SUPPORT 
  
> El objeto status no admite esta operación, como se indica por la ausencia de la marca STATUS_FLUSH_QUEUES en la propiedad PR_RESOURCE_METHODS **(** [PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del objeto de estado.
    
## <a name="remarks"></a>Comentarios

El **método IMAPIStatus::FlushQueues** solicita que la cola MAPI o un proveedor de transporte envíen inmediatamente todos los mensajes de la cola saliente o reciban todos los mensajes de la cola entrante. **FlushQueues** solo se implementa mediante el objeto de estado de la cola MAPI y los objetos de estado que suministran los proveedores de transporte. 
  
MAPI_E_BUSY deben devolverse para las solicitudes asincrónicas para que los clientes puedan continuar trabajando. 
  
De forma predeterminada, **FlushQueues** es una operación sincrónica; el control no vuelve al autor de la llamada hasta que se haya completado el vaciado. Solo la operación de vaciado realizada por la cola MAPI puede ser asincrónica; los clientes solicitan este comportamiento estableciendo FLUSH_ASYNC_OK marca. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La implementación de **FlushQueues** de un proveedor de transporte remoto establece bits en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la fila de estado del objeto de inicio de sesión para controlar cómo se vacían las colas. Si un visor remoto pasa la marca FLUSH_UPLOAD, el método **FlushQueues** debe establecer los STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE bits. Si un visor remoto pasa la marca FLUSH_DOWNLOAD, el método **FlushQueues** debe establecer los STATUS_OUTBOUND_ENABLED y STATUS_OUTBOUND_ACTIVE bits. **FlushQueues** debe devolver S_OK. A continuación, la cola MAPI iniciará las acciones adecuadas para cargar y descargar mensajes. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Una llamada al objeto de estado de cola MAPI es una directiva para transferir todos los mensajes al proveedor de transporte adecuado o desde él. Cuando se llama al objeto de estado de un proveedor de transporte individual, solo se ven afectados los mensajes de ese proveedor.
  
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[Propiedad canónica PidTagStatusCode](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

