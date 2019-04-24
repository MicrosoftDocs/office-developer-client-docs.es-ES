---
title: Proveedor de transporte y modelo operativo de administrador de trabajos en cola MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356612"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Proveedor de transporte y modelo operativo de administrador de trabajos en cola MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La inicialización, el inicio, el procesamiento, el apagado y la desinicialización del proveedor de transporte se realizan mediante una serie de llamadas de la cola MAPI al proveedor de transporte. Las llamadas se ordenan de la siguiente manera:
  
1. La cola MAPI llama a la función [XPProviderInit](xpproviderinit.md) , pasa un objeto de soporte, obtiene el objeto de proveedor y comprueba que el proveedor de transporte y la cola MAPI admiten un intervalo de números de versión MAPI compatible. 
    
2. La cola MAPI llama al método [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) de la interfaz [IXPProvider: IUnknown](ixpprovideriunknown.md) . Se establece una sesión entre la cola MAPI y el proveedor de transporte con las credenciales de la sección actual del perfil. El proveedor de transporte devuelve un objeto de inicio de sesión. 
    
3. La cola MAPI llama al método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) . El proveedor de transporte devuelve una lista de los identificadores únicos (UID) y los tipos de direcciones de correo electrónico que aceptará. 
    
4. El proveedor de transporte llama al método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) para crear su fila en la tabla de estado de MAPI. 
    
5. La cola MAPI llama al método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) para habilitar la transmisión y recepción de mensajes. 
    
6. Si el proveedor de transporte lo solicita en su devolución para la llamada **TransportLogon** , la cola MAPI llama periódicamente al método [IXPLogon:: idle](ixplogon-idle.md) . El procesamiento en inActividad es útil si el proveedor de transporte debe sondear el sistema de mensajería subyacente en busca de nuevos mensajes o realizar otras tareas de baja prioridad. 
    
7. La cola MAPI y el proveedor de transporte envían y reciben mensajes. Para obtener más información, vea [modelo de envío de mensajes](message-submission-model.md) y modelo de recepción de [mensajes](message-reception-model.md). Los servicios de cola MAPI transportan solicitudes de transporte y llamadas en objetos de soporte, mensajes y datos adjuntos.
    
8. La cola MAPI llama al método **TransportNotify** para deshabilitar la transmisión y recepción de mensajes. 
    
9. La cola MAPI libera los objetos de inicio de sesión y proveedor. Para obtener más información, vea el método [IXPProvider:: Shutdown](ixpprovider-shutdown.md) . 
    

