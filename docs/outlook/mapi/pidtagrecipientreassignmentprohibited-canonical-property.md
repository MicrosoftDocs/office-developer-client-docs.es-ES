---
title: Propiedad canónica PidTagRecipientReassignmentProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0176485ca9b84260176e3be8ec9c8f42cf755cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820045"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>Propiedad canónica PidTagRecipientReassignmentProhibited

  
  
**Hace referencia a**: Outlook 
  
Especifica si agregar destinatarios adicionales, al reenviar el mensaje, está prohibido para el mensaje de correo electrónico.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Identificador:  <br/> |0x002B  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Sobres MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad se establece en función de valor de **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) del mensaje de correo electrónico. Si **PR_SENSITIVITY** está establecido en "0 x 00000000" (normal) o "0 x 00000003" (confidencial), esta propiedad se debe establecer en "0 x 00" o absent lo que significa que agregar destinatarios adicionales o diferentes para el mensaje de correo electrónico se permite. Si el correo electrónico **PR_SENSITIVITY del objeto** se establece en "0 x 00000001" (personal) o "0 x 00000002" (privado), esta propiedad se debe establecer "0 x 01" para evitar que agregar destinatarios adicionales o diferentes de este correo electrónico a través de reenvío. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

