---
title: Modelo de envío de mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 653a9df6ec414aa18c44d8035a59f021d7cc19b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818408"
---
# <a name="message-submission-model"></a>Modelo de envío de mensaje

  
  
**Se aplica a**: Outlook 
  
Envío de mensajes se realiza mediante una serie de llamadas desde la cola de MAPI para el proveedor de transporte. Las llamadas se ordenan de la siguiente manera:
  
1. La cola MAPI llama a [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), pasando un [IMessage: IMAPIProp](imessageimapiprop.md) una instancia para comenzar el proceso. 
    
2. El proveedor de transporte, a continuación, coloca un valor de referencia: un identificador definido por el transporte en futuro usa referencias a este mensaje, en la ubicación que se hace referencia en **SubmitMessage**.
    
3. El proveedor de transporte tiene acceso a los datos del mensaje mediante el uso de la instancia que se pase **IMessage** . Para cada destinatario en el pasado **IMessage** para la que acepta responsabilidad, el proveedor de transporte establece la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) y, a continuación, se devuelve.
    
4. El proveedor de transporte puede usar el método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar si reconoce todos los destinatarios que no se puede entregar a, o para crear un informe de entrega estándar. **StatusRecips** es una comodidad para los proveedores de transporte que ha determinado que algunos de los destinatarios no se puede entregar a o que han recibido la información de entrega de su sistema de mensajería subyacente que es posible que la aplicación cliente o de usuario encontrar útil. 
    
5. Llamada de la cola MAPI a [IXPLogon::EndMessage](ixplogon-endmessage.md) es la entregue responsabilidad final para el mensaje de la cola de MAPI para el proveedor de transporte. 
    
6. La cola MAPI puede usar [IXPLogon::TransportNotify](ixplogon-transportnotify.md) para cancelar el mensaje de procesamiento durante las llamadas a **SubmitMessage** o **EndMessage** . 
    

