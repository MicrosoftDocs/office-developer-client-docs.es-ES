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
ms.openlocfilehash: 30aaaaa250155215149a941da7f7e528d65b8dc3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592202"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obliga a todos los mensajes en espera de ser enviados o recibidos para cargarse o descargarse inmediatamente. El objeto de estado de cola de impresión MAPI y objetos de estado que implementan los proveedores de transporte admiten este método.
  
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
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpTargetTransport_ . El parámetro _cbTargetTransport_ se establece únicamente en las llamadas al objeto de estado de la cola MAPI. Para las llamadas a un proveedor de transporte, el parámetro _cbTargetTransport_ se establece en 0. 
    
 _lpTargetTransport_
  
> [entrada] Un puntero al identificador del proveedor de transporte que se a vaciar las colas de mensajes de entrada. El parámetro _lpTargetTransport_ se establece únicamente en las llamadas al objeto de estado de la cola MAPI. Para las llamadas a un proveedor de transporte, el parámetro _lpTargetTransport_ se establece en NULL. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la operación de vaciado. Se pueden establecer los siguientes indicadores:
    
FLUSH_ASYNC_OK 
  
> La operación de vaciado puede producirse de forma asincrónica. Esta marca sólo se aplica a objetos de estado de la cola MAPI. 
    
FLUSH_DOWNLOAD 
  
> Se deben vaciar las colas de mensajes entrantes.
    
FLUSH_FORCE 
  
> La operación de vaciado debe producirse independientemente de la forma, a pesar de las posibilidades de una disminución del rendimiento. Este indicador se debe establecer cuando el destino es de un proveedor de transporte asincrónico.
    
FLUSH_NO_UI 
  
> El objeto de estado no debe mostrar un indicador de progreso.
    
FLUSH_UPLOAD 
  
> Se deben vaciar las colas de mensajes salientes.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La operación de vaciado fue correcta.
    
MAPI_E_BUSY 
  
> Otra operación está en curso; se debe permitir para llevar a cabo o se debe detener, antes de que se puede iniciar esta operación.
    
MAPI_E_NO_SUPPORT 
  
> El objeto de estado no es compatible con esta operación, tal como se indica por la ausencia de la marca STATUS_FLUSH_QUEUES en propiedad de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) del objeto de estado.
    
## <a name="remarks"></a>Comentarios

El método **IMAPIStatus::FlushQueues** solicita que la cola MAPI o un proveedor de transporte inmediatamente enviar todos los mensajes en la cola de salida o recibir todos los mensajes de la cola entrante. **FlushQueues** se implementa solo por el objeto de estado de cola de impresión MAPI y objetos de estado que suministro de proveedores de transporte. 
  
MAPI_E_BUSY se deben devolver para las solicitudes asincrónicas para que los clientes pueden continuar trabajo. 
  
De forma predeterminada, **FlushQueues** es una operación sincrónica; control no vuelve al autor de la llamada hasta que haya finalizado el vaciado. Sólo la operación de vaciado realizada por la cola MAPI puede ser asincrónica; los clientes solicitan este comportamiento estableciendo el indicador FLUSH_ASYNC_OK. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Implementación del proveedor de transporte remoto de **FlushQueues** establece bits en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) en la fila de estado del objeto de inicio de sesión para controlar cómo se vacían colas. Si un visor remoto pasa el indicador FLUSH_UPLOAD, el método **FlushQueues** debe establecer los bits STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE. Si un visor remoto pasa el indicador FLUSH_DOWNLOAD, el método **FlushQueues** debe establecer los bits STATUS_OUTBOUND_ENABLED y STATUS_OUTBOUND_ACTIVE. **FlushQueues** , a continuación, se debe devolver S_OK. La cola MAPI, a continuación, iniciará las acciones adecuadas para cargar y descargar los mensajes. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Una llamada al objeto de estado de cola de impresión MAPI es una directiva para transferir todos los mensajes a o desde el proveedor de transporte apropiado. Cuando se llama el objeto de estado de un proveedor de transporte individual, sólo los mensajes de ese proveedor se ven afectados.
  
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[Propiedad canónica PidTagStatusCode](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

