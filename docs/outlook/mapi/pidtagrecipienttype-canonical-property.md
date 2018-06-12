---
title: Propiedad canónico PidTagRecipientType
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0218ff558e9dfca2f73bbad2dc42cdb7bd7121fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820071"
---
# <a name="pidtagrecipienttype-canonical-property"></a>Propiedad canónico PidTagRecipientType

  
  
**Se aplica a**: Outlook 
  
Contiene el tipo de destinatario para un destinatario del mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Identificador:  <br/> |0x0C15  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatario MAPI  <br/> |
   
## <a name="remarks"></a>Notas

El tipo de destinatario contenido en esta propiedad consta de un valor requerido y un indicador opcional.
  
Esta propiedad debe contener exactamente uno de los siguientes valores:
  
MAPI_TO 
  
> El destinatario es un servidor principal (a) del destinatario. Los clientes son necesarios para administrar a destinatarios principales. Todos los dem�s tipos son opcionales.
    
MAPI_CC 
  
> El destinatario es un destinatario de copia (CC), un destinatario que recibe un mensaje además de los destinatarios principales.
    
MAPI_BCC 
  
> El destinatario es un destinatario de copia oculta (CCO). Destinatarios principales y de copia oculta son conscientes de la existencia de destinatarios CCO. 
    
MAPI_P1 
  
> El destinatario no recibió correctamente el mensaje en el intento anterior. Se trata de un nuevo envío de una transmisión anterior.
    
Además, se puede establecer la marca siguiente:
  
MAPI_SUBMITTED 
  
> El destinatario ya ha recibido el mensaje y no es necesario que volverá a aparecer. Se trata de un nuevo envío de una transmisión anterior. Este indicador se establece en junto con los valores **MAPI_TO**, **MAPI_CC**y **MAPI_BCC** . 
    
El valor de MAPI_P1 y el indicador **MAPI_SUBMITTED** se usa cuando un mensaje es que se retransmite debido a no entrega a uno o varios de los destinatarios. Para esta retransmisión, el cliente establece **MAPI_SUBMITTED** en todos los destinatarios que no es necesario volver al mensaje pero que deben mostrarse en la lista de destinatarios. Para cada destinatario que no ha recibido el mensaje anteriormente, el cliente conserva el destinatario original con su valor **PR_RECIPIENT_TYPE** sin cambios, pero además envía una copia del destinatario con MAPI_P1 en lugar del valor original. Esta copia, que se descarta antes de la entrega real, fuerza al destinatario en el sobre P1 y garantiza la retransmisión físico a ese destinatario. La propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) se establece en FALSE para los destinatarios MAPI_P1.
  
Cuando un cliente, muestra un formulario de volver a enviar, sólo a los destinatarios MAPI_P1 están visibles. A menos que el usuario escribe a los destinatarios adicionales, cuando el mensaje se entrega, la lista de destinatarios aparece exactamente igual que cuando se envió el mensaje por primera vez. 
  
El **PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) y las propiedades de **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) están relacionados con tipo de destinatario. Cuando un cliente llama a **IMAPIProp::SaveChanges un mensaje** y hay al menos un destinatario en la lista de destinatarios, el proveedor de almacén de mensajes establece estas propiedades como se indica a continuación: 
  
|**Propiedad**|**Descripción**|
|:-----|:-----|
|PR_DISPLAY_TO DE MAPI  <br/> |Se establece en TRUE si uno o varios de los destinatarios son **MAPI_TO** destinatarios.  <br/> |
|PR_DISPLAY_CC  <br/> |Se establece en TRUE si uno o varios de los destinatarios son **MAPI_CC** destinatarios.  <br/> |
| PR_DISPLAY_BCC  <br/> |Se establece en TRUE si uno o varios de los destinatarios son destinatarios **MAPI_BCC** .  <br/> |
   
En X.400, el contenedor de entrega o P1 es la información necesaria para enviar un mensaje, incluidas las propiedades de la dirección del destinatario y los indicadores de opciones de control de entrega y respuestas. El contenedor de P2 o para mostrar es la información suele mostrarse para cada destinatario que no sea el texto del mensaje. Normalmente incluye el asunto, importancia, prioridad, confidencialidad y el tiempo de envío, así como los nombres de los destinatarios principales y copiados. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Ver también



[Propiedad canónico PidTagRecipientStatus](pidtagrecipientstatus-canonical-property.md)
  
[Propiedad canónico PidTagDisplayTo](pidtagdisplayto-canonical-property.md)
  
[Propiedad canónico PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)
  
[Propiedad canónico PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI para nombres canónicos (propiedad)](mapping-mapi-names-to-canonical-property-names.md)

