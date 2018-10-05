---
title: Propiedad canónica PidTagAttachMimeTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f05fa0816db3b412329372ad392c673c240eb59e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389102"
---
# <a name="pidtagattachmimetag-canonical-property"></a>Propiedad canónica PidTagAttachMimeTag

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene información de formato sobre datos adjuntos de extensiones multipropósito de correo Internet (MIME). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W  <br/> |
|Identificador:  <br/> |0x370E  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Si la propiedad **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) contiene el valor **OID_MIMETAG**, el proveedor de transporte debe tener un aspecto en estas propiedades para determinar cómo se aplica formato a los datos adjuntos. 
  
Estas propiedades se copian desde el parámetro de tipo de contenido del encabezado MIME entrante. La composición de la cadena se define en el documento RFC 1521. El formato es tipo/subtipo, como aplicación/binario o texto sin formato. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica las propiedades de mensajes codificados con derechos administrados.
    
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

