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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327247"
---
# <a name="pidtagattachmimetag-canonical-property"></a>Propiedad canónica PidTagAttachMimeTag

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene información de formato sobre los datos adjuntos de extensiones multipropósito de correo de Internet (MIME). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W  <br/> |
|Identificador:  <br/> |0x370E  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Si la **propiedad PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) contiene el valor **OID_MIMETAG**, el proveedor de transporte debe buscar estas propiedades para determinar cómo se formatearán los datos adjuntos. 
  
Estas propiedades se copian del parámetro Content-type del encabezado MIME entrante. La composición de la cadena se define en el documento RFC 1521. El formato es tipo/subtipo, como application/binary o text/plain. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica las propiedades de los mensajes codificados con derechos administrados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

