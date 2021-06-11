---
title: Modelo de recepción de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415120"
---
# <a name="message-reception-model"></a>Modelo de recepción de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El proveedor de transporte controla si la cola MAPI debe sondear para el correo entrante o si realiza una llamada a la cola MAPI cuando llega el nuevo correo. El proveedor de transporte establece la SP_LOGON_POLL cuando devuelve de [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para solicitar el sondeo. De lo contrario, el proveedor de transporte [usa IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) cuando el correo entrante está disponible. Después de saber que el correo entrante está disponible, la cola MAPI abre un nuevo mensaje y pide al proveedor de transporte que almacene las propiedades del mensaje recibido en el mensaje. 
  
Este proceso funciona de la siguiente manera:
  
1. Los mensajes disponibles se indican mediante el proveedor de transporte que llama a **IMAPISupport::SpoolerNotify** o por la cola MAPI que llama a [IXPLogon::P oll](ixplogon-poll.md).
    
2. La cola MAPI llama [a IXPLogon::StartMessage](ixplogon-startmessage.md) para iniciar el proceso. 
    
3. El proveedor de transporte coloca un valor de referencia en la ubicación a la que se hace referencia en **StartMessage**. Estos valores de referencia permiten al proveedor de transporte y a la cola MAPI realizar un seguimiento del mensaje que se está procesando cuando hay varios mensajes que entregar.
    
4. El proveedor de transporte almacena los datos del mensaje en la instancia [IMessage : IMAPIProp](imessageimapiprop.md) pasada. 
    
5. El proveedor de transporte llama al [método IMAPIProp::SaveChanges](imapiprop-savechanges.md) en la instancia **de IMessage** y devuelve desde **StartMessage**.
    
6. La cola MAPI llama [a IXPLogon::TransportNotify](ixplogon-transportnotify.md) si debe detener la entrega de mensajes. 
    
> [!NOTE]
> Si un proveedor de transporte debe entregar un gran número de mensajes y el proveedor de transporte usa **IMAPISupport::SpoolerNotify** en lugar de **IXPLogon::P oll**, debe tenerse cuidado de no llamar a **SpoolerNotify** con demasiada frecuencia para no privar a otros proveedores de transporte de tiempo de CPU. La cola MAPI tiene lógica para evitar que esto suceda, pero en general el intervalo entre las llamadas **SpoolerNotify** debe ser mayor que el tiempo que tarda el proveedor de transporte en procesar un mensaje. >, es posible que la cola MAPI no procese un mensaje entrante inmediatamente. La cola MAPI puede pedir al proveedor de transporte que realice otras tareas antes de recibir el mensaje entrante. 
  

