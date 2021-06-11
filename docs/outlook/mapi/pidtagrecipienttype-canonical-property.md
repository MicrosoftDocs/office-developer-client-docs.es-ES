---
title: Propiedad canónica PidTagRecipientType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355261"
---
# <a name="pidtagrecipienttype-canonical-property"></a>Propiedad canónica PidTagRecipientType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el tipo de destinatario de un destinatario de mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Identificador:  <br/> |0x0C15  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatario MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

El tipo de destinatario contenido en esta propiedad consta de un valor obligatorio y una marca opcional.
  
Esta propiedad debe contener exactamente uno de los siguientes valores:
  
MAPI_TO 
  
> El destinatario es un destinatario principal (Para). Los clientes son necesarios para controlar los destinatarios principales. Todos los dem�s tipos son opcionales.
    
MAPI_CC 
  
> El destinatario es un destinatario de copia de carbono (CC), un destinatario que recibe un mensaje además de los destinatarios principales.
    
MAPI_BCC 
  
> El destinatario es un destinatario de copia de carbono ciego (CCO). Los destinatarios principales y de copia de carbono no son conscientes de la existencia de destinatarios CCO. 
    
MAPI_P1 
  
> El destinatario no recibió correctamente el mensaje en el intento anterior. Se trata de un nuevo envío de una transmisión anterior.
    
Además, se puede establecer la siguiente marca:
  
MAPI_SUBMITTED 
  
> El destinatario ya ha recibido el mensaje y no necesita volver a recibirlo. Se trata de un nuevo envío de una transmisión anterior. Esta marca se establece junto con los **MAPI_TO**, **MAPI_CC** y **MAPI_BCC** valores. 
    
El MAPI_P1 y la marca **MAPI_SUBMITTED** se usan cuando se retransmite un mensaje debido a que no se entrega a uno o varios de los destinatarios previstos. Para esta retransmisión, el  cliente establece MAPI_SUBMITTED en todos los destinatarios que no necesitan el mensaje de nuevo, pero que deben mostrarse en la lista de destinatarios. Para todos los destinatarios que no recibieron el mensaje anteriormente, el cliente conserva el destinatario original con su valor **PR_RECIPIENT_TYPE** sin cambios, pero además envía una copia del destinatario con MAPI_P1 en lugar del valor original. Esta copia, que se descarta antes de la entrega real, fuerza al destinatario en el sobre P1 y garantiza la retransmisión física a ese destinatario. La **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) se establece en FALSE para MAPI_P1 destinatarios.
  
Cuando un cliente muestra un formulario de reenmiende, solo están visibles MAPI_P1 destinatarios. A menos que el usuario escriba destinatarios adicionales, cuando se entregue el mensaje, la lista de destinatarios aparecerá exactamente igual que cuando se envió el mensaje por primera vez. 
  
Las **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) y **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) están relacionadas con el tipo de destinatario. Cuando un cliente llama a **IMAPIProp::SaveChanges** de un mensaje y hay al menos un destinatario en la lista de destinatarios, el proveedor del almacén de mensajes establece estas propiedades de la siguiente manera: 
  
|**Propiedad**|**Descripción**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |Se establece en TRUE si uno o varios de los destinatarios son **MAPI_TO** destinatarios.  <br/> |
|PR_DISPLAY_CC  <br/> |Se establece en TRUE si uno o varios de los destinatarios son **MAPI_CC** destinatarios.  <br/> |
| PR_DISPLAY_BCC  <br/> |Se establece en TRUE si uno o varios de los destinatarios son **MAPI_BCC** destinatarios.  <br/> |
   
En X.400, el sobre de entrega o P1 es la información necesaria para entregar un mensaje, incluidas las propiedades de dirección del destinatario y las marcas de opción que controlan la entrega y las respuestas. El sobre para mostrar o P2 es la información que normalmente se muestra a cada destinatario que no sea el propio texto del mensaje. Normalmente incluye el asunto, la importancia, la prioridad, la confidencialidad y el tiempo de envío, así como los nombres de destinatarios principales y copiados. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagRecipientStatus](pidtagrecipientstatus-canonical-property.md)
  
[Propiedad canónica PidTagDisplayTo](pidtagdisplayto-canonical-property.md)
  
[Propiedad canónica PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)
  
[Propiedad canónica PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

