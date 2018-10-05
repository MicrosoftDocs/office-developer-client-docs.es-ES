---
title: Propiedad canónica PidTagDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2bf862317ca1d2f2a09a71e1af62b82661b33326
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383852"
---
# <a name="pidtagdisplaycc-canonical-property"></a>Propiedad canónica PidTagDisplayCc

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de ASCII de los nombres para mostrar de los destinatarios del mensaje con copia (CC), separados por punto y coma (;). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W  <br/> |
|Identificador:  <br/> |0x0E03  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Comentarios

El almacén de mensajes calcula estas propiedades en los objetos de mensaje con el método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . El almacén de mensajes también mantiene estas propiedades para que siempre refleja el último estado guardado de un mensaje. El valor se sincroniza en el momento de todas las llamadas a [IMAPIProp::SaveChanges](imapiprop-savechanges.md). 
  
Si un mensaje no tiene ningún destinatarios en copia oculta, el almacén de mensajes debe responder a una llamada [IMAPIProp::GetProps](imapiprop-getprops.md) con un valor devuelto de S_OK y una cadena vacía para estas propiedades. 
  
Debido a la necesidad de posible para la localización, MAPI proporciona estas instrucciones para todos los nombres de los destinatarios:
  
- Todos los nombres de deberían poder ser localizada. 
    
- El punto y coma debe ser el carácter que se usa para separar los nombres en las propiedades de **PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC**y **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)). Punto y coma no se permite dentro de nombres de los destinatarios en MAPI. 
    
- Los clientes deben traducir cada punto y coma detectado en esta propiedad para un carácter de separador localizadas antes de realizar la información de la propiedad visible en la interfaz de usuario. 
    
- Cuando el reenvío de mensajes, no es necesario traducir los caracteres de separador en la línea de destinatarios con copia oculta los clientes. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

