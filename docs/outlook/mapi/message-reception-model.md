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
  
El proveedor de transporte controla si la cola MAPI debe sondearla para el correo entrante o si realiza una devolución de llamada a la cola MAPI cuando llega correo nuevo. El proveedor de transporte establece la marca SP_LOGON_POLL cuando vuelve de [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) para solicitar el sondeo. De lo contrario, el proveedor de transporte usa [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) cuando el correo entrante está disponible. Una vez que se ha familiarizado con el correo entrante disponible, la cola MAPI abre un nuevo mensaje y pide al proveedor de transporte que almacene las propiedades del mensaje recibido en el mensaje. 
  
Este proceso funciona de la siguiente manera:
  
1. Los mensajes disponibles los indica el proveedor de transporte que llama a **IMAPISupport:: SpoolerNotify** o por el administrador de trabajos en cola MAPI llamando a [IXPLogon::P Oll](ixplogon-poll.md).
    
2. La cola MAPI llama a [IXPLogon:: StartMessage](ixplogon-startmessage.md) para iniciar el proceso. 
    
3. El proveedor de transporte coloca un valor de referencia en la ubicación a la que se hace referencia en **StartMessage**. Estos valores de referencia permiten al proveedor de transporte y a la cola MAPI realizar un seguimiento del mensaje que se está procesando cuando hay varios mensajes que entregar.
    
4. El proveedor de transporte almacena los datos del mensaje en la instancia de [IMessage: IMAPIProp](imessageimapiprop.md) pasada. 
    
5. El proveedor de transporte llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) en la instancia **IMessage** y vuelve de **StartMessage**.
    
6. La cola MAPI llama a [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) si debe detener la entrega de mensajes. 
    
> [!NOTE]
> Si un proveedor de transporte debe entregar un gran número de mensajes y el proveedor de transporte usa **IMAPISupport:: SpoolerNotify** en lugar de **IXPLogon::P Oll**, debe tenerse cuidado de no llamar a **SpoolerNotify** con demasiada frecuencia para privar a otros proveedores de transporte de tiempo de CPU. La cola MAPI tiene lógica para evitar que esto suceda, pero, en general, el intervalo entre llamadas **SpoolerNotify** debe ser mayor que el tiempo que tarda el proveedor de transporte en procesar un mensaje. > también puede que la cola MAPI no procese un mensaje entrante inmediatamente. La cola MAPI puede pedir al proveedor de transporte que realice otras tareas antes de recibir el mensaje entrante. 
  

