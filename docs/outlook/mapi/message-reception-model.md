---
title: Modelo de recepción del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cecdb2c30d6c9df2aafbeed43714269b863ebc48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19818388"
---
# <a name="message-reception-model"></a>Modelo de recepción del mensaje

  
  
**Hace referencia a**: Outlook 
  
El proveedor de transporte controla si la cola MAPI debe sondear de para el correo entrante o si realiza una devolución de llamada a la cola MAPI cuando llegue correo nuevo. El proveedor de transporte establece la marca SP_LOGON_POLL cuando se devuelve desde [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para solicitar el sondeo. De lo contrario, el proveedor de transporte usa [SpoolerNotify](imapisupport-spoolernotify.md) cuando el correo entrante está disponible. Después de que el correo entrante está disponible de aprendizaje, la cola MAPI abre un nuevo mensaje y solicita el proveedor de transporte para almacenar las propiedades del mensaje recibido en el mensaje. 
  
Este proceso funciona de la siguiente manera:
  
1. Mensajes disponibles se indican por el proveedor de transporte de llamada **SpoolerNotify** o por la cola MAPI al llamar a [IXPLogon::Poll](ixplogon-poll.md).
    
2. La cola MAPI llama a [IXPLogon::StartMessage](ixplogon-startmessage.md) para iniciar el proceso. 
    
3. El proveedor de transporte, coloca un valor de referencia en la ubicación que se hace referencia en **desea iniciar**. Estos valores de referencia permitir que el proveedor de transporte y la cola de MAPI para realizar un seguimiento de mensaje que se está procesando cuando hay varios mensajes para entregar.
    
4. El proveedor de transporte almacena los datos del mensaje en el pasado [IMessage: IMAPIProp](imessageimapiprop.md) instancia. 
    
5. El proveedor de transporte llama al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en la instancia de **IMessage** y se devuelve desde **desea iniciar**.
    
6. La cola MAPI llama a [IXPLogon::TransportNotify](ixplogon-transportnotify.md) si debe detener la entrega de mensajes. 
    
> [!NOTE]
> Si un proveedor de transporte debe entregar a un gran número de mensajes y el proveedor de transporte está usando **SpoolerNotify** en lugar de **IXPLogon::Poll**, debe tener cuidado no para llamar a **SpoolerNotify** demasiado con frecuencia en orden para no PRIVARLE otros proveedores de transporte de tiempo de CPU. La cola MAPI tienen lógica para evitar que esto ocurra, pero en general, el intervalo entre llamadas **SpoolerNotify** debe ser mayor que el tiempo que tarda el proveedor de transporte para procesar un mensaje. > También, la cola MAPI no puede procesar un mensaje entrante inmediatamente. La cola MAPI puede pedir el proveedor de transporte para llevar a cabo otras tareas antes de que recibe el mensaje entrante. 
  

