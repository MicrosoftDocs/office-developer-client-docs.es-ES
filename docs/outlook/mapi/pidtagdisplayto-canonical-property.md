---
title: Propiedad canónica PidTagDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0c7ae8951b02f099161871b17ff59ea23f8fbcc4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396046"
---
# <a name="pidtagdisplayto-canonical-property"></a>Propiedad canónica PidTagDisplayTo

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de los nombres para mostrar de la principal (a) de los destinatarios del mensaje, separados por punto y coma (;). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISPLAY_TO DE MAPI, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W  <br/> |
|Identificador:  <br/> |0x0E04  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Comentarios

El almacén de mensajes calcula estas propiedades en los objetos de mensaje con el método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . El almacén de mensajes también mantiene estas propiedades para que siempre refleja el último estado guardado de un mensaje. El valor se sincroniza en el momento de todas las llamadas al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
Si un mensaje no tiene ningún destinatario principal, el almacén de mensajes debe responder a una llamada [IMAPIProp::GetProps](imapiprop-getprops.md) con un valor devuelto de S_OK y una cadena vacía para **PR_DISPLAY_TO de MAPI**. 
  
Debido a la necesidad de posible para la localización, MAPI proporciona estas instrucciones para todos los nombres de los destinatarios:
  
- Todos los nombres de deberían poder ser localizada. 
    
- El punto y coma debe ser el carácter que se usa para separar los nombres en las propiedades de **PR_DISPLAY_TO de MAPI** , **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) y **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)). Punto y coma no se permite dentro de nombres de los destinatarios en MAPI. 
    
- Los clientes deben traducir cada punto y coma que encontró en el **PR_DISPLAY_TO de MAPI** y las propiedades relacionadas en un carácter separador localizadas antes de realizar la información visible en la interfaz de usuario. 
    
- Cuando el reenvío de mensajes, los clientes no es necesario traducir los caracteres de separador de la línea de destinatario principal. 
    
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

