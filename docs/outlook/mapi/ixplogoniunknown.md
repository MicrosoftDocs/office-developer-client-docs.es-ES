---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432537"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona a la cola MAPI acceso a un proveedor de transporte. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Expuesto por:  <br/> |Objetos de inicio de sesión de transporte  <br/> |
|Implementado por:  <br/> |Proveedores de transporte  <br/> |
|Llamado por:  <br/> |La cola MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IXPLogon  <br/> |
|Tipo de puntero:  <br/> |IXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Devuelve los tipos de destinatarios que controla el proveedor de transporte.  <br/> |
|**RegisterOptions** <br/> | *No se admite ni se documenta.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Indica la ocurrencia de un evento sobre el que el proveedor de transporte solicitó la notificación.  <br/> |
|[Inactivo](ixplogon-idle.md) <br/> |Indica que el sistema está inactivo, lo que permite al proveedor de transporte realizar operaciones de prioridad baja.  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Inicia el proceso de cierre de sesión.  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Indica que la cola MAPI tiene un mensaje para que el proveedor de transporte entregue.  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |Informa al proveedor de transporte de que la cola MAPI completó su procesamiento en un mensaje saliente.  <br/> |
|[Sondeo](ixplogon-poll.md) <br/> |Indica si el proveedor de transporte ha recibido uno o más mensajes entrantes.  <br/> |
|[StartMessage](ixplogon-startmessage.md) <br/> |Inicia la transferencia de un mensaje entrante del proveedor de transporte a la cola MAPI.  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Abre el objeto de estado del proveedor de transporte.  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |Comprueba el estado externo del proveedor de transporte.  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Solicita que el proveedor de transporte entregue inmediatamente todos los mensajes entrantes o salientes pendientes.  <br/> |
   
## <a name="see-also"></a>Consulte también



[Interfaces MAPI](mapi-interfaces.md)

