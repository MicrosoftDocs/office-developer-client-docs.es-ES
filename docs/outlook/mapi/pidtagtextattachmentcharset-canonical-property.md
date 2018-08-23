---
title: Propiedad canónica PidTagTextAttachmentCharset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTextAttachmentCharset
api_type:
- COM
ms.assetid: d347c949-d0c3-4a36-8447-3fa01111cdc1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cec34819cfa2c6e790f8808eb5bab70412f286b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591432"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a>Propiedad canónica PidTagTextAttachmentCharset

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el valor de conjunto de caracteres de un mensaje de los datos adjuntos.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |Ninguna  <br/> |
|Identificador:  <br/> |0x371B  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Los datos de esta propiedad se derivarán de un campo de encabezado Content-Type MIME que comienza por "texto /", si un parámetro "charset" está presente.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.
    
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

