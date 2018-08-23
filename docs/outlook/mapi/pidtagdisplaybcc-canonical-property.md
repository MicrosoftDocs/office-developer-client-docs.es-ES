---
title: Propiedad canónica PidTagDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cd37d72d6a214f91e371b7126c90e3fda25cde2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578902"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>Propiedad canónica PidTagDisplayBcc

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de ASCII de los nombres para mostrar de los destinatarios del mensaje de copia oculta (CCO), separados por punto y coma (;).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W  <br/> |
|Identificador:  <br/> |0x0E02  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Comentarios

El almacén de mensajes calcula estas propiedades en los objetos de mensaje con el método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . El almacén de mensajes también mantiene estas propiedades para que siempre refleja el último estado guardado de un mensaje. El valor se sincroniza en el momento de todas las llamadas al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
Si un mensaje no tiene ningún destinatarios en copia oculta, el almacén de mensajes debe responder a una llamada [IMAPIProp::GetProps](imapiprop-getprops.md) con un valor devuelto de S_OK y una cadena vacía para **PR_DISPLAY_BCC**. 
  
Debido a la necesidad de posible para la localización, MAPI proporciona estas instrucciones para todos los nombres de los destinatarios:
  
- Todos los nombres de deberían poder ser localizada. 
    
- El punto y coma debe ser el carácter que se usa para separar los nombres en el **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) y las propiedades **PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Punto y coma no se permite dentro de nombres de los destinatarios en MAPI. 
    
- Los clientes deben traducir cada punto y coma detectado en esta propiedad para un carácter de separador localizadas antes de realizar la información de la propiedad visible en la interfaz de usuario. 
    
- Cuando el reenvío de mensajes, no es necesario traducir los caracteres de separador en la línea de destinatarios con copia oculta los clientes. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Describe el formato de los mensajes que se utiliza para enviar información relacionada con el uso compartido de carpetas en el cliente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

