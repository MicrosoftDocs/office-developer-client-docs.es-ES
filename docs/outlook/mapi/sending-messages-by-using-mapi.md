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
ms.openlocfilehash: 6a3172dcd962c04d72aacd14d2e42990fb0f78c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593455"
---
# <a name="sending-messages-by-using-mapi"></a>Enviar mensajes con MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente de llaman al método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar un mensaje. **SubmitMessage** llama a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para guardar el mensaje antes de transferir el control a cualquiera la cola MAPI o directamente a un proveedor de transporte. 
  
La cola MAPI recibe el mensaje si se produce alguna de las siguientes opciones:
  
- El proveedor de almacén de mensajes y el proveedor de transporte no están íntimamente relacionadas.
    
- El mensaje requiere preprocesamiento.
    
- El almacén de mensajes acoplado y el transporte no pueden controlar todos los destinatarios a quienes se envía el mensaje.
    
Un almacén de mensajes acoplado debe tener en cuenta el estado de un mensaje antes de que presenta a la cola MAPI para descargarse a un proveedor de transporte. Hay situaciones en las que es posible que aparezca un mensaje requerir a la cola MAPI, pero la cola MAPI debe realmente no participar.
  
Por ejemplo, considere la situación donde un usuario envía un mensaje de la Bandeja de entrada. El cliente está usando un almacén acoplado y transporte. Si el almacén de mensajes acoplado usa ubicación del mensaje como el único criterio para que decidir sobre si deben o no permitir a la cola MAPI administrar el mensaje, la cola MAPI siempre recibirán el mensaje. Para evitar este tipo de problema, un almacén de mensajes acoplado debe comprobar el estado del mensaje además de la ubicación del mensaje. En concreto, el proveedor de transporte no debería solicitar que la cola MAPI descargar los mensajes que se envían de forma activa.
  
El proceso de transmisión de mensajes implica el proveedor de almacenamiento de mensajes, uno o varios proveedores de transporte y MAPI. En los temas de esta sección proporcionan información detallada acerca de las funciones específicas en el proceso de transmisión de mensajes.
  
## <a name="see-also"></a>Recursos adicionales



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

