---
title: Enviar mensajes con MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339756"
---
# <a name="sending-messages-by-using-mapi"></a>Enviar mensajes con MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente llaman al método [IMessage:: SubmitMessage](imessage-submitmessage.md) para enviar un mensaje. **SubmitMessage** llama a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para guardar el mensaje antes de transferir el control a la cola de impresión MAPI o directamente a un proveedor de transporte. 
  
La cola MAPI recibe el mensaje si se produce alguna de las siguientes acciones:
  
- El proveedor de almacenamiento de mensajes y el proveedor de transporte no están estrechamente acoplados.
    
- El mensaje requiere preprocesamiento.
    
- El almacén de mensajes y el transporte estrechamente acoplados no pueden administrar todos los destinatarios a los que se dirige el mensaje.
    
Un almacén de mensajes estrechamente acoplado debe tener en cuenta el estado de un mensaje antes de presentarlo a la cola MAPI que se va a descargar en un proveedor de transporte. Hay situaciones en las que puede parecer que un mensaje requiere la cola MAPI, pero la cola MAPI no debería implicarse realmente.
  
Por ejemplo, considere la situación en la que un usuario envía un mensaje desde la bandeja de entrada. El cliente usa un almacén y transporte estrechamente acoplados. Si el almacén de mensajes muy acoplado usa la ubicación del mensaje como criterio único para decidir si se va a permitir o no que la cola MAPI controle el mensaje, la cola MAPI recibirá siempre el mensaje. Para evitar este tipo de problemas, un almacén de mensajes estrechamente acoplado debe comprobar el estado del mensaje además de la ubicación del mensaje. En concreto, el proveedor de transporte no debe solicitar que la cola MAPI Descargue los mensajes que se envían de forma activa.
  
El proceso de transmisión de mensajes implica el proveedor de almacenamiento de mensajes, uno o varios proveedores de transporte y MAPI. En los temas de esta sección se proporciona información detallada sobre roles específicos en el proceso de transmisión de mensajes.
  
## <a name="see-also"></a>Vea también



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

