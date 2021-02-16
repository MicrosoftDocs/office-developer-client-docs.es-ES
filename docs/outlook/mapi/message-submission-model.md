---
title: Modelo de envío de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421126"
---
# <a name="message-submission-model"></a>Modelo de envío de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El envío de mensajes se realiza mediante una serie de llamadas desde la cola MAPI al proveedor de transporte. Las llamadas se secuencian de la siguiente manera:
  
1. La cola MAPI llama a [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), pasando una [instancia de IMessage : IMAPIProp,](imessageimapiprop.md) para iniciar el proceso. 
    
2. A continuación, el proveedor de transporte coloca un valor de referencia (un identificador definido por el transporte usado en futuras referencias a este mensaje) en la ubicación a la que se hace referencia en **SubmitMessage**.
    
3. El proveedor de transporte tiene acceso a los datos del mensaje mediante la instancia **de IMessage** pasada. Para cada destinatario en el **IMessage** pasado para el que acepta responsabilidad, el proveedor de transporte establece la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) y, a continuación, devuelve.
    
4. El proveedor de transporte puede usar el método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar si reconoce algún destinatario al que no se puede entregar o para crear un informe de entrega estándar. **StatusRecips** es una comodidad para los proveedores de transporte que han determinado que algunos de los destinatarios no se pueden entregar o que han recibido información de entrega de su sistema de mensajería subyacente que el usuario o la aplicación cliente pueden encontrar útiles. 
    
5. La llamada de la cola MAPI a [IXPLogon::EndMessage](ixplogon-endmessage.md) es la entrega de responsabilidad final del mensaje de la cola MAPI al proveedor de transporte. 
    
6. La cola MAPI puede usar [IXPLogon::TransportNotify para](ixplogon-transportnotify.md) cancelar el procesamiento de mensajes durante las llamadas **SubmitMessage** o **EndMessage.** 
    

