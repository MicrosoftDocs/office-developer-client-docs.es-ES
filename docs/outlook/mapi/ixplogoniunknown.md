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
ms.openlocfilehash: 0b16fba054533f1cb5d21f3f4b1788c073eca13b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818028"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Proporciona el acceso a la cola de impresión MAPI a un proveedor de transporte. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Expuestos por:  <br/> |Objetos de inicio de sesión de transporte  <br/> |
|Se implementa mediante:  <br/> |Proveedores de transporte  <br/> |
|Llamado por:  <br/> |La cola MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IXPLogon  <br/> |
|Tipo de puntero:  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Devuelve los tipos de destinatarios que administra el proveedor de transporte.  <br/> |
|**RegisterOptions** <br/> | *No se admiten o documentado.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Indica la aparición de un evento sobre el que el proveedor de transporte solicita la notificación.  <br/> |
|[Inactividad](ixplogon-idle.md) <br/> |Indica que el sistema está inactivo, habilitar el proveedor de transporte realizar operaciones de prioridad baja.  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Inicia el proceso de cierre de sesión.  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Indica que la cola MAPI tiene un mensaje para el proveedor de transporte entregar.  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |Informa al proveedor de transporte que la cola MAPI completó su procesamiento en un mensaje de salida.  <br/> |
|[Sondeo](ixplogon-poll.md) <br/> |Indica si el proveedor de transporte ha recibido uno o más mensajes entrantes.  <br/> |
|[Desea iniciar](ixplogon-startmessage.md) <br/> |Inicia a la transferencia de un mensaje entrante desde el proveedor de transporte a la cola MAPI.  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Se abre el objeto de estado del proveedor de transporte.  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |Comprobaciones de estado externo del proveedor de transporte.  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Solicitudes que el proveedor de transporte entrega inmediatamente todos los mensajes entrantes o salientes pendientes.  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

