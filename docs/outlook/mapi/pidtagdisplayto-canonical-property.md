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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360791"
---
# <a name="pidtagdisplayto-canonical-property"></a>Propiedad canónica PidTagDisplayTo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una lista de los nombres para mostrar de los destinatarios del mensaje principal (Para), separados por punto y coma (;). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W  <br/> |
|Identificador:  <br/> |0x0E04  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

El almacén de mensajes calcula estas propiedades en objetos de mensaje mediante el [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md) El almacén de mensajes también mantiene estas propiedades para que siempre refleje el último estado guardado de un mensaje. El valor se sincroniza en el momento de cada llamada al método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
Si un mensaje no tiene destinatarios principales, el almacén de mensajes debe responder a una llamada [IMAPIProp::GetProps](imapiprop-getprops.md) con un valor devuelto de S_OK y una cadena vacía para **PR_DISPLAY_TO**. 
  
Debido a la posible necesidad de localización, MAPI proporciona estas directrices para todos los nombres de destinatarios:
  
- Todos los nombres deben poder localizarse. 
    
- El punto y coma debe ser el carácter que se usa para separar los nombres de las propiedades **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) **y PR_DISPLAY_TO** datos. No se permiten puntos y comas dentro de los nombres de destinatario en MAPI. 
    
- Los clientes deben traducir cada punto y coma encontrado en el **PR_DISPLAY_TO** y las propiedades relacionadas a un carácter separador localizado antes de hacer que la información sea visible en la interfaz de usuario. 
    
- Al reenviar mensajes, los clientes no necesitan traducir los caracteres separadores en la línea de destinatario principal. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

