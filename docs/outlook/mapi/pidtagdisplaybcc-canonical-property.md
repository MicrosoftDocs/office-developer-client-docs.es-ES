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
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360819"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>Propiedad canónica PidTagDisplayBcc

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista ASCII de los nombres para mostrar de los destinatarios del mensaje de copia oculta (CCO), separados por punto y coma (;).
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W  <br/> |
|Identificador:  <br/> |0x0E02  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

El almacén de mensajes calcula estas propiedades en objetos de mensaje mediante el método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) . El almacén de mensajes también mantiene estas propiedades para que siempre refleje el último estado guardado de un mensaje. El valor se sincroniza en el momento de cada llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
  
Si un mensaje no tiene destinatarios ocultos de copia, el almacén de mensajes debe responder a una llamada de [IMAPIProp:: GetProps](imapiprop-getprops.md) con un valor devuelto de S_OK y una cadena vacía para **PR_DISPLAY_BCC**. 
  
Debido a la posible necesidad de localización, MAPI proporciona estas directrices para todos los nombres de los destinatarios:
  
- Todos los nombres deben poder localizarse. 
    
- El punto y coma debe ser el carácter que se usa para separar los nombres en las propiedades **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) y **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). No se permiten signos de punto y coma en los nombres de los destinatarios en MAPI. 
    
- Los clientes deben traducir cada punto y coma encontrado en esta propiedad a un carácter separador localizado antes de hacer visible la información de propiedad en la interfaz de usuario. 
    
- Al reenviar mensajes, no es necesario que los clientes traduzcan los caracteres separadores de la línea de destinatarios con copia oculta. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Describe el formato de los mensajes usados para enviar información relacionada con carpetas de uso compartido en el cliente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

