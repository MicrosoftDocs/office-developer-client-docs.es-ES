---
title: Proveedor de transporte y modelo operativo de cola MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426628"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Proveedor de transporte y modelo operativo de cola MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La inicialización, el inicio, el procesamiento, el apagado y la deserialización del proveedor de transporte se logran mediante una serie de llamadas desde la cola MAPI al proveedor de transporte. Las llamadas se secuencian de la siguiente manera:
  
1. La cola MAPI llama a la función [XPProviderInit,](xpproviderinit.md) pasa un objeto de compatibilidad, obtiene el objeto de proveedor y comprueba que el proveedor de transporte y la cola MAPI admiten un intervalo compatible de números de versión MAPI. 
    
2. La cola MAPI llama al método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) de la [interfaz IXPProvider : IUnknown.](ixpprovideriunknown.md) Se establece una sesión entre la cola MAPI y el proveedor de transporte con las credenciales de la sección actual del perfil. El proveedor de transporte devuelve un objeto de inicio de sesión. 
    
3. La cola MAPI llama al método [IXPLogon::AddressTypes.](ixplogon-addresstypes.md) El proveedor de transporte devuelve una lista de los identificadores únicos (UID) y los tipos de direcciones de correo electrónico que aceptará. 
    
4. El proveedor de transporte llama al [método IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para crear su fila en la tabla de estado MAPI. 
    
5. La cola MAPI llama al método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) para habilitar la transmisión y recepción de mensajes. 
    
6. Si el proveedor de transporte lo solicita en su devolución para la llamada **TransportLogon,** la cola MAPI llama periódicamente al método [IXPLogon::Idle.](ixplogon-idle.md) El procesamiento inactivo es útil si el proveedor de transporte necesita sondear el sistema de mensajería subyacente para buscar mensajes nuevos o realizar otras tareas de prioridad baja. 
    
7. La cola MAPI y el proveedor de transporte envían y reciben mensajes. Para obtener más información, vea [El modelo de envío de mensajes y](message-submission-model.md) el modelo de recepción de [mensajes.](message-reception-model.md) Las solicitudes de transporte de servicios de cola MAPI y las llamadas en los objetos de soporte técnico, mensaje y datos adjuntos.
    
8. La cola MAPI llama al **método TransportNotify** para deshabilitar la transmisión y recepción de mensajes. 
    
9. La cola MAPI libera los objetos de inicio de sesión y proveedor. Para obtener más información, consulta el [método IXPProvider::Shutdown.](ixpprovider-shutdown.md) 
    

