---
title: Envío de mensajes mediante MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438725"
---
# <a name="sending-messages-by-using-mapi"></a>Envío de mensajes mediante MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente llaman al [método IMessage::SubmitMessage](imessage-submitmessage.md) para enviar un mensaje. **SubmitMessage** llama [a IMAPIProp::SaveChanges](imapiprop-savechanges.md) para guardar el mensaje antes de transferir el control a la cola MAPI o directamente a un proveedor de transporte. 
  
La cola MAPI recibe el mensaje si se produce alguna de las siguientes situaciones:
  
- El proveedor de almacenamiento de mensajes y el proveedor de transporte no están estrechamente acoplados.
    
- El mensaje requiere preprocesamiento.
    
- El almacenamiento y el transporte de mensajes estrechamente acoplados no pueden controlar todos los destinatarios a los que se dirige el mensaje.
    
Un almacén de mensajes estrechamente acoplado debe tener en cuenta el estado de un mensaje antes de presentarlo en la cola MAPI para que se descargue a un proveedor de transporte. Hay situaciones en las que puede parecer que un mensaje requiere la cola MAPI, pero la cola MAPI realmente no debería estar implicada.
  
Por ejemplo, considere la situación en la que un usuario envía un mensaje desde la Bandeja de entrada. El cliente usa un almacenamiento y transporte estrechamente acoplados. Si el almacén de mensajes estrechamente acoplado usa la ubicación del mensaje como único criterio para decidir si se va a permitir que la cola MAPI controle el mensaje, la cola MAPI siempre recibirá el mensaje. Para evitar este tipo de problema, un almacén de mensajes estrechamente acoplado debe comprobar el estado del mensaje además de la ubicación del mensaje. En concreto, el proveedor de transporte no debe solicitar que la cola MAPI descargue ningún mensaje enviado activamente.
  
El proceso de transmisión de mensajes implica el proveedor de almacenamiento de mensajes, uno o más proveedores de transporte y MAPI. Los temas de esta sección proporcionan información detallada sobre roles específicos en el proceso de transmisión de mensajes.
  
## <a name="see-also"></a>Consulte también



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

